---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-bake/common-issues/normal-texture-looks-faceted.html"
breadcrumb-title: ''
description: Correction de l'aspect des facettes dans les textures normales en lissant les normales des maillages et en ajustant les paramètres des groupes de lissage.
helpx_creative_field: ""
helpx_description: bakers > Common Issues > Normal texture looks faceted
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: La texture normale a l'air facettisée
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 0%

---


# La texture normale a l&#39;air facettisée

>[!WARNING]
>
> **Problème**
> 
> La texture Normale ressemble à une facette ou chaque face du maillage y est visible après cuisson.
> 
> ![](../../assets/normal-faceted.jpg)

>[!NOTE]
>
> **Explication**
> 
> La raison principale pour laquelle la cuisson d&#39;une normale produirait ce résultat est que les normales à maillage poly bas ne sont pas définies correctement. Chaque arête de chaque face est une arête dure, ce qui fait que la projection des rayons lors de la correspondance avec le maillage de poly élevé ignore les informations de voisinage et crée des jointures ou des informations inconscientes. Bien que le résultat puisse sembler correct sur le maillage, cela peut entraîner des problèmes d&#39;ombrage ultérieurement et doit être résolu.

>[!NOTE]
>
> **Solution**
> 
> La solution principale est de retravailler la normale du sommet ou le maillage bas poly, le nom exact du processus dépend du logiciel de modélisation 3D :
> 
> * Utilisez **normales moyennes** en Maya, Houdini.
> * Utilisez **un groupe de lissage** dans 3DS Max.
> * Utilisez **ombrage lisse** dans Blender.
> * Les maillages exportés depuis zBrush seront toujours à facettes et doivent être nettoyés dans un autre logiciel.
> 
> Notez que ce n&#39;est peut-être pas suffisant : assurez-vous que les paramètres enregistrent/génèrent également la normale au sommet ou les informations d&#39;ombrage lors de l&#39;exportation d&#39;un maillage.
