---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-integrations/renderers/maxwell/maxwell-substance-painter.html"
breadcrumb-title: ''
description: Exportez les textures de Substance Painter pour le rendu Maxwell à l’aide des modèles de sortie et des paramètres de matière appropriés.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Renderers > Maxwell > Maxwell - Substance Painter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Maxwell - Substance Painter
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4a060ee1aaa1731c04e70d5512e3271cd63d0381
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 0%

---


# Maxwell - Substance Painter

Substance Painter 2020.1 (6.1.0) prend en charge les [Modèles de sortie](https://experienceleague.adobe.com/fr/docs/substance-3d-painter/using/getting-started/export/export) Maxwell pour les propriétés Métallique/Rugosité et specular/Éclat. Vous pouvez simplement exporter à l’aide du Modèle de sortie Maxwell**.\
Maxwell 5.1.0** s’intègre à Substance Painter pour vous permettre d’importer facilement des textures et de configurer automatiquement un matériau Maxwell.

## Exportation de textures

Vous pouvez choisir les Modèles de sortie Maxwell (rugosité métallique) ou Maxwell (brillance Specular) pour exporter des textures en vue d’un rendu dans Maxwell.

![](../../../assets/maxwell-output.png){width="500px"}

## Application de textures dans Maxwell

Vous pouvez utiliser l&#39;intégration de Substance Painter dans Maxwell pour créer automatiquement un matériau avec les cartes exportées à partir de la Substance Painter appliquée.\
Pour commencer, cliquez avec le bouton droit de la souris dans la liste des matériaux et sélectionnez **Nouveau>Substance Painter**.

![](https://helpx-prod.scene7.com/is/image/HelpxProd/maxwell-painter?$png$&jpegSize=100&wid=413)

Accédez à l’emplacement où vous avez exporté les textures de Substance Painter et sélectionnez l’une des cartes comme couleur de base. Lorsque vous cliquez sur Ouvrir, l’intégration crée un nouveau matériau Maxwell avec les cartes attribuées.\
Si plusieurs ensembles de textures sont exportés à partir de Substance Painter, l’intégration utilise la convention de dénomination de la texture pour attribuer les textures correspondantes.

![](https://helpx-prod.scene7.com/is/image/HelpxProd/image-material?$png$&jpegSize=100&wid=620){width="600px"}

Vous pouvez ensuite attribuer la matière à la ressource dans votre scène.

![](../../../assets/assigned.png){width="500px"}

Toutes les matières utilisées à l’aide de l’intégration de la Substance Painter.

![](https://helpx-prod.scene7.com/is/image/HelpxProd/materials-assigned?$pjpeg$&jpegSize=300&wid=1511){width="800px"}
