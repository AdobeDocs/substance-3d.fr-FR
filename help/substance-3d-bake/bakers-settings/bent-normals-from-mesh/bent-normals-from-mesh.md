---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-bake/bakers-settings/bent-normals-from-mesh.html"
breadcrumb-title: ''
description: Calculez les textures normales courbées qui décrivent la direction moyenne de l’éclairage ambiant à partir de maillages à poly-interpolés.
helpx_creative_field: ""
helpx_description: bakers > Bakers Settings > Bent Normals from Mesh
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Normales courbées à partir d'un filet
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 3%

---


# Normales courbées à partir d&#39;un filet

Les normales recourbées de mesh baker calculent une texture qui décrit la direction moyenne de l&#39;éclairage ambiant. Ce boulanger est dérivé de l&#39;Occlusion [ambiante de Mesh](../../bakers-settings/ambient-occlusion-from/ambient-occlusion-from-mesh.md) baker.

**Disponible dans :**

* Painter
* Designer
* Automation Toolkit

## Paramètres

| *Paramètre* | *Description* |
| --- | --- |
| **Rayons secondaires** | Quantité de rayons d’occlusion. Une valeur élevée produira moins de bruit mais sera plus longue à calculer. |
| Distance D&#39;Occlusion De **Min** | Distance minimale à laquelle les rayons d&#39;occlusion atteindront la géométrie poly élevée&#x200B;**.** |
| **Distance d&#39;occlusion maximale** | Distance maximale à laquelle les rayons d&#39;occlusion atteindront la géométrie du poly élevé. |
| **Par rapport au cadre de sélection** | Si cette option est activée, les calculs de distance de rayon sont basés sur l&#39;espace normalisé (0 à 1) du maillage à faible poly. Si cette option est désactivée, le calcul de la distance de rayon est basé sur les unités spécifiées dans le maillage low-poly lors de son exportation (mètres, centimètres, etc.). |
| **Angle de répartition** | Angle de diffusion maximal des rayons d&#39;occlusion. La valeur par défaut est 180. |
| **Distribution** | Distribution angulaire des rayons d’occlusion.Valeurs possibles :<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Cosine</strong> (par défaut)</li><li data-preserve-html="true"><strong>Uniforme</strong></li></ul> |
| **Ignorer l&#39;arrière-plan** | Si cette option est activée, les rayons d’occlusion ignorent les frappes sur une face arrière (si la normale du poly élevé est orientée dans la direction opposée en tant que poly bas à partir duquel le rayon est déclenché). La plupart du temps, ce paramètre doit être activé pour éviter les artefacts. |
| **Auto-occlusion** | Correspondance par nom pour les rayons d’occlusion. Indique comment les boulangers doivent correspondre à une géométrie de poly faible et élevé. Il peut être utilisé pour filtrer le processus de cuisson sans avoir besoin de séparer manuellement les maillages (éclater).Valeurs possibles :<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Toujours</strong> (par défaut) : le maillage low-poly est mis en correspondance avec chaque maillage high-poly.</li><li data-preserve-html="true"><strong>Par nom de maillage</strong> : filtrez les maillages par leur nom pour éviter toute correspondance avec une géométrie indésirable.</li></ul>Pour en savoir plus sur la correspondance de la géométrie, voir : [Correspondance par nom](../../features/matching-by-name/matching-by-name.md). |
| **Type de mappage** | Définit le type de la texture de sortie.Valeurs possibles :<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Espace universel</strong></li><li data-preserve-html="true"><strong>Espace tangent</strong> (par défaut)</li></ul> |
| **Orientation normale** | Contrôle le format normal de la texture de sortie si **Type de cache** est défini sur Espace tangent.Valeurs possibles :<ul data-preserve-html="true"><li data-preserve-html="true"><strong>OpenGL</strong> <strong> <br/></strong></li><li data-preserve-html="true"><strong>DirectX</strong> (par défaut)<strong> <br/></strong></li></ul> |
