---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/bakers-settings/transferred-texture-from-mesh.html"
breadcrumb-title: ''
description: Transférez les textures entre les maillages en fonction de leurs UV, y compris la prise en charge des conversions de cartes normales.
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

La texture Transférée de mesh baker permet de convertir une texture d&#39;un filet à un autre en fonction de leurs UV respectifs. Ce boulanger prend également en charge le transfert de cartes normales (qui nécessitent des conversions spéciales). Pour fonctionner, les deux maillages nécessitent des définitions UV.

**Disponible dans :**

* Substance Designer
* Substance Automation Toolkit

## Paramètres

| *Paramètre* | *Description* |
| --- | --- |
| **Fichier de texture** | Chemin vers le fichier de texture d’entrée qui sera transféré. |
| **Ensemble UV** | UV de maillage à utiliser sur le maillage en poly-élevé pour lire la texture et la projeter sur le maillage en poly-faible. |
| **Mode de filtrage** | Définit la méthode d’interpolation de pixel de la texture.Valeurs possibles :<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Au plus proche</strong> : aucune interpolation. Utilisez le pixel le plus proche trouvé à une position donnée. Précis, mais peut créer un crénelage.</li><li data-preserve-html="true"><strong>Bilinéaire</strong> (par défaut) : utilisez les quatre pixels les plus proches à une position donnée. Pas de crénelage, mais peut être flou.</li></ul> |
| **Carte des normales** | Si cette option est activée, elle indique au boulanger que la texture d’entrée à transférer est une texture normale. Cela indique au boulanger d’appliquer des conversions spéciales à la texture pour la rendre compatible avec le filet cible. |
| **Type de mappage** | Définit le type de texture normale utilisé pour la texture d&#39;entrée.Valeurs possibles :<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Espace universel</strong></li><li data-preserve-html="true"><strong>Espace tangent</strong> (par défaut)</li></ul> |
| **Orientation normale** | Définit le format normal de la texture d&#39;entrée si **Type de mappage** est défini sur **Espace tangent**. Valeurs possibles :<ul data-preserve-html="true"><li data-preserve-html="true"><strong>OpenGL</strong></li><li data-preserve-html="true"><strong>DirectX</strong> (par défaut)</li></ul> |
