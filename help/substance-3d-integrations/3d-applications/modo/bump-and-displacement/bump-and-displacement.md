---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/3d-applications/modo/bump-and-displacement.html"
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

La Substance peut avoir une sortie height facultative. Vous pouvez l’utiliser comme displacement ou bosse. Lorsque vous activez l’height, il est défini sur l’effet de texture relief. Pour Unity, il sera réglé sur Unity Bump et Unreal sera Unreal Bump. Vous pouvez ensuite sélectionner la matière de l&#39;élément de Substance et définir l&#39;amplitude de relief en conséquence. Si vous souhaitez utiliser l’height comme displacement, vous pouvez modifier l’effet de calque Matériau sur Ombrage de surface > Displacement. Ensuite, dans la Référence de matière, définissez la distance de Displacement appropriée.

![](../../../assets/bump-1.png)

Dans cet exemple, j’ai utilisé le matériau Irréel, mais j’ai remplacé l’effet de calque Relief irréel par Displacement. Ensuite, sur la matière de l&#39;élément de Substance, je définis la distance du Displacement et le niveau de subdivision de rendu en conséquence.

![](../../../assets/dis.png)
