---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-bake/common-issues/black-shading-cross-are-visible-on-the-mesh-surface.html"
breadcrumb-title: ''
description: Corrigez les artefacts en ombrage noir visibles sur les surfaces du maillage en corrigeant l’espace de tangente et les calculs normaux.
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


# Croix en ombrage noire visible sur la surface du maillage

Des artefacts en ombrage noir apparaissent sur plusieurs zones du maillage lorsque l’éclairage est insuffisant.

![](../../assets/black-shading-cross.jpg)


## Explication

Une croix ombrée noire signifie généralement que la map normal ne correspond pas au maillage, généralement parce que la géométrie du maillage a changé ou a été calculée d’une manière différente du calcul effectué par le baker. Par exemple : la triangulation du maillage est différente entre le baker et le viewport qui rend le maillage et sa map normal.

## Solution

Assurez-vous que l’application affichant le maillage et sa map normal sont synchronisées avec la façon dont la texture a été bake. Cela implique :

* Vérifiez que le Repère tangent est identique entre le lecteur et le baker.
* Vérifiez que le format Normal est identique entre la vue et le baker.
* Vérifiez que la triangulation est identique entre le visualiseur et le baker. Voir [cette page](../../guides/triangulating-before-bak/triangulating-before-baking.md) pour plus d&#39;informations.
