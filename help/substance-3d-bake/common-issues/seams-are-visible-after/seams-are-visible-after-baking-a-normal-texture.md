---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/common-issues/seams-are-visible-after-baking-a-normal-texture.html"
breadcrumb-title: ''
description: Éliminez les coutures visibles dans les textures normales cuites en ajustant le remplissage, l’anticrénelage et la disposition UV.
helpx_creative_field: ""
helpx_description: bakers > Common Issues > Seams are visible after baking a normal texture
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Les coutures sont visibles après cuisson d’une texture normale
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 0%

---


# Les coutures sont visibles après cuisson d’une texture normale

>[!WARNING]
>
> **Problème**
> 
> Les coutures de texture normales sont visibles aux bordures UV du filet, même après un cuisson propre.

>[!NOTE]
>
> **Explication**
> 
> Même après une cuisson parfaite, les coutures peuvent toujours être visibles. La raison principale est qu&#39;une information de surface approximative normale dans une texture. Parfois, la texture manque de précision ou doit trop compenser la géométrie des poly faible et élevé pour être suffisamment précise. Dans d&#39;autres cas, le rendu de la géométrie avec sa texture normale peut affecter son aspect.

>[!NOTE]
>
> **Solution**
> 
> Quelques solutions possibles peuvent être essayées pour réduire l&#39;intensité des coutures avec des cartes normales :
> 
> * Souvent, les UV ne sont pas alignés sur les pixels, ce qui entraîne un crénelage et produit des coutures. Voir [cette page](../../common-issues/aliasing-on-uv-seams/aliasing-on-uv-seams.md) pour plus d&#39;informations.
>   * L’augmentation de la résolution de la texture peut réduire cet effet.
>   * L’alignement des bordures UV sur les pixels est un autre moyen de réduire cet effet.
> * Augmentez le paramètre de **qualité** du shader. La qualité de l’ombrage peut affecter le calcul des reflets de specular. Si certains Îlots UV subissent une rotation et que ce paramètre est trop faible, des coutures visibles peuvent apparaître. Voir [cette page](https://helpx.adobe.com/substance-3d/unlisted/documentation/spdoc/pbr-metal-rough-172818827.html) pour plus d&#39;informations.
