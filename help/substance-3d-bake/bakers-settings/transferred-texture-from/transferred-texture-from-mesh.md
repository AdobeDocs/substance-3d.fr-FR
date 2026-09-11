---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-bake/bakers-settings/transferred-texture-from-mesh.html"
breadcrumb-title: ''
description: Transférer des textures entre les maillages en fonction de leurs UV, y compris la prise en charge des conversions de maps normal.
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

Le baker de Texture transférée à partir du maillage permet de convertir une texture d&#39;un maillage à un autre en fonction de leurs UV respectifs. Ce baker prend également en charge le transfert ou les maps normal (qui nécessitent des conversions spéciales). Pour fonctionner, les deux maillages ont besoin d&#39;UV de définition.

**Disponible dans :**

* Substance Designer
* Substance Automation Toolkit

## Paramètres

| *Paramètre* | *Description* |
| --- | --- |
| **Fichier de Texture** | Chemin d’accès au fichier de texture d’entrée qui sera transféré. |
| **Ensemble d&#39;UV** | Maillage d&#39;UV à utiliser sur le maillage à poly élevé pour lire la texture et la projeter sur le maillage à poly faible. |
| **Mode de filtrage** | Définit la manière dont l’interpolation en pixels de la texture doit être effectuée.Valeurs possibles :<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Au plus proche</strong> : aucune interpolation. Utilisez le pixel le plus proche trouvé à une position donnée. Précis, mais peut créer un crénelage.</li><li data-preserve-html="true"><strong>Bilinéaire</strong> (par défaut) : utilisez les quatre pixels les plus proches à une position donnée. Pas de crénelage, mais peut être flou.</li></ul> |
| **Map normal** | Si cette option est activée, indique au baker que la texture d&#39;entrée à transférer est une map normal. Cela indique le baker d’application de conversions spéciales à la texture pour la rendre compatible avec le maillage cible. |
| **Type de mappage** | Définit le type de map normal de la texture d&#39;entrée.Valeurs possibles :<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Espace monde</strong></li><li data-preserve-html="true"><strong>Repère tangent</strong> (par défaut)</li></ul> |
| **Orientation normale** | Définit le format normal de la texture d&#39;entrée si le **type de mappage** est défini sur **Repère tangent**. Valeurs possibles :<ul data-preserve-html="true"><li data-preserve-html="true"><strong>OpenGL</strong></li><li data-preserve-html="true"><strong>DirectX</strong> (par défaut)</li></ul> |
