---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unreal-engine/unreal-engine-4/blueprints-ue4/blueprintue4-dynamic-material-instance.html"
breadcrumb-title: ''
description: Créez des instances de matériau dynamique à partir de matériaux de Substance lors de l’exécution dans Moteur irréel 4 à l’aide de Blueprints.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unreal Engine > Unreal Engine 4 > Blueprints - UE4 > Blueprint(UE4) Dynamic Material Instance
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Instance de Matériau dynamique Blueprint(UE4)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '458'
ht-degree: 0%

---


# Blueprint(UE4) : instance de Matériau dynamique

Vous pouvez créer une instance de Graphe Substance pour créer une Instance de graphe dynamique lors de l’exécution.

1. Créez une variable de type Substance Instance Factory et définissez la valeur par défaut sur Imported Substance Factory.
1. Ajoutez un nœud Créer une Instance de graphe et connectez l&#39;instance de Substance Factory à l&#39;entrée Factory. Définissez un nom d’instance.
1. Créez une autre variable de type Substance Instance Factory. Cette action contiendra une référence au matériau de substance dynamique.
1. Définissez la variable du matériau de substance dynamique avec la valeur renvoyée par le nœud Créer une Instance de graphe.
1. Créez une variable de type Matériau. Il s’agira du modèle de matériau. Dans l’Explorateur de contenu, dupliquez le matériau UE4 généré par la Substance. Définissez ce matériau dupliqué comme entrée pour la variable de modèle de matériau.
1. Ajoutez une instance de Matériau dynamique et définissez la variable Modèle de Matériau comme parent.

   ![](../../../../../assets/rt-01.png){width="800px"}
1. Créez une variable de type Matériau. Il s’agira de l’instance de Matériau dynamique (MID). Définissez la valeur renvoyée par l’instance de Matériau dynamique sur la variable.

   ![](../../../../../assets/rt-02.png){width="800px"}
1. Ajoutez un nœud de Matériau Set et définissez la valeur de la variable MID comme entrée de Matériau. Pour la cible, définissez-la sur l’objet auquel vous souhaitez appliquer le matériau.
1. Créez une variable de type Nom. Cette variable contiendra le nom des canaux définis dans le matériau. Initialisez ceci avec une valeur de « NONE »
1. Ajoutez un nœud Get Substance Textures et définissez l&#39;Instance de graphe sur la variable d&#39;Instance de graphe dynamique.
1. Ajoutez un nœud For Loop. Ici, vous passez en revue les Textures de Substance. Prenez le résultat des Textures Get Substance comme tableau d&#39;entrée.

   ![](../../../../../assets/rt-03.png){width="800px"}
1. Ajoutez un nœud Substance Get Channel avec l&#39;élément array de la boucle for comme entrée.
1. Ajoutez un nœud Séquence. Ici, nous allons d’abord exécuter le résultat du nœud Obtenir le canal.
1. Ajoutez un commutateur sur ESubChannelType après la séquence Puis 0 avec la valeur de retour Obtenir le canal comme sélection. Ici, nous vérifions les noms des canaux.
1. Définissez la variable Nom MID sur les noms de canal dans le Matériau de Substance dupliqué à partir de l’étape 5. *Voir l’image du matériau.*
1. Dans le nœud Séquence Then 1, vous allez configurer le processus d’affectation des noms de canal au matériau dynamique.
1. Obtenez la variable de nom MID et ajoutez un nœud de chaîne égal avec la valeur « NONE ». Il s&#39;agit de la valeur qui initialisera la variable.
1. Ajoutez un nœud de branche avec la condition du nœud Equal.
1. Ajoutez une valeur de paramètre de Texture de jeu de Substances. La cible est la variable MID et le nom du paramètre est la variable de nom MID. La valeur est l&#39;élément Array du nœud ForEachLoop.

![](../../../../../assets/material-1.png){width="800px"}
