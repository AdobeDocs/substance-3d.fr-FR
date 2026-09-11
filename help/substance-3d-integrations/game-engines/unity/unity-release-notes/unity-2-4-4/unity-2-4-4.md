---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unity/unity-release-notes/unity-2-4-4.html"
breadcrumb-title: ''
description: Consultez les notes de mise à jour du plug-in Unity version 2.4.4 pour en savoir plus sur les nouvelles fonctionnalités, les améliorations et les correctifs de bogues.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unity > Unity Release Notes > Unity 2.4.4
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Unité 2.4.4
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 0%

---


# Unité 2.4.4

Publié en février 2020

* Ajouté : prise en charge appropriée pour 2019.3 : correction des modifications de l’API Unity qui ont enfreint l’objet scriptable du plug-in Substance. Objets retravaillés à utiliser avec les mises à jour d’API 2019.3. Fixe : l’utilisation d’un matériau personnalisé fait que le matériau devient noir à la fermeture de la lecture.
* Fixe : Crash lors de l’utilisation de la fonction Duplicate() dans un script, puis de l’entrée et de la sortie de la lecture.
* Correction : réinitialisation de la répétition, des paramètres et du shader du Matériau en 2019.3
* Correction : le Shader de Matériau HDRP n’actualise pas les modifications de paramètre
* Fixe - Mappage de masque HDRP non mis à jour
* Fixe - Ajouter un paramètre de chaîne pour la fonction Duplicate
* Correction : correction de la prise en charge de Linux dans la dernière version d’Unity Stable
* Correction : problème d’adresse lié au fait que le code binaire doit être désactivé pour iOS

Problèmes connus :

* Si vous renommez la ressource HDRP, le plug-in ne générera pas de mappage de masque.
* Lors de l’utilisation du plug-in Substance dans un projet HDRP, la compression Brut définit les textures de niveaux de gris sur Alpha 8.
* GameObjects sera désélectionné en mode Lecture
* Cliquer sur « Générer des cartes mip » sur un graphe de Substance en mode Lecture, puis modifier les paramètres entraîne un blocage infini.
