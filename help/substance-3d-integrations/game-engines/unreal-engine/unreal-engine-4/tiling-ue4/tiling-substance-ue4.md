---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unreal-engine/unreal-engine-4/tiling-substance-ue4.html"
breadcrumb-title: ''
description: Juxtaposer les textures de Substance dans le Moteur irréel 4 en ajoutant des nœuds de coordonnées de Texture et des paramètres scalaires aux matériaux.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unreal Engine > Unreal Engine 4 > Tiling Substance - UE4
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Répétition Substance - UE4
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 0%

---


# Répétition Substance - UE4

Pour placer une texture Substance en mosaïque, vous devez ajouter un nœud Coordonnées de Texture et le multiplier par un paramètre scalaire.

<https://docs.unrealengine.com/latest/INT/Engine/Rendering/Materials/ExpressionReference/Coordinates/#texturecoordinate>

Pour créer des paramètres pour la mosaïque U et V, vous pouvez utiliser un vecteur d’ajout et le multiplier par le TexCord. Cela vous permet de définir indépendamment les valeurs des carreaux U et V.

![](../../../../assets/tiling-3.png){width="800px"}
