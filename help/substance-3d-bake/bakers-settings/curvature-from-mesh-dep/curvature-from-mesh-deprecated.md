---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-bake/bakers-settings/curvature-from-mesh-deprecated.html"
breadcrumb-title: ''
description: Référence pour la courbe obsolète de Mesh baker. Utilisez plutôt la courbe mise à jour de Mesh Baker.
helpx_creative_field: ""
helpx_description: bakers > Bakers Settings > Curvature from Mesh (deprecated)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Courbure à partir du filet (obsolète)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 0%

---


# Courbure à partir du filet (obsolète)

La courbure du boulanger de maillage génère une texture de courbure à partir de maillages à poly élevé. Il est plus lent que le boulanger de base [courbure](../../bakers-settings/curvature/curvature.md), mais produit des résultats plus précis.

**Disponible dans :**

* Substance Designer
* Substance Automation Toolkit

>[!NOTE]
>
> Depuis Substance Designer 2019.3, ce boulanger est obsolète. Nous vous recommandons donc d&#39;utiliser le nouveau boulanger [Courbure à partir du maillage](../../bakers-settings/curvature-from-mesh/curvature-from-mesh.md).

## Paramètres

| *Paramètre* | *Description* |
| --- | --- |
| **Intensité** | Intensité des détails de courbure. Ce paramètre est désactivé si **Saturation tamisée** est activée. |
| **Tamisé** **Saturé** | Si cette option est activée, les détails de la courbure seront adoucis. |
| **Agrandir la plage** | Si cette option est activée, les détails de la courbure s’adaptent à la capacité de la plage de textures. Cela signifie que les valeurs très fortes seront définies comme le maximum et que toutes les autres valeurs seront mises à l’échelle en fonction de cet extrême. |
