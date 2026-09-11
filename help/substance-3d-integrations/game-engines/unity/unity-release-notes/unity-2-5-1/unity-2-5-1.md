---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-integrations/game-engines/unity/unity-release-notes/unity-2-5-1.html"
breadcrumb-title: ''
description: Consultez les notes de mise à jour du plug-in Unity version 2.5.1 pour en savoir plus sur les nouvelles fonctionnalités, les améliorations et les correctifs de bogues.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unity > Unity Release Notes > Unity 2.5.1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Unity 2.5.1
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 0%

---


# Unity 2.5.1

Publié le 21 mai 2020

Ajouté

* Prise en charge du pipeline de rendu universel : les textures de Substance utiliseront automatiquement des nuanceurs et des matériaux URP

Fixe

* Paramètre de résolution maximale du Moteur CPU de la Substance :
  * Mise à jour du nom du champ dans le menu Paramètres de Substance de « Verrouille de Texture \*\* » vers « Résolution maximale du Moteur CPU de la Substance »
  * Une notification d’avertissement s’affiche indiquant que tous les matériaux Substance seront réimportés lorsque le paramètre est modifié
* Suppression du message de débogage superflu qui s&#39;affichait lors de l&#39;installation (« TextureClamp = 4096 Unity.Moteur.Debug:Log(Object) »)
* Projet HDRP : les propriétés de Matériau qui se trouvent à la fois dans les matériaux standard et HDRP seront reportées lorsque des packages comprenant des Substances seront importés
* Les masques de réflexion et HDRP se créent et fonctionnent comme prévu lors de l’importation d’un matériau de Substance d’un package de Substance qui se trouvait dans la version précédente d’Unity
* Le matériau de Substance dupliqué aura la couleur prévue et ne sera plus jaune lors de l’utilisation de la fonction dupliquée
* La source de Substance se charge comme prévu après la fermeture et la réouverture d’Unity
* Crashs lors de l’importation d’un package dans un projet HDRP (par intermittence)
* Le curseur fonctionne comme prévu pour les matériaux de Substance avec un paramètre exposé dont l’éditeur est défini sur Couleur (niveaux de gris)
* Par crash lorsque vous cliquez sur « Rétablir la préconfiguration par défaut » avec des graphes de Substance qui n’ont pas de résolution par défaut
* Crash lors de la modification de la taille de sortie d’un matériau de Substance lorsque le paramètre de taille de sortie n’est pas exposé
* La création de contenu pour iOS n’échouera pas
* Les scripts utilisant des matériaux de Substance s’exécutent lors de la création pour Windows Standalone
