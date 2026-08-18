---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-integrations/game-engines/unity/publishing-for-mobile.html"
breadcrumb-title: ''
description: Optimisez les matériaux de Substance pour les plateformes mobiles dans Unity en ajustant les paramètres et les résolutions de texture.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unity > Publishing for Mobile
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Publication pour mobile
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---


# Publication pour mobile

>[!NOTE]
>
> **Taille de la texture sur les appareils mobiles**
> 
> La résolution de la texture définie dans l’éditeur Unity sera la taille publiée dans le binaire de l’application. La réduction de la résolution du matériau de Substance permet de créer des textures avec des fichiers plus petits.

## Plates-formes

## Apple iOS

1. Assurez-vous que le module iOS est téléchargé pour la version d’Unity correspondante.
1. Dans Unity, remplacez la cible de build par iOS.
1. Ouvrez les paramètres du lecteur et modifiez le champ « Identification - Identificateur de lot » pour lui donner un aspect plus unique. (par exemple : com.Adobe.iosProject)
1. Construisez et exécutez le jeu.
1. Dans Xcode, cliquez sur l’appareil iOS et remplacez le menu déroulant « Signature - Équipe » par votre ID d’équipe de développement.
1. Sur l’appareil iOS, accédez à Paramètres - Général - Gestion des appareils et cliquez sur Approbation sur l’ID de l’équipe de développement qui s’affiche.
1. Exécutez à nouveau la génération Xcode en cliquant sur le bouton Générer et exécuter le schéma actuel (le bouton Lecture ).
1. Le jeu doit s’exécuter sur l’appareil iOS.

## Système d’exploitation Android

1. Assurez-vous que le module Android est téléchargé pour la version d’Unity correspondante.
1. Dans Unity, remplacez la cible de build par Android.
1. Ouvrez les paramètres du lecteur et modifiez le champ « Identification - Identificateur de lot » pour lui donner un aspect plus unique. (par exemple : com.Adobe.androidProject)
1. Construisez et exécutez le jeu.
1. Le jeu doit être exécuté sur l&#39;appareil Android.
