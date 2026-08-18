---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unreal-engine/unreal-engine-4/working-with-displacement-ue4.html"
breadcrumb-title: ''
description: Activez la facettisation et utilisez des cartes de displacement à partir des matériaux de Substance dans Unreal Engine 4 pour les détails de surface.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unreal Engine > Unreal Engine 4 > Working with Displacement - UE4
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Utilisation de Displacement - UE4
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 0%

---


# Utilisation de Displacement - UE4

Pour utiliser displacement, vous devez activer la facettisation sur votre matière.

![](../../../../assets/tess.png){width="600px"}

Pour utiliser la sortie height, vous devez double-cliquer sur la sortie dans l&#39;instance de Substance Factory pour créer l&#39;height. L’Height n’est pas activé par défaut. Vous pouvez ensuite faire glisser cette sortie height dans votre matière.

![](../../../../assets/height-1.png){width="800px"}

Une fois que vous avez ajouté la sortie height à votre matière, vous devrez créer quelques nœuds pour piloter le modificateur Displacement universel et facettisation.

1. Créez 2 paramètres scalaires. L&#39;un sera la distance et l&#39;autre sera le multiplicateur de la facettisation.
1. Multipliez la couche rouge entre l’Height et le paramètre Distance
1. Ajoutez un nœud VertexNormalWS et multipliez-le avec la sortie du multiplicateur à l’étape 2.
1. Entrez le multiple de la normale du sommet (VertexNormal) au Displacement universel sur le matériau.
1. Prenez le paramètre Multiplicateur de facettisation et saisissez-le dans le Multiplicateur de facettisation du matériau.

![](../../../../assets/setup-3.png){width="800px"}

>[!NOTE]
>
> Les autres textures de sortie ont été omises dans cette image pour simplifier le graphique. Ici, seuls les nœuds Displacement et Multiplicateur sont affichés pour plus de clarté.
