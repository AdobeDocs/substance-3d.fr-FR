---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/bakers-settings/curvature-from-mesh.html"
breadcrumb-title: ''
description: Générez des textures de courbure précises à partir de maillages à poly élevé en utilisant le raytracing pour une détection précise des contours.
helpx_creative_field: ""
helpx_description: bakers > Bakers Settings > Curvature from Mesh
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Courbure à partir du filet
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 0%

---


# Courbure à partir du filet

La courbure du boulanger de maillage génère une texture de courbure à partir de maillages à poly élevé. Il est plus lent que le boulanger de base [courbure](../../bakers-settings/curvature/curvature.md), mais produit des résultats plus précis.

**Disponible dans :**

* Substance Designer
* Substance Automation Toolkit
* Substance Painter

## Paramètres

| *Paramètre* | *Description* |
| --- | --- |
| **Rayons secondaires** | Quantité de rayons émis pour lire la géométrie voisine. Une valeur élevée génère moins de bruit, mais son calcul est plus long. La valeur par défaut est 32. |
| **Rayon d&#39;échantillonnage** | Distance de prise en compte de la géométrie avoisinante pour calculer la courbure à la surface de la géométrie. Des valeurs élevées peuvent produire des contours plus épais, tandis que des valeurs faibles peuvent produire des contours plus fins mais manquer d’informations. |
| **Par Rapport Au Cadre De Sélection** | Définit si le rayon d&#39;échantillonnage est relatif à la taille du maillage ou s&#39;il est défini comme une distance basée sur une unité. |
| **Auto-intersection** | Correspondance par nom de rayons de courbure. Indique comment les boulangers doivent correspondre à une géométrie de poly faible et élevé. Il peut être utilisé pour filtrer le processus de cuisson sans avoir besoin de séparer manuellement les maillages (éclater).Valeurs possibles :<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Toujours</strong> (par défaut) : le maillage low-poly est mis en correspondance avec chaque maillage high-poly.</li><li data-preserve-html="true"><strong>Par nom de maillage</strong> : filtrez les maillages par leur nom pour éviter toute correspondance avec une géométrie indésirable.</li></ul>Pour en savoir plus sur la correspondance de la géométrie, voir : [Correspondance par nom](../../features/matching-by-name/matching-by-name.md). |
| **Limites de mappage tonal automatique** | Contrôle la manière dont les valeurs de courbure doivent être écrites dans la texture. Si cette option est activée, la plage de valeurs sera normalisée entre 0 et 1 en fonction des valeurs minimale et maximale trouvées pendant le processus de cuisson. Si cette option est désactivée, les valeurs minimale et maximale sont définies manuellement.  **Remarque :** lors de la cuisson de carreaux UDIM/UV, ce paramètre doit être désactivé pour rendre le mappage tonal uniforme et non spécifique par carreau, sinon cela pourrait créer des coutures entre chaque texture. Pour trouver manuellement les bonnes valeurs min/max, cuire d&#39;abord avec ce paramètre activé, puis examinez la console/le journal pour voir quelles valeurs le boulanger a produites. |
| **Mappage Tonal** | Si l&#39;option **Limites de mappage tonal automatique** est désactivée, définit la valeur minimale pour mettre à l&#39;échelle le résultat de courbure afin qu&#39;il rentre dans la texture. |
| **Mappage Tonal Max** | Si l&#39;option **Limites de mappage tonal automatique** est désactivée, définit la valeur maximale pour mettre à l&#39;échelle le résultat de courbure afin qu&#39;il rentre dans la texture. |
| **Carte des normales** | Tracé facultatif d’une texture normale. Peut être utilisé pour remplacer le calcul interne du boulanger. |
| **Espace universel** | Si cette option est activée, la texture normale est interprétée comme espace universel normal et non comme espace tangent. |
| **Orientation normale** | Format de la texture normale si elle est dans l’espace tangent.Valeurs possibles :<ul data-preserve-html="true"><li data-preserve-html="true"><strong>DirectX</strong> (par défaut)</li><li data-preserve-html="true"><strong>OpenGL</strong></li></ul> |
