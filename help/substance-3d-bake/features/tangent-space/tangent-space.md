---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/features/tangent-space.html"
breadcrumb-title: ''
description: Découvrez comment Substance Baker gère les calculs d’espace tangent et personnalise l’algorithme pour votre workflow.
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

Substance Bakers peut charger les Tangentes et les Binormales présentes sur le maillage en bas-poly ou les recalculer. Lors de leur recalcul, il est possible de définir un algorithme d&#39;espace tangent personnalisé (par défaut, il s&#39;agit de MikkTSpace).

## Liste des plug-ins d’espace tangent

## Substance Painter

En Substance Painter, le plug-in Tangent Space ne peut pas être modifié, il sera toujours **MikkTSpace**. Cependant, il existe un paramètre pour modifier légèrement son comportement afin de le rendre compatible avec d&#39;autres applications :

| *Paramètre* | *Compatible* *Application* |
| --- | --- |
| **Calculer l&#39;espace tangent par fragment : désactivé** | Compatible avec xNormal, Unity 5.3 ou version plus récente. |
| **Calculer l&#39;espace tangent par fragment : activé** | Compatible avec Unreal Engine 4, Blender et Unity HDRP workflow. |

## Substance Designer

Substance Designer prend en charge l’algorithme suivant :

| *Nom de fichier* | *Description* |
| --- | --- |
| **mikktspace.dll** | MikkTSpace, algorithme Tangent Space basé sur les travaux de Morten S. Mikkelsen.Compatible avec xNormal, Unity 5.3 ou version plus récente. |
| **mikkunrealtspace.dll** | MikkTSpace, algorithme Tangent Space basé sur les travaux de Morten S. Mikkelsen.Compatible avec Unreal Engine 4, Blender et Unity HDRP workflow. |
| **unitytspace.dll** | Algorithme de l&#39;espace tangent basé sur Unity 4. |

>[!NOTE]
>
> Il est possible d’écrire un plug-in Tangent Space personnalisé. Un fichier d&#39;en-tête nommé **tangentspaceplugin.h** est disponible dans le dossier d&#39;installation sous **Substance Designer/SDK/tangentspace** et peut être utilisé comme interface.

## Définition d’un espace tangent personnalisé

## Substance Painter

Substance Painter ne prend pas en charge les plug-ins Tangent Space personnalisés pour le moment. Cela signifie que si les tangentes et les binormales ne sont pas présentes sur le maillage low-poly (utilisé pour créer le projet), elles seront recalculées en fonction de l&#39;algorithme MikkTSpace.

## Substance Designer

Pour définir l’algorithme d’espace tangent en Substance Designer, procédez comme suit :

1. Sélectionnez **Modifier** > **Préférences**.

   ![](../../assets/sd-edit-pref.png)
1. Cliquez sur **Projets**.

   ![](../../assets/sd-pref-projects.png)
1. Accédez à l&#39;onglet **Général**. Faites défiler jusqu&#39;à ce que la section **Scènes 3D** soit visible.

   ![](../../assets/sd-tab-general.png)
1. Cliquez sur les **trois points** (...) pour charger un plug-in personnalisé.

## Substance Automation Toolkit

Lorsque vous utilisez Automation Toolkit, il est possible de spécifier le plug-in Tangent Space avec un argument de ligne de commande spécifique :

```
sbsbaker normal-from-mesh --tangent-space-plugin "C:/Substance Designer/plugins⁄tangentspace⁄mikktspace.dll" ...
```
