---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-bake/bakers-settings/curvature.html"
breadcrumb-title: ''
description: Extrayez les informations de courbure de votre maillage pour créer des textures qui mettent en évidence les cavités et les bords de votre géométrie.
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

Le baker Curvature permet d&#39;extraire une texture de courbure. Cette texture contient des informations sur les cavités et les arêtes associées à la géométrie.

Les propriétés de texture sont définies comme suit :

* Les valeurs noires représentent les zones concaves.
* Les valeurs de blanc représentent des zones convexes.
* Les valeurs de gris représentent des zones neutres (principalement plates).

**Disponible dans :**

* Substance Designer
* Substance Automation Toolkit
* Substance Painter

## Paramètres

| *Paramètre* | *Description* |
| --- | --- |
| **Algorithme** | Définit le mode de calcul des informations de courbure sur le maillage. |
| **Détails** | Contrôle la force des informations dans la courbure. Une valeur élevée peut produire plus de détails, mais moins subtils. |
| **Activer les coutures** | Si cette option est activée, le boulanger tente de réduire les coutures entre les Îlots UV en copiant les texels au niveau des bordures d’un côté à l’autre. |
| **Coutures** **Intensité** | Si **Activer les coutures** est activé, ce paramètre contrôle la force de la correction des coutures. |
