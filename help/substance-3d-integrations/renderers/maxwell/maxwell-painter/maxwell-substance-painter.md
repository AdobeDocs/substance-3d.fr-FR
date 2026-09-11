---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-integrations/renderers/maxwell/maxwell-substance-painter.html"
breadcrumb-title: ''
description: Exportez les textures de Substance Painter pour le moteur de rendu Maxwell en utilisant les modèles de sortie et les paramètres de matériau appropriés.
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

Substance Painter 2020.1 (6.1.0) prend en charge les [Modèles de sortie](https://experienceleague.adobe.com/fr/docs/substance-3d-painter/using/getting-started/export/export) Maxwell pour les applications métallique/rugosité et specular/brillance. Vous pouvez simplement exporter à l’aide du Modèle de sortie Maxwell**.\
Maxwell 5.1.0** s’intègre à Substance Painter, ce qui vous permet d’importer facilement des textures et de configurer automatiquement un matériau Maxwell.

## Exportation de textures

Vous pouvez choisir les Modèles de sortie Maxwell (Métallique rugosité) ou Maxwell (Brillance Specular) pour exporter des textures pour le rendu dans Maxwell.

![](../../../assets/maxwell-output.png){width="500px"}

## Application de Textures dans Maxwell

Vous pouvez utiliser l’intégration de Substance Painter dans Maxwell pour créer automatiquement un matériau avec les mappages exportés à partir de la Substance Painter appliquée.\
Pour commencer, cliquez avec le bouton droit de la souris dans la liste par Matériau et sélectionnez **Nouveau>Substance Painter**.

![](https://helpx-prod.scene7.com/is/image/HelpxProd/maxwell-painter?$png$&jpegSize=100&wid=413)

Accédez à l’emplacement où vous avez exporté les textures de Substance Painter et sélectionnez l’une des cartes, par exemple base color. Lorsque vous cliquez sur Ouvrir, l’intégration crée un nouveau matériau Maxwell avec les mappages attribués.\
Si plusieurs jeux de textures sont exportés à partir de la Substance Painter, l’intégration utilise la convention de nommage de la texture pour attribuer des mappages de texture correspondants.

![](https://helpx-prod.scene7.com/is/image/HelpxProd/image-material?$png$&jpegSize=100&wid=620){width="600px"}

Vous pouvez ensuite attribuer le matériau à la ressource dans votre scène.

![](../../../assets/assigned.png){width="500px"}

Tous les matériaux appliqués à l’aide de l’intégration de la Substance Painter.

![](https://helpx-prod.scene7.com/is/image/HelpxProd/materials-assigned?$pjpeg$&jpegSize=300&wid=1511){width="800px"}
