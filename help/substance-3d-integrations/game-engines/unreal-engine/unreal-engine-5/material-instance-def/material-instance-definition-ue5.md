---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unreal-engine/unreal-engine-5/material-instance-definition-ue5.html"
breadcrumb-title: ''
description: Créez des définitions d’instance de Matériau avec des matériaux de Substance dans Unreal Moteur 5 pour optimiser les performances de rendu GPU.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unreal Engine > Unreal Engine 5 > Material Instance Definition - UE5
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Définition d'instance de matériau - UE5
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 0%

---


# Définition d&#39;instance de matériau - UE5

Vous pouvez utiliser des instances de Matériau UE5 avec des Substances. Cela économisera une étape importante du processus de rendu GPU en ne téléchargeant pas de nouveau matériau dans le processus. Un MID peut être créé à l’exécution ou dans l’éditeur. Avec la version 5.0.0, nous avons ajouté la prise en charge complète de l’instanciation de matériau.

## Création d&#39;une instance de matériau dans l&#39;éditeur

1. Cliquez avec le bouton droit de la souris sur le matériau UE5 créé par la substance et choisissez Créer une instance de Matériau. Un matériau d’instance UE5 est alors créé.

   ![](https://helpx-prod.scene7.com/is/image/HelpxProd/screen-shot-2022-03-31-at-6-07-08-pm?$png$&jpegSize=300&wid=1472)
1. Cliquez avec le bouton droit de la souris sur la fabrique d&#39;instances Substance et choisissez Créer une instance de graphe. Une instance du graphe est ainsi créée, ainsi qu&#39;un autre matériau UE5. Supprimez le matériau UE5 nouvellement créé, car il ne sera pas utilisé.

   ![](../../../../assets/screen-shot-2022-03-31-at-6-10-38-pm.png)
1. Double-cliquez sur l&#39;occurrence de matériau que vous avez créée à l&#39;étape 1 et activez les paramètres Texture pour toutes les textures.
1. Définissez la texture sur la nouvelle texture INST créée à l’étape 2. Cette opération définit l’instance de matériau pour utiliser les cartes de sortie Substance du graphique d’instance.

   ![](../../../../assets/screen-shot-2022-03-31-at-6-13-18-pm.png)

Vous avez maintenant une instance de matériau UE5 qui utilise un ensemble spécifique de textures Substance. Il s&#39;agit d&#39;une façon plus optimisée de travailler avec plusieurs substances dans un projet UE5. Pour savoir comment créer un MID à l’aide d’un plan directeur, consultez cette page. [Blueprint(UE5) : instance de Matériau dynamique](https://helpx.adobe.com/substance-3d/unlisted/documentation/integrations/blueprint-dynamic-material-instance-152535142.html)
