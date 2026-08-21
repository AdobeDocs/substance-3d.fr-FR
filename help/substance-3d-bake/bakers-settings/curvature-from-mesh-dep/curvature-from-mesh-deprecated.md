---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-bake/bakers-settings/curvature-from-mesh-deprecated.html"
breadcrumb-title: ''
description: Référence pour la courbe obsolète de Mesh baker. Utilisez plutôt la courbure mise à jour de Mesh baker.
helpx_creative_field: ""
helpx_description: bakers > Bakers Settings > Curvature from Mesh (deprecated)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Courbure du maillage (obsolète)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 0%

---


# Courbure du maillage (obsolète)

La texture de courbure de mesh baker génère une texture de courbure à partir de maillages à poly élevé. Elle est plus lente que la base [courbure](../../bakers-settings/curvature/curvature.md) mais produit des résultats plus précis.

**Disponible en :**

* Concepteur de substance
* Boîte à outils d&#39;automatisation des substances

>[!NOTE]
>
> Depuis Substance Designer 2019.3, ce boulanger est obsolète et nous vous recommandons d&#39;utiliser plutôt le nouveau boulanger [Curvature from mesh](../../bakers-settings/curvature-from-mesh/curvature-from-mesh.md).

## Paramètres

| *Paramètre* | *Description* |
| --- | --- |
| **Intensité** | Intensité des détails de courbure. Ce paramètre est désactivé si **Saturation douce** est activé. |
| **Doux** **Saturé** | Si cette option est activée, les détails de la courbure sont adoucis. |
| **Maximiser la plage** | Si cette option est activée, les détails de la courbure seront ajustés à l&#39;intérieur de la capacité de la plage de texture. Cela signifie que des valeurs très fortes seront définies comme le maximum et que toutes les autres valeurs seront mises à l’échelle en fonction de cette valeur extrême. |
