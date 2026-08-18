---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/bakers-settings/ambient-occlusion-from-mesh.html"
breadcrumb-title: ''
description: Créez des textures d’occlusion ambiante précises à partir de maillages à poly élevé à l’aide de techniques de lancer de rayon pour un réalisme amélioré.
helpx_creative_field: ""
helpx_description: bakers > Bakers Settings > Ambient Occlusion from Mesh
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Occlusion ambiante à partir du filet
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '531'
ht-degree: 2%

---


# Occlusion ambiante à partir du filet

L&#39;Occlusion ambiante de mesh baker permet de cuire une texture d&#39;Occlusion ambiante à partir de maillages en poly élevé. Il est plus lent que le boulanger de base de l&#39;[occlusion ambiante](../../bakers-settings/ambient-occlusion/ambient-occlusion.md), mais produit des résultats plus précis.

**Disponible dans :**

* Substance Designer
* Substance Automation Toolkit
* Substance Painter

## Paramètres

| *Paramètre* | *Description* |
| --- | --- |
| **Rayons secondaires** | Quantité de rayons d’occlusion. Une valeur élevée génère moins de bruit, mais son calcul est plus long. La valeur par défaut est 64. |
| Distance D&#39;Occlusion De **Min** | Distance minimale à laquelle les rayons d’occlusion atteindront la géométrie poly élevée. La valeur par défaut est 0,00001. |
| **Distance d&#39;occlusion maximale** | Distance maximale à laquelle les rayons d&#39;occlusion atteindront la géométrie du poly élevé. La valeur par défaut est 0,1. |
| **Par rapport au cadre de sélection** | Si cette option est activée, les unités sont calculées par rapport au cadre de sélection de l’objet (1,0 correspondant à la longueur en diagonale du cadre de sélection). Si cette option est désactivée, les unités utilisées pour les distances d’occlusion minimale et maximale sont celles définies lors de l’exportation du maillage (mètres, centimètres ou toute autre unité de la scène exportée). |
| **Angle de répartition** | Angle de diffusion maximal des rayons d&#39;occlusion. La valeur par défaut est 180. |
| **Distribution** | Distribution angulaire des rayons d’occlusion. Définit la manière dont les rayons sont dispersés à l’intérieur d’un cône de la taille de l’angle de dispersion.Valeurs possibles :<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Cosine</strong> (par défaut) : réaliste, mais peut entraîner une ligne blanche dans les zones obstruées très fines. Plus adapté à l&#39;ombrage et à l&#39;éclairage.</li><li data-preserve-html="true"><strong>Uniforme</strong> : utile pour créer des dégradés linéaires. Plus adapté au masquage de calque et à d’autres types de filtrage.</li></ul> |
| **Ignorer l&#39;arrière-plan** | Ces paramètres définissent si les rayons d’occlusion ignorent les coups sur une face arrière (si la normale du poly élevé est orientée dans la direction opposée en tant que poly bas à partir duquel le rayon est déclenché). La plupart du temps, ce paramètre doit être activé pour éviter les artefacts. Valeurs possibles :<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Jamais</strong> (par défaut) : les faces arrière ne sont jamais ignorées</li><li data-preserve-html="true"><strong>Toujours</strong> : les faces arrière sont toujours ignorées</li><li data-preserve-html="true"><strong>Par nom de maillage</strong> : les faces arrière sont ignorées uniquement pour les maillages qui correspondent au mot-clé de suffixe. Voir les [paramètres communs](../../bakers-settings/common-parameters/common-parameters.md).</li></ul> |
| **Auto-occlusion** | Correspondance par nom pour les rayons d’occlusion. Indique comment les boulangers doivent correspondre à une géométrie de poly faible et élevé. Il peut être utilisé pour filtrer le processus de cuisson sans avoir besoin de séparer manuellement les maillages (éclater).Valeurs possibles :<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Toujours</strong> (par défaut) : le maillage low-poly est mis en correspondance avec chaque maillage high-poly.</li><li data-preserve-html="true"><strong>Par nom de maillage</strong> : filtrez les maillages par leur nom pour éviter toute correspondance avec une géométrie indésirable.</li></ul>Pour en savoir plus sur la correspondance de la géométrie, voir : [Correspondance par nom](../../features/matching-by-name/matching-by-name.md). |
| **Carte des normales** | Tracé facultatif d’une texture normale. Peut être utilisé pour remplacer le calcul interne du boulanger. |
| **Espace universel** | Si cette option est activée, la texture normale est interprétée comme espace universel normal et non comme espace tangent. |
| **Orientation normale** | Format de la texture normale si elle est dans l’espace tangent.Valeurs possibles :<ul data-preserve-html="true"><li data-preserve-html="true"><strong>DirectX</strong> (par défaut)</li><li data-preserve-html="true"><strong>OpenGL</strong></li></ul> |
| **Atténuation** | Définit la façon dont l&#39;occlusion est atténuée par la distance d&#39;occlusion.Valeurs possibles :<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Aucun</strong> : aucune atténuation.</li><li data-preserve-html="true"><strong>Linéaire</strong> (par défaut) : atténuation progressive.</li><li data-preserve-html="true"><strong>Lisse</strong> : atténuation douce.</li></ul> |
| **Plan Au Sol** | Si cette option est activée, simulez un plan sous le cadre de sélection du maillage sur l’axe XZ pour entrer en collision avec des rayons secondaires. Cela simule une ombre provenant d&#39;un plan d&#39;étage invisible. |
| **Décalage du plan au sol** | Permet d’éloigner le plan du filet pour réduire l’intensité de l’effet. La valeur est absolue et non relative au maillage. |
