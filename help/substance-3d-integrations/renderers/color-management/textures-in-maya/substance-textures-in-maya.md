---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-integrations/renderers/color-management/substance-textures-in-maya.html"
breadcrumb-title: ''
description: Configurez les paramètres d’espace colorimétrique pour les textures de Substance dans Maya pour assurer une gestion et un rendu des couleurs précis.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Renderers > Color Management > Substance textures in Maya
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Textures de Substance en maya
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---


# Textures de Substance en maya

L&#39;espace colorimétrique que vous définissez pour les mappages dépend des paramètres et des règles établis dans les [paramètres de gestion des couleurs Maya](https://help.autodesk.com/view/MAYAUL/2020/ENU/?guid=GUID-B260195C-A0FE-4F51-9EA2-099B61B7725A).

La Substance du plug-in Maya est définie sur « Ignorer les règles du fichier d’espace colorimétrique » sur le nœud de fichier. Le plug-in prend en charge le paramètre d’espace colorimétrique indépendamment de la gestion des couleurs à l’aide des éléments suivants :

BaseColor, Diffuse, Emissive, Specular = sRGB\
Normal, height, displacement, rugosité, métallique = RAW

En règle générale, vous devrez définir l’espace colorimétrique sur RAW pour les images représentant des données non colorimétriques. Toutefois, ce paramètre peut être affecté par les règles que vous avez définies dans la Gestion des couleurs.

![](../../../assets/raw.png)
