---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/common-issues/mesh-parts-bleed-between-each-other.html"
breadcrumb-title: ''
description: Empêchez les pièces de maillage de se fondre les unes dans les autres pendant la cuisson en utilisant l'option Correspondance par nom ou en ajustant les distances.
helpx_creative_field: ""
helpx_description: bakers > Common Issues > Mesh parts bleed between each other
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Les parties du maillage se fondent les unes dans les autres
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 0%

---


# Les parties du maillage se fondent les unes dans les autres

>[!WARNING]
>
> **Problème**
> 
> La géométrie du maillage est appliquée à d&#39;autres pièces et crée des artefacts.
> 
> ![](../../assets/bleed-example.png)

>[!NOTE]
>
> **Explication**
> 
> Le processus de cuisson envoie des rayons de la surface de maille à faible poly pour atteindre la maille à fort poly pour créer une correspondance. Parfois, les rayons vont trop loin et atteignent la mauvaise géométrie, créant le saignement et les artefacts.

>[!NOTE]
>
> **Solution**
> 
> Quelques solutions sont disponibles pour éviter ce problème :
> 
> * Utilisez la fonction [ Correspondance par nom ](../../features/matching-by-name/matching-by-name.md) pour isoler les maillages
> * Utilisez une [cage](https://helpx.adobe.com/substance-3d/unlisted/documentation/bake/cage-projection-172822982.html) pour limiter la distance de rayon.
> * Remplacez la distance de rayon par défaut dans les paramètres communs de baker par une valeur inférieure.
