---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-bake/bakers-settings/curvature-from-mesh.html"
breadcrumb-title: ''
description: Générez des textures de courbure précises à partir de maillages à poly élevé à l'aide du lancer de rayons pour une détection de bord précise.
helpx_creative_field: ""
helpx_description: bakers > Bakers Settings > Curvature from Mesh
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Courbure du maillage
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 0%

---


# Courbure du maillage

La texture de courbure de mesh baker génère une texture de courbure à partir de maillages à poly élevé. Elle est plus lente que la base [courbure](../../bakers-settings/curvature/curvature.md) mais produit des résultats plus précis.

**Disponible en :**

* Concepteur de substance
* Boîte à outils d&#39;automatisation des substances
* Substance Painter

## Paramètres

| *Paramètre* | *Description* |
| --- | --- |
| **Rayons secondaires** | Quantité de rayons émis pour lire la géométrie voisine. Une valeur élevée produira moins de bruit, mais son calcul sera plus long. La valeur par défaut est 32. |
| **Rayon d’échantillonnage** | Mesure dans laquelle la géométrie voisine est prise en compte pour calculer la courbure à la surface de la géométrie. Des valeurs élevées peuvent produire des arêtes plus fortes tandis que des valeurs plus faibles peuvent produire des arêtes plus fines mais ne pas fournir d&#39;informations. |
| **Relatif Au Cadre De Sélection** | Définit si le rayon d&#39;échantillonnage est relatif à la taille du maillage ou s&#39;il est défini comme une distance basée sur une unité. |
| **Intersection automatique** | Correspondance par nom des rayons de courbure. Indique comment les boulangers doivent correspondre à une géométrie de poly faible et élevé. Il peut être utilisé pour filtrer le processus de cuisson sans avoir à séparer manuellement les maillages (éclater).Valeurs possibles :<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Always</strong> (par défaut) : un maillage low-poly est mis en correspondance avec chaque maillage high-poly.</li><li data-preserve-html="true"><strong>Par nom de maillage</strong> : filtrez les maillages en fonction de leur nom pour éviter toute correspondance avec une géométrie indésirable.</li></ul>Pour en savoir plus sur la correspondance de géométries, voir : [Correspondance par nom](../../features/matching-by-name/matching-by-name.md). |
| **Limites automatiques du mappage de tonalité** | Contrôle la manière dont les valeurs de courbure doivent être écrites dans la texture. Si cette option est activée, la plage de valeurs sera normalisée entre 0 et 1 en fonction des valeurs minimale et maximale trouvées pendant le processus de cuisson. Si cette option est désactivée, les valeurs minimale et maximale sont définies manuellement.  **Remarque :** lors de la cuisson de tuiles UDIM/UV, ce paramètre doit être désactivé pour rendre le mappage de tons uniforme et non spécifique par tuile, sinon cela pourrait créer des jointures entre chaque texture. Pour trouver manuellement les bonnes valeurs min/max, cuire d&#39;abord avec ce paramètre activé, puis jetez un œil à la console/au journal pour voir quelles valeurs le boulanger a produit. |
| **Min Tonemapping** | Si l&#39;option **Limites automatiques de correspondance de ton** est désactivée, définit la valeur minimale pour mettre à l&#39;échelle le résultat de la courbure afin qu&#39;il s&#39;adapte à la texture. |
| **Mappage de tonalité max** | Si l&#39;option **Limites de mappage automatique de la tonalité** est désactivée, définit la valeur maximale pour mettre à l&#39;échelle le résultat de la courbure afin qu&#39;il s&#39;adapte à la texture. |
| **Carte normale** | Chemin facultatif vers une texture normale. Peut être utilisé pour remplacer le calcul interne du boulanger. |
| **Espace mondial** | Si cette option est activée, la texture normale est interprétée comme normale de l&#39;espace universel au lieu d&#39;un espace tangent. |
| **Orientation normale** | Format de la texture Normale si dans l&#39;Espace Tangent. Valeurs possibles :<ul data-preserve-html="true"><li data-preserve-html="true"><strong>DirectX</strong> (par défaut)</li><li data-preserve-html="true"><strong>OpenGL </strong></li></ul> |
