---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/bakers-settings/ambient-occlusion-from-mesh.html"
breadcrumb-title: ''
description: Créez des textures d'occlusion ambiantes précises à partir de mailles à poly élevé en utilisant des techniques de lancer de rayons pour un réalisme amélioré.
helpx_creative_field: ""
helpx_description: bakers > Bakers Settings > Ambient Occlusion from Mesh
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Occlusion ambiante du maillage
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '531'
ht-degree: 2%

---


# Occlusion ambiante du maillage

L&#39;Occlusion Ambiante de mesh baker permet de cuire une texture Occlusion Ambiante à partir de maillages poly élevés. Elle est plus lente que la base [occlusion ambiante](../../bakers-settings/ambient-occlusion/ambient-occlusion.md) mais produit des résultats plus précis.

**Disponible en :**

* Concepteur de substance
* Boîte à outils d&#39;automatisation des substances
* Substance Painter

## Paramètres

| *Paramètre* | *Description* |
| --- | --- |
| **Rayons secondaires** | Quantité de rayons occlusifs. Une valeur élevée produira moins de bruit, mais son calcul sera plus long. La valeur par défaut est 64. |
| **Distance min. de l&#39;occluseur** | Distance minimale à laquelle les rayons d&#39;occlusion atteignent la géométrie poly élevée. La valeur par défaut est 0,00001. |
| **Distance max. de l&#39;occluseur** | Distance maximale à laquelle les rayons d&#39;occlusion atteignent la géométrie poly élevée. La valeur par défaut est 0,1. |
| **Relatif au cadre de sélection** | Si cette option est activée, les unités sont relatives au cadre de sélection de l&#39;objet (1,0 étant la longueur diagonale du cadre de sélection). Si cette option est désactivée, les unités utilisées pour les distances d&#39;occultation minimale et maximale sont celles définies lors de l&#39;exportation du maillage (mètres, centimètres ou toute autre unité de la scène exportée). |
| **Angle de propagation** | Angle de diffusion maximal des rayons d&#39;occlusion. La valeur par défaut est 180. |
| **Distribution** | Distribution angulaire des rayons d’occlusion. Définit la manière dont les rayons sont diffusés à l’intérieur d’un cône de la taille de l’angle de propagation.Valeurs possibles :<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Cosine</strong> (par défaut) : réaliste, mais peut conduire à une ligne blanche dans des zones obstruées très minces. Plus adapté pour l&#39;ombrage et l&#39;éclairage.</li><li data-preserve-html="true"><strong>Uniforme</strong> : utile pour créer des dégradés linéaires. Convient mieux au masquage de couches et à d&#39;autres types de filtrage.</li></ul> |
| **Ignorer la face arrière** | Ce paramètre définit si les rayons d&#39;occlusion ignorent les accès sur une face arrière (si la normale du poly élevé est orientée dans la direction opposée comme le poly bas à partir duquel le rayon est tiré). La plupart du temps, ce paramètre doit être activé pour éviter les artefacts. Valeurs possibles :<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Jamais</strong> (par défaut) : les faces arrière ne sont jamais ignorées</li><li data-preserve-html="true"><strong>Always</strong> : les faces arrière sont toujours ignorées</li><li data-preserve-html="true"><strong>Par nom de maillage</strong> : les faces arrière ne sont ignorées que pour les maillages qui correspondent au mot-clé suffixe. Voir les [paramètres communs](../../bakers-settings/common-parameters/common-parameters.md).</li></ul> |
| **Auto-Occlusion** | Correspondance par nom pour les rayons d&#39;occlusion. Indique comment les boulangers doivent correspondre à une géométrie de poly faible et élevé. Il peut être utilisé pour filtrer le processus de cuisson sans avoir à séparer manuellement les maillages (éclater).Valeurs possibles :<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Always</strong> (par défaut) : un maillage low-poly est mis en correspondance avec chaque maillage high-poly.</li><li data-preserve-html="true"><strong>Par nom de maillage</strong> : filtrez les maillages en fonction de leur nom pour éviter toute correspondance avec une géométrie indésirable.</li></ul>Pour en savoir plus sur la correspondance de géométries, voir : [Correspondance par nom](../../features/matching-by-name/matching-by-name.md). |
| **Carte normale** | Chemin facultatif vers une texture normale. Peut être utilisé pour remplacer le calcul interne du boulanger. |
| **Espace mondial** | Si cette option est activée, la texture normale est interprétée comme normale de l&#39;espace universel au lieu d&#39;un espace tangent. |
| **Orientation normale** | Format de la texture Normale si dans l&#39;Espace Tangent. Valeurs possibles :<ul data-preserve-html="true"><li data-preserve-html="true"><strong>DirectX</strong> (par défaut)</li><li data-preserve-html="true"><strong>OpenGL </strong></li></ul> |
| **Atténuation** | Définit comment l&#39;occlusion est atténuée par la distance d&#39;occlusion.Valeurs possibles :<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Aucune</strong> : aucune atténuation.</li><li data-preserve-html="true"><strong>Linéaire</strong> (par défaut) : atténuation progressive.</li><li data-preserve-html="true"><strong>Lisse</strong> : atténuation douce.</li></ul> |
| **Plan de masse** | Si cette option est activée, simulez un plan sous le cadre de sélection du maillage sur l&#39;axe XZ pour entrer en collision avec des rayons secondaires. Cela simule l&#39;ombrage provenant d&#39;un plan d&#39;étage invisible. |
| **Décalage du plan de masse** | Permet d&#39;éloigner le plan du maillage pour réduire l&#39;intensité de l&#39;effet. La valeur est absolue et non relative au maillage. |
