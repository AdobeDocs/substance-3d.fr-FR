---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unity/substance-3d-for-unity-scripting/class-documentation/substanceruntimegraph-class.html"
breadcrumb-title: ''
description: Documentation de référence pour la classe SubstanceRuntimeGraph utilisée pour les opérations de graphique d’exécution dans Unity.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unity > Substance 3D for Unity Scripting > Class Documentation > SubstanceRuntimeGraph Class
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: SubstanceRuntimeGraph, classe
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '290'
ht-degree: 0%

---


# SubstanceRuntimeGraph, classe

## Référence de classe Adobe.Substance.Runtime.SubstanceRuntimeGraph

Classe qui fournit une fonctionnalité d’exécution pour modifier les entrées et effectuer le rendu des graphiques Substance, permettant à Substance ←GraphSO de générer ses actifs à l’exécution.

Diagramme d&#39;héritage pour Adobe.Substance.Runtime.SubstanceRuntimeGraph :

![](../../../../../assets/image2022-10-14-17-53-23-1.png)

### Fonctions de membre public

```
• void AttachGraph (SubstanceGraphSO graph)
```


Attache un nouvel objet graphe à ce gestionnaire d&#39;exécution.

```
• void SetInputFloat (string inputName, float value)
```


Mettre à jour l&#39;entrée flottante de la Substance

```
• float GetInputFloat (string inputName)
```


Obtenir l’entrée Substance flottante

```
• void SetInputVector2 (string inputName, Vector2 value)
```


Mettre à jour l’entrée Substance Vector2

```
• Vector2 GetInputVector2 (string inputName)
```


Obtenir l’entrée Substance Vector2

```
• void SetInputVector3 (string inputName, Vector3 value)
```


Mettre à jour l’entrée Substance Vector3

```
• Vector3 GetInputVector3 (string inputName)
```


Obtenir l’entrée Substance Vector3.

```
• void SetInputVector4 (string inputName, Vector4 value)
```


Mettre à jour l’entrée Substance Vector4

```
• Vector4 GetInputVector4 (string inputName)
```


Obtenir l’entrée Substance Vector4

```
• void SetInputColor (string inputName, Color value)
```


Mettre à jour l&#39;entrée de couleur de Substance

```
• Color GetInputColor (string inputName)
```


Obtenir la couleur de Substance

```
• void SetInputBool (string inputName, bool value)
```


Mettre à jour l&#39;entrée booléenne de la Substance

```
• bool GetInputBool (string inputName)
```


Obtenir la saisie booléenne de Substance.

```
• void SetInputInt (string inputName, int value)
```


Mettre à jour l&#39;entrée d&#39;entrée Substance

```
• int GetInputInt (string inputName)
```


Obtenir une entrée Substance

```
• void SetInputVector2Int (string inputName, Vector2Int value)
```


Mettez À Jour L’Entrée Substance Vector2Int.

```
• Vector2Int GetInputVector2Int (string inputName)
```


Obtenir un tableau de 2 int.

```
• void SetInputVector3Int (string inputName, Vector3Int value)
```


Mettez à jour l’entrée Substance Vector3Int.

```
• Vector3Int GetInputVector3Int (string inputName)
```


Obtenir un tableau de 3 int (valeurs x, y et z de Vector3Int)

```
• void SetInputVector4Int (string inputName, int x, int y, int z, int w)
```


Mettre à jour l’entrée Substance Vector4Int

```
• int[ ] GetInputVector4Int (string inputName)
```


Obtenir un tableau de 4 int (valeurs x, y, z et w de Vector4Int)

```
• void SetInputString (string inputName, string value)
```


Mettre à jour la chaîne de Substance Entrée.

```
• string GetInputString (string inputName)
```


Obtenir une entrée de chaîne de Substance.

```
• SubstanceInputDescription GetInputDescription (string inputName)
```


Renvoie la description d’entrée complète du nom d’entrée cible.

```
• void SetInputTexture (string inputName, Texture2D value)
```


Mettez à jour Substance Texture2D Input.

```
• Vector2Int GetTexturesResolution ()
```


Renvoie la résolution de sortie de la texture d&#39;instance.

```
• void SetTexturesResolution (Vector2Int size)
```


Définit la résolution de sortie de la texture d’instance.

```
• bool HasInput (string inputName)
```


Renvoie true si cette instance de substance a une entrée avec un nom donné.

```
• List< Texture2D > GetGeneratedTextures ()
```


Renvoie une liste contenant toutes les textures de sortie de l’instance Substance.

```
•  Texture2D GetOutputTexture (string outputName)
```


Renvoie la texture de sortie pour un nom de sortie donné.

```
• void Render ()
```


Rend l’instance Substance de manière synchrone.

```
• Task RenderAsync ()
```


Effectue le rendu de l’instance de substance de manière asynchrone.

```
• void LoadPreset (string presetXML)
```


Utilise un fichier XML prédéfini pour définir les paramètres d’entrée du graphique.

```
• string CreatePresetFromCurrentState ()
```


Enregistre l’état actuel du graphique dans un fichier XML prédéfini.

## Attributs publics

```
• SubstanceGraphSO GraphSO
```


Instance de substance cible.

## Fonctions de membre protégées

```
• void Awake ()
```


En cas d’éveil, SubstanceRuntime sera utilisé pour créer une instance pour le SubstanceGraphSO joint dans la substance

SDK.

```
• void Update ()
```


Vérifiez les résultats du rendu dans la file d’attente de traitement simultané.

```
• void OnDestroy ()
```


Supprime le gestionnaire SDK Substance.

## Propriétés

```
• Material DefaulMaterial [get]
```


Matière principale générée par l’instance de substance.
