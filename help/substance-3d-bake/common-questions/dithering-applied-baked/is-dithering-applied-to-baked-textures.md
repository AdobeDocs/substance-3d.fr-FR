---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-bake/common-questions/is-dithering-applied-to-baked-textures.html"
breadcrumb-title: ''
description: Déterminez si le tramage est appliqué aux textures cuites et comment il affecte la qualité de la texture.
helpx_creative_field: ""
helpx_description: "bakers > Common Questions > Is dithering applied to baked textures "
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 'Le tramage est-il appliqué aux textures cuites ? '
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 0%

---


# Le tramage est-il appliqué aux textures cuites au four ?

>[!WARNING]
>
> **Question**
> 
> Les Bakers supportent-ils la texture [tramage](https://en.wikipedia.org/wiki/Dither) et si oui, quand est-ce qu&#39;elle est appliquée ?

>[!NOTE]
>
> **Explication**
> 
> Le tramage est appliqué pour éviter le bandage dans les mappages normaux 8 bits par exemple :
> 
> ![](../../assets/dither.jpg)

>[!NOTE]
>
> **Solution : Concepteur de substance**
> 
> Le tramage est automatiquement appliqué dans les situations suivantes :
> 
> * Lorsqu’une sortie Baker est enregistrée dans un fichier de texture 8 bits
> * Lorsqu’une sortie Baker est utilisée dans un nœud bitmap d’un graphique défini sur 8 bits.

>[!NOTE]
>
> **Solution : Peintre De Substance**
> 
> Le tramage est une option qui peut être activée ou désactivée pendant le processus d’exportation. Elle est uniquement appliquée lors de l’exportation au format de fichier 8 bits pour les canaux Normal, Déplacement et Hauteur.

>[!NOTE]
>
> **Solution : Substance Automation Toolkit**
> 
> Le tramage n’est pas pris en charge pour le moment.
