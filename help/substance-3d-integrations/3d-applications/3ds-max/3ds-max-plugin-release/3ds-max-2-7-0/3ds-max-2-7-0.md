---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/3d-applications/3ds-max/3ds-max-plugin-release-notes/3ds-max-2-7-0.html"
breadcrumb-title: ''
description: Consultez les notes de mise à jour du module externe 3ds Max version 2.7.0 pour en savoir plus sur les nouvelles fonctionnalités, les améliorations et les correctifs de bogues.
helpx_creative_field: ""
helpx_description: Substance 3D Integrations
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3ds Max 2.7.0
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 0%

---


# 3ds Max 2.7.0

<b>Ajouté/Mis À Jour :</b>

* Mise à niveau du moteur de Substance vers la version 9 dans le plug-in 3ds Max, améliorant les performances et la compatibilité.

<b>Fixe :</b>

* Correction d’un problème de crash dans les versions 2019, 2022, 2023 et 2024 de 3ds Max, en raison duquel le crash du programme était provoqué par le glissement d’un nœud Substance 2 dans l’éditeur de Matériau d’ardoise. Le nœud Substance 2 peut désormais être glissé et déposé en toute sécurité dans l’éditeur de Matériau d’ardoise.
* Correction d’un problème dans le plug-in de Substance pour 3ds Max, en raison duquel la sélection de « Substance vers Arnold » et d’autres workflows ne créaient pas de nœuds pertinents dans l’éditeur d’ardoise de Matériau, mais ouvraient par erreur un Maxscript avec une erreur de compilation. Les nœuds des workflows comme Arnold sont désormais correctement générés et connectés automatiquement.
* Correction d’un problème en raison duquel l’exportation d’actifs de départ/de paramètres prédéfinis (.sbsar - feuille de texture Substance 2) à partir de Substance 3D Sampler et leur conversion en système de rendu Corona (versions 6 à 9hf1) dans 3ds Max entraînaient des matériaux corrompus, un rendu avec une base color noire et des normales de bosse rompues. En outre, cette mise à jour résout l’inaccessibilité de l’onglet des propriétés de Substance de données dans les matériaux, un problème qui affectait également les conversions en Vray.
* Correction d’un problème dans le plug-in 3ds Max en raison duquel le branchement ou le débranchement des entrées des textures Substance 2 vers le Matériau Corona provoquait des crashs.
* Correction du problème de compatibilité dans 3ds Max 2024 en raison duquel les scripts Python incorporés ou appelés dans un fichier MaxScript n’étaient pas autorisés par défaut.
* Correction d’un problème dans le plug-in 3Ds Max en raison duquel l’importation et l’exécution du plug-in Substance to Corona entraînaient l’affichage de matériaux noirs et brillants dans les aperçus et les rendus shader. Ce problème a été résolu, ce qui garantit un affichage et un rendu corrects des cartes de Substance avec le rendu Corona.

Cette version est publiée pour 3ds Max 2021, 2022 et 2023
