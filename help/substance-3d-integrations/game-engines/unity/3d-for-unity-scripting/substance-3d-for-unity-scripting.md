---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unity/substance-3d-for-unity-scripting.html"
breadcrumb-title: ''
description: Utilisez l’API Substance 3D dans Unity pour écrire des scripts qui mettent à jour et modifient les paramètres de Substance à l’exécution.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unity > Substance 3D for Unity Scripting
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Substance 3D pour les scripts Unity
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 0%

---


# Substance 3D pour les scripts Unity

Cette section de la documentation contient des détails sur l’API Substance 3D que nous fournissons via le plug-in Substance 3D pour Unity. À l’aide des API de Substance de données, vous pouvez écrire des scripts pour mettre à jour et modifier les paramètres de Substance de données lors de l’exécution.

## Présentation de l’API

Le plug-in est divisé en 3 assemblys différents.

* Adobe.Substance
* Adobe.Substance.Editor
* Adobe.Substance.Runtime

### Adobe.Substance

Contient des composants partagés pour interagir avec le SDK Substance et générer des objets Unity correspondants. Il dispose également de structures de données de marshaling pour la communication entre C# et l&#39;API C++ du SDK Substance.

#### Adobe.Substance.Editor

Contient des classes spécifiques à l&#39;éditeur pour gérer l&#39;affichage des informations sur les objets de Substance Unity ainsi que le pipeline d&#39;importation pour quand des fichiers sbsar sont ajoutés au projet. La classe SubstanceEditorEngine est un singleton qui gère la durée de vie du moteur Substance et de toutes ses instances gérées.

#### Adobe.Substance.Runtime

Cette classe a des composants qui géreront la création et la gestion des objets de Substance de données pendant l&#39;exécution. SubstanceRuntime est l’équivalent de la classe SubstanceEditorEngine pour le runtime. Il gère l’initialisation du moteur Substance ainsi que l’instanciation de toute instance Substance avec laquelle les scripts utilisateur interagiront.

## Utilisation du runtime

Pour que les entrées d’instance de Substance soient modifiées lors de l’exécution, il est nécessaire d’ajouter un matériau SubstanceRuntime←- à votre scène (idéalement au même GameObject que votre matériau Substance). Cette classe agit comme un assistant pour configurer le matériau à l&#39;aide de Adobe.Substance.Runtime.SubstanceRuntime singleton qui gère l&#39;instanciation des objets du SDK Substance à l&#39;exécution.

## Exemples de code

L’exemple suivant montre comment modifier les paramètres d’entrée lors de l’exécution à l’aide de SubstanceRuntimeGraph.

### Modification des paramètres

```
using System.Collections; 

using System.Collections.Generic; 

using UnityEngine; 

using Adobe.Substance.Runtime; 

public class scifiScript: MonoBehaviour { 

  public Adobe.Substance.Runtime.SubstanceRuntimeGraph mySubstance; 

  // Use this for initialization 

  void Start() { 

    UpdateSubstance(); 

  } 

  public void UpdateSubstance() { 

    // panel color 

    mySubstance.SetInputColor("paint_color", new Color(0.237 f, 0.834 f, 0.045 f, 1.0 f)); 

    // panel size 

    mySubstance.SetInputVector2("square_open", new Vector2(0.101 f, 0.209 f)); 

    // wear level 

    mySubstance.SetInputFloat("wear_level", 0.977 f); 

    // Submit async render. 

    mySubstance.RenderAsync(); 

  } 

}
```


Vous pouvez également utiliser SubstanceRuntimeGraph pour avoir accès aux informations d’entrée et de sortie sur votre matériau de Substance.

#### Obtenir des informations d’entrée

```
using System.Collections; 

using System.Collections.Generic; 

using UnityEngine; 

using Adobe.Substance.Runtime; 

public class scifiScript: MonoBehaviour { 

  public Adobe.Substance.Runtime.SubstanceRuntimeGraph mySubstance; 

  // Use this for initialization 

  void Start() { 

    UpdateSubstance(); 

  } 

  public void UpdateSubstance() { 

    SubstanceInputDescription desc = mySubstance.GetInputDescription("paint_color"); 

    Debug.Log($ "Input: {desc.Identifier}"); 

    Debug.Log($ "Index: {desc.Index}"); 

    Debug.Log($ "Type: {desc.Type}"); 

    Debug.Log($ "Label: {desc.Label}"); 

  } 

}
```


L’exemple suivant montre comment créer un menu de paramètres prédéfinis personnalisé dans l’éditeur avec SubstanceEditorTools.

##### Création de commandes prédéfinies.

```
using System.Collections; 

using System.Collections.Generic; 

using UnityEngine; 

using Adobe.Substance.Runtime; 

public class scifiScript: MonoBehaviour { 

  public Adobe.Substance.Runtime.SubstanceRuntimeGraph mySubstance; 

  // Use this for initialization 

  void Start() { 

    UpdateSubstance(); 

  } 

  public void UpdateSubstance() { 

    SubstanceInputDescription desc = mySubstance.GetInputDescription("paint_color"); 

    Debug.Log($ "Input: {desc.Identifier}"); 

    Debug.Log($ "Index: {desc.Index}"); 

    Debug.Log($ "Type: {desc.Type}"); 

    Debug.Log($ "Label: {desc.Label}"); 

  } 

}
```
