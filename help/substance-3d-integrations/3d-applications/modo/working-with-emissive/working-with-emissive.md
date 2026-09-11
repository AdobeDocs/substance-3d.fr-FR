---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/3d-applications/modo/working-with-emissive.html"
breadcrumb-title: ''
description: Configurez les propriétés d’emissive des matériaux de Substance dans MODO pour contrôler la quantité de lumière et les paramètres de couleur.
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

## Utilisation de l’Emissive (quantité et couleur lumineuses)

La Substance peut avoir une sortie emissive facultative. Vous pouvez l’utiliser en tant que Quantité lumineuse et Couleur dans MODO. Lorsque vous activez la sortie emissive, elle est définie sur l’effet Quantité de luminosité. Par défaut, cette couche est interprétée comme linéaire sous l’onglet Texture de l’image fixe.\
Cliquez avec le bouton droit de la souris sur la texture dans l’arborescence du Shader et choisissez Dupliquer. Définissez ensuite la texture d’emissive dupliquée sur l’effet Couleur lumineuse. Vous pouvez ensuite modifier les valeurs haute et basse de la texture pilotant l’effet Quantité de luminosité pour intensifier davantage la valeur.

>[!NOTE]
>
> Pour le jeu de textures sur Couleur lumineuse, vous devez définir l’interprétation sur sRVB dans l’onglet Image fixe.

Pour obtenir un effet d’épanouissement, vous devez activer l’effet d’épanouissement dans le panneau Rendu et définir le seuil et le rayon.

![](../../../assets/bloom.png)

Pour les matériaux Unreal et Unity, la sortie Emissive est traitée spécifiquement par le matériau.\
Irréel = Emissive irréelle\
Unity = Unity Emission

Les textures Emissive irréelle et Émission d&#39;unité doivent être modifiées de Linéaire à sRVB dans l&#39;onglet Image fixe.
