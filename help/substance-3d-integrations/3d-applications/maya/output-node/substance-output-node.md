---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/3d-applications/maya/substance-output-node.html"
breadcrumb-title: ''
description: Comprendre comment fonctionnent les nœuds de sortie de Substance dans Maya pour connecter les textures calculées aux réseaux de shader.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > Maya > Substance Output Node
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Nœud de sortie de Substance
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---


# Nœud de sortie de Substance

Le nœud de sortie de Substance est une référence à la texture calculée à partir de la Substance Engine. Il est relié au nœud de Substance. Lorsqu&#39;une sortie est créée sur le nœud de Substance, le moteur de Substance calcule la texture et ces données sont conservées en RAM. Si vous utilisez le moteur GPU, les données sont calculées sur le GPU et renvoyées à la mémoire à l’aide du moteur de Fusion GPU de Substance. Les sorties sur le nœud de Substance qui ne sont pas activées ne sont pas calculées.

![](../../../assets/outputnode.png)

Sur ce nœud, vous pouvez voir les informations de sortie telles que l&#39;Identifiant, l&#39;étiquette et l&#39;utilisation définis sur la sortie dans la Substance Designer. Ce nœud vous permet également de Baker la texture sur le disque dans la section Mise en cache de sortie.
