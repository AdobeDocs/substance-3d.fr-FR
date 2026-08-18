---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unreal-engine/unreal-engine-5/tiling-substance-ue5.html"
breadcrumb-title: ''
description: Juxtaposer les textures de Substance dans Unreal Engine 5 en ajoutant des nœuds de coordonnées de texture et des paramètres scalaires aux matériaux.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unreal Engine > Unreal Engine 5 > Tiling Substance - UE5
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Substance de mosaïque - UE5
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 0%

---


# Substance de mosaïque - UE5

Pour placer une texture Substance en mosaïque, vous devez ajouter un nœud de coordonnées de texture et le multiplier par le paramètre scalaire.

<https://docs.unrealengine.com/latest/INT/Engine/Rendering/Materials/ExpressionReference/Coordinates/#texturecoordinate>

Pour créer des paramètres pour la mosaïque U et V, vous pouvez utiliser un vecteur d’ajout et le multiplier par le TexCord. Cela vous permet de définir indépendamment les valeurs des carreaux U et V.

![](../../../../assets/tiling-3.png){width="800px"}
