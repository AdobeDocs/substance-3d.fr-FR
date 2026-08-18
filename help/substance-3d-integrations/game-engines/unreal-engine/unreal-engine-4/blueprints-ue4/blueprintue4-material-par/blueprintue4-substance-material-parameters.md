---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unreal-engine/unreal-engine-4/blueprints-ue4/blueprintue4-substance-material-parameters.html"
breadcrumb-title: ''
description: Modifiez les paramètres des matériaux de Substance lors de l’exécution dans Unreal Engine 4 à l’aide des nœuds Blueprint pour le contrôle dynamique des matériaux.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unreal Engine > Unreal Engine 4 > Blueprints - UE4 > Blueprint(UE4) Substance material parameters
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Blueprint(UE4) Substance paramètres de matériau
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 0%

---


# Blueprint(UE4) : paramètres des matériaux de Substance

## Modification d’un paramètre flottant :

Vous allez utiliser le nœud [Définir la valeur flottante d&#39;entrée](https://helpx.adobe.com/substance-3d/unlisted/documentation/integrations/blueprint-node-reference-151584784.html) pour modifier un paramètre float, color(float4) et une substance booléenne.

1. Créez une variable avec un type « Instance de Graphe Substance » comme Référence.
1. Créez un nœud flottant d’entrée défini et définissez la cible comme variable d’instance de Graphe Substance.
1. Dans le nœud Définir les valeurs flottantes d&#39;entrée, définissez l&#39;identificateur sur le nom du paramètre de Substance à modifier.\
   *\* Vous pouvez rechercher le nom de l&#39;identificateur en ouvrant la Substance INST et en plaçant le curseur de la souris sur le nom du paramètre. Le nom de l&#39;identifiant apparaîtra dans la fenêtre contextuelle de l&#39;info-bulle.*
1. Sur le nœud flottant d&#39;entrée, faites glisser une connexion et créez un nœud de tableau Make. Le nœud Make Array aura un index de 0. L’index de 0 correspond à la valeur flottante.
1. Créez un nœud de rendu asynchrone ou synchronisé et connectez la ligne d’exécution du flottant Définir l’entrée au nœud de rendu. Définissez Instances sur Rendu sur la variable Instance de Graphe Substance.\
   *\* Async n’est pas bloquant et Sync est bloquant.*

![](../../../../../assets/steps.png){width="800px"}

## Paramètres booléens

Les paramètres booléens sont modifiés à l’aide de l’option Définir le bol d’entrée.

![](../../../../../assets/setbool.png){width="800px"}

## Paramètres de couleur

Les paramètres de couleur sont modifiés à l’aide de l’option Définir la couleur d’entrée.

![](../../../../../assets/setcolor.png){width="800px"}

## Modification d&#39;un paramètre Integer :

Les paramètres d’entier fonctionnent de la même manière que la valeur flottante Définir l’entrée. Vous allez utiliser le nœud Set Input Integer.

![](../../../../../assets/int.png)

## Identifiants

Vous pouvez trouver l&#39;identifiant d&#39;un paramètre dans la substance INST. Déplacez la souris sur le paramètre et l’info-bulle affiche le nom de l’identifiant. Il s’agit du nom défini dans le champ d’identificateur de la sortie en Substance Designer.

![](../../../../../assets/indent-1.png){width="800px"}
