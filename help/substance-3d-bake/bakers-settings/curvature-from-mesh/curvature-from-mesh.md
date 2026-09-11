---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/bakers-settings/curvature-from-mesh.html"
breadcrumb-title: ''
description: Générez des textures de courbure précises à partir de maillages à poly élevé en utilisant le raytracing pour une détection précise des contours.
helpx_creative_field: ""
helpx_description: bakers > Bakers Settings > Curvature from Mesh
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Courbure du Maillage
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 0%

---


# Courbure du Maillage

La Courbure provenant du baker de maillage génère une texture de courbure provenant de maillages à poly élevé. Il est plus lent que le baker de base de [courbure](../../bakers-settings/curvature/curvature.md), mais produit des résultats plus précis.

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
| **Auto-intersection** | Correspondance par nom de rayons de courbure. Indique comment les bakers doivent correspondre à la géométrie des polygones bas et haut. Il peut être utilisé pour filtrer le processus de baking sans avoir à écarter manuellement les maillages (éclater).Valeurs possibles :<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Toujours</strong> (par défaut) : le maillage de faible niveau de polyvalence correspond à tous les maillages de niveau élevé.</li><li data-preserve-html="true"><strong>Par nom de Maillage</strong> : filtrez les maillages par leur nom pour éviter toute correspondance avec une géométrie indésirable.</li></ul>Pour en savoir plus sur la correspondance de la géométrie, voir : [Correspondance par nom](../../features/matching-by-name/matching-by-name.md). |
| **Limites de mappage tonal automatique** | Contrôle la manière dont les valeurs de courbure doivent être écrites dans la texture. Si cette option est activée, la plage de valeurs sera normalisée entre 0 et 1 en fonction des valeurs minimale et maximale trouvées pendant le processus de baking. Si cette option est désactivée, les valeurs minimale et maximale sont définies manuellement.  **Remarque :** lors du baking des UDIM/Tuiles UV, ce paramètre doit être désactivé pour rendre le mappage de tonalité uniforme et non spécifique par mosaïque, sinon cela peut créer des seams entre chaque texture. Pour rechercher manuellement les bonnes valeurs min/max, bakez d’abord avec ce paramètre activé, puis examinez la console/le journal pour voir quelles valeurs le baker a générées. |
| **Mappage Tonal** | Si **Limites de mappage tonal automatique** est désactivé, définit la valeur minimale pour mettre à l&#39;échelle le résultat de la courbure afin qu&#39;il rentre dans la texture. |
| **Mappage Tonal Max** | Si **Limites de mappage tonal automatique** est désactivé, définit la valeur maximale pour mettre à l&#39;échelle le résultat de la courbure afin qu&#39;il rentre dans la texture. |
| **Map normal** | Chemin facultatif vers une texture normale. Peut être utilisé pour remplacer le calcul intérieur du baker. |
| **Espace monde** | Si cette option est activée, la texture normale est interprétée comme une Normale de l&#39;espace monde et non comme un Repère tangent. |
| **Orientation normale** | Format de la texture Normal si dans Repère tangent.Valeurs possibles :<ul data-preserve-html="true"><li data-preserve-html="true"><strong>DirectX</strong> (par défaut)</li><li data-preserve-html="true"><strong>OpenGL</strong></li></ul> |
