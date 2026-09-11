---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-integrations/3d-applications/blender/physical-size-in-blender.html"
breadcrumb-title: ''
description: Utilisez les paramètres de taille physique pour mettre à l’échelle les matériaux de Substance en fonction des dimensions réelles dans Blender.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > Blender > Physical size in Blender
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Taille physique dans le mélangeur
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 0%

---


# Taille physique dans le mélangeur

La taille physique dans les matériaux de Substance permet de mettre les matériaux à l’échelle en fonction de leur taille dans le monde. Les dimensions sont définies dans les applications de Substance comme Designer et affichées dans la section Taille physique du panneau des plug-ins.

![](../../../assets/blender-physical-size.png)

Lorsque la Taille physique est activée, les matériaux s’affichent en mosaïque en fonction de leur taille réelle, en centimètres. La répétition du matériau reste la même quelle que soit l’échelle des objets. La fonction peut être activée en basculant vers le shader Taille physique dans le panneau du module complémentaire. Après avoir ajusté l’échelle d’un objet, l’échelle doit être appliquée en appuyant sur Ctrl/Cmd+A pour afficher la Texture de Taille physique avec précision.

## Réglage de la Taille physique

Les valeurs du nœud de mappage peuvent être ajustées pour un contrôle artistique de la répétition de la Taille physique. En outre, un objet tel que Empty peut être utilisé pour l&#39;entrée Coordonnées de Texture afin de contrôler le mappage de texture à l&#39;aide des transformations de l&#39;objet d&#39;entrée (voir l&#39;exemple ci-dessous).

![](../../../assets/blender-physical-szie-empty.gif)
