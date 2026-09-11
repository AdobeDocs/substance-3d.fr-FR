---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unreal-engine/unreal-engine-4/blueprints-ue4/blueprintue4-aggregate-substance.html"
breadcrumb-title: ''
description: Combinez plusieurs matériaux de Substance à l’exécution dans Unreal Moteur 4 à l’aide des nœuds d’agrégation Blueprint pour les workflows avancés.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unreal Engine > Unreal Engine 4 > Blueprints - UE4 > Blueprint(UE4) Aggregate Substance
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Blueprint(UE4) Substance agrégée
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 0%

---


# Blueprint(UE4) : Substance globale

Le nouveau nœud substance agrégé vous permet de prendre deux usines d&#39;instances de substance et de créer une nouvelle usine d&#39;instances à l&#39;exécution qui peut être utilisée pour créer une nouvelle instance de graphe. Ce qui rend cela spécial, c&#39;est que vous pouvez connecter des textures de sortie de l&#39;une des instances de graphe combinées aux images d&#39;entrée de l&#39;autre instance de graphe combinée. Pour créer une instance de graphe Substance à partir de cette nouvelle usine, consultez notre documentation sur les instances de graphe d’exécution. [Définition d&#39;instance de Matériau - UE4](https://helpx.adobe.com/substance-3d/unlisted/documentation/integrations/material-instance-definition-157352129.html)

1. Importez les Substances à utiliser.
1. Créez une variable « AggregateGraphInstance » de type **Instance de Graphe Substance**.
1. Créer une variable de type **Matériau** et **Instance de Matériau dynamique**
1. Créez une **connexion de Substance** et définissez les identifiants d&#39;entrée et de sortie.
1. Créez **une fabrique d&#39;instances de Substance d&#39;agrégation** et définissez la fabrique de sortie et d&#39;entrée.
1. Créez une **Instance de graphe** et définissez un nom d&#39;instance.
1. Définissez la variable **Instance de graphe d&#39;agrégation**.
1. Obtenez des textures de substance à partir de l&#39;Instance de graphe Agrégat à l&#39;étape 7 en utilisant **Obtenir des Textures de Substance**.
1. Créez une **instance de Matériau dynamique** en utilisant la variable de matériau de l&#39;étape 3 comme parent.
1. Définissez la variable MID à l’étape 3.
1. Définissez le matériau du maillage à l&#39;aide de **Définir le Matériau** avec la variable MID.

   ![](../../../../../assets/a2-3.png){width="800px"}
1. Définissez les canaux du matériau comme indiqué dans la documentation sur les instances de Matériau dynamique (étapes 11 à 19)\
   [Blueprint(UE4) : instance de Matériau dynamique](https://helpx.adobe.com/substance-3d/unlisted/documentation/integrations/blueprint-dynamic-material-instance-152535142.html)

   ![](../../../../../assets/a4-3.png){width="800px"}
