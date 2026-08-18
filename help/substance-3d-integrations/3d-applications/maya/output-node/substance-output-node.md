---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-integrations/3d-applications/maya/substance-output-node.html"
breadcrumb-title: ''
description: Découvrez comment fonctionnent les nœuds de sortie de Substance dans Maya pour connecter des textures calculées à des réseaux de nuanceurs.
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

Le nœud de sortie Substance est une référence à la texture calculée à partir de la Substance Engine. Il est relié au nœud de Substance. Lorsqu&#39;une sortie est créée sur le nœud de Substance de données, le moteur de Substance de données calcule la texture et ces données sont conservées en RAM. Si vous utilisez le moteur GPU, les données sont calculées sur le GPU et renvoyées en mémoire à l’aide du moteur de fusion GPU de Substance. Les sorties sur le nœud de Substance qui ne sont pas activées ne sont pas calculées.

![](../../../assets/outputnode.png)

Sur ce nœud, vous pouvez voir les informations de sortie telles que l’identifiant, l’étiquette et l’utilisation définis sur la sortie dans la Substance Designer. Ce nœud vous permet également d’ancrer la texture sur le disque dans la section Mise en cache de la sortie.
