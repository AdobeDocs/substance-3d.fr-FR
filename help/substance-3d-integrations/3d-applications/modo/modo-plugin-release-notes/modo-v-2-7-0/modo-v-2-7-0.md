---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/3d-applications/modo/modo-plugin-release-notes/modo-v-2-7-0.html"
breadcrumb-title: ''
description: Consultez les notes de mise à jour du module externe MODO version 2.7.0 pour en savoir plus sur les nouvelles fonctionnalités, les améliorations et les correctifs de bogues.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > MODO > Modo Plugin Release Notes > Modo v. 2.7.0
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Modo v. 2.7.0
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 0%

---


# Modo v. 2.7.0

* De nombreux correctifs
* Prise en charge des fichiers flottants 32 bits
* Textures 4k dans le moteur CPU et 8 k dans le moteur GPU
* nouveau format LPK pour la version du plug-in
* nouveau menu Kit pour le plug-in Substance
* Prise en charge de glTF / Principled shader pour MODO 12.0
* Ajout d’un chemin relatif pour les fichiers de Substance de données
* Prise en charge Linux
* Nouvelle interface utilisateur pour charger et enregistrer des paramètres prédéfinis
* Les paramètres prédéfinis intégrés sont chargés à partir de Designer.
* Boîte d’avertissement de mémoire GPU supprimée
* Commandes de chargement/d’enregistrement des paramètres prédéfinis modifiées

  Les nouvelles commandes disponibles sont les suivantes :

  **substance.getsbsname** Convertissez l&#39;identificateur d&#39;un objet substance en son nom interne

  Tous ces éléments attendent un nom interne propre acquis auprès de substance.getsbsname :

  **substance.setpreset** Définit le paramètre prédéfini actuel d&#39;une Substance sur l&#39;index **substance.getpresetindex** Obtient l&#39;index du paramètre prédéfini actuel **substance.getpresetat** Renvoie le nom de chaîne d&#39;un paramètre prédéfini à un **index substance.getpresetcount** retourne le nombre de paramètres prédéfinis d&#39;une Substance de données **substance.savepresetfile** Enregistre un paramètre prédéfini de la configuration actuelle dans le chemin de fichier donné **substance.loadpresetfile** Charge un fichier de paramètre prédéfini dans la Substance indiquée

  Commandes de l’interface utilisateur :

  Commande d&#39;interface utilisateur **substance.loadpresetui** pour le chargement d&#39;une commande d&#39;interface utilisateur **substance.savepresetui** prédéfinie pour l&#39;enregistrement d&#39;une commande d&#39;interface utilisateur **substance.selectpresetui** prédéfinie pour la définition du préréglage
