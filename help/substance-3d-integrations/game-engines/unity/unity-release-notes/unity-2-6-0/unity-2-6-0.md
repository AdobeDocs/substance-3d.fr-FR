---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unity/unity-release-notes/unity-2-6-0.html"
breadcrumb-title: ''
description: Consultez les notes de mise à jour du plug-in Unity version 2.6.0 pour en savoir plus sur les nouvelles fonctionnalités, les améliorations et les correctifs de bogues.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unity > Unity Release Notes > Unity 2.6.0
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Unity 2.6.0
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 0%

---


# Unity 2.6.0

Publié le 7 juin 2021

Mis à jour/ajouté :

* Nouveau workflow pour l’accès à la Substance Source ! L’action de Substance Source accède désormais à l’onglet Source dans le lanceur de Substances, ce qui permet d’envoyer les actifs directement à Unity
* Les informations de version du plug-in peuvent être copiées dans le presse-papiers
* Suppression de « Générer à la charge » des paramètres de la cible

Correctifs :

* Dans les projets HDRP, le mode Displacement revient à la valeur par défaut (facettisation) lorsqu’une modification est apportée au paramètre matériau
* La taille de la résolution ne s’affiche pas dans la fenêtre Inspecteur
* Impossible d’installer le plug-in vers Unity versions 2020.2 et ultérieures

Problèmes connus :

* L’erreur Accès refusé et/ou le crash se produit lors de la mise à jour du plug-in à partir des versions antérieures 2.5.4 et antérieures
  * Solution : les versions 2.5.4 et antérieures du plug-in doivent être désinstallées des versions 2020.2 et ultérieures du projet Unity avant d’installer la version 2.6.0 du plug-in
* Les aperçus de texture pour les fichiers image ne s’afficheront pas dans l’inspecteur lorsque le plug-in Substance est installé
  * La source de ce problème existe au sein d’Unity et il est prévu qu’Unity y remédie dans leurs versions 2021.2 (actuellement en version bêta)
