---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unity/rendering-color-space.html"
breadcrumb-title: ''
description: Configurez les paramètres d’espace colorimétrique d’Unity pour assurer un rendu correct des matériaux de Substance avec des nuanceurs basés physiquement.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unity > Rendering Color Space
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Rendu de l’espace colorimétrique
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 0%

---


# Rendu de l’espace colorimétrique

Les textures de Substance sont conçues pour être utilisées avec un shader basé sur Physique. Pour obtenir de meilleurs résultats, vous devez définir l’espace colorimétrique sur Linéaire dans les Paramètres d’Unity Player.

1. Accédez à Modifier > Paramètres du projet > Lecteur.
1. Dans la section Rendu, définissez l’espace colorimétrique sur Linéaire. (Unity utilise par défaut l’espace gamma, ce qui est incorrect et donnera une couleur de texture incorrecte).

   >[!NOTE]
   >
   > **Informations**
   > 
   > Les options sRVB des textures sont désactivées si le paramètre d’espace colorimétrique dans Unity est défini sur Gamma

   ![](../../../assets/rendering-4.png){width="600px"}
