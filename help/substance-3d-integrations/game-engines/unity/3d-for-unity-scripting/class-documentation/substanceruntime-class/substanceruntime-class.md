---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-integrations/game-engines/unity/substance-3d-for-unity-scripting/class-documentation/substanceruntime-class.html"
breadcrumb-title: ''
description: Documentation de référence pour la classe SubstanceRuntime utilisée pour les opérations matérielles de Substance d’exécution dans Unity.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unity > Substance 3D for Unity Scripting > Class Documentation > SubstanceRuntime Class
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: SubstanceRuntime, classe
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 1%

---


# SubstanceRuntime, classe

## Référence de classe Adobe.Substance.Runtime.SubstanceRuntime

Classe Singleton qui gère l&#39;initialisation du moteur de Substance de données et qui est utilisée pour obtenir des gestionnaires natifs vers des instances substance.\
Diagramme d&#39;héritage pour Adobe.Substance.Runtime.SubstanceRuntime :

![](../../../../../assets/image2022-6-22-14-35-28.png)

### Fonctions de membre public

```
• SubstanceNativeGraph InitializeInstance (SubstanceGraphSO substanceInstance)
```


Crée un handle de SDK de Substance pour un SubstanceGraphSO donné.

### Propriétés

```
• static SubstanceRuntime Instance [get]
```


Instance singleton.

### Description détaillée

Classe Singleton qui gère l&#39;initialisation du moteur de Substance de données et qui est utilisée pour obtenir des gestionnaires natifs vers des instances substance.

### Documentation sur les fonctions de membre

#### InitializeInstance()

```
SubstanceNativeGraph Adobe.Substance.Runtime.SubstanceRuntime.InitializeInstance  

( SubstanceGraphSO substanceInstance ) [inline]
```


Crée un handle de SDK de Substance pour un SubstanceGraphSO donné.

**Paramètres**

|  |  |
| --- | --- |
| substanceInstance | Target SubstanceGraphSO |


**Retours**

Handle qui communique avec le SDK Substance

### Documentation de la propriété

#### Instance

```
SubstanceRuntime Adobe.Substance.Runtime.SubstanceRuntime.Instance [static], [get]
```


Instance singleton.

Instance singleton globale.

>[!NOTE]
>
> NativeGraph.InRenderWork est uniquement destiné à un usage interne pour communiquer avec la Substance Engine de données et ne doit pas être utilisé pour des workflows personnalisés.
