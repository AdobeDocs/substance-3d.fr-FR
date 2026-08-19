---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/common-issues/black-shading-cross-are-visible-on-the-mesh-surface.html"
breadcrumb-title: ''
description: Correction des artefacts d'ombrage noir visibles sur les surfaces maillées en corrigeant l'espace tangent et les calculs normaux.
helpx_creative_field: ""
helpx_description: bakers > Common Issues > Black shading cross are visible on the mesh surface
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Les ombres noires sont visibles sur la surface du maillage
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 0%

---


# La croix d&#39;ombrage noire est visible sur la surface du maillage

Les artefacts d&#39;ombrage noir apparaissent sur plusieurs zones du maillage lorsque l&#39;éclairage est faible.

![](../../assets/black-shading-cross.jpg)


## Explication

Une croix ombrée noire signifie généralement que la carte normale ne correspond pas au maillage, généralement parce que la géométrie du maillage a changé ou a été calculée d&#39;une manière différente du calcul effectué par le boulanger. Par exemple : la triangulation du maillage est différente entre le boulanger et la fenêtre d’affichage qui effectue le rendu du maillage et de sa texture normale.

## Solution

Assurez-vous que l&#39;application affichant le maillage et sa texture normale sont synchronisées avec la manière dont la texture a été cuite. Cela implique :

* Vérifiez que l&#39;espace tangent est identique entre la visionneuse et le boulanger.
* Vérifiez que le format Normal est identique entre la vue et le boulanger.
* Vérifiez que la Triangulation est identique entre la visionneuse et le boulanger. Voir [cette page](../../guides/triangulating-before-bak/triangulating-before-baking.md) pour plus d’informations.
