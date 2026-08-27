---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-bake/common-questions/is-dithering-applied-to-baked-textures.html"
breadcrumb-title: ''
description: Comprendre si le dithering est appliqué à des textures bake et comment il affecte la qualité de la texture.
helpx_creative_field: ""
helpx_description: "bakers > Common Questions > Is dithering applied to baked textures "
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 'Application du dithering aux textures bake '
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 0%

---


# Le dithering est-il appliqué aux textures bake ?

>[!WARNING]
>
> **Question**
> 
> Les Bakers prennent-ils en charge la texture [dithering](https://en.wikipedia.org/wiki/Dither) et, dans l&#39;affirmative, quand est-elle appliquée ?

>[!NOTE]
>
> **Explication**
> 
> Le dithering est utilisé pour éviter les effets de bande dans les maps normal 8 bits, par exemple :
> 
> ![](../../assets/dither.jpg)

>[!NOTE]
>
> **Solution : Substance Designer**
> 
> Le dithering est automatiquement appliqué dans les situations suivantes :
> 
> * Lors de l’enregistrement d’une sortie de Baker dans un fichier de texture 8 bits
> * Lorsqu’une sortie de Baker est utilisée dans un nœud bitmap d’un graphe défini sur 8 bits.

>[!NOTE]
>
> **Solution : Substance Painter**
> 
> Dithering est une option qui peut être activée ou désactivée pendant le processus d’exportation. Elle s’applique uniquement lors de l’exportation au format de fichier 8 bits pour les canaux Normal, Displacement et Height.

>[!NOTE]
>
> **Solution : Substance Automation Toolkit**
> 
> Dithering n’est pas pris en charge pour le moment.
