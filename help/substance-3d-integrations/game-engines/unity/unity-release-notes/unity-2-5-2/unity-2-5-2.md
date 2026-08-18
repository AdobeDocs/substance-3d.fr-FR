---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unity/unity-release-notes/unity-2-5-2.html"
breadcrumb-title: ''
description: Consultez les notes de mise à jour du plug-in Unity version 2.5.2 pour en savoir plus sur les nouvelles fonctionnalités, les améliorations et les correctifs de bogues.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unity > Unity Release Notes > Unity 2.5.2
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Unity 2.5.2
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---


# Unity 2.5.2

Publié le 23 juillet 2020

Ajouté :

* Fonction « IsProcessing() » qui indique si le moteur de rendu est occupé ou inactif (non occupé)

Fixe :

* Ne plus afficher d&#39;erreur lors de la définition des paramètres 2048 clamp et 4096 target
* Les propriétés de matériau seront reportées lors de la mise à niveau vers HDRP et/ou URP à partir de Standard
* Les scripts modifiant les matériaux de Substance fonctionneront comme prévu lors du déploiement sur mobile
* La couche rouge n’est plus copiée dans l’Alpha et l’Alpha par défaut est Blanc
* Blocage lors de la modification des paramètres de la cible dans Mac
* Erreur NullReferenceException supprimée lors de la création d&#39;une matière Unity
* Erreur supprimée lors de la fermeture du mode de lecture après la modification des propriétés de mosaïque
* Activation de l’instanciation GPU
* Les matières utilisant la transparence ne disparaissent pas ou ne deviennent pas incorrectement noires lorsque le mode de lecture est existant
* Les matériaux de Substance ne seront pas détruits dans le projet HDRP lors de la mise à niveau du plug-in
