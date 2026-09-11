---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-bake/common-issues/normal-texture-looks-faceted.html"
breadcrumb-title: ''
description: Corrigez les textures normales à facettes en lissant les normales des maillages et en ajustant les paramètres du groupe de lissage.
helpx_creative_field: ""
helpx_description: bakers > Common Issues > Normal texture looks faceted
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: La texture normale semble facettisée
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 0%

---


# La texture normale semble facettisée

>[!WARNING]
>
> **Problème**
> 
> La texture Normale a l&#39;air à facettes ou chaque face du maillage y est visible après le baking.
> 
> ![](../../assets/normal-faceted.jpg)

>[!NOTE]
>
> **Explication**
> 
> La principale raison pour laquelle baker une normale produirait ce résultat est que les normales ne sont pas définies correctement. Chaque bord de chaque face est un bord dur, ce qui fait que la projection de rayon pendant l&#39;appariement avec le maillage de haut-poly ignore l&#39;information de voisinage et crée des seams ou des informations inconscientes. Même si le résultat peut sembler correct sur le maillage, cela peut entraîner des problèmes d’ombrage par la suite et doit être résolu.

>[!NOTE]
>
> **Solution**
> 
> La solution principale est de retravailler la normale du vertex ou le maillage low poly, le nom exact du processus dépend du logiciel de modélisation 3D :
> 
> * Utilisez des **normales moyennes** dans Maya, Houdini.
> * Utilisez **un groupe de lissage** dans 3DS Max.
> * Utilisez **une ombre lisse** dans Blender.
> * Les maillages exportés depuis zBrush seront toujours à facettes et devront être nettoyés dans un autre logiciel.
> 
> Notez que ce n’est peut-être pas suffisant : assurez-vous que les paramètres enregistrent/génèrent également les informations de normalité ou d’ombrage du vertex lors de l’exportation d’un maillage.
