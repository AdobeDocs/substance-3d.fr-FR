---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unreal-engine/unreal-engine-4/live-link-in-ue4.html"
breadcrumb-title: ''
description: Utilisez Live Link dans Unreal Engine 4 pour synchroniser en temps réel les matériaux de Substance entre Painter et UE4.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unreal Engine > Unreal Engine 4 > Live Link in UE4
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Live Link dans UE4
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 0%

---


# Live Link dans UE4

>[!WARNING]
>
> Live Link dans Unreal Engine n’est plus pris en charge. Les utilisateurs disposant d’une ancienne version du plug-in où Live Link est utilisé pourront toujours utiliser la fonctionnalité.

>[!WARNING]
>
> Live Link ne fonctionne pas avec les maillages UE4 BSP. La ressource que vous envoyez doit être un fichier de modèle importé dans votre projet UE4

## Établissement d’un lien vers la Substance Painter

1. Substance Painter ouverte
1. Cliquez avec le bouton droit de la souris sur la ressource que vous souhaitez envoyer à Painter dans l’Explorateur de contenu et choisissez « Envoyer à Painter ».

   ![](../../../../assets/link1-22.png){width="400px"}
1. Le maillage apparaîtra dans la Substance Painter et vous pourrez commencer la texturation. Pendant que vous travaillez, les textures seront envoyées à UE4 et appliquées aux matériaux. Le point vert sur l’icône UE4 de la barre d’outils indique que le lien est en direct et qu’il envoie des textures.

   ![](../../../../assets/icon-12.png)

   1. Vous pouvez interrompre la diffusion des données dans les options de configuration du plug-in. Accédez à Plug-ins > dcc-live-link et choisissez Configurer. Désactivez l&#39;option Activer la diffusion en continu pour interrompre l&#39;envoi des données à UE4.

      ![](https://helpx-prod.scene7.com/is/image/HelpxProd/config-6?$png$&jpegSize=100&wid=393)
1. Les textures de Painter apparaîtront dans l&#39;Explorateur de contenu et seront appliquées au matériau dans UE4.

   ![](../../../../assets/link3-11.png){width="500px"}
1. Un projet de Substance Painter (.spp) sera créé dans le dossier du projet UE4 dans un dossier intitulé  ».sp »

   ![](../../../../assets/link4-5.png)

## Rétablissement d’un lien vers la Substance Painter

Vous pouvez reprendre là où vous vous étiez arrêté après avoir fermé Painter ou Unity.

1. Ouvrez le projet .spp dans la Substance Painter située dans votre dossier Projet Unity > Actifs >.sp.
1. Cliquez avec le bouton droit de la souris sur le maillage dans l’Explorateur de contenu et choisissez « Envoyer vers Painter » pour rétablir le lien.

   ![](../../../../assets/link5-3.png){width="600px"}
