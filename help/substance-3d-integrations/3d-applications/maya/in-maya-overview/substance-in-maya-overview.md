---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-integrations/3d-applications/maya/substance-in-maya-overview.html"
breadcrumb-title: ''
description: Découvrez le plug-in Substance pour Maya et apprenez à importer et à utiliser des matériaux Substance dans votre workflow.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > Maya > Substance in Maya Overview
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Substance en Maya Aperçu
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 0%

---


# Substance en Maya Aperçu

## Présentation des plug-ins

Le plug-in Substance vous permet de charger un matériau de Substance créé dans Substance Designer directement dans Maya. Le plug-in créera un matériau Maya et alimentera les textures de substance dans les entrées des canaux de matériau. Vous pouvez ensuite apporter des modifications aux paramètres de substance et les textures seront automatiquement mises à jour.

>[!NOTE]
>
> Assurez-vous que le plug-in est chargé dans Paramètres/Préférences ->Gestionnaire de plug-ins Maya

![](https://helpx-prod.scene7.com/is/image/HelpxProd/plugin-4?$png$&jpegSize=100&wid=618)

## Ouverture d’une Substance

1. Ouvrez l&#39;Hypershade et dans l&#39;Éditeur de nœuds, faites un clic droit et balayez vers le haut dans le menu de marquage pour choisir Créer un nœud. La fenêtre Créer un nœud s’ouvre. À partir de là, vous pouvez rechercher le nœud de Substance.

   ![](../../../assets/createnode.png)

   Vous pouvez également appuyer sur la touche tab dans l’éditeur de nœuds et dans le champ de texte, tapez substance. Les options substance seront alors filtrées. Dans les options, choisissez Texture de Substance.
1. Sélectionnez le nœud de Substance et dans l’Éditeur de propriétés, puis naviguez pour charger un fichier de Substance (.sbsar).

   ![](../../../assets/1.png)
1. La liste déroulante Graphe sélectionné s’affiche si la Substance contient plusieurs graphes. Le graphe choisi sera utilisé pour créer le matériau.
1. Le bouton Informations sur le Graphe affiche les attributs de graphe définis dans la Substance Designer.
1. Définissez la résolution en choisissant une valeur dans la liste déroulante Largeur et Height. Le verrouillage des taux est activé par défaut.
1. Activer les sorties du cache sur le disque afin de bake les sorties de Substance de données sur le disque afin qu’elles puissent être utilisées avec des systèmes de rendu tels qu’Arnold. Le fichier mis en cache sera relu par le plug-in à l’aide d’un nœud de fichier Maya.

   ![](../../../assets/outputsettings.png)
1. Choisissez un flux de production pour le moteur de rendu que vous utilisez et cliquez sur le bouton Créer un réseau Shader. Un réseau shader est créé pour le workflow de rendu. Vous pouvez maintenant appliquer le matériau dans la scène.

   ![](../../../assets/createnetwork.gif){width="1000px"}
