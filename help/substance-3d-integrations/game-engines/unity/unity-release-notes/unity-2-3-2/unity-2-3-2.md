---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-integrations/game-engines/unity/unity-release-notes/unity-2-3-2.html"
breadcrumb-title: ''
description: Consultez les notes de mise à jour du plug-in Unity version 2.3.2 pour en savoir plus sur les nouvelles fonctionnalités, les améliorations et les correctifs de bogues.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unity > Unity Release Notes > Unity 2.3.2
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Unité 2.3.2
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 0%

---


# Unité 2.3.2

## Nouvelles fonctionnalités :

* Sérialisation des matériaux
* Reflet : Le plug-in permet désormais d’importer d’anciens fichiers de Substance de données dans des packages (automatiquement mis à jour vers de nouvelles données de Substance de données lors de l’importation)
* Les propriétés des matériaux sont reportées sur l&#39;importation des emballages contenant des données de Substance
  * Remarque : cela s’applique uniquement aux packs créés à l’aide de la mise à jour 2.3.0 ou ultérieure
* Ajout du bouton Cuire la texture au menu du graphique de Substance

### Correctifs de bogues :

* Correction d’un problème en raison duquel la mosaïque de matériaux de Substance était réinitialisée si le dossier Bibliothèque était supprimé.
* Amélioration de la vitesse à la sortie du mode Lecture
* Correction d’un crash lors de la mise à jour du plug-in lorsque la DLL de Substance était utilisée
* Le dossier Allegorithmic ne peut plus être supprimé dans Unity.
  * Remarque : le contenu du dossier Allegorithmic ne peut pas être modifié. Sa suppression dans Unity peut provoquer plusieurs problèmes, entraînant la réapparition magique du dossier Allegorithmic lorsque Unity est fermé et rouvert. Un avertissement indique maintenant à l’utilisateur de le supprimer avec Unity fermé manuellement à partir du dossier Actifs du projet
* Amélioration de la vitesse à la sortie du mode Lecture
* Correction d’un bug qui réinitialisait les propriétés du matériau de la Substance lorsque le dossier Bibliothèque était supprimé

## Problèmes connus :

**Module externe Core Substance**

* L’utilisateur doit désactiver « Activer le code en bits » dans le menu Paramètres de génération de Xcode pour générer pour iOS.
* Les Substances ne fonctionnent pas avec les offres groupées de ressources
* Les icônes d’aperçu de Substance dans l’Explorateur d’actifs deviennent toutes l’icône Substance S après une réimportation

**Scripts**

* Les scripts ne fonctionnent pas à l’exécution si le projet est défini sur x86 dans les paramètres de génération
* Problèmes d’utilisation du back-end de script il2cpp avec certaines plateformes de build

**Substance Painter Live Link**

* La création d’un projet après avoir peint avec Substance Live Link rétablit le maillage peint à un matériau par défaut
* Canal AO non envoyé avec Painter Live Link
* Les maillages avec plusieurs matières ne fonctionnent pas dans Unity Live Link
* La façon dont Unity LiveLink utilise SimpleJson entre en conflit avec d’autres instances de SimpleJson dans un projet
