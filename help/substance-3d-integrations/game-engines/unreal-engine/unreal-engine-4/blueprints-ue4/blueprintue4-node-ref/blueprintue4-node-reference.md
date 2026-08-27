---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unreal-engine/unreal-engine-4/blueprints-ue4/blueprintue4-node-reference.html"
breadcrumb-title: ''
description: Guide de référence pour tous les nœuds Substance Blueprint disponibles dans Unreal Moteur 4 pour les opérations de matériau.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unreal Engine > Unreal Engine 4 > Blueprints - UE4 > Blueprint(UE4) Node Reference
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Référence du nœud Blueprint(UE4)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '856'
ht-degree: 0%

---


# Blueprint(UE4) : Référence du nœud

## Nœuds de Substance généraux :

| Nom | Entrées | Description |
| --- | --- | --- |
| **GetSubstances** | Matériau | Renvoie un tableau d&#39;instances de Graphe Substance utilisées par un matériau. Si vous créez un matériau qui utilise des sorties de texture de données provenant de deux instances de graphe différentes, cette fonction renvoie ces deux instances de graphe. |
| **GetSubstanceTextures** | **SubstanceGraphInstance** | Retourne un tableau de toutes les textures activées et actuellement calculées à partir du paramètre d&#39;entrée Instance de Graphe Substance. |
| **GetGraphName** | **SubstanceGraphInstance** | Renvoie le nom du graphe tel que défini dans Designer. |
| **GetFactoryName** | **SubstanceGraphInstance** | Renvoie le nom de **GraphInstanceFactory** qui a été utilisé pour créer **SubstanceGraphInstance** qui est passé dans ce nœud. |
| **GetSubstanceLoadingProgress** | AUCUN | Renvoie une valeur flottante comprise entre 0 et 1 avec le pourcentage du nombre de substances entièrement chargées. |
| **CreateGraphInstance** | Entrée : **SubstanceInstanceFactory** - Usine à partir de laquelle vous souhaitez créer une instance de graphe.Entrée : **GraphIndex** (int) - Index du graphe que vous souhaitez créer. Entrée : **InstanceName** (FString) : nom que vous souhaitez donner à votre nouvelle instance. | Renvoie une nouvelle instance de graphique autonome qui persiste jusqu’à la fermeture de l’application. |
| **DuplicateGraphInstance** | **SubstanceGraphInstance** : instance de graphique dont vous souhaitez créer une copie. | Renvoie une nouvelle instance de graphique autonome qui persiste jusqu’à la fermeture de l’application. |
| **EnableInstanceOutcomes** | Entrée : **SubstanceGraphInstance** : instance de graphique contenant la sortie pour activer l&#39;entrée : **OutputIndices** (tableau int32) : indices des sorties que vous souhaitez activer. (Sous réserve de modification) | Si cette option est désactivée précédemment, crée la ou les sorties de texture de transmises dans **SubstanceGraphInstance**. Cela a la même fonctionnalité que l&#39;activation d&#39;une sortie de l&#39;éditeur **SubstanceGraphInstance**. *REMARQUE : cela ne mettra pas à jour votre matière avec la texture nouvellement créée. Cela doit être géré en définissant un paramètre d&#39;échantillonnage au moment de l&#39;exécution à l&#39;aide de la nouvelle sortie.* |
| **DisableInstanceOutcomes** | Entrée : **SubstanceGraphInstance** : instance de graphe à laquelle vous souhaitez appliquer des valeurs.Entrée : **SubstanceGraphInstance** : instance de graphe à partir de laquelle vous souhaitez obtenir les valeurs. | Restaure toutes les valeurs d&#39;entrée modifiées du paramètre d&#39;entrée Instance de Graphe Substance. |
| **SetGraphInstanceOutputSize** | Entrée : **SubstanceGraphInstance** Entrée : Largeur - Résolution de la texture de la coordonnée X Entrée : Height - Résolution de la texture de la coordonnée Y | Définit la résolution de texture de toutes les sorties générées à partir de cette instance de graphique avec les tailles transmises par les paramètres. Remarque - Max. 2048 sur CPU EngineNote - Max. 4096 sur GPU Engine |
| **Rendu asynchrone** | **SubstanceGraphInstance** | Recalcule les textures de sortie de l’entrée Instance de Graphe Substance. (Non bloquant) |
| **SyncRendering** | **SubstanceGraphInstance** | Recalcule les textures de sortie de l’entrée Instance de Graphe Substance. (Blocage) |

## Fonctions spécifiques à l’Instance de graphe :

Peut uniquement être appelé à partir d&#39;une instance de graphe

| Nom | Entrée | Description |
| --- | --- | --- |
| **GetInputNames** | AUCUN | Renvoie un tableau de chaînes contenant tous les noms de paramètres d&#39;entrée. |
| **GetInputType** | AUCUN | Renvoie le type de données associé à cette entrée. |
| **SetInputInt** | Entrée : **Identifiant** (chaîne)Entrée : **InputValues** (tableau int) | Modifiez la valeur d’une entrée trouvée par l’identificateur. À partir d&#39;un jeu, vous devez effectuer le rendu de substance à l&#39;aide de **AyncRender** ou de **SyncRender** pour que les modifications soient appliquées. |
| **SetInputFloat** | Entrée : **Identifiant** (chaîne)Entrée : **InputValues** (tableau flottant) | Modifiez la valeur d’une entrée trouvée par l’identificateur. À partir d&#39;un jeu, vous devez effectuer le rendu de substance à l&#39;aide de **AyncRender** ou de **SyncRender** pour que les modifications soient appliquées. |
| **GetInputInt** | Entrée : **Identificateur** (Chaîne) | Renvoie un tableau d’unités avec les valeurs actuelles d’un paramètre d&#39;entrée. |
| **GetInputFloat** | Identifiant (Chaîne) | Renvoie un tableau de valeurs flottantes avec les valeurs actuelles d&#39;un paramètre d&#39;entrée. |
| **SetInputBool** | Entrée : **Bool** (Booléen)Entrée : **Identifiant** (Chaîne) | Prend une valeur booléenne pour attribuer un type de valeur d&#39;entrée basculable. Auparavant, cela n&#39;était possible qu&#39;en définissant une valeur int de 1 ou de 0 convertie à un bool. |
| **GetInputBool** | Entrée : **Identificateur** (Chaîne) | Renvoie la valeur booléenne actuelle d&#39;une entrée. |
| **SetIputColor** | Entrée : **Couleur** (LinearColor)Entrée : **Identifiant** (FString) | Prend une valeur FLinearColor à laquelle affecter un type de valeur d&#39;entrée de couleur. Auparavant, cela n&#39;était possible qu&#39;en définissant une valeur de flotteur et en passant un tableau de flotteurs. |
| **GetInputColor** | Entrée : Identifier (FString) | Renvoie la valeur de couleur actuelle au format UE4. |
| **CreateAggregateSubstanceFactory** | Entrée : **Output Factory** (SubstanceInstanceFactory)*Usine créant les sorties qui seront utilisées comme entrée dans la fabrique d’entrée.* Entrée : **Index des graphiques Output Factory** (entier)*Quel graphique dans la substance vous souhaitez utiliser pour la combinaison.* Entrée : **Input Factory** (SubstanceInputFactory)*Usine utilisant les sorties comme images d’entrée à partir de Output Factory. Entrée :**Connections**(Array of SubstanceConnections)*Cette opération peut être créée à l’aide du nœud de plan directeur Make Array. Une connexion Substance est la façon dont vous pouvez agréger le nœud avec quelles entrées lier à quelles sorties.* ** Return (SubstanceInstanceFactory)***Peut être utilisé pour créer une instance de graphique de la nouvelle instance combinée.* | Le nouveau nœud Substance agrégé vous permet de prendre deux usines d&#39;instances Substance et de créer une nouvelle usine d&#39;instances à l&#39;exécution, qui peut être utilisée pour créer une nouvelle instance de graphe. Ce qui rend cela spécial, c&#39;est que vous pouvez connecter des textures de sortie de l&#39;une des instances de graphe combinées aux images d&#39;entrée de l&#39;autre instance de graphe combinée. Pour créer une instance de graphe Substance à partir de cette nouvelle usine, consultez notre documentation sur les instances de graphe d’exécution. |
| **SubstanceConnectionStruct** | Entrée : **Identifiant de sortie** (FString)*identifiant de la sortie de la texture à enchaîner dans une entrée.* Entrée : **Identifiant d&#39;entrée** (FString) | Utilisé par Create Aggregate Substance Factory pour spécifier comment enchaîner chaque texture de sortie avec de nouvelles textures d&#39;entrée. |
