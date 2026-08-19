---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/bakers-settings/curvature.html"
breadcrumb-title: ''
description: Extrayez les informations de courbure du maillage pour créer des textures qui mettent en évidence les cavités et les arêtes de la géométrie.
helpx_creative_field: ""
helpx_description: bakers > Bakers Settings > Curvature
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Courbure
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 3%

---


# Courbure

Le Curvature baker permet d&#39;extraire une texture de courbure. Cette texture contient des informations sur les cavités et les arêtes liées à la géométrie.

Les propriétés de texture sont définies comme suit :

* Les valeurs noires représentent des zones concaves.
* Les valeurs blanches représentent des zones convexes.
* Les valeurs de gris représentent des zones neutres (principalement plates).

**Disponible dans :**

* Concepteur de substance
* Boîte à outils d&#39;automatisation des substances
* Substance Painter

## Paramètres

| *Paramètre* | *Description* |
| --- | --- |
| **Algorithme** | Définit la manière dont les informations de courbure seront calculées sur le maillage. |
| **Détails** | Contrôle la force des informations dans la courbure. Une valeur élevée peut produire plus de détails, mais moins subtils. |
| **Activer les coutures** | Si cette option est activée, le boulanger essaiera de réduire les jointures entre les îles UV en copiant les texels aux bordures d&#39;un côté à l&#39;autre. |
| **Coutures** **Intensité** | Si **Activer les coutures** est activé, ce paramètre contrôle la force de la fixation des coutures. |
