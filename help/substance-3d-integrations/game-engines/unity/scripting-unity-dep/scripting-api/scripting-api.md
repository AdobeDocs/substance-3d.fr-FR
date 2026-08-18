---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unity/scripting-in-unity-deprecated/scripting-api.html"
breadcrumb-title: ''
description: Documentation de référence pour l’API de script Unity de Substance obsolète pour la prise en charge des projets hérités.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unity > Scripting in Unity (Deprecated) > Scripting API
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: API de script
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '1074'
ht-degree: 1%

---


# API de script

## Substance dans l’API Unity - 2.2.0

## paramètres des matériaux de Substance

| Méthode publique | Description | Paramètre |
| --- | --- | --- |
| **float** *GetInputFloat*(**string** inputName) public | Obtenir Une Entrée De Substance **Float** | **Chaîne** *inputName* Nom de l&#39;entrée dans le SBSAR |
| **int** *SetInputFloat*(**string** inputName, **float** value) public | Mettre à jour l&#39;entrée de Substance **flottante** | **Chaîne** i *nputName* Nom de l&#39;entrée dans la valeur SBSAR **Float** *value* utilisée pour mettre à jour le paramètre |
| public **void** *SetInputVector2*(**string** inputName, **Vector2** value) | Mettre À Jour L&#39;Entrée **Vecteur2** De La Substance | **Chaîne** *inputName* Nom de l&#39;entrée dans les valeurs SBSAR **Vector2** *input* utilisées pour mettre à jour le paramètre |
| public **vector2** *GetInputVector2*(**string** inputName) | Obtenir Une Entrée De Substance **Vectorielle2** | **Chaîne** « inputName » Nom de l&#39;entrée dans le SBSAR |
| public **void** *SetInputVector3*(**string** inputName, **Vector3** value) | Mettre à jour l&#39;entrée de Substance **vectorielle3** | **Chaîne** *inputName* Nom de l&#39;entrée dans les valeurs SBSAR **Vector3** *value* utilisées pour mettre à jour le paramètre |
| public **vector3** *GetInputVector3*(**string** inputName) | Obtenir Une Entrée De Substance **Vectorielle3** | **Chaîne** *inputName* Nom de l&#39;entrée dans le SBSAR |
| **void** *SetInputVector4*(**string** inputName, **Vector4** value) public | Mettre À Jour L&#39;Entrée **Vecteur4** De La Substance | **String** *inputName* Nom de l&#39;entrée dans les valeurs **Vector4** *value* SBSAR utilisées pour mettre à jour le paramètre |
| **vector4** *GetInputVector4*(**string** inputName) public | Obtenir Une Entrée De Substance **Vectorielle4** | **String** inputName Nom de l&#39;entrée dans le SBSAR |
| **void** *SetInputColor*(**string** inputName, **Color** value) public | Mettre à jour l&#39;entrée de Substance **couleur** | **String** inputName Nom de l&#39;entrée dans la valeur SBSAR **Color** utilisée pour mettre à jour le paramètre |
| **color** *GetInputColor*(**string** inputName, **int** dataType) public | Obtenir la Substance **couleur** | **String** *inputName* Nom de l&#39;entrée dans le SBSAR **Int** *dataType* |
| **void** *SetInputBool*(**string** inputName, **bool** value) public | Mettre à jour l&#39;entrée de Substance **booléenne** | **String** *inputName* Nom de l&#39;entrée dans la valeur SBSAR **Bool** *value* utilisée pour mettre à jour le paramètre |
| **bool** *GetInputBool*(**string** inputName) public | Obtenir La Substance **Booléenne** | **Chaîne** *inputName* Nom de l&#39;entrée dans le SBSAR |
| **void** *SetInputInt*(**string** inputName, **int** value) public | Mettre À Jour L&#39;Entrée **Int** De La Substance | **String** *inputName* Nom de l&#39;entrée dans la valeur SBSAR **Int** *value* utilisée pour mettre à jour le paramètre |
| **int** *GetInputInt*(**string** inputName) public | Obtenir Une Entrée De Substance **Int** | **Chaîne** *inputName* Nom de l&#39;entrée dans le SBSAR |
| **void** *SetInputVector2Int*(**string** inputName public, **int** x, **int** y) | Entrée De Mise À Jour De La Substance **Vector2Int** | **String** *inputName* Nom de l&#39;entrée dans la valeur SBSAR **Int** *x* utilisée pour mettre à jour le paramètre **Int** y Valeur utilisée pour mettre à jour le paramètre |
| **int[] Substance.Game.SubstanceGraph**.*GetInputVector2Int*( string inputName) | Obtenir un tableau de 2 int (valeurs x et y de Vector2Int) | **String** *inputName* Nom de l&#39;entrée dans la valeur SBSAR **Int** *x* utilisée pour mettre à jour le paramètre **Int** y Valeur utilisée pour mettre à jour le paramètre |
| **void Substance.Game.SubstanceGraph**.*SetInputVector3Int*( string inputName, int x, int y, int z) | Mettre à jour l’entrée Substance Vector3Int | **Chaîne** *inputName* Nom de l&#39;entrée dans la valeur SBSAR **Int** *x* utilisée pour mettre à jour le paramètre **Int** y Valeur utilisée pour mettre à jour le paramètre **Int** z Valeur utilisée pour mettre à jour le paramètre |
| **int[] Substance.Game.SubstanceGraph**.*GetInputVector3Int*( string inputName) | Obtenir un tableau de 3 int (valeurs x, y et z de Vector3Int) | **Chaîne** *inputName* Nom de l&#39;entrée dans la valeur SBSAR **Int** *x* utilisée pour mettre à jour le paramètre **Int** y Valeur utilisée pour mettre à jour le paramètre **Int** z Valeur utilisée pour mettre à jour le paramètre |
| **void Substance.Game.SubstanceGraph**.*SetInputVector4Int*( string inputName, int x, int y, int z, int w) | Mettre à jour l’entrée Substance Vector4Int | **Chaîne** *inputName* Nom de l&#39;entrée dans le SBSAR **Int** *x* Valeur utilisée pour mettre à jour le paramètre **Int** y Valeur utilisée pour mettre à jour le paramètre **Int** z Valeur utilisée pour mettre à jour le paramètre **Int** w Valeur utilisée pour mettre à jour le paramètre |
| **int[] Substance.Game.SubstanceGraph**.*GetInputVector4Int*( string inputName) | Obtenir un tableau de 4 int (valeurs x, y, z et w de Vector4Int) | **Chaîne** *inputName* Nom de l&#39;entrée dans le SBSAR **Int** *x* Valeur utilisée pour mettre à jour le paramètre **Int** y Valeur utilisée pour mettre à jour le paramètre **Int** z Valeur utilisée pour mettre à jour le paramètre **Int** w Valeur utilisée pour mettre à jour le paramètre |
| **void Substance.Game.SubstanceGraph**.*SetInputString*( string inputName, string value) | Mettre à jour la chaîne de Substance Entrée | **String** *inputName* Nom de l&#39;entrée dans la **String** *value* SBSAR utilisée pour mettre à jour le paramètre |
| **string Substance.Game.SubstanceGraph**.*GetInputString*( string inputName) | Obtenir la saisie de la chaîne de Substance | **Chaîne** *inputName* Nom de l&#39;entrée dans le SBSAR |
| **void Substance.Game.SubstanceGraph**.*SetInputTexture*( string inputName, Texture2D value) | Mettre à jour l&#39;entrée Substance Texture2D | **String** *inputName* Nom de l&#39;entrée dans la **Texture2D** *valeur* SBSAR utilisée pour mettre à jour le paramètre |
| **Texture2D Substance.Game.SubstanceGraph**.*GetInputTexture*( string inputName) | Obtenir une entrée Substance Texture2D | **Chaîne** *inputName* Nom de l&#39;entrée dans le SBSAR |
| **VectorInt Substance.Game.SubstanceGraph**.*GetTexturesResolution*() | Obtenez la résolution des textures Paramètres de cible du graphique (x = largeur, y = height, les valeurs peuvent être 32, 64, 128, 256, 512, 1024, 2048 et 4096) | None |
| **int Substance.Game.SubstanceGraph**.*SetTexturesResolution*( taille de Vector2Int) | Définissez la résolution des textures des paramètres de cible du graphique (x = largeur, y = height, les valeurs peuvent être 32, 64, 128, 256, 512, 1024, 2048 et 4096). Renvoie 0 en cas de réussite, sinon : -1. | **Vector2Int** *size* utilisé pour mettre à jour le paramètre**.** |
| **List Substance.Game.SubstanceGraph**.*GetGeneratedTextures*() | Renvoie tous les objets Substance Texture2D utilisés par l’ombrage de matière du graphe. | None |
| **int Substance.Game.SubstanceGraph**.*Bake*( Texture2D texture, string absoluPath) | Générez des fichiers .png pour tous les objets Texture2D de Substance utilisés par l’ombrage de matériau du graphique. | None |
| **** Substance.Game.** SubstanceGraph**.*Dupliquer*() | Duplication d’un Graphe Substance | None |
| **Substance.Game.SubstanceGraph**.*Dupliquer*(chaîne newGraphName) | Dupliquez un Graphe Substance et donnez-lui un nom (le matériau correspondant aura également le même nom) | **String newGraphName** |
| **** Substance.Game.** SubstanceGraph**.*GetInputProperties*() | Interrogation des informations d’entrée procédurale, renvoie un tableau de « InputProperties », avec :public struct InputProperties { nom de chaîne publique ; // libellé de chaîne publique inputName ; // libellé du widget dans le groupe de chaînes publiques de l’interface utilisateur ; // groupe du widget dans la chaîne publique de l’interface utilisateur[] componentLabels ; // pour les curseurs (jusqu’à 4 libellés) de chaîne publique[] enumOptions ; // pour optionMenupublic InputPropertiesType ; public Vector4 maximum ; // pour les curseurs public Vector4 minimum ; // pour les curseurs public float step ; // pour les curseurs public InputPropertiesType Booléenne = 0,// 0 Float, // 1 Vector2, // 2 Vector3, // 3 Vector4, // 4 Color, // 5 Enum, // 6 Texture, // 7 String, // 8 Invalid = -1// -1 }; | None |
| **bool** **Substance.Game.SubstanceGraph**.*HasInput*(**string** inputName) | Vérifiez si une entrée existe dans un graphique, puis renvoyez la valeur true/false : | **Chaîne** *inputName* Nom de l&#39;entrée dans le SBSAR |
| **bool** **Substance.Game.SubstanceGraph**.*IsInputVisible*(**string** inputName) | Vérifier si une entrée visible est visible, renvoie true/false | **Chaîne** *inputName* Nom de l&#39;entrée dans le SBSAR |

## Rendu

| Méthode publique | Description | Paramètre |
| --- | --- | --- |
| public **void** *QueueForRender*() | Ajouter un graphique en Substance à la file d’attente | None |
| ***mySubstance.**RenderAsync()* | Rendu asynchrone de tous les graphiques de Substance en file d’attente | None |
| ***mySubstance.**RenderSync()* | Rendu synchrone de tous les graphiques de Substance en file d’attente | None |

## Scripts en mode éditeur :

Pour rendre permanentes les modifications apportées au graphique en mode Éditeur, une réimportation de chaque Substance correspondante doit être effectuée. Cela se fait avec la fonction suivante :

```
static void ReImportSubstance(Substance.Game.Substance pSubstance)

{



// Re-import Substance object:

SubstanceImporter importer = AssetImporter.GetAtPath(pSubstance.assetPath) as SubstanceImporter;

importer.CommitSubstanceToImporter(pSubstance); // plugin function

EditorUtility.SetDirty(importer);

importer.SaveAndReimport();



}
```


(avec « CommitSubstanceToImporter », une fonction de module externe de Substance de données : copiez tous les paramètres graphiques et/ou entrées modifiés vers l’objet importateur de Substances de données, qui est ensuite sérialisé sur le disque via le mécanisme d’importateur d’Unity)
