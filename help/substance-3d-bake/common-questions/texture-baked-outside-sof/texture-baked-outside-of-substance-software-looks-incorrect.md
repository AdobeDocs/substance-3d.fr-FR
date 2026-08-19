---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/common-questions/texture-baked-outside-of-substance-software-looks-incorrect.html"
breadcrumb-title: ''
description: Dépannez pourquoi les textures cuits en dehors du logiciel Substance semblent incorrectes et apprenez à résoudre les problèmes d'espace colorimétrique.
helpx_creative_field: ""
helpx_description: bakers > Common Questions > Texture baked outside of Substance software looks incorrect
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: La texture cuite en dehors du logiciel Substance semble incorrecte
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4a060ee1aaa1731c04e70d5512e3271cd63d0381
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---


# La texture cuite en dehors du logiciel Substance semble incorrecte

>[!WARNING]
>
> **Question**
> 
> Pourquoi la texture que j&#39;ai cuite avec une application externe et pas le Substance Bakers a-t-elle un aspect incorrect dans Substance Painter ?

>[!NOTE]
>
> **Solution**
> 
> Il n’existe pas de solution immédiate à ce problème, car de nombreux facteurs peuvent y contribuer :
> 
> * Vérifiez que le format normal entre le logiciel Substance et l&#39;application externe est le même. OpenGL est [X+, Y+, Z+] et DirectX est [X+, Y-, Z+]
>   * Dans Substance Painter, le format normal peut être modifié dans la [ configuration du projet ](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/interface/project-configuration).
>   * Dans Concepteur de substance, le format normal peut être modifié dans les [préférences du projet](https://experienceleague.adobe.com/en/docs/substance-3d-designer/using/workspace/preferences/project-settings).
> * Vérifiez que le maillage a été triangulé avant de le cuire au four et de l&#39;importer dans le logiciel Substance. Voir [cette page](../../guides/triangulating-before-bak/triangulating-before-baking.md) pour plus d’informations.
