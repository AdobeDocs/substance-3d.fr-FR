---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unity/scripting-in-unity-deprecated/api-overview.html"
breadcrumb-title: ''
description: Présentation de référence de l’API Substance Unity obsolète pour les projets hérités et les besoins en matière de scripts.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unity > Scripting in Unity (Deprecated) > API Overview
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Présentation de l’API
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 0%

---


# Présentation de l’API

## Substance.Jeu

```
Using Substance.Game
```


Substance.Game est l&#39;assembly qui contient les classes utilisées pour le script. Ces classes sont les suivantes :

**Substance.Game.**&#x200B;**Substance** : fait référence au fichier sbsar

**Substance.Game.SubstanceGraph** : graphique individuel dans le sbsar.*(anciennement ProceuralMaterial dans Unity 2017)*

## Processus de script

1. Création d’une instance de SubstanceGraph
1. Définissez les paramètres de l’instance de graphe.
1. Placer la Substance dans la file d&#39;attente de rendu : QueueForRender() ajoutera le graphique Substance à une file d&#39;attente. Cette liste sera traitée lors du prochain appel à RenderAsync ou RenderSync.

### Paramètres d&#39;instance de graphique

```
// panel color 

mySubstance.SetInputColor("paint_color", color); 

 

// panel size 

mySubstance.SetInputVector2("square_open", panelSize); 

 

// wear level 

mySubstance.SetInputFloat("wear_level", wearLevel);
```


La valeur entre guillemets est le paramètre Identificateur défini dans la Substance Designer.

Dans l’Inspecteur Unity, vous pouvez passer la souris sur un paramètre pour afficher une info-bulle présentant le nom de l’identificateur défini dans la Substance Designer.

![](../../../../assets/tooltip-6.png)

### Mise en file d’attente de la substance pour le rendu

```
// queue the substance to render 

mySubstance.QueueForRender(); 

 

//render all substances async 

Substance.Game.Substance.RenderAsync();
```


![](../../../../assets/unityscript.gif)

>[!NOTE]
>
> Actuellement, nous ne prenons en charge que l’architecture x86\_64. Vous devez définir x86\_64 dans les paramètres de construction

![](../../../../assets/arch.png)
