---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-bake/common-issues/aliasing-on-uv-seams.html"
breadcrumb-title: ''
description: Corrigez les artefacts de crénelage qui apparaissent sur les coutures UV pendant la cuisson en ajustant les paramètres de lissage et de remplissage.
helpx_creative_field: ""
helpx_description: bakers > Common Issues > Aliasing on UV Seams
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Crénelage sur les coutures UV
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 0%

---


# Crénelage sur les coutures UV

>[!WARNING]
>
> **Problème**
> 
> Des points ou points sombres apparaissent sur la bordure des coutures UV après la cuisson :
> 
> ![](../../assets/edge-aliasing.png)

>[!NOTE]
>
> **Explication**
> 
> Lorsque le boulanger écrit des informations dans la texture, celles-ci doivent être converties de la géométrie en pixels. Le traitement de ces informations peut introduire un [crénelage](https://en.wikipedia.org/wiki/Aliasing). Le crénelage se produit souvent parce que la géométrie des UV n’est pas alignée avec la grille de pixels ou parce que les UV ne couvrent pas suffisamment de pixels pour fournir une résolution suffisante.
> 
> Dans les images suivantes, la géométrie est l&#39;incrustation rouge. Le boulanger marque un pixel comme plein si plus de la moitié de sa surface est couverte par la géométrie (les carrés blancs sont des pixels pleins et les carrés noirs sont des pixels vides). Sur l&#39;image de droite, la grille de pixels a une résolution double, ce qui permet une représentation plus précise de la géométrie.
> 
> ![](../../assets/aliasing-example-large.png)
> 
> ![](../../assets/aliasing-example-small.png)

>[!NOTE]
>
> **Solution**
> 
> * Augmentez la résolution de la texture de sortie des boulangers.
> * Augmentez le paramètre de lissage (remarque : le calcul peut prendre plus de temps).
> * Alignez les UV sur la grille de pixels dans l’éditeur UV du logiciel de modélisation 3D.
> * Donnez un meilleur rapport Texel aux UV.
