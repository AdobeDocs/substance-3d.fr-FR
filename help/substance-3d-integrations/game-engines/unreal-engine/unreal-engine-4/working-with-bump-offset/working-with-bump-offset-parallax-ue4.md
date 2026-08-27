---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-integrations/game-engines/unreal-engine/unreal-engine-4/working-with-bump-offset-parallax-ue4.html"
breadcrumb-title: ''
description: Utilisez la texture Décalage de relief avec des matériaux de Substance dans le Moteur irréel 4 pour créer une illusion de profondeur et des détails de surface.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unreal Engine > Unreal Engine 4 > Working with Bump Offset (Parallax) - UE4
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Utilisation du décalage de relief (parallaxe) - UE4
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 0%

---


# Utilisation du décalage de relief (parallaxe) - UE4

Le mapping **Décalage de relief** donne à une surface une illusion de profondeur en modifiant les coordonnées des UV de manière créative pour aider à déplacer davantage les texels de la surface de l&#39;objet, donnant l&#39;illusion que la surface a plus de détails qu&#39;elle n&#39;en a en réalité. Dans cet exemple de procédure, nous allons non seulement expliquer comment vous pouvez trouver l&#39;expression de Matériau de décalage de relief, mais également comment vous pouvez utiliser le nœud de décalage de relief dans vos Matériaux.

<https://docs.unrealengine.com/latest/INT/Engine/Rendering/Materials/HowTo/BumpOffset/>

Pour utiliser la sortie height, vous devez double-cliquer sur la sortie dans l&#39;instance de Substance Factory pour créer l&#39;height. L’Height n’est pas activé par défaut. Vous pouvez ensuite faire glisser cette sortie height dans votre matière.

![](../../../../assets/height-1.png){width="600px"}

Créez un nœud de décalage de relief, puis branchez la couche rouge de l’height dans l’Height. Vous pouvez ensuite entrer un TexCord dans l’entrée Coordonnée du décalage de relief. Enfin, la sortie du décalage de bosse est branchée sur l&#39;entrée d&#39;UV pour toutes les textures de Substance.

![](../../../../assets/bump.png){width="800px"}
