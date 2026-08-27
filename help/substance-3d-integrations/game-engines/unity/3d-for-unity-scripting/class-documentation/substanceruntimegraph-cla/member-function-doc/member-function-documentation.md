---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-integrations/game-engines/unity/substance-3d-for-unity-scripting/class-documentation/substanceruntimegraph-class/member-function-documentation.html"
breadcrumb-title: ''
description: Documentation détaillée de toutes les fonctions membres de la classe SubstanceRuntimeGraph dans les scripts Unity.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unity > Substance 3D for Unity Scripting > Class Documentation > SubstanceRuntimeGraph Class > Member Function Documentation
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Documentation sur les fonctions de membre
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '662'
ht-degree: 2%

---


# Documentation sur les fonctions de membre

## AttachGraph()

```
void Adobe.Substance.Runtime.SubstanceRuntimeGraph.AttachGraph  

( SubstanceGraphSO graph ) [inline]
```


Attache un nouvel objet graphe à ce gestionnaire d&#39;exécution.

**Paramètres**

|  |  |
| --- | --- |
| graphe | Graphique Substance cible. |

### CreatePresetFromCurrentState()

```
string Adobe.Substance.Runtime.SubstanceRuntimeGraph.CreatePresetFromCurrentState ( ) [inline]
```


Enregistre l’état actuel du graphique dans un fichier XML prédéfini.

**Retours**

Paramètre prédéfini créé à l’aide de l’état actuel des entrées de graphique.

### GetGeneratedTextures()

```
List< Texture2D > Adobe.Substance.Runtime.SubstanceRuntimeGraph.GetGeneratedTextures ( ) [inline]
```


Renvoie une liste contenant toutes les textures de sortie de l’instance Substance.

**Retours**

Texture de sortie.

### GetInputBool()

```
bool Adobe.Substance.Runtime.SubstanceRuntimeGraph.GetInputBool ( string inputName ) [inline]
```


Obtenir la saisie booléenne de Substance.

**Paramètres**

|  |  |
| --- | --- |
| inputName | Nom de l&#39;entrée dans le SBSAR. |


**Retours**

Valeur d’entrée actuelle.

### GetInputColor()

```
Color Adobe.Substance.Runtime.SubstanceRuntimeGraph.GetInputColor ( string inputName ) [inline]
```


Obtenir la couleur de Substance

**Paramètres**

|  |  |
| --- | --- |
| inputName | Nom de l&#39;entrée dans le SBSAR |


**Retours**

Valeur d’entrée actuelle.

### GetInputDescription()

```
SubstanceInputDescription Adobe.Substance.Runtime.SubstanceRuntimeGraph.GetInputDescription ( string inputName ) [inline]
```


Renvoie la description d’entrée complète du nom d’entrée cible.

**Paramètres**

|  |  |
| --- | --- |
| inputName | Nom de l’entrée cible. |


**Retours**

Description complète de l’entrée cible.

### GetInputFloat()

```
float Adobe.Substance.Runtime.SubstanceRuntimeGraph.GetInputFloat ( string inputName ) [inline]
```


Obtenir l’entrée Substance flottante

**Paramètres**

|  |  |
| --- | --- |
| inputName | Nom de l&#39;entrée dans le SBSAR |


**Retours**

Valeur d’entrée actuelle.

### GetInputInt()

```
int Adobe.Substance.Runtime.SubstanceRuntimeGraph.GetInputInt ( string inputName ) [inline]
```


Obtenir une entrée Substance

**Paramètres**

|  |  |
| --- | --- |
| inputName | Nom de l&#39;entrée dans le SBSAR |


**Retours**

Valeur d’entrée actuelle.

### GetInputString()

```
string Adobe.Substance.Runtime.SubstanceRuntimeGraph.GetInputString ( string inputName ) [inline]
```


Obtenir une entrée de chaîne de Substance.

**Paramètres**

|  |  |
| --- | --- |
| inputName | Nom de l&#39;entrée dans le SBSAR |


**Retours**

Saisir la valeur actuelle.

### GetInputVector2()

```
Vector2 Adobe.Substance.Runtime.SubstanceRuntimeGraph.GetInputVector2 ( string inputName ) [inline]
```


Obtenir l’entrée Substance Vector2

**Paramètres**

|  |  |
| --- | --- |
| inputName | Nom de l&#39;entrée dans le SBSAR |


**Retours**

Valeur d’entrée actuelle.

### GetInputVector2Int()

```
Vector2Int Adobe.Substance.Runtime.SubstanceRuntimeGraph.GetInputVector2Int ( string inputName ) [inline]
```


Obtenir un tableau de 2 int.

**Paramètres**

|  |  |
| --- | --- |
| inputName | Nom de l&#39;entrée dans le SBSAR |


**Retours**

Valeur d’entrée actuelle.

### GetInputVector3()

```
Vector3 Adobe.Substance.Runtime.SubstanceRuntimeGraph.GetInputVector3 ( string inputName ) [inline]
```


Obtenir l’entrée Substance Vector3.

**Paramètres**

|  |  |
| --- | --- |
| inputName | Nom de l&#39;entrée dans le SBSAR |


**Retours**

Valeur d’entrée actuelle.

### GetInputVector3Int()

```
Vector3Int Adobe.Substance.Runtime.SubstanceRuntimeGraph.GetInputVector3Int ( string inputName ) [inline]
```


Obtenir un tableau de 3 int (valeurs x, y et z de Vector3Int)

**Paramètres**

|  |  |
| --- | --- |
| inputName | Nom de l&#39;entrée dans le SBSAR |


**Retours**

Valeur d’entrée actuelle.

### GetInputVector4()

```
Vector4 Adobe.Substance.Runtime.SubstanceRuntimeGraph.GetInputVector4 ( string inputName ) [inline]
```


Obtenir l’entrée Substance Vector4

**Paramètres**

|  |  |
| --- | --- |
| inputName | Nom de l&#39;entrée dans le SBSAR |


**Retours**

Valeur d’entrée actuelle.

### GetInputVector4Int()

```
int[] Adobe.Substance.Runtime.SubstanceRuntimeGraph.GetInputVector4Int ( string inputName ) [inline]
```


Obtenir un tableau de 4 int (valeurs x, y, z et w de Vector4Int)

**Paramètres**

|  |  |
| --- | --- |
| inputName | Nom de l&#39;entrée dans le SBSAR |


**Retours**

Valeur d’entrée actuelle.

### GetOutputTexture()

```
Texture2D Adobe.Substance.Runtime.SubstanceRuntimeGraph.GetOutputTexture ( string outputName ) [inline]
```


Renvoie la texture de sortie pour un nom de sortie donné.

**Paramètres**

|  |  |
| --- | --- |
| outputName | Nom de la sortie. |


**Retours**

Texture de sortie.

### GetTexturesResolution()

```
Vector2Int Adobe.Substance.Runtime.SubstanceRuntimeGraph.GetTexturesResolution ( ) [inline]
```


Renvoie la résolution de sortie de la texture d&#39;instance.

**Retours**

Résolution de sortie actuelle.

### HasInput()

```
bool Adobe.Substance.Runtime.SubstanceRuntimeGraph.HasInput ( string inputName ) [inline]
```


Renvoie true si cette instance de substance a une entrée avec un nom donné.

**Paramètres**

|  |  |
| --- | --- |
| inputName | Saisir un nom. |


**Retours**

TRUE si l&#39;instance substance a une entrée avec le nom donné.

### LoadPreset()

```
void Adobe.Substance.Runtime.SubstanceRuntimeGraph.LoadPreset ( string presetXML ) [inline]
```


Utilise un fichier XML prédéfini pour définir les paramètres d’entrée du graphique.

**Paramètres**

|  |  |
| --- | --- |
| presetXML | Données XML prédéfinies. |

### RenderAsync()

```
Task Adobe.Substance.Runtime.SubstanceRuntimeGraph.RenderAsync ( ) [inline]
```


Effectue le rendu de l’instance de substance de manière asynchrone.

**Retours**

Tâche qui se termine une fois le rendu terminé.

### SetInputBool()

```
void Adobe.Substance.Runtime.SubstanceRuntimeGraph.SetInputBool ( string inputName, 

bool value ) [inline]
```


Mettre à jour l&#39;entrée booléenne de la Substance

**Paramètres**

|  |  |
| --- | --- |
| inputName | Nom de l&#39;entrée dans le SBSAR |
| valeur | Valeur utilisée pour mettre à jour le paramètre |

### SetInputColor()

```
void Adobe.Substance.Runtime.SubstanceRuntimeGraph.SetInputColor ( string inputName, 

Color value ) [inline]
```


Mettre à jour l&#39;entrée de couleur de Substance

**Paramètres**

|  |  |
| --- | --- |
| inputName | Nom de l&#39;entrée dans le SBSAR |
| valeur | Valeur utilisée pour mettre à jour le paramètre |

### SetInputFloat()

```
void Adobe.Substance.Runtime.SubstanceRuntimeGraph.SetInputFloat ( string inputName, 

float value ) [inline]
```


Mettre à jour l&#39;entrée flottante de la Substance

**Paramètres**

|  |  |
| --- | --- |
| inputName | Nom de l&#39;entrée dans le SBSAR |
| valeur | Valeur utilisée pour mettre à jour le paramètre |

### SetInputInt()

```
void Adobe.Substance.Runtime.SubstanceRuntimeGraph.SetInputInt ( string inputName, 

int value ) [inline]
```


Mettre à jour l&#39;entrée d&#39;entrée Substance

**Paramètres**

|  |  |
| --- | --- |
| inputName | Nom de l&#39;entrée dans le SBSAR |
| valeur | Valeur utilisée pour mettre à jour le paramètre |

### SetInputString()

```
void Adobe.Substance.Runtime.SubstanceRuntimeGraph.SetInputString ( string inputName, 

string value ) [inline]
```


Mettre à jour la chaîne de Substance Entrée.

**Paramètres**

|  |  |
| --- | --- |
| inputName | Nom de l&#39;entrée dans le SBSAR |
| valeur | Valeur utilisée pour mettre à jour le paramètre |

### SetInputTexture()

```
void Adobe.Substance.Runtime.SubstanceRuntimeGraph.SetInputTexture (string inputName, 

Texture2D value ) [inline]
```


Mettez à jour l’entrée Substance Texture 2D.

**Paramètres**

|  |  |
| --- | --- |
| inputName | Nom de l&#39;entrée dans le SBSAR |
| valeur | Valeur utilisée pour mettre à jour le paramètre |

### SetInputVector2()

```
void Adobe.Substance.Runtime.SubstanceRuntimeGraph.SetInputVector2 ( string inputName, 

Vector2 value ) [inline]
```


Mettre à jour l’entrée Substance Vector2

**Paramètres**

|  |  |
| --- | --- |
| inputName | Nom de l&#39;entrée dans le SBSAR |
| valeur | Valeur utilisée pour mettre à jour le paramètre |

### SetInputVector2Int()

```
void Adobe.Substance.Runtime.SubstanceRuntimeGraph.SetInputVector2Int ( string inputName, 

Vector2Int value ) [inline]
```


Mettez À Jour L’Entrée Substance Vector2Int.

**Paramètres**

|  |  |
| --- | --- |
| inputName | Nom de l&#39;entrée dans le SBSAR |
| valeur | Valeur utilisée pour mettre à jour le paramètre |

### SetInputVector3()

```
void Adobe.Substance.Runtime.SubstanceRuntimeGraph.SetInputVector3 ( string inputName, 

Vector3 value ) [inline]
```


Mettre à jour l’entrée Substance Vector3

**Paramètres**

|  |  |
| --- | --- |
| inputName | Nom de l&#39;entrée dans le SBSAR |
| valeur | Valeur utilisée pour mettre à jour le paramètre |

### SetInputVector3Int()

```
void Adobe.Substance.Runtime.SubstanceRuntimeGraph.SetInputVector3Int ( string inputName, 

Vector3Int value ) [inline]
```


Mettez à jour l’entrée Substance Vector3Int.

**Paramètres**

|  |  |
| --- | --- |
| inputName | Nom de l&#39;entrée dans le SBSAR |
| valeur | Valeur utilisée pour mettre à jour le paramètre |

### SetInputVector4()

```
void Adobe.Substance.Runtime.SubstanceRuntimeGraph.SetInputVector4 ( string inputName, 

Vector4 value ) [inline]
```


Mettre à jour l’entrée Substance Vector4

**Paramètres**

|  |  |
| --- | --- |
| inputName | Nom de l&#39;entrée dans le SBSAR |
| valeur | Valeur utilisée pour mettre à jour le paramètre |

### SetInputVector4Int()

```
void Adobe.Substance.Runtime.SubstanceRuntimeGraph.SetInputVector4Int ( string inputName, 

int x, 

int y, 

int z, 

int w ) [inline]
```


Mettre à jour l’entrée Substance Vector4Int

**Paramètres**

|  |  |
| --- | --- |
| inputName | Nom de l&#39;entrée dans le SBSAR |
| x | Valeur utilisée pour mettre à jour le paramètre |
| y | Valeur utilisée pour mettre à jour le paramètre |
| z | Valeur utilisée pour mettre à jour le paramètre |
| w | Valeur utilisée pour mettre à jour le paramètre |

### SetTexturesResolution()

```
void Adobe.Substance.Runtime.SubstanceRuntimeGraph.SetTexturesResolution ( Vector2Int size ) [inline]
```


Définit la résolution de sortie de la texture d’instance.

**Paramètres**

|  |  |
| --- | --- |
| taille |  |
