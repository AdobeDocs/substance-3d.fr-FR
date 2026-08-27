---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/common-questions/texture-baked-outside-of-substance-software-looks-incorrect.html"
breadcrumb-title: ''
description: Dépannez les raisons pour lesquelles les textures bake en dehors des logiciels de Substance semblent incorrectes et découvrez comment résoudre les problèmes d’espace colorimétrique.
helpx_creative_field: ""
helpx_description: bakers > Common Questions > Texture baked outside of Substance software looks incorrect
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: La texture cuite en dehors du logiciel de Substance semble incorrecte
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4a060ee1aaa1731c04e70d5512e3271cd63d0381
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---


# La texture cuite en dehors du logiciel de Substance semble incorrecte

>[!WARNING]
>
> **Question**
> 
> Pourquoi la texture que j&#39;ai bake avec une application externe et non les Substance Bakers semblent-elles incorrectes en Substance Painter ?

>[!NOTE]
>
> **Solution**
> 
> Il n’existe pas de solution immédiate à ce problème car de nombreux facteurs peuvent y contribuer :
> 
> * Vérifiez que le format habituel entre le logiciel de Substance de données et l’application externe est le même. OpenGL est [X+, Y+, Z+] et DirectX est [X+, Y-, Z+]
>   * En Substance Painter, le format normal peut être modifié dans la [configuration du projet](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/interface/project-configuration).
>   * En Substance Designer, le format normal peut être modifié dans les [préférences du projet](https://experienceleague.adobe.com/en/docs/substance-3d-designer/using/workspace/preferences/project-settings).
> * Vérifiez que le maillage a été triangulé avant de le bake et de l’importer dans le logiciel de Substance. Voir [cette page](../../guides/triangulating-before-bak/triangulating-before-baking.md) pour plus d&#39;informations.
