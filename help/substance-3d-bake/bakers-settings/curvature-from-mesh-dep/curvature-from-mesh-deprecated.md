---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/bakers-settings/curvature-from-mesh-deprecated.html"
breadcrumb-title: ''
description: Référence de la Courbure obsolète du baker de Maillage. Utilisez plutôt la Courbure mise à jour du baker Maillage.
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
> Depuis Substance Designer 2019.3, ce baker est obsolète et nous vous recommandons d&#39;utiliser le nouveau baker [Courbure du maillage](../../bakers-settings/curvature-from-mesh/curvature-from-mesh.md) à la place.

## Paramètres

| *Paramètre* | *Description* |
| --- | --- |
| **Intensité** | La force des détails de la courbure. Ce paramètre est désactivé si **Saturation tamisée** est activée. |
| **Tamisé** **Saturé** | Si cette option est activée, les détails de la courbure seront adoucis. |
| **Plage maximale** | Si cette option est activée, les détails de la courbure seront ajustés à la capacité de la plage de textures. Cela signifie que les valeurs très fortes seront définies comme le maximum et que toutes les autres valeurs seront mises à l’échelle en fonction de cet extrême. |
