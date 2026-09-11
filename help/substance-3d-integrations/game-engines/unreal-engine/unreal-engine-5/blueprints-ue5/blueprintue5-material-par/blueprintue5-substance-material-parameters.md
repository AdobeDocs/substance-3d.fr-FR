---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unreal-engine/unreal-engine-5/blueprints-ue5/blueprintue5-substance-material-parameters.html"
breadcrumb-title: ''
description: Modifiez les paramètres de matériau de Substance à l’exécution dans Moteur irréel 5 à l’aide des nœuds Blueprint pour le contrôle de matériau dynamique.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unreal Engine > Unreal Engine 5 > Blueprints - UE5 > Blueprint(UE5) Substance material parameters
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Paramètres du matériau de Substance Blueprint(UE5)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 0%

---


# Blueprint(UE5) : paramètres de matériau de Substance

## Modification d’un paramètre flottant :

Vous allez utiliser le [nœud de Flottant d&#39;entrée](https://helpx.adobe.com/substance-3d/unlisted/documentation/integrations/blueprint-node-reference-151584784.html) pour modifier les paramètres float, color(float4) et Booléen substance.

1. Créez une variable avec un type « Instance de Graphe Substance » comme Référence.\
   \**Pour ce faire, ajoutez une variable dans l’onglet Mon plan directeur et nommez-la. Dans la liste déroulante, recherchez Instance de Graphe Substance > Référence d’objet. Faites glisser la variable dans le graphe et sélectionnez Obtenir (Nom de la variable). Définissez l&#39;instance de Graphe Substance dans la section Valeur par défaut de l&#39;onglet Détails.*
1. Créez un nœud de Flottant d’entrée Set et définissez la cible comme variable Instance de Graphe Substance. Il peut être nécessaire de décocher la case Contexte dans la fenêtre de recherche pour afficher tous les résultats.
1. Sur le nœud Définir le Flottant d&#39;entrée, définissez Identifiant comme nom du paramètre de Substance à modifier.\
   *\* Vous pouvez rechercher le nom de l&#39;Identifiant en ouvrant la Substance INST et en passant la souris sur le nom du paramètre. Le nom de l&#39;Identifiant apparaîtra dans la fenêtre contextuelle de l&#39;info-bulle.*
1. Sur le nœud de Flottant d&#39;entrée, faites glisser une connexion et créez un nœud de tableau Make. Le nœud Make Array aura un index de 0. L’index de 0 correspond à la valeur flottante.
1. Créez un nœud de rendu Async ou Sync et connectez la ligne d’exécution du Flottant Définir l’entrée au nœud de rendu. Définissez Instances sur Rendu sur la variable Instance de Graphe Substance.\
   *\* Async n’est pas bloquant et Sync est bloquant.*

![](../../../../../assets/steps.png){width="800px"}

## paramètres de Booléen

Les paramètres du Booléen sont modifiés à l’aide de Définir le livre d’entrée.

![](../../../../../assets/setbool.png){width="800px"}

## Paramètres de couleur

Les paramètres de couleur sont modifiés à l’aide de l’option Définir la couleur d’entrée.

![](../../../../../assets/setcolor.png){width="800px"}

## Modification d’un paramètre d’Entier :

Les paramètres d’Entier fonctionnent de la même manière que le Flottant Définir l’entrée. Vous allez utiliser le nœud Définir l’Entier d’entrée.

![](../../../../../assets/int.png)

## Identifiants

L&#39;identifiant d&#39;un paramètre se trouve dans la substance INST. Déplacez la souris sur le paramètre et l’info-bulle affiche le nom de l’identifiant. Il s’agit du nom défini dans le champ identifiant de la sortie dans la Substance Designer.

![](../../../../../assets/screen-shot-2022-04-01-at-4-50-02-pm-copy.png)
