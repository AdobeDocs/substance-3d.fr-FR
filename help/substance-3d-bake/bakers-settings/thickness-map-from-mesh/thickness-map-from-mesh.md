---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-bake/bakers-settings/thickness-map-from-mesh.html"
breadcrumb-title: ''
description: Générez des maps thickness en convertissant les rayons vers l’intérieur à partir des surfaces de maillage pour les utiliser dans les ombrages SSS et le masquage.
helpx_creative_field: ""
helpx_description: bakers > Bakers Settings > Thickness Map from Mesh
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Map thickness depuis le maillage
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 5%

---


# Map thickness depuis le maillage

La Map thickness du maillage est très similaire au baker de l’ambient occlusion, mais elle convertit les rayons de la surface du maillage vers l’intérieur. Cette texture peut être utilisée dans un shader de diffusion de sous-surface (SSS) ou pour des textures de masquage.

Les propriétés de la texture sont définies comme suit :

* Les valeurs noires représentent les parties minces du modèle.
* Les valeurs de blanc représentent les parties épaisses du modèle.

**Disponible dans :**

* Substance Painter
* Substance Designer
* Substance Automation Toolkit

## Paramètres

| *Paramètre* | *Description* |
| --- | --- |
| **Rayons secondaires** | Montant des rayons d&#39;occlusion. Une valeur élevée génère moins de bruit, mais son calcul est plus long. La valeur par défaut est 64. |
| **Distance d&#39;occlusion Min** | Distance minimale à laquelle les rayons d&#39;occlusion atteindront la géométrie en poly élevé. La valeur par défaut est 0,00001. |
| **Distance d&#39;occlusion max** | Distance maximale à laquelle les rayons d&#39;occlusion atteindront la géométrie du poly élevé. La valeur par défaut est 0,1. |
| **Par rapport au cadre de sélection** | Si cette option est activée, les unités sont calculées par rapport au cadre de sélection de l’objet (1,0 correspondant à la longueur en diagonale du cadre de sélection). Si cette option est désactivée, les unités utilisées pour les distances d&#39;occlusion minimale et maximale sont celles définies lors de l’exportation de votre maillage (mètres, centimètres ou toute autre unité de la scène exportée). |
| **Angle de répartition** | Angle de diffusion maximal des rayons d&#39;occlusion. La valeur par défaut est 180. |
| **Distribution** | Distribution angulaire des rayons d’occlusion.Valeurs possibles :<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Cosine</strong> (par défaut)</li><li data-preserve-html="true"><strong>Uniforme</strong></li></ul> |
| **Ignorer l&#39;arrière-plan** | Si cette option est activée, les rayons d&#39;occlusion ignorent les coups sur une face arrière (si la normale du poly élevé face dans la direction opposée comme le poly bas à partir duquel le rayon est déclenché). La plupart du temps, ce paramètre doit être activé pour éviter les artefacts. |
| **Auto-occlusion** | Correspondance par nom pour les rayons d&#39;occlusion. Indique comment les bakers doivent correspondre à la géométrie des polygones bas et haut. Il peut être utilisé pour filtrer le processus de baking sans avoir à écarter manuellement les maillages (éclater).Valeurs possibles :<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Toujours</strong> (par défaut) : le maillage de faible niveau de polyvalence correspond à tous les maillages de niveau élevé.</li><li data-preserve-html="true"><strong>Par nom de Maillage</strong> : filtrez les maillages par leur nom pour éviter toute correspondance avec une géométrie indésirable.</li></ul>Pour en savoir plus sur la correspondance de la géométrie, voir : [Correspondance par nom](../../features/matching-by-name/matching-by-name.md). |
| **Normalisation Automatique** | Définit si les valeurs de sortie doivent être mises à l’échelle pour s’adapter à une plage de 0 à 1 (le point le plus clair est défini sur blanc pur et le point le plus sombre sur noir pur). |
