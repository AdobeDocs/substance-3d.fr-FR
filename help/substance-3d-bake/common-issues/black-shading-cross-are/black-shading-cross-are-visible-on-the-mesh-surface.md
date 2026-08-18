---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/common-issues/black-shading-cross-are-visible-on-the-mesh-surface.html"
breadcrumb-title: ''
description: Corrigez les artefacts d'ombrage noir visibles sur les surfaces maillées en corrigeant l'espace tangentiel et les calculs normaux.
helpx_creative_field: ""
helpx_description: bakers > Common Issues > Black shading cross are visible on the mesh surface
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Des croix en ombrage noir sont visibles sur la surface du filet
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 0%

---


# Une croix en ombrage noir est visible sur la surface du filet

Des artefacts en ombrage noir apparaissent sur plusieurs zones du filet lorsque l’éclairage est insuffisant.

![](../../assets/black-shading-cross.jpg)


## Explication

Une croix ombrée noire signifie généralement que la carte normale ne correspond pas au maillage, généralement parce que la géométrie du maillage a changé ou a été calculée d&#39;une manière différente du calcul effectué par le boulanger. Par exemple, la triangulation du filet est différente entre le boulanger et la fenêtre d’affichage qui affiche le filet et sa texture normale.

## Solution

Assurez-vous que l’application affichant le maillage et sa texture normale sont synchronisées avec la façon dont la texture a été cuite. Cela implique :

* Vérifiez que l&#39;espace tangent est identique entre le visualiseur et le boulanger.
* Vérifiez que le format Normal est identique entre la vue et le boulanger.
* Vérifiez que la triangulation est identique entre l&#39;observateur et le boulanger. Voir [cette page](../../guides/triangulating-before-bak/triangulating-before-baking.md) pour plus d&#39;informations.
