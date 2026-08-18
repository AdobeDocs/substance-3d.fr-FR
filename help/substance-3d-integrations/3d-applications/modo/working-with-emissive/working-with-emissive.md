---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/3d-applications/modo/working-with-emissive.html"
breadcrumb-title: ''
description: Configurez les propriétés émissives des matériaux de Substance dans MODO pour contrôler la quantité de lumière et les paramètres de couleur.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > MODO > Working with Emissive
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Utilisation d’Emissive
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 0%

---


# Utilisation d’Emissive

## Utilisation de l’option Émissif (quantité et couleur lumineuses)

La Substance peut avoir une sortie émissive facultative. Vous pouvez l’utiliser en tant que Quantité lumineuse et Couleur dans MODO. Lorsque vous activez la sortie émissive, elle est définie sur l’effet Quantité de luminosité. Par défaut, cette couche est interprétée comme linéaire sous l’onglet Image de texture fixe.\
Cliquez avec le bouton droit sur la texture dans l’arborescence du nuanceur et choisissez Dupliquer. Définissez ensuite la texture émissive dupliquée sur l’effet Couleur lumineuse. Vous pouvez ensuite apporter des modifications à la valeur haute et basse de la texture qui pilote l’effet Quantité de luminosité pour intensifier davantage la valeur.

>[!NOTE]
>
> Pour la texture définie sur Couleur lumineuse, vous devez définir l’interprétation sur sRVB dans l’onglet Image fixe.

Pour obtenir un effet d’épanouissement, vous devez activer l’effet d’épanouissement dans le panneau Rendu et définir le seuil et le rayon.

![](../../../assets/bloom.png)

Pour les matériaux Unreal et Unity, la sortie Emissive est traitée spécifiquement par le matériau.\
Irréel = irréel émissif\
Unity = Unity Emission

Les textures Unity Emission et Unreal Emissive doivent être remplacées par sRVB dans l’onglet Image fixe.
