---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-bake/common-issues/seams-are-visible-after-baking-a-normal-texture.html"
breadcrumb-title: ''
description: Éliminez les coutures visibles dans les textures normales cuites en ajustant le remplissage, le lissage et la disposition UV.
helpx_creative_field: ""
helpx_description: bakers > Common Issues > Seams are visible after baking a normal texture
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Les coutures sont visibles après cuisson d'une texture normale
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 0%

---


# Les coutures sont visibles après cuisson d&#39;une texture normale

>[!WARNING]
>
> **Problème**
> 
> Les coutures normales de la carte sont visibles au niveau des bordures UV du maillage, même après une cuisson propre.

>[!NOTE]
>
> **Explication**
> 
> Même après une cuisson parfaite, les coutures peuvent encore être visibles. La raison principale est qu&#39;une information de surface approximative normale est dans une texture. Parfois, la texture manque de précision ou doit compenser trop de choses entre la géométrie de poly basse et haute pour être suffisamment précise. Dans d&#39;autres cas, le rendu de la géométrie avec sa texture normale peut affecter son aspect.

>[!NOTE]
>
> **Solution**
> 
> Quelques solutions possibles peuvent être essayées pour réduire l&#39;intensité des coutures avec des cartes normales :
> 
> * Souvent, les UV ne sont pas alignés sur les pixels, ce qui entraîne un crénelage et produit des jointures. Voir [cette page](../../common-issues/aliasing-on-uv-seams/aliasing-on-uv-seams.md) pour plus d’informations.
>   * L’augmentation de la résolution de la texture peut être un moyen de réduire cet effet.
>   * L’alignement des bordures UV sur les pixels est une autre façon de réduire cet effet.
> * Augmentez le paramètre **qualité** du nuanceur. La qualité de l&#39;ombrage peut affecter la façon dont les réflexions spéculaires sont calculées. Si certains îlots UV sont tournés et que ce paramètre est trop faible, il peut produire des coutures visibles. Voir [cette page](https://helpx.adobe.com/fr/substance-3d/unlisted/documentation/spdoc/pbr-metal-rough-172818827.html) pour plus d’informations.
