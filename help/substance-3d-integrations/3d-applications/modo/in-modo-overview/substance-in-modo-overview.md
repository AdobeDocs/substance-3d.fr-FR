---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-integrations/3d-applications/modo/substance-in-modo-overview.html"
breadcrumb-title: ''
description: Découvrez le plug-in Substance pour MODO et apprenez à importer et à utiliser des matériaux de Substance dans votre workflow.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > MODO > Substance in MODO Overview
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Présentation de la Substance dans MODO
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 5%

---


# Présentation de la Substance dans MODO

## Présentation :

## Ouverture d’une Substance

1. Créez un matériau ou sélectionnez un groupe de matériaux.
1. Sous Texture > Substance, choisissez Créer une Substance ou utilisez le bouton Créer sous les options du kit de Substance. Cela créera un matériau de Substance dans l&#39;arbre du nuanceur.
1. Cliquez sur Charger sbsar pour charger un fichier sbsar.

   ![](../../../assets/load-1.png)

## Création de sorties

À l&#39;aide du **Mode Ombrage par défaut**, vous pouvez créer des sorties à l&#39;aide du workflow Métal/Rugosité.

1. Dans la section Sorties des Propriétés de la Substance, cliquez sur les sorties nécessaires à l’ombrage. La texture de Substance sera générée et ajoutée à l’arbre du nuanceur avec l’effet de calque Matériau correct. Pour le mode Ombrage avec principes, vous aurez besoin des éléments suivants :

   | Sortie de Substance | Espace colorimétrique | Effet Calque de matériau (mode Ombrage de principe) |
   | --- | --- | --- |
   | Couleur de base | sRVB | Couleur diffuse |
   | Normale | Linéaire | Normal |
   | Rugosité | Linéaire | Rugosité |
   | Métallique | Linéaire | Métallique |

   ![](../../../assets/outputs-3.png)

## Modification de la résolution/des paramètres

Vous pouvez modifier les paramètres de Substance pour mettre à jour ou modifier les textures générées. La modification d’un paramètre entraîne le recalcul par la Substance Engine des textures intégrées dans le matériau MODO.

1. Accédez aux Propriétés de Substance du matériau de Substance et, dans la section Ajustements, modifiez l&#39;un des paramètres.

   ![](../../../assets/params.png)
1. Vous pouvez modifier la résolution des textures générées à l’aide du menu déroulant Taille de sortie. Les Substances peuvent être définies pour générer jusqu’à 8K. Le [moteur GPU Substance](../../../3d-applications/modo/modo-switch-engine/modo-switch-engine.md) est requis pour la sortie 8K.
