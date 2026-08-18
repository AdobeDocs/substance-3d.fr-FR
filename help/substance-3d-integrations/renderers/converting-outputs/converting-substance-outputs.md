---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-integrations/renderers/converting-substance-outputs.html"
breadcrumb-title: ''
description: Découvrez comment convertir les sorties de matériau Substance pour qu’elles correspondent à différents workflows et exigences de rendu.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Renderers > Converting Substance outputs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Conversion de sorties de Substance
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 1%

---


# Conversion de sorties de Substance

## Substance Painter

Vous pouvez exporter les mappages convertis à partir de Substance Painter. Un large éventail de paramètres prédéfinis de rendu est pris en charge. Il suffit de sélectionner un paramètre prédéfini pour convertir les types de mappages. (la conversion est basée sur le flux de production métal/brut).

![](../../assets/convertpainter.png){width="800px"}

## Plug-in de Substance

Le plug-in Substance génère des sorties et crée automatiquement des matériaux pour des workflows spécifiques. Cependant, avec les applications DCC et les systèmes de rendu tiers, vous devrez peut-être convertir manuellement les sorties métalliques/brutes. Les intégrations suivantes prennent en charge les workflows de rendu automatique et convertissent correctement tous les types de mappages si nécessaire :

* [Substance en Maya](../../3d-applications/maya/using-workflows/using-workflows.md)
* [Substance dans 3ds Max](../../3d-applications/3ds-max/3ds-max.md)

## Substances personnalisées

Si vous créez une Substance personnalisée, vous pouvez créer les sorties spécifiques dont vous avez besoin pour les systèmes de rendu tels que Vray et Corona. À l’aide du nœud de conversion Métal/Rugosité (Bibliothèque>Utilitaires PBR), vous pouvez facilement convertir la couleur de base, la rugosité et les cartes métalliques dans le système de rendu spécifique.

![](../../assets/convert-designer.png){width="600px"}
