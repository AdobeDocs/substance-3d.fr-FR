---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/bakers-settings/bent-normals-from-mesh.html"
breadcrumb-title: ''
description: Calculez des textures de bents normals qui décrivent la direction moyenne de l’éclairage ambiant à partir de maillages à polygone de mesure.
helpx_creative_field: ""
helpx_description: bakers > Bakers Settings > Bent Normals from Mesh
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Bents normals du Maillage
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 3%

---


# Bents normals du Maillage

Les Bents normals du baker maillage calculent une texture qui décrit la direction moyenne de l’éclairage ambiant. Ce baker est dérivé du baker [Ambient occlusion du Maillage](../../bakers-settings/ambient-occlusion-from/ambient-occlusion-from-mesh.md).

**Disponible dans :**

* Painter
* Designer
* Automation Toolkit

## Paramètres

| *Paramètre* | *Description* |
| --- | --- |
| **Rayons secondaires** | Montant des rayons d&#39;occlusion. Une valeur élevée produira moins de bruit mais sera plus longue à calculer. |
| **Distance d&#39;occlusion Min** | Distance minimale à laquelle les rayons d&#39;occlusion atteindront la géométrie en poly élevé&#x200B;**.** |
| **Distance d&#39;occlusion max** | Distance maximale à laquelle les rayons d&#39;occlusion atteindront la géométrie du poly élevé. |
| **Par rapport au cadre de sélection** | Si cette option est activée, les calculs de distance des rayons sont basés sur l&#39;espace normalisé (0 à 1) du maillage à faible poly. Si cette option est désactivée, le calcul de distance de rayon est basé sur les unités spécifiées dans le maillage low-poly lors de son exportation (mètres, centimètres, etc.). |
| **Angle de répartition** | Angle de diffusion maximal des rayons d&#39;occlusion. La valeur par défaut est 180. |
| **Distribution** | Distribution angulaire des rayons d’occlusion.Valeurs possibles :<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Cosine</strong> (par défaut)</li><li data-preserve-html="true"><strong>Uniforme</strong></li></ul> |
| **Ignorer l&#39;arrière-plan** | Si cette option est activée, les rayons d&#39;occlusion ignorent les coups sur une face arrière (si la normale du poly élevé face dans la direction opposée comme le poly bas à partir duquel le rayon est déclenché). La plupart du temps, ce paramètre doit être activé pour éviter les artefacts. |
| **Auto-occlusion** | Correspondance par nom pour les rayons d&#39;occlusion. Indique comment les bakers doivent correspondre à la géométrie des polygones bas et haut. Il peut être utilisé pour filtrer le processus de baking sans avoir à écarter manuellement les maillages (éclater).Valeurs possibles :<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Toujours</strong> (par défaut) : le maillage de faible niveau de polyvalence correspond à tous les maillages de niveau élevé.</li><li data-preserve-html="true"><strong>Par nom de Maillage</strong> : filtrez les maillages par leur nom pour éviter toute correspondance avec une géométrie indésirable.</li></ul>Pour en savoir plus sur la correspondance de la géométrie, voir : [Correspondance par nom](../../features/matching-by-name/matching-by-name.md). |
| **Type de mappage** | Définit le type de la texture de sortie.Valeurs possibles :<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Espace monde</strong></li><li data-preserve-html="true"><strong>Espace de Tangente</strong> (par défaut)</li></ul> |
| **Orientation normale** | Contrôle le format normal de la texture de sortie si **Type de cache** est défini sur Repère tangent. Valeurs possibles :<ul data-preserve-html="true"><li data-preserve-html="true"><strong>OpenGL</strong> <strong> <br/></strong></li><li data-preserve-html="true"><strong>DirectX</strong> (par défaut)<strong> <br/></strong></li></ul> |
