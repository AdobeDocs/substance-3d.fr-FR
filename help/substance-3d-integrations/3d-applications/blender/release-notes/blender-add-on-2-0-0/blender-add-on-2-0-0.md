---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/3d-applications/blender/release-notes/blender-add-on-2-0-0.html"
breadcrumb-title: ''
description: Consultez les notes de mise à jour du module complémentaire Blender version 2.0.0 pour en savoir plus sur les nouvelles fonctionnalités, les améliorations et les correctifs de bogues.
helpx_creative_field: ""
helpx_description: Substance 3D Integrations
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Module complémentaire 2.0.0
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 0%

---


# Module complémentaire 2.0.0

Substance 3D Addon 2.0 est une mise à jour transformative pour les utilisateurs de Blender, avec une architecture de plug-in entièrement refactorisée. Cette refonte se concentre sur une intégration transparente, des performances améliorées et une base flexible pour les futures extensions. Il ne s’agit pas seulement d’une mise à niveau, mais d’une refonte de la façon dont les matériaux de Substance sont manipulés dans Blender, pour répondre aux besoins en constante évolution des professionnels de la 3D.

<b>Principaux aspects de la version 2.0:</b>

* Architecture refactorisée - structure de plug-in améliorée pour des performances et une intégration accrues
* Prise en charge de l’extension future : la mise à jour jette les bases pour l’ajout facile de nouvelles fonctionnalités à l’avenir
* Compatibilité plus large : entièrement compatible avec les versions 3.0 et ultérieures de Blender, y compris la prise en charge des utilisateurs de Mac

<b>Ajouté/Mis À Jour :</b>

* [SRE] Prise en charge de la sélection de Substances Engine (GPU par défaut)
* [SRE] Nouveaux formats d’image pour exporter les textures
* [SRE] Sélection du Nombre de bits par pixel pour chaque type de mappage
* [BLD] Prise en charge des sorties de valeur
* [BLD] Prise en charge des entrées de chaîne
* [SRE] Ajout de l’option permettant de sélectionner le dossier temporaire par défaut pour la destination d’exportation de l’image

<b>Fixe :</b>

* [SRE] Amélioration globale des performances
* [BLD] Correction des problèmes de communication entre les outils d&#39;intégration et Blender
* [BLD] Échec de l&#39;installation/du démarrage des outils d&#39;intégration
* [BLD] Les outils d&#39;intégration ne se terminent pas lorsque vous fermez Blender
* [BLD] Matière non mise à jour lors de la modification du type de fichier d&#39;un mappage
* [SRE] Toutes les cartes des matériaux sont exportées en permanence
* [SRE] Les outils d’intégration exportent des cartes de normales avec des marches d’escalier
* [SRE] Le chargement de la Substance ne se termine jamais
* [SRE] Les unités de Taille physique ne sont pas ajustées à la scène
* [BLD] Les paramètres prédéfinis générés dans Blender ne fonctionnent pas avec d’autres intégrations
* [BLD] La matière ne se met pas à jour dans Cycles
* [BLD] Les limites souples et dures des entrées sont ignorées
* [BLD] L&#39;intensité des couleurs ne se met pas à jour correctement lors du réglage d&#39;un paramètre
* [SRE] Échec de la désinstallation des outils d’intégration
* [SRE] Nous avons résolu le problème de duplication de plusieurs matériaux qui entraînait une erreur.
* [SRE] L’espace colorimétrique des nœuds d’image correspond désormais correctement aux préférences de l’utilisateur.

<b>Problèmes connus :</b>

* Lors de l’utilisation de Blender v4.0+, les sockets ne sont pas dans l’ordre après avoir été activés et désactivés plusieurs fois
* Appuyez sur Ctrl+Z pour annuler les modifications et risquez de provoquer des erreurs
* Le chargement d’un fichier vide ou d’un dossier au lieu d’un fichier .sbsar peut interrompre le plug-in
* Prise en charge du mode sans tête du mélangeur
