---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-integrations/3d-applications/3ds-max/substance-in-3ds-max-overview.html"
breadcrumb-title: ''
description: Découvrez le module externe Substance pour 3ds Max et apprenez à importer et à utiliser des matériaux de Substance dans vos projets.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > 3ds Max > Substance in 3ds Max Overview
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Présentation de la Substance dans 3ds Max
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---


# Présentation de la Substance dans 3ds Max

## Présentation des plug-ins :

## Ouverture d’une Substance

1. Ouvrez l’éditeur d’ardoise, recherchez Substance et faites glisser le nœud Substance 2 vers la vue.
1. Double-cliquez sur le nœud de Substance pour activer les propriétés et, sous Explorateur de packages de Substances, chargez une Substance.

   >[!NOTE]
   >
   > Vous pouvez également glisser-déposer le fichier .sbsar dans l’éditeur d’ardoise pour créer automatiquement le nœud et importer la barre d’état système.
1. Si une Substance contient plusieurs graphes, vous pouvez choisir celui que vous voulez sortir en tant que matière dans le menu déroulant Graphe sélectionné.

   ![](https://helpx-prod.scene7.com/is/image/HelpxProd/max8?$png$&jpegSize=100&wid=341)

   ![](../../../assets/max1.png)
1. Une fois le nœud de Substance sélectionné, accédez au menu Substance et choisissez un moteur de rendu pris en charge. La matière sera créée et prête à être appliquée à l&#39;objet. Les textures de Substance sont liées au matériau de rendu.

   | Moteurs de rendu pris en charge |
   | --- |
   | Arnold |
   | Vray |
   | Corona |
   | Octane |

   ![](../../../assets/max3.png)

## Modification de la résolution :

1. Définissez la résolution souhaitée pour les textures de Substance calculées dans les Paramètres de sortie de Substance.
1. Pour une résolution allant jusqu&#39;à 8K, assurez-vous d&#39;utiliser le GPU, qui est défini dans les [Paramètres de Substance](../../../3d-applications/3ds-max/settings-1/substance-settings.md).

   ![](../../../assets/max6.png)

## Modification des paramètres :

1. Double-cliquez sur le nœud de Substance pour charger les paramètres de Substance dans la fenêtre des paramètres.
1. Modifiez les paramètres pour mettre à jour automatiquement les textures de Substance.

   ![](https://helpx-prod.scene7.com/is/image/HelpxProd/max4?$png$&jpegSize=200&wid=1276){width="500px"}

## Définition de l’aperçu de la sortie :

Vous pouvez définir un canal spécifique pour la vignette du nœud de Substance.

1. Dans la liste déroulante Aperçu de la sortie, choisissez le canal à utiliser pour la vignette du nœud.

   ![](../../../assets/max7.png)

## Substances de mosaïque :

Vous pouvez utiliser les propriétés Coordonnées pour afficher en mosaïque les textures de Substance et définir les couches de texture.

![](../../../assets/max10.png)
