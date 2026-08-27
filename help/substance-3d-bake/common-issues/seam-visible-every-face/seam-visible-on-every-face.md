---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-bake/common-issues/seam-visible-on-every-face.html"
breadcrumb-title: ''
description: Corrigez les seams visibles sur chaque face en vérifiant l’UV, le lissage des groupes et les problèmes de topologie de maillage.
helpx_creative_field: ""
helpx_description: bakers > Common Issues > Seam visible on every face
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Couture visible sur chaque face
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 0%

---


# Couture visible sur chaque face

>[!WARNING]
>
> **Problème**
> 
> Un seam est visible sur quelques arêtes de la géométrie même s&#39;il n&#39;y a aucun seam présent :
> 
> ![](../../assets/seam-every-face.jpg)

>[!NOTE]
>
> **Explication**
> 
> Si vous n&#39;utilisez pas de [cage](https://helpx.adobe.com/fr/substance-3d/unlisted/documentation/bake/cage-projection-172822982.html), le processus de Bake lancera des rayons dans la direction des normales de vertex du maillage en bas-poly. Si chaque normale de vertex est divisée (ce qui signifie que chaque face ne partage pas les mêmes normales de vertex que la face voisine), les rayons ne seront pas envoyés dans la même direction sur les . Cela entraîne une division car les informations de chaque côté des arêtes sont différentes.
> 
> Ce problème est également exacerbé par le crénelage, comme expliqué dans [cette page](../../common-issues/aliasing-on-uv-seams/aliasing-on-uv-seams.md).

>[!NOTE]
>
> **Solution**
> 
> Seules deux solutions sont possibles ici :
> 
> * Utilisez une [cage](https://helpx.adobe.com/fr/substance-3d/unlisted/documentation/bake/cage-projection-172822982.html) pour contrôler la direction du rayon au lieu de laisser le baker le calculer à partir de la géométrie en bas-poly.
> * Fusionnez les normales de vertex du maillage low-poly (adoucissez-les / appliquez un groupe de lissage commun).
