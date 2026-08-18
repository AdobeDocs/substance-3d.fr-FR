---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-integrations/game-engines/unreal-engine/unreal-engine-5/installing-to-source-builds-ue5.html"
breadcrumb-title: ''
description: Installez le plug-in Substance 3D dans les versions sources d’Unreal Engine 5 pour des modifications de moteur personnalisées.
helpx_creative_field: ""
helpx_description: Substance 3D Integrations
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Installation dans les versions sources - UE5
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 0%

---


# Installation dans les versions sources - UE5

Le plug-in Substance peut être utilisé avec les versions d’Unreal Engine construites à partir de la source. Pour ce faire, le plug-in peut être installé dans un dossier C++project ou dans le dossier du moteur d’une version source.

>[!NOTE]
>
> Ces méthodes nécessitent que vous ayez une version du plug-in téléchargée à partir du marketplace. Le dossier du plug-in Substance peut être transféré entre les ordinateurs et les versions UE.

## Installation dans un dossier de projet C++

1. Dans le dossier du projet, créez un dossier Plug-ins s’il n’en existe pas déjà un.
1. Dans le dossier Plug-ins, créez un dossier Runtime.
1. Placez le dossier Substance dans le dossier Runtime. UTILISATEURS DE LINUX : Après l’étape 3, recherchez le dossier « include » dans le dossier de la Substance de données et renommez-le en majuscules (include > Include).
1. Lancez Unreal Engine.
1. Ouvrez le projet C++ via le lanceur.
1. Après le lancement du projet, Unreal Engine vous demandera si vous souhaitez reconstruire les composants du plug-in avant le lancement, sélectionnez oui. Cela se fera via Microsoft Visual Studio (Windows, Linux) ou Xcode (Mac).
1. Unreal Engine se ferme, mais les composants se construisent en arrière-plan. Ce processus peut prendre environ 5 minutes. Une fois terminé, le projet s&#39;ouvrira. En cas d’échec, une fenêtre d’erreur s’affiche.

## Installation dans le dossier du moteur

>[!NOTE]
>
> Les étapes ci-dessus doivent être suivies pour reconstruire le dossier Binaries du plug-in avant que le plug-in ne puisse être installé dans le dossier Engine.

1. Copiez le dossier de la Substance dans le dossier du projet > Plug-ins > Runtime.
1. Ouvrez le dossier de la version d’Unreal Engine et accédez à Moteur > Plug-ins > Marketplace.
1. Collez le dossier Substance.
1. Ouvrez l’éditeur Unreal Engine. Créez un projet si nécessaire.
1. Ouvrez le menu Plug-ins et vérifiez que le plug-in de Substance est activé.
