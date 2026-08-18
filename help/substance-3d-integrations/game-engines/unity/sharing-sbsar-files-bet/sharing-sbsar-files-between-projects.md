---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-integrations/game-engines/unity/sharing-sbsar-files-between-projects.html"
breadcrumb-title: ''
description: Partagez des fichiers SBSAR de Substance entre des projets Unity tout en conservant les réglages de paramètres à l’aide de fichiers prédéfinis.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unity >Sharing sbsar Files Between Projects
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Partage De Fichiers Sbsar Entre Projets
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 0%

---


# Partage De Fichiers Sbsar Entre Projets

Il est possible de partager des fichiers .sbsar entre des projets et des ordinateurs tout en conservant les mêmes réglages de paramètres avec l’utilisation de fichiers .sbsprs.

Une fois que la matière du projet d’origine a été modifiée pour adopter les paramètres qui seront partagés, accédez aux paramètres prédéfinis dans le panneau Inspecteur. Dans les paramètres prédéfinis, créez un nouveau paramètre prédéfini et nommez-le. Ce nouveau paramètre prédéfini nommé apparaîtra dans la liste des paramètres prédéfinis pour ce matériau. Une fois cela fait, exportez le paramètre prédéfini pour l’enregistrer localement.

Lorsque vous utilisez le fichier .sbsar dans un autre projet ou ordinateur, incluez également le fichier de paramètre prédéfini exporté. Une fois le fichier sbsar importé dans le projet Unity, accédez aux paramètres prédéfinis et choisissez l’option d’importation. Sélectionnez le fichier prédéfini de l’étape précédente et importez-le. Un paramètre prédéfini avec les paramètres du projet précédent doit être ajouté à la liste des paramètres prédéfinis.

Répétez l’opération pour toutes les matières partagées.
