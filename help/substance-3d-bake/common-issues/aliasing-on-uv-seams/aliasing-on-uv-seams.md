---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/common-issues/aliasing-on-uv-seams.html"
breadcrumb-title: ''
description: Correction des artefacts de crénelage qui apparaissent sur les coutures UV lors de la cuisson en ajustant les paramètres d'anti-crénelage et de remplissage.
helpx_creative_field: ""
helpx_description: bakers > Common Issues > Aliasing on UV Seams
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Aliasage sur coutures UV
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 0%

---


# Aliasage sur coutures UV

>[!WARNING]
>
> **Problème**
> 
> Des taches sombres ou des points apparaissent sur le bord des coutures UV après cuisson :
> 
> ![](../../assets/edge-aliasing.png)

>[!NOTE]
>
> **Explication**
> 
> Lorsque Baker écrit des informations dans la texture, elles doivent être converties de la géométrie en pixels. Le traitement de ces informations peut introduire des [alias](https://en.wikipedia.org/wiki/Aliasing). Le crénelage se produit souvent parce que la géométrie des UV n&#39;est pas alignée avec la grille de pixels ou parce que les UV ne couvrent pas suffisamment de pixels pour fournir une résolution suffisante.
> 
> Dans les images suivantes, la géométrie est la superposition rouge. Le boulanger marque un pixel comme plein si plus de la moitié de sa surface est recouverte par la géométrie (les carrés blancs sont des pixels pleins et les carrés noirs sont des pixels vides). Sur l’image de droite, la grille de pixels a une résolution double, ce qui permet une représentation plus précise de la géométrie.
> 
> ![](../../assets/aliasing-example-large.png)
> 
> ![](../../assets/aliasing-example-small.png)

>[!NOTE]
>
> **Solution**
> 
> * Augmentez la résolution de texture de sortie des boulangers.
> * Augmentez le paramètre Anti-crénelage (remarque : le calcul peut prendre plus de temps).
> * Alignez les UV sur la grille de pixels dans l’éditeur d’UV du logiciel de modélisation 3D.
> * Donnez un meilleur rapport Texel aux UV.
