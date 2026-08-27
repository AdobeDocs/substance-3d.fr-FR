---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unity/unity-plugin-overview.html"
breadcrumb-title: ''
description: Découvrez le plug-in Substance 3D pour Unity, notamment la prise en charge des versions, les fonctionnalités et les fonctionnalités d’intégration.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unity > Unity Plugin Overview
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Présentation du plug-in Unity
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 0%

---


# Présentation du plug-in Unity

## Prise en charge des versions Unity

La version 3.0.0 du plug-in Adobe Substance 3D pour Unity prend actuellement en charge Unity 2020 LTS et les versions ultérieures.

## Téléchargement du package de Substance

1. Le plug-in peut être téléchargé à partir du magasin de ressources Unity : <https://assetstore.unity.com/packages/tools/utilities/substance-3d-for-unity-beta-213208>

## Importation d&#39;une matière de Substance

1. Cliquez avec le bouton droit de la souris dans la fenêtre Projet et choisissez Importer la ressource, ou faites glisser le Matériau de Substance à importer dans le panneau Vue du projet.
1. Recherchez le Matériau de Substance à importer. Les Matériaux de Substance portent l’extension de fichier « .sbsar ».
1. Le matériau de Substance sera importé dans votre projet Unity.

   1. L’actif sbsar crée un fichier d’importation principal et un dossier contenant les textures de sortie et un matériau Unity généré.
1. Vous pouvez ensuite glisser-déposer le matériau sur un maillage dans la vue Scène, puis modifier les paramètres dans l’Inspecteur.

   ![](../../../assets/window-overview.png){width="1000px"}

>[!NOTE]
>
> **Conversion de Maps normal**
> 
> La Substance dans le plug-in Unity convertit automatiquement DirectX en OpenGL. Lorsque vous utilisez des matériaux de [Substance Source](https://source.substance3d.com/), il n&#39;est pas nécessaire de changer l&#39;orientation normale en OGL. Si vous créez votre propre matériau en Substance Designer, assurez-vous de travailler avec le shader par défaut, car le module externe se chargera automatiquement de la conversion. Pour plus d’informations, voir Utilisation des normales dans Unity.

## Modification des paramètres

Les paramètres et les résolutions peuvent être définis dans la fenêtre Inspecteur. Voir [Modification des paramètres](../../../game-engines/unity/changing-parameters/changing-parameters.md).

[unity\_tweaking\_parameters.mp4](https://helpx.adobe.com/content/dam/help/en/substance-3d/documentation/download/attachments/186056716/unity-tweaking-parameters.mp4)

## Prise en charge du pipeline de rendu Unity

Le plug-in Substance 3D prend en charge les formats HDRP et URP. De plus amples renseignements seront bientôt disponibles.

## Tutoriel
