---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-bake/features/tangent-space.html"
breadcrumb-title: ''
description: Découvrez comment Substance Bakers gère les calculs d’espace de tangente et personnalise l’algorithme pour votre workflow.
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

Substance Bakers peut charger les Tangentes et les Binormals présents sur le maillage à faible niveau de poly ou les recalculer. Lors de leur recalcul, il est possible de définir un algorithme de Repère tangent personnalisé (par défaut, c&#39;est MikkTSpace).

## Liste des plug-ins Repère tangent

## Substance Painter

Dans la Substance Painter, le Plugin de repère tangent ne peut pas être modifié, il sera toujours **MikkTSpace**. Cependant, il existe un paramètre pour modifier légèrement son comportement afin de le rendre compatible avec d&#39;autres applications :

| *Paramètre* | *Compatible* *Application* |
| --- | --- |
| **Espace de tangente de calcul par fragment : désactivé** | Compatible avec xNormal, Unity 5.3 ou version plus récente. |
| **Espace de tangente de calcul par fragment : activé** | Compatible avec Unreal Moteur 4, Blender et Unity HDRP workflow. |

## Substance Designer

Substance Designer prend en charge l’algorithme suivant :

| *Nom de fichier* | *Description* |
| --- | --- |
| **mikktspace.dll** | MikkTSpace, algorithme de Repère tangent basé sur les travaux de Morten S. Mikkelsen.Compatible avec xNormal, Unity 5.3 ou version plus récente. |
| **mikkunrealtspace.dll** | MikkTSpace, algorithme de Repère tangent basé sur les travaux de Morten S. Mikkelsen.Compatible avec Unreal Moteur 4, Blender et Unity HDRP workflow. |
| **unitytspace.dll** | Algorithme de repère tangent basé sur Unity 4. |

>[!NOTE]
>
> Il est possible d&#39;écrire un Plugin de repère tangent personnalisé. Un fichier d&#39;en-tête nommé **tangentspaceplugin.h** est disponible dans le dossier d&#39;installation sous **Substance Designer/SDK/tangentspace** et peut être utilisé comme interface.

## Définition d’un Repère tangent personnalisé

## Substance Painter

Substance Painter ne prend pas en charge les plug-ins de Repère tangent personnalisés pour le moment. Cela signifie que si des Tangentes et des binormaux ne sont pas présents sur le maillage low-poly (utilisé pour la création du projet), ils seront recalculés en fonction de l&#39;algorithme MikkTSpace.

## Substance Designer

Pour définir l’algorithme d’espace de tangente dans la Substance Designer, procédez comme suit :

1. Sélectionnez **Modifier** > **Préférences**.

   ![](../../assets/sd-edit-pref.png)
1. Cliquez sur **Projets**.

   ![](../../assets/sd-pref-projects.png)
1. Accédez à l&#39;onglet **Général**. Faites défiler jusqu&#39;à ce que la section **Scènes 3D** soit visible.

   ![](../../assets/sd-tab-general.png)
1. Cliquez sur les **trois points** (...) pour charger un plug-in personnalisé.

## Substance Automation Toolkit

Lors du baking avec Automation Toolkit, il est possible de spécifier le Plugin de repère tangent avec un argument de ligne de commande spécifique :

```
sbsbaker normal-from-mesh --tangent-space-plugin "C:/Substance Designer/plugins⁄tangentspace⁄mikktspace.dll" ...
```
