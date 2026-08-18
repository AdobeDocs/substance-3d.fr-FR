---
source-git-commit: a517442244806bc6aef0f5bfb165c5d4f67341be
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 0%

---
# Convertisseur Markdown en PDF

Ce dossier contient un script de prétraitement et de conversion permettant de générer des versions PDF des pages de documentation à partir de ce référentiel.

## Pourquoi cela existe-t-il

Les fichiers sources de documentation utilisent une syntaxe de markdown spécifique à la plate-forme Adobe (accordéons, légendes d’alerte et extensions d’attribut d’image) que les outils de markdown classiques ne comprennent pas. Ce script normalise cette syntaxe et convertit le fichier en PDF à l&#39;aide de [md-to-pdf](https://github.com/simonhaenisch/md-to-pdf), tout en compressant les images pour conserver une taille de fichier de sortie gérable.

## Conditions préalables

- [Node.js](https://nodejs.org/) (v18 ou version ultérieure)
- Les dépendances sont déjà installées dans `node_modules/`. Si vous devez les réinstaller, exécutez `npm ci` à partir de ce dossier.

## Utilisation

Exécutez le script à partir de la **racine du référentiel**, en transmettant le chemin d&#39;accès au fichier markdown à convertir :

```
node "scripts/Md to PDF converter/preprocess-for-pdf.js" <path/to/file.md>
```

**Exemple :**

```
node "scripts/Md to PDF converter/preprocess-for-pdf.js" help/substance-3d-general/openpbr/openpbr-overview.md
```

Le PDF est écrit dans le **même répertoire que le fichier source**. Les fichiers temporaires créés lors de la conversion (`*.pdf-ready.md` et `_pdf-images/`) sont automatiquement supprimés en cas de réussite. Si la conversion échoue, ils sont laissés en place pour faciliter le débogage.

## Rôle du script

| Syntaxe source | sortie PDF |
|---|---|
| `+++Title` / `+++` blocs accordéon | Titre `#####` avec contenu toujours visible |
| `>[!NOTE]` légendes d&#39;alerte | Guillemet-bloc standard avec préfixe **Remarque :** en gras |
| `![](path){width="N"}` attributs d&#39;image | Balise `<img>` conservant la largeur spécifiée |
| Image Markdown liée aux fichiers `.pdf` | Supprimé (références d’auto-téléchargement web uniquement) |
| Clé frontmatter `hold:` | Supprimé (métadonnées de plateforme uniquement) |
| Toutes les images | Redimensionné jusqu’à 1 200 px de large, réencodé en JPEG avec une qualité de 80 % |
| Tous les tableaux | Bordures et arrière-plans supprimés par injection de code CSS |
