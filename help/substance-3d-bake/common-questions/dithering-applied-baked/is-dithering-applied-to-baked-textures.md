---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/common-questions/is-dithering-applied-to-baked-textures.html"
breadcrumb-title: ''
description: Découvrez si l’interpolation est appliquée aux textures cuites et comment elle affecte la qualité de la texture.
helpx_creative_field: ""
helpx_description: "bakers > Common Questions > Is dithering applied to baked textures "
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 'L’interpolation est-elle appliquée aux textures cuites ? '
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 0%

---


# L’interpolation est-elle appliquée aux textures cuites ?

>[!WARNING]
>
> **Question**
> 
> Les Bakers prennent-ils en charge le [tramage](https://en.wikipedia.org/wiki/Dither) de texture et, le cas échéant, quand est-il appliqué ?

>[!NOTE]
>
> **Explication**
> 
> L’interpolation est appliquée pour éviter les effets de bande dans les cartes normales 8 bits, par exemple :
> 
> ![](../../assets/dither.jpg)

>[!NOTE]
>
> **Solution : Substance Designer**
> 
> L’interpolation est automatiquement appliquée dans les situations suivantes :
> 
> * Lors de l’enregistrement d’une sortie Baker dans un fichier de texture 8 bits
> * Lorsqu’une sortie Baker est utilisée dans un nœud bitmap d’un graphique défini sur 8 bits.

>[!NOTE]
>
> **Solution : Substance Painter**
> 
> L’interpolation est une option qui peut être activée ou désactivée pendant le processus d’exportation. Elle s’applique uniquement lors de l’exportation au format de fichier 8 bits pour les canaux Normal, Displacement et Height.

>[!NOTE]
>
> **Solution : Substance Automation Toolkit**
> 
> L’interpolation n’est pas prise en charge pour le moment.
