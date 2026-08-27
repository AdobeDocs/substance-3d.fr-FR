---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/3d-applications/blender/release-notes/add-on-0-9-3/add-on-2-0-0-plus.html"
breadcrumb-title: ''
description: Consultez les notes de mise à jour pour le module complémentaire Blender version 2.0.0 et ultérieure pour en savoir plus sur les nouvelles fonctionnalités et améliorations.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > Blender > Release Notes > Add-on 2.0.0
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Module complémentaire 2.0.0
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '738'
ht-degree: 0%

---


# Module complémentaire 2.0.0+

## Module complémentaire 2.2

<b>Ajouté :</b>

* Prise en charge du moteur de rendu Octane
* Prise en charge initiale de Redshift
* Prise en charge initiale de Renderman

<b>Mise à jour :</b>

* Mise à niveau vers la dernière version de Connecteur
* Ajout d’une fonctionnalité permettant de recevoir des paramètres prédéfinis à l’aide du Connecteur
* Amélioration de la fonctionnalité de préconfiguration d’importation : désormais, toutes les instances d’un SBSAR qui incluent le matériau ajouteront la préconfiguration
* Fonctionnalité de Connecteur standardisée

<b>Fixe :</b>

* Bogue de persistance dans lequel l’image d&#39;entrée ne fonctionnait pas après l’enregistrement du fichier de fusion
* Problème de réseau shader ne fonctionnant pas lors de la mise à jour du paramètre prédéfini shader
* URL incorrecte dans le bouton de téléchargement du plug-in
* Répétition inversée en octane
* Valeurs d’entrée non fonctionnelles avec des systèmes de rendu tiers
* Problème en raison duquel le paramètre de valeur d’entrée flottante n’a pas été créé
* Les espaces colorimétriques du moteur de rendu ne fonctionnent pas correctement
* paramètres prédéfinis shader non filtrage par le moteur de rendu disponible

## Module complémentaire 2.1.1

Cette mise à jour inclut la prise en charge de Blender 4.0+ et plusieurs nouvelles fonctionnalités dans les préférences du module complémentaire. Nous avons également ajouté la prise en charge de Substance Connector pour le transfert transparent de données entre Substance 3D Sampler et Blender (Envoyer à) et avons résolu certains bugs. Retrouvez les notes de mise à jour détaillées ci-dessous.

<b>Ajouté/Mis À Jour :</b>

* Ajout de la fonctionnalité Substance Connector (prend en charge les fichiers SBSAR et USD).
* Prise en charge de Blender 4.0+.
* Prise en charge de SRE version 2.1.0.
* Dans les préférences du module complémentaire :
  * Possibilité de choisir le chemin d’installation des outils d’intégration de Substance.
  * Bouton permettant de réinitialiser les outils d’intégration au chemin par défaut.
  * Bouton pour ouvrir le dossier Outils d’intégration.
  * Ajout Appliquer le type pour attribuer une matière (Insérer : définissez-le comme matière principale, Ajouter : ajoutez-le au bas de la liste).
  * Ajout d’une case à cocher pour sélectionner le comportement par défaut des groupes d’entrée (réduits/développés).
  * Ajout d’une case à cocher pour sélectionner le comportement par défaut de la seule propriété de mise à jour des textures.
  * Démarrez automatiquement le Substance Remote Engine lors de l’ouverture de Blender (il est important de l’activer si vous utilisez Connector).
* Dans le module complémentaire :
  * Ajout de textures de mise à jour uniquement (permet de modifier les paramètres sans refaire le graphique des nœuds).
  * Ajout des boutons Développer tous les groupes et Réduire tous les groupes.
  * Ajout d’un groupe Image d’entrée pour regrouper toutes les images d’entrée si nécessaire dans un SBSAR.
  * Les entrées de paramètres sont désormais affichées dans le même ordre que Designer.
  * Ajout d’une prévisualisation sous forme de vignettes pour chaque matériau de Substance.

<b>Fixe :</b>

* Correction d’un bogue de groupe d’entrée Général vide.

<b>Problèmes Connus :</b>

* La fonctionnalité permettant de sélectionner automatiquement SBSAR lors de la sélection d’un objet ne fonctionne pas pour le moment. Elle est donc désactivée.

## Module complémentaire 2.0.0

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
