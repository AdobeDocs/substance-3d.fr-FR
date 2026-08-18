---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-integrations/3d-applications/3ds-max/3ds-max-plugin-release-notes/3ds-max-3-0-0-plus.html"
breadcrumb-title: ''
description: Consultez les notes de mise à jour du module externe 3ds Max version 3.0.0 et ultérieure pour en savoir plus sur les nouvelles fonctionnalités, les améliorations et les correctifs de bogues.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > 3ds Max > 3ds Max Plugin Release Notes > 3ds Max 3.0.0
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3Ds Max 3.0.0
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 0%

---


# 3ds Max 3.0.0+

## 3ds Max 3.0.4

<b>Ajouté/Mis À Jour :</b>

* Mise à jour des icônes du plug-in de Substance avec les dernières icônes.
* Ajout de la prise en charge de l’envoi et de la réception de paramètres prédéfinis via Connecteur dans le plug-in.
* Gestionnaire de menus intégré à partir du paramètre de notification pour remplacer l’utilisation de l’interface principale.

<b>Fixe :</b>

* Résolution d’un problème en raison duquel les matériaux Substance 2 pouvaient ne pas parvenir à s’afficher dans IR/Production avec Corona lorsque l’éditeur de matériaux Slate est ouvert et que la texture plaquée Substance 2 est sélectionnée.
* Résolution d’un problème en raison duquel les mises à jour du connecteur Sampler créaient de nouveaux nœuds Substance 2 au lieu de mettre à jour les nœuds existants.
* Résolution d’un problème de blocage dans le plug-in 3ds Max lors de l’ajout d’un nœud Substance 2. Cela a permis de s’assurer que l’utilisation de l’importation par lots pour charger des fichiers .sbsar n’ouvrait plus l’éditeur de script.
* Résolution du problème de chargement du plug-in 3DSMax 2025 en raison d’un fichier .dll incompatible lors de l’utilisation du programme d’installation .msi.

## 3ds Max 3.0.2

<b>Ajouté/Mis À Jour :</b>

* Gestion standardisée des icônes dans le plug-in Substance en incorporant toutes les icônes existantes dans les fichiers qrc et rcc, en s&#39;alignant sur les méthodes préférées d&#39;Autodesk et en assurant un chargement cohérent dans le panneau de graphiques SBSAR.
* Amélioration de la réactivité de la fenêtre Paramètres de Substance dans le plug-in pour s’assurer que les champs de saisie et leurs descriptions s’affichent correctement lors du réglage de la taille de la fenêtre.
* Le plug-in Substance est désormais compatible avec Corona 11.

<b>Fixe :</b>

* Correction d’un problème en raison duquel la rugosité de la Couleur de l&#39;éclat et du reflet ne se connectaient pas automatiquement aux matériaux V-Ray. Désormais, les deux propriétés seront automatiquement liées lors de la création d’un workflow dans V-Ray et Arnold.
* Correction d’un problème d’interface utilisateur dans le plug-in en raison duquel le réglage du paramètre Limite des cœurs du processeur affichait de manière incorrecte les valeurs à deux chiffres si la valeur enregistrée était un seul chiffre.
* Correction d’une erreur de rendu dans la console pour le plug-in 3ds Max v3.0.0 liée à la fonction de compatibilité des Substances. Désormais, les nœuds Substance créés à l’aide du menu Importation par lot de Substances s’affichent comme prévu.
