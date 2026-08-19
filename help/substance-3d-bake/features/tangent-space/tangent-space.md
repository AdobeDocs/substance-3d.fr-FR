---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-bake/features/tangent-space.html"
breadcrumb-title: ''
description: Découvrez comment Substance Bakers gère les calculs d’espace tangent et personnalise l’algorithme de votre workflow.
helpx_creative_field: ""
helpx_description: bakers > Features > Tangent Space
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Repère tangent
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 2%

---


# Repère tangent

Substance Bakers peut charger les Tangentes et Binormales présentes sur le maillage low-poly ou les recalculer. Lors de leur recalcul, il est possible de définir un algorithme d&#39;espace tangent personnalisé (par défaut, il s&#39;agit de MikkTSspace).

## Liste des modules externes d&#39;espace tangent

## Substance Painter

Dans Substance Painter le plugin Tangent Space ne peut pas être changé, il sera toujours **MikkTSpace**. Cependant, il existe un paramètre pour modifier légèrement son comportement afin de le rendre compatible avec d’autres applications :

| *Paramètre* | *Compatible* *Application* |
| --- | --- |
| **Calculer l&#39;espace tangent par fragment : désactivé** | Compatible avec xNormal, Unity 5.3 ou version ultérieure. |
| **Calculer l&#39;espace tangent par fragment : Activé** | Compatible avec Unreal Engine 4, Blender et Unity HDRP. |

## Concepteur de substance

Substance Designer prend en charge l&#39;algorithme suivant :

| *Nom de fichier* | *Description* |
| --- | --- |
| **mikktspace.dll** | MikkTSpace, algorithme de Tangent Space basé sur le travail de Morten S. Mikkelsen.Compatible avec xNormal, Unity 5.3 ou version ultérieure. |
| **mikkunrealtspace.dll** | MikkTSpace, algorithme de Tangent Space basé sur le travail de Morten S. Mikkelsen.Compatible avec Unreal Engine 4, Blender et Unity HDRP. |
| **unitytspace.dll** | Algorithme de l&#39;espace tangent basé sur Unity 4. |

>[!NOTE]
>
> Il est possible d’écrire un plug-in Tangent Space personnalisé. Un fichier d’en-tête nommé **tangentspaceplugin.h** est disponible dans le dossier d’installation sous **Substance Designer/SDK/tangentspace** et peut être utilisé comme interface.

## Définition d’un espace tangent personnalisé

## Substance Painter

Substance Painter ne prend pas en charge les modules externes Tangent Space personnalisés pour le moment. Cela signifie que si les Tangentes et les Binormales ne sont pas présentes sur le maillage low-poly (utilisé pour créer le projet), elles seront recalculées en fonction de l&#39;algorithme MikkTSpace.

## Concepteur de substance

Pour définir l’algorithme de l’espace tangent dans le Concepteur de substances, procédez comme suit :

1. Choisissez **Modifier** > **Préférences**.

   ![](../../assets/sd-edit-pref.png)
1. Cliquez sur **Projets**.

   ![](../../assets/sd-pref-projects.png)
1. Accédez à l’onglet **Général**. Faites défiler l’écran jusqu’à ce que la section **Scènes 3D** soit visible.

   ![](../../assets/sd-tab-general.png)
1. Cliquez sur les **trois points** (...) pour charger un module externe personnalisé.

## Boîte à outils d&#39;automatisation des substances

Lors de la cuisson avec Automation Toolkit, il est possible de spécifier le plug-in Tangent Space avec un argument de ligne de commande spécifique :

```
sbsbaker normal-from-mesh --tangent-space-plugin "C:/Substance Designer/plugins⁄tangentspace⁄mikktspace.dll" ...
```
