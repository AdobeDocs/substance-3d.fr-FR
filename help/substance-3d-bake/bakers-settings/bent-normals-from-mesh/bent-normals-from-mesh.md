---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/bakers-settings/bent-normals-from-mesh.html"
breadcrumb-title: ''
description: Calcule les textures normales courbées qui décrivent la direction moyenne de l'éclairage ambiant à partir de maillages à polygone élevé.
helpx_creative_field: ""
helpx_description: bakers > Bakers Settings > Bent Normals from Mesh
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Normales courbées du maillage
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 3%

---


# Normales courbées du maillage

Les normales courbées de mesh baker calculent une texture qui décrit la direction moyenne de l&#39;éclairage ambiant. Ce boulanger est dérivé du [Ambient Occlusion de Mesh](../../bakers-settings/ambient-occlusion-from/ambient-occlusion-from-mesh.md).

**Disponible en :**

* Painter
* Designer
* Boîte à outils d’automatisation

## Paramètres

| *Paramètre* | *Description* |
| --- | --- |
| **Rayons secondaires** | Quantité de rayons occlusifs. Une valeur élevée produira moins de bruit, mais sera plus longue à calculer. |
| **Distance min. de l&#39;occluseur** | Distance minimale à laquelle les rayons d&#39;occlusion atteignent la géométrie poly élevée**.** |
| **Distance max. de l&#39;occluseur** | Distance maximale à laquelle les rayons d&#39;occlusion atteignent la géométrie poly élevée. |
| **Relatif au cadre de sélection** | Si cette option est activée, les calculs de distance de rayon sont basés sur l&#39;espace normalisé (0 à 1) du maillage à faible poly. Si cette option est désactivée, le calcul de la distance de rayon est basé sur les unités spécifiées dans le maillage à faible poly lors de son exportation (mètres, centimètres, etc.). |
| **Angle de propagation** | Angle de diffusion maximal des rayons d&#39;occlusion. La valeur par défaut est 180. |
| **Distribution** | Distribution angulaire des rayons d’occlusion.Valeurs possibles :<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Cosine</strong> (par défaut)</li><li data-preserve-html="true"><strong> Uniforme </strong></li></ul> |
| **Ignorer la face arrière** | Si cette option est activée, les rayons d&#39;occlusion ignorent les accès sur une face arrière (si la normale du poly élevé est orientée dans la direction opposée comme le poly bas à partir duquel le rayon est déclenché). La plupart du temps, ce paramètre doit être activé pour éviter les artefacts. |
| **Auto-Occlusion** | Correspondance par nom pour les rayons d&#39;occlusion. Indique comment les boulangers doivent correspondre à une géométrie de poly faible et élevé. Il peut être utilisé pour filtrer le processus de cuisson sans avoir à séparer manuellement les maillages (éclater).Valeurs possibles :<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Always</strong> (par défaut) : un maillage low-poly est mis en correspondance avec chaque maillage high-poly.</li><li data-preserve-html="true"><strong>Par nom de maillage</strong> : filtrez les maillages en fonction de leur nom pour éviter toute correspondance avec une géométrie indésirable.</li></ul>Pour en savoir plus sur la correspondance de géométries, voir : [Correspondance par nom](../../features/matching-by-name/matching-by-name.md). |
| **Type de carte** | Définit le type de la texture de sortie.Valeurs possibles :<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Espace mondial</strong></li><li data-preserve-html="true"><strong>Espace tangent</strong> (par défaut)</li></ul> |
| **Orientation normale** | Contrôle le format normal de la texture de sortie si **Type de tapis** est défini sur Espace tangent. Valeurs possibles :<ul data-preserve-html="true"><li data-preserve-html="true"><strong>OpenGL </strong> <strong> <br/></strong></li><li data-preserve-html="true"><strong>DirectX</strong> (par défaut)<strong> <br/></strong></li></ul> |
