---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-bake/bakers-settings/transferred-texture-from-mesh.html"
breadcrumb-title: ''
description: Transférer les textures entre les maillages en fonction de leurs UV, y compris la prise en charge des conversions de carte normales.
helpx_creative_field: ""
helpx_description: bakers > Bakers Settings > Transferred Texture from Mesh
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Texture transférée à partir du maillage
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 3%

---


# Texture transférée à partir du maillage

La texture transférée de mesh baker permet de convertir une texture d&#39;un maillage à un autre en fonction de leurs UV respectifs. Ce boulanger prend également en charge le transfert de cartes normales (qui nécessitent des conversions spéciales). Pour fonctionner, les deux maillages ont besoin de définitions UV.

**Disponible dans :**

* Concepteur de substance
* Boîte à outils d&#39;automatisation des substances

## Paramètres

| *Paramètre* | *Description* |
| --- | --- |
| **Fichier de texture** | Chemin d’accès au fichier de texture d’entrée qui sera transféré. |
| **Ensemble UV** | Des UV de maillage à utiliser sur le maillage à poly élevé pour lire la texture et la projeter sur le maillage à poly faible. |
| **Mode de filtrage** | Définit la manière dont l’interpolation en pixels de la texture doit être effectuée.Valeurs possibles :<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Plus proche</strong> : sans interpolation, utilisez le pixel le plus proche trouvé à une position donnée. Précis mais peut créer un alias.</li><li data-preserve-html="true"><strong>Bilinéaire</strong> (par défaut) : utilisez les quatre pixels les plus proches pour une position donnée. Aucun alias, mais peut être flou.</li></ul> |
| **Carte normale** | Si cette option est activée, indique au boulanger que la texture d&#39;entrée à transférer est une texture normale. Cela indique au boulanger d&#39;appliquer des conversions spéciales à la texture pour la rendre compatible avec le maillage cible. |
| **Type de carte** | Définit le type de texture normale de la texture d&#39;entrée.Valeurs possibles :<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Espace mondial</strong></li><li data-preserve-html="true"><strong>Espace tangent</strong> (par défaut)</li></ul> |
| **Orientation normale** | Définit le format normal de la texture d’entrée si **Type de carte** est défini sur **Espace tangent**.Valeurs possibles :<ul data-preserve-html="true"><li data-preserve-html="true"><strong>OpenGL </strong></li><li data-preserve-html="true"><strong>DirectX</strong> (par défaut)</li></ul> |
