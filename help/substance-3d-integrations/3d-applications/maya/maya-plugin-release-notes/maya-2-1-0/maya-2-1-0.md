---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-integrations/3d-applications/maya/maya-plugin-release-notes/maya-2-1-0.html"
breadcrumb-title: ''
description: Consultez les notes de mise à jour pour le plug-in Maya version 2.1.0 pour en savoir plus sur les nouvelles fonctionnalités, les améliorations et les correctifs de bogues.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > Maya > Maya Plugin Release Notes > Maya 2.1.0
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Maya 2.1.0
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 0%

---


# Maya 2.1.0

Substance dans Maya 2.1.0 changelog

* Compatibilité garantie avec Python 3
* Substances Engine mises à jour vers la version 7.2.9
* Correction d’une erreur avec des noms de variables de mel global en conflit lors de l’application d’un workflow
* Le workflow Redshift définit désormais Fresnel sur Metalness
* Ajout d’un nouveau fichier de plug-in, substanceLink, qui gère l’interopérabilité avec d’autres programmes de Substance et le lanceur de Substance
* Si vous ouvrez Substance Source maintenant, le lanceur de Substances s’ouvre dans l’onglet Source si le plug-in substanceLink est chargé
* Le plug-in substanceLink permet au lanceur d’envoyer des documents de Substance Source à l’intégration Maya lorsque l’interface utilisateur est ajoutée
* Commandes de script ajoutées pour obtenir les versions internes de la bibliothèque et ouvrir le lanceur Substance à la page source
* Les liens de sites Web s&#39;ouvrent désormais à [substance3d.com](http://substance3d.com) au lieu de [allegorithmic.com](http://allegorithmic.com)
* La documentation et les liens source, lors de l’ouverture d’une page web, ouvrent désormais le navigateur par défaut défini par l’utilisateur
* Sous Windows, Internet Explorer n’est plus ouvert
* Ajout d’un nouveau lien à la Substance share dans le tiroir et le menu
* Ajout de nouvelles commandes pour interroger la version et le hachage de l&#39;éditeur de Substance de données
* Dans Maya LT, la version a été supprimée du menu des paramètres
* About menu n&#39;est plus écrit en PySide2 et Python, mais en code natif en utilisant Qt à la place. Il est désormais disponible en Maya LT, où il ne l’était pas auparavant.
* Le menu À propos contient des informations de diagnostic différentes ; il affiche maintenant le hachage git pour correspondre au changement dans le contrôle de code source
* La copie du menu À propos dans le presse-papiers aura désormais également ce hachage git, ainsi que la version de Maya pour laquelle le plug-in est conçu.
* Les licences de la fenêtre À propos s’ouvrent désormais sous forme de fichier texte
* Prise en charge de Maya 2017 ajoutée
* Le générateur de script de workflow ne produit plus de chaînes pour le membre « commande ». Tous les workflows existants seront correctement traités.

Commandes de script ajoutées :\
substance :\
\* substanceUtilityGetLinkerVersion\
\* substanceUtilityGetLinkerHash\
\* substanceUiOpenAboutWindow\
\* substanceUiOpenSourceWebsite\
\* substanceUiOpenDocumentation\
\* substanceUiOpenShareWebsite

substanceLink :\
\* substanceLinkGetLinkVersion\
\* substanceLinkGetPortalCliVersion\
\* substanceLinkOpenLauncher

Cette version est publiée pour Maya 2017, 2018, 2019 et 2020 sur Windows,\
Linux et Macos. Il est également publié pour Maya LT 2018, 2019 et 2020 sur\
Windows et MacOS.
