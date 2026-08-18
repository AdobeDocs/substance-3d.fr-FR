---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/common-issues/normal-texture-looks-faceted.html"
breadcrumb-title: ''
description: Corrigez l’apparence des facettes dans les textures normales en lissant les normales du maillage et en ajustant les paramètres du groupe de lissage.
helpx_creative_field: ""
helpx_description: bakers > Common Issues > Normal texture looks faceted
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Texture normale à facettes
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 0%

---


# Texture normale à facettes

>[!WARNING]
>
> **Problème**
> 
> La texture Normale a l&#39;air facettisée ou chaque face du filet y est visible après sa cuisson.
> 
> ![](../../assets/normal-faceted.jpg)

>[!NOTE]
>
> **Explication**
> 
> La raison principale pour laquelle la cuisson d&#39;une normale produirait ce résultat est que les normales de maillage poly bas ne sont pas définies correctement. Chaque bord de chaque face est un bord dur, ce qui fait que la projection des rayons pendant la correspondance avec le maillage en polypole ignore les informations voisines et crée des coutures ou des informations inconscientes. Bien que le résultat semble correct sur le maillage, cela peut entraîner des problèmes d&#39;ombrage par la suite et doit être résolu.

>[!NOTE]
>
> **Solution**
> 
> La solution principale est de retravailler la normale du sommet ou le maillage bas poly, le nom exact du processus dépend du logiciel de modélisation 3D :
> 
> * Utilisez des **normales moyennes** dans Maya, Houdini.
> * Utilisez **un groupe de lissage** dans 3DS Max.
> * Utilisez **une ombre lisse** dans Blender.
> * Les filets exportés à partir de zBrush seront toujours à facettes et devront être nettoyés dans un autre logiciel.
> 
> Notez que cela peut ne pas être suffisant : assurez-vous que les paramètres enregistrent/génèrent également les informations de normale de sommet ou d&#39;ombrage lors de l&#39;exportation d&#39;un filet.
