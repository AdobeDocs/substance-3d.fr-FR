---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-integrations/3d-applications/modo/bump-and-displacement.html"
breadcrumb-title: ''
description: Utilisez les cartes de relief et de displacement des matériaux de Substance dans MODO pour ajouter des détails de surface et de la profondeur à vos modèles.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > MODO > Bump and Displacement
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Bosse et Displacement
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 0%

---


# Bosse et Displacement

Utilisation des reliefs et des Displacements

La Substance peut avoir une sortie height facultative. Vous pouvez l’utiliser comme displacement ou bosse. Lorsque vous activez l’height, il est défini sur l’effet texture de relief. Pour Unity, il sera réglé sur Unity Bump et Unreal sera Unreal Bump. Vous pouvez ensuite sélectionner le matériau de l’élément de Substance et définir l’amplitude de relief en conséquence. Si vous souhaitez utiliser l’height comme displacement, vous pouvez modifier l’effet de calque de Matériau sur Ombrage de surface > Displacement. Ensuite, dans la référence de Matériau, définissez la distance de Displacement appropriée.

![](../../../assets/bump-1.png)

Dans cet exemple, j’ai utilisé l’effet matériau irréel, mais j’ai remplacé l’effet Calque relief irréel par Displacement. Ensuite, sur le Matériau de l&#39;élément de Substance, je définis la distance du Displacement et le niveau de subdivision de rendu en conséquence.

![](../../../assets/dis.png)
