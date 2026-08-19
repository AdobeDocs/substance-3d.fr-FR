---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/common-questions/what-is-the-difference-between-the-opengl-and-directx-normal-format.html"
breadcrumb-title: ''
description: Découvrez les différences entre les formats de carte OpenGL et DirectX normaux et quand utiliser chacun d’eux.
helpx_creative_field: ""
helpx_description: "bakers > Common Questions > What is the difference between the OpenGL and DirectX normal format "
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 'Quelle est la différence entre le format normal OpenGL et DirectX ? '
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 0%

---


# Quelle est la différence entre le format normal OpenGL et DirectX ?

>[!WARNING]
>
> **Question**
> 
> Quelle est la différence entre le format normal OpenGL et DirectX ?

>[!NOTE]
>
> **Explication**
> 
> OpenGL et DirectX sont deux API graphiques (ensembles de fonctions) que les programmeurs utilisent dans leur application pour dialoguer avec le GPU (Graphic Processing Unit). En termes de textures normales, la différence se traduit dans la manière dont la couche verte d&#39;une texture RGB doit être interprétée. OpenGL s’attend à ce que le premier pixel se trouve en bas tandis que DirectX s’attend à ce qu’il se trouve en haut. C&#39;est souvent pourquoi, dans diverses discussions techniques, il est recommandé d&#39;essayer d&#39;inverser le canal vert d&#39;une carte normale pour voir si elle se comporte mieux lorsqu&#39;elle inverse les valeurs des pixels (en premier lieu, elle devient la dernière). OpenGL peut être appelé **Y+** (de bas en haut) tandis que DirectX est appelé **Y-** (de haut en bas).
> 
> Pour savoir quel format utiliser, reportez-vous à l’application cible dans laquelle vos textures seront utilisées.
