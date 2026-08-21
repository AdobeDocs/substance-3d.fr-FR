---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-bake/bakers-settings/ambient-occlusion.html"
breadcrumb-title: ''
description: Découvrez comment utiliser Ambient Occlusion baker pour générer des textures d’ombre ambiantes à l’aide d’algorithmes rapides accélérés par GPU.
helpx_creative_field: ""
helpx_description: bakers > Bakers Settings > Ambient Occlusion
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Occlusion ambiante
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 4%

---


# Occlusion ambiante

L&#39;Ambient Occlusion baker permet de cuire une texture d&#39;ombre ambiante. Ce boulanger utilise un algorithme rapide exécuté sur le GPU.

**Disponible en :**

* Concepteur de substance
* Boîte à outils d&#39;automatisation des substances

>[!WARNING]
>
> * Ce boulanger n&#39;est peut-être pas pris en charge sur les anciens GPU.
> * La cuisson à haute résolution sur les GPU bas de gamme/mobiles peut entraîner un blocage.

## Paramètres

| *Nom* | *Description* |
| --- | --- |
| **Carte normale** | Entrez un fichier de mappage normal qui peut être utilisé pour fournir des détails de géométrie supplémentaires sur la surface du maillage à prendre en compte lors du calcul de Baker. Ce paramètre est facultatif. |
| **Espace mondial** | Si cette option est activée, spécifiez que la carte normale d&#39;entrée se trouve dans l&#39;espace universel (au lieu de l&#39;espace tangent). Si aucun mappage normal d’entrée n’est fourni, ces paramètres sont ignorés/désactivés. |
| **Inverser la normale** | Calculer la carte d&#39;occlusion ambiante avec des normales inversées (peut être utilisé pour générer une carte d&#39;épaisseur). |
| **Utiliser des pièces maillées non sélectionnées** | Utilisez des parties de maillage non sélectionnées du maillage pour créer la carte d&#39;occlusion ambiante. |
| **Qualité** | Choisissez la qualité de la carte Occlusion ambiante. Une qualité supérieure est plus lente à calculer.Valeurs disponibles :<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Faible</strong> (3 passes)</li><li data-preserve-html="true"><strong></strong> (par défaut, 5 passes)</li><li data-preserve-html="true"><strong>Élevée</strong> (10 passes)</li><li data-preserve-html="true"><strong>Très haut</strong> (16 passes)</li></ul> |
| **Biais de précision** | Précision de l&#39;occlusion ambiante. Une valeur faible donnera une précision plus élevée, mais peut produire des artefacts plus grands. |
| **Fondu de distance** | Diffusion de l’occlusion ambiante. |
