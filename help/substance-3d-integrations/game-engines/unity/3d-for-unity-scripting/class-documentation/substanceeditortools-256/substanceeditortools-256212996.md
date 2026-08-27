---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-integrations/game-engines/unity/substance-3d-for-unity-scripting/class-documentation/substanceeditortools-256212996.html"
breadcrumb-title: ''
description: Documentation de référence pour la classe SubstanceEditorTools utilisée pour la gestion des matériaux de Substance dans Unity.
helpx_creative_field: ""
helpx_description: Substance 3D Integrations
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: SubstanceEditorTools
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---


# SubstanceEditorTools

## Référence de classe Adobe.SubstanceEditor.SubstanceEditorTools

Outils et utilitaires à utiliser par les utilisateurs sur les scripts de l’éditeur.

Diagramme d&#39;héritage pour Adobe.SubstanceEditor.SubstanceEditorTools :

![](../../../../../assets/image2022-10-14-17-53-23.png)

### Fonctions de membre public statique

```
• static void SetGraphFloatInput (SubstanceGraphSO graph, int inputId, float value)
```


Définir l&#39;entrée flottante du graphique.

```
• static void SetGraphFloat2Input (SubstanceGraphSO graph, int inputId, Vector2 value)
```


Définissez l’entrée graph float2.

```
• static void SetGraphFloat3Input (SubstanceGraphSO graph, int inputId, Vector3 value)
```


Définissez l’entrée graph float3.

```
• static void SetGraphFloat4Input (SubstanceGraphSO graph, int inputId, Vector3 value)
```


Définissez l’entrée graph float4.

```
• static void SetGraphIntInput (SubstanceGraphSO graph, int inputId, int value)
```


Définissez l’entrée Graphe.

```
• static void SetGraphInt2Input (SubstanceGraphSO graph, int inputId, Vector2Int value)
```


Définissez l’entrée int2 du graphique.

```
• static void SetGraphInt3Input (SubstanceGraphSO graph, int inputId, Vector3Int value)
```


Définissez l’entrée graph int3.

```
• static void SetGraphInt4Input (SubstanceGraphSO graph, int inputId, int value0, int value1, int value2, int value3)
```


Définissez l’entrée graph int4.

```
• static void SetGraphInputString (SubstanceGraphSO graph, int inputId, string value)
```


Définissez l’entrée de chaîne de graphique.

```
• static void SetGraphInputTexture (SubstanceGraphSO graph, int inputId, Texture2D value)
```


Définissez l’entrée de texture du graphique.

```
• static void RenderGraph (SubstanceGraphSO graph)
```


Rend le graphique cible et met à jour ses actifs.

```
• static string CreatePresetFromCurrentState (SubstanceGraphSO graph)
```


Crée un fichier XML prédéfini à partir de l’état actuel de l’objet graphe.

```
• static List< SubstanceGraphSO > GetGraphs (this SubstanceFileSO fileSO)
```


Renvoie la liste des objets SubstanceGraphSO associés à un objet SubstanceFileSO.
