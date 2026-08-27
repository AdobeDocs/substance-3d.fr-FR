---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-integrations/game-engines/unreal-engine/unreal-engine-4/material-instance-definition-ue4.html"
breadcrumb-title: ''
description: Créez des définitions d’instance de Matériau avec des matériaux de Substance dans Unreal Moteur 4 pour optimiser les performances de rendu GPU.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unreal Engine > Unreal Engine 4 > Material Instance Definition - UE4
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Définition d'instance de matière - UE4
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 0%

---


# Définition d&#39;instance de matière - UE4

Vous pouvez utiliser des instances de Matériau UE4 avec des Substances. Cela économisera une étape importante du processus de rendu GPU en ne téléchargeant pas un nouveau matériau à traiter. Un MID peut être créé à l’exécution ou dans l’éditeur. Avec la version 4.24.0.3, nous avons ajouté la prise en charge complète de l&#39;instanciation de matériau et introduit un nouveau workflow de modèle de matériau avec des sorties numériques prises en charge par la Substance Engine. Les modèles de matériau vous permettent de définir exactement comment vous souhaitez configurer vos nuanceurs de matériau de Substance dans UE4.

Lorsque vous importez un fichier sbsar, vous pouvez choisir le modèle à utiliser.

![](../../../../assets/ue4-material-templates.png)

Nous livrons des modèles pour travailler avec des matériaux alignés au monde, de displacement et de réfraction qui ont des contrôles intégrés pour ajuster les paramètres de répétition, de taille de texture, de displacement et d&#39;emissive. Le système de modèles matériau vous permet également de fournir vos propres modèles personnalisés.

![](../../../../assets/ue4-material-instance-params.png)

## Création d&#39;une instance de matériau dans l&#39;éditeur

1. Cliquez avec le bouton droit de la souris sur le matériau UE4 créé par la substance et choisissez Créer une instance de Matériau. Un matériau d’instance UE4 est alors créé.

   ![](https://helpx-prod.scene7.com/is/image/HelpxProd/01-12?$png$&jpegSize=100&wid=592){width="560px"}
1. Cliquez avec le bouton droit de la souris sur la fabrique d&#39;instances Substance et choisissez Créer une instance de graphe. Une instance du graphe est ainsi créée, ainsi qu&#39;un autre matériau UE4. Supprimez le matériau UE4 nouvellement créé, car il ne sera pas utilisé.

   ![](../../../../assets/02-10.png){width="300px"}
1. Double-cliquez sur l&#39;occurrence de matériau que vous avez créée à l&#39;étape 1 et activez les paramètres Texture pour toutes les textures.
1. Définissez la texture sur la nouvelle texture INST créée à l’étape 2. Cette opération définit l’instance de matériau pour utiliser les cartes de sortie Substance du graphique d’instance.

   ![](https://helpx-prod.scene7.com/is/image/HelpxProd/03-6?$png$&jpegSize=200&wid=1011){width="800px"}

Vous avez maintenant une instance de matériau UE4 qui utilise un ensemble spécifique de textures Substance. Il s&#39;agit d&#39;une façon plus optimisée de travailler avec plusieurs substances dans un projet UE4. Pour savoir comment créer un MID à l’aide d’un plan directeur, consultez cette page. [Blueprint(UE4) : instance de Matériau dynamique](https://helpx.adobe.com/fr/substance-3d/unlisted/documentation/integrations/blueprint-dynamic-material-instance-152535142.html)
