---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unity/optimization-guidelines.html"
breadcrumb-title: ''
description: Suivez les directives d’optimisation pour équilibrer la complexité des matériaux de Substance avec les performances de rendu dans Unity.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unity > Optimization Guidelines
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Directives d’optimisation
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4a060ee1aaa1731c04e70d5512e3271cd63d0381
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 0%

---


# Directives d’optimisation

Plus les matériaux de Substance sont complexes, plus la puissance de traitement nécessaire à leur rendu est importante. Les matériaux de Substance doivent donc **trouver un équilibre entre complexité et vitesse de rendu**. Cela est *particulièrement* important s&#39;ils sont utilisés dans des applications graphiques en temps réel, telles que les jeux.

Lors de la création de vos propres matériaux de Substance personnalisés, veillez à suivre les instructions d’optimisation ci-dessous.

[Directives d’optimisation des Substances Designer](https://docs.substance3d.com/display/SDDOC/Performance+Optimization+Guidelines)

Les nœuds dont la résolution absolue est égale ou supérieure à 4K constituent une mise en garde importante.

>[!WARNING]
>
> **Faites attention aux paramètres de résolution et de rapport à la résolution parent !**\
> Les valeurs élevées affectent considérablement les performances. Pensez donc à la manière dont le matériau est susceptible d&#39;être utilisé et à la possibilité de réduire la taille des données concernées.
>   
> Le moteur CPU de la Substance peut calculer à 4K, mais il est très lent et peut provoquer un blocage ou un éventuel blocage de l’intégration.

Dans l&#39;exemple suivant, la taille de sortie d&#39;un nœud [Tile Sampler](https://experienceleague.adobe.com/en/docs/substance-3d-designer/using/substance-graphs/nodes-reference-for-substance-graphs/node-library/texture-generators/patterns/tile-sampler) est définie sur [Absolue](https://experienceleague.adobe.com/en/docs/substance-3d-designer/using/substance-graphs/output-size) 4096. Il force plusieurs nœuds en aval à calculer à 4K avant d’être réduit pour la résolution de sortie finale de 2048.

![](../../../assets/absolute.png){width="1000px"}
