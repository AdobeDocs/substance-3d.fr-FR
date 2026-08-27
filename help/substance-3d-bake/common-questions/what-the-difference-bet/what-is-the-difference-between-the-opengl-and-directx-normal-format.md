---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-bake/common-questions/what-is-the-difference-between-the-opengl-and-directx-normal-format.html"
breadcrumb-title: ''
description: Découvrez les différences entre OpenGL et les formats de map normaux et quand les utiliser.
helpx_creative_field: ""
helpx_description: "bakers > Common Questions > What is the difference between the OpenGL and DirectX normal format "
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 'Quelle est la différence entre le format OpenGL et le format normal de DirectX ? '
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 0%

---


# Quelle est la différence entre le format OpenGL et le format normal de DirectX ?

>[!WARNING]
>
> **Question**
> 
> Quelle est la différence entre le format OpenGL et le format normal de DirectX ?

>[!NOTE]
>
> **Explication**
> 
> OpenGL et DirectX sont deux API graphiques (ensembles de fonctions) que les programmeurs utilisent dans leur application pour dialoguer avec le GPU (unité de traitement graphique). En termes de textures normales, la différence se traduit dans la façon dont la couche verte d&#39;une texture RGB doit être interprétée. OpenGL s’attend à ce que le premier pixel soit en bas et le DirectX en haut. C&#39;est souvent pourquoi, dans diverses discussions techniques, il est recommandé d&#39;essayer d&#39;inverser la couche verte d&#39;une texture normale pour voir si elle se comporte mieux car elle inverse les valeurs de pixels (la première devient la dernière). OpenGL peut être appelé **Y+** (de bas en haut) tandis que DirectX est appelé **Y-** (de haut en bas).
> 
> Pour savoir quel format utiliser, reportez-vous à l’application cible dans laquelle vos textures seront utilisées.
