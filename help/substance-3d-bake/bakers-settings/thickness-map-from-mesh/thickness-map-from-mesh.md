---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/bakers-settings/thickness-map-from-mesh.html"
breadcrumb-title: ''
description: Générez des cartes d'épaisseur en projetant des rayons vers l'intérieur à partir des surfaces maillées pour les utiliser dans les ombrages SSS et le masquage.
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

La carte d&#39;épaisseur du maillage est très similaire à celle du boulanger d&#39;occlusion ambiant, mais elle projette des rayons de la surface du maillage vers l&#39;intérieur. Cette texture peut être utilisée dans un nuanceur de dispersion de sous-surface (SSS) ou pour masquer des textures.

Les propriétés de texture sont définies comme suit :

* Les valeurs noires représentent les parties fines du modèle.
* Les valeurs blanches représentent les parties épaisses du modèle.

**Disponible en :**

* Substance Painter
* Concepteur de substance
* Boîte à outils d&#39;automatisation des substances

## Paramètres

| *Paramètre* | *Description* |
| --- | --- |
| **Rayons secondaires** | Quantité de rayons occlusifs. Une valeur élevée produira moins de bruit, mais son calcul sera plus long. La valeur par défaut est 64. |
| **Distance min. de l&#39;occluseur** | Distance minimale à laquelle les rayons d&#39;occlusion atteignent la géométrie poly élevée. La valeur par défaut est 0,00001. |
| **Distance max. de l&#39;occluseur** | Distance maximale à laquelle les rayons d&#39;occlusion atteignent la géométrie poly élevée. La valeur par défaut est 0,1. |
| **Relatif au cadre de sélection** | Si cette option est activée, les unités sont relatives au cadre de sélection de l&#39;objet (1,0 étant la longueur diagonale du cadre de sélection). Si cette option est désactivée, les unités utilisées pour les distances d&#39;occultation minimale et maximale sont celles définies lors de l&#39;exportation du maillage (mètres, centimètres ou toute autre unité de la scène exportée). |
| **Angle de propagation** | Angle de diffusion maximal des rayons d&#39;occlusion. La valeur par défaut est 180. |
| **Distribution** | Distribution angulaire des rayons d’occlusion.Valeurs possibles :<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Cosine</strong> (par défaut)</li><li data-preserve-html="true"><strong> Uniforme </strong></li></ul> |
| **Ignorer la face arrière** | Si cette option est activée, les rayons d&#39;occlusion ignorent les accès sur une face arrière (si la normale du poly élevé est orientée dans la direction opposée comme le poly bas à partir duquel le rayon est déclenché). La plupart du temps, ce paramètre doit être activé pour éviter les artefacts. |
| **Auto-Occlusion** | Correspondance par nom pour les rayons d&#39;occlusion. Indique comment les boulangers doivent correspondre à une géométrie de poly faible et élevé. Il peut être utilisé pour filtrer le processus de cuisson sans avoir à séparer manuellement les maillages (éclater).Valeurs possibles :<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Always</strong> (par défaut) : un maillage low-poly est mis en correspondance avec chaque maillage high-poly.</li><li data-preserve-html="true"><strong>Par nom de maillage</strong> : filtrez les maillages en fonction de leur nom pour éviter toute correspondance avec une géométrie indésirable.</li></ul>Pour en savoir plus sur la correspondance de géométries, voir : [Correspondance par nom](../../features/matching-by-name/matching-by-name.md). |
| **Normalisation automatique** | Définit si les valeurs de sortie doivent être mises à l’échelle pour s’adapter à une plage comprise entre 0 et 1 (le point le plus clair est défini sur blanc pur et le point le plus sombre est défini sur noir pur). |
