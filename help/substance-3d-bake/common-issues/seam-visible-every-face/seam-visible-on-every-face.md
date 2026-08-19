---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/common-issues/seam-visible-on-every-face.html"
breadcrumb-title: ''
description: Corrigez les coutures visibles sur chaque face en vérifiant le déballage UV, les groupes de lissage et les problèmes de topologie de maillage.
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
> Une soudure est visible sur quelques arêtes de la géométrie, même si aucune soudure UV n&#39;est présente :
> 
> ![](../../assets/seam-every-face.jpg)

>[!NOTE]
>
> **Explication**
> 
> Si vous n&#39;utilisez pas de [cage](https://helpx.adobe.com/substance-3d/unlisted/documentation/bake/cage-projection-172822982.html), le processus de Baking lancera des rayons dans la direction des normales des sommets du maillage à faible poly. Si chaque normale de sommet est fractionnée (ce qui signifie que chaque face ne partage pas les mêmes normales de sommet que la face voisine), les rayons ne seront pas envoyés dans la même direction sur les arêtes. Il en résulte un fractionnement, car les informations de chaque côté des arêtes sont différentes.
> 
> Ce problème est également exacerbé par les alias, comme expliqué dans [cette page](../../common-issues/aliasing-on-uv-seams/aliasing-on-uv-seams.md).

>[!NOTE]
>
> **Solution**
> 
> Seules deux solutions sont possibles ici :
> 
> * Utilisez une [cage](https://helpx.adobe.com/substance-3d/unlisted/documentation/bake/cage-projection-172822982.html) pour contrôler la direction du rayon au lieu de laisser le boulanger le calculer à partir de la géométrie low-poly.
> * Fusionner les normales des sommets du maillage bas-poly ensemble (les adoucir / appliquer un groupe de lissage commun).
