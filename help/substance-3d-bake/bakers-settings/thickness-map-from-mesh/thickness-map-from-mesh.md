---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-bake/bakers-settings/thickness-map-from-mesh.html"
breadcrumb-title: ''
description: Générez des cartes de thickness en projetant des rayons vers l’intérieur à partir des surfaces de maillage pour les utiliser dans les ombrages SSS et le masquage.
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

La texture de Thickness du maillage est très similaire à l&#39;environnement du boulanger d&#39;occlusion, mais elle projette des rayons de la surface du maillage vers l&#39;intérieur. Cette texture peut être utilisée dans un nuanceur de diffusion de sous-surface (SSS) ou pour masquer des textures.

Les propriétés de texture sont définies comme suit :

* Les valeurs noires représentent les parties minces du modèle.
* Les valeurs de blanc représentent les parties épaisses du modèle.

**Disponible dans :**

* Substance Painter
* Substance Designer
* Substance Automation Toolkit

## Paramètres

| *Paramètre* | *Description* |
| --- | --- |
| **Rayons secondaires** | Quantité de rayons d’occlusion. Une valeur élevée génère moins de bruit, mais son calcul est plus long. La valeur par défaut est 64. |
| Distance D&#39;Occlusion De **Min** | Distance minimale à laquelle les rayons d’occlusion atteindront la géométrie poly élevée. La valeur par défaut est 0,00001. |
| **Distance d&#39;occlusion maximale** | Distance maximale à laquelle les rayons d&#39;occlusion atteindront la géométrie du poly élevé. La valeur par défaut est 0,1. |
| **Par rapport au cadre de sélection** | Si cette option est activée, les unités sont calculées par rapport au cadre de sélection de l’objet (1,0 correspondant à la longueur en diagonale du cadre de sélection). Si cette option est désactivée, les unités utilisées pour les distances d’occlusion minimale et maximale sont celles définies lors de l’exportation du maillage (mètres, centimètres ou toute autre unité de la scène exportée). |
| **Angle de répartition** | Angle de diffusion maximal des rayons d&#39;occlusion. La valeur par défaut est 180. |
| **Distribution** | Distribution angulaire des rayons d’occlusion.Valeurs possibles :<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Cosine</strong> (par défaut)</li><li data-preserve-html="true"><strong>Uniforme</strong></li></ul> |
| **Ignorer l&#39;arrière-plan** | Si cette option est activée, les rayons d’occlusion ignorent les frappes sur une face arrière (si la normale du poly élevé est orientée dans la direction opposée en tant que poly bas à partir duquel le rayon est déclenché). La plupart du temps, ce paramètre doit être activé pour éviter les artefacts. |
| **Auto-occlusion** | Correspondance par nom pour les rayons d’occlusion. Indique comment les boulangers doivent correspondre à une géométrie de poly faible et élevé. Il peut être utilisé pour filtrer le processus de cuisson sans avoir besoin de séparer manuellement les maillages (éclater).Valeurs possibles :<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Toujours</strong> (par défaut) : le maillage low-poly est mis en correspondance avec chaque maillage high-poly.</li><li data-preserve-html="true"><strong>Par nom de maillage</strong> : filtrez les maillages par leur nom pour éviter toute correspondance avec une géométrie indésirable.</li></ul>Pour en savoir plus sur la correspondance de la géométrie, voir : [Correspondance par nom](../../features/matching-by-name/matching-by-name.md). |
| **Normalisation Automatique** | Définit si les valeurs de sortie doivent être mises à l’échelle pour s’adapter à une plage de 0 à 1 (le point le plus clair est défini sur blanc pur et le point le plus sombre sur noir pur). |
