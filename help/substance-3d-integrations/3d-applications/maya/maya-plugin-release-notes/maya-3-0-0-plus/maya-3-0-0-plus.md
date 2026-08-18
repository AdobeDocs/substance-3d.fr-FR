---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/3d-applications/maya/maya-plugin-release-notes/maya-3-0-0-plus.html"
breadcrumb-title: ''
description: Consultez les notes de mise à jour pour le plug-in Maya version 3.0.0 et ultérieure pour en savoir plus sur les nouvelles fonctionnalités, les améliorations et les correctifs de bogues.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > 3ds Max > 3ds Max Plugin Release Notes > Maya 3.0.0
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Maya 3.0.0
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---


# Maya 3.0.0 ou version ultérieure

## Maya 3.0.3

<b>Ajouté/Mis À Jour :</b>

* Amélioration du système de mise en cache du plug-in Maya pour ne mettre en cache qu’une seule fois lors de la création initiale du réseau, avec la mise en cache manuelle activée.
* Une option permettant de modifier l’emplacement du dossier « substance » dans le plug-in Maya a été fournie.
* Mise à jour du système d&#39;importation de workflow du plug-in Maya pour assurer la compatibilité avec la mise à jour d&#39;Autodesk vers Python 3.12.
* Mise à jour des icônes du plug-in de Substance avec les dernières icônes.
* Ajout de la prise en charge de l’envoi et de la réception de paramètres prédéfinis via Connecteur dans le plug-in.

<b>Fixe :</b>

* Résolution d’un problème en raison duquel le chargement/déchargement du plug-in de Substance pour Maya produisait un écran d’erreur et se bloquait.
* Correction des problèmes de mise en cache, en particulier la vérification de la référence correcte des fichiers .exr et la réduction des blocages liés à la mise en cache dans les scènes volumineuses.
* Résolution du problème en raison duquel l’aperçu du matériau dans la fenêtre Exemple ne s’affichait pas lorsqu’un fichier SBSAR était chargé dans le plug-in Maya.
* Résolution du problème où le connecteur ne parvient pas à recevoir le fichier SBSAR si au moins un fichier SBSAR est déjà dans Hypershade.
