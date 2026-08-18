---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-integrations/game-engines/unity/unity-release-notes/unity-2-3-4.html"
breadcrumb-title: ''
description: Consultez les notes de mise à jour du plug-in Unity version 2.3.4 pour en savoir plus sur les nouvelles fonctionnalités, les améliorations et les correctifs de bogues.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unity > Unity Release Notes > Unity 2.3.4
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Unité 2.3.4
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 0%

---


# Unité 2.3.4

>[!WARNING]
>
> **L’utilisation du plug-in avec Unity 2019.2 générera l’erreur suivante :**
> 
> InspectorSubstanceImporter.OnInspectorGUI doit appeler ApplyRevertGUI pour éviter tout comportement inattendu.\
> UnityEditor.Experimental.AssetImporters.AssetImporterEditor:OnDisable()\
> Substance.Editor.InspectorSubstanceImporter:OnDisable()
> 
> Cette erreur peut être supprimée et n’affectera pas les fonctionnalités du plug-in

>[!WARNING]
>
> **Veuillez lire : rupture des matériaux de Substance :**\
> Les matériaux de Substance qui contiennent une sortie personnalisée avec une utilisation vide seront interrompus lors de l’importation. En outre, les matériaux de Substance contenant des utilisations en double seront cassés.\
> Les fichiers sbsar plus anciens de GameTextures.com ne sont actuellement pas compatibles avec le plug-in Substance in Unity. Ces matériaux qui contiennent des sorties Utilisation non prises en charge sont cassés. Avant d’utiliser le plug-in, assurez-vous d’effectuer une sauvegarde de votre projet.

## Nouvelles fonctionnalités :

* Ajout de la prise en charge de Substance Engine v7
* Prise en charge de Linux ajoutée

### Correctifs de bogues :

* Problèmes résolus liés à l’importation d’une Substance sans textures
* Correction d’un problème en raison duquel le processus de réflexion ne fonctionnait pas correctement dans Unity 2019.x
* Correction des problèmes de manipulation des préfabrications lors de l’importation d’un pack contenant des préfabrications avec des matériaux de Substance
* Affectations de matière/texture fixes non reportées après le processus de réflexion
* Correction d’un problème lié à la modification des ombrages provoquant la rupture des matériaux
* Correction d’un problème en raison duquel la rugosité n’était pas tassée dans la couche alpha métallique
* Correction d’un problème en raison duquel, lorsque le plug-in de Substance était installé, la modification des paramètres d’importation pour les textures non Substance annulait certaines options.
* Correction d’un problème en raison duquel la Substance Source ne s’ouvrait pas sur Mac.

## Problèmes connus :

**Module externe Core Substance**

* L’utilisateur doit désactiver « Activer le code en bits » dans le menu Paramètres de génération de Xcode pour générer pour iOS.
* Les Substances ne fonctionnent pas avec les offres groupées de ressources
* Les icônes d’aperçu de Substance dans l’Explorateur d’actifs deviennent toutes l’icône Substance S après une réimportation
* Les matériaux de Substance personnalisés dont la sortie avec l’utilisation est définie sur vide cassent le matériau
* Les matériaux de Substance personnalisés qui ont des utilisations en double cassent le matériau
* L’éditeur doit être redémarré après l’importation du plug-in sur Linux

**Scripts**

* Les scripts ne fonctionnent pas à l’exécution si le projet est défini sur x86 dans les paramètres de génération
* Problèmes d’utilisation du back-end de script il2cpp avec certaines plateformes de build

**Substance Painter Live Link**

* La création d’un projet après avoir peint avec Substance Live Link rétablit le maillage peint à un matériau par défaut
* Canal AO non envoyé avec Painter Live Link
* Les maillages avec plusieurs matières ne fonctionnent pas dans Unity Live Link
* La façon dont Unity LiveLink utilise SimpleJson entre en conflit avec d’autres instances de SimpleJson dans un projet
