---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-integrations/3d-applications/blender/release-notes/add-on-0-9-1.html"
breadcrumb-title: ''
description: Consultez les notes de mise à jour du module complémentaire Blender version 0.9.1 pour en savoir plus sur les nouvelles fonctionnalités, les améliorations et les correctifs de bogues.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > Blender > Release Notes > Add-on 0.9.1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Add-on 0.9.1
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '463'
ht-degree: 0%

---


# Add-on 0.9.1

**Notes de mise à jour pour la version 0.91+** du module complémentaire

* Remarque : *La version 0.91+ du plug-in n’est pas rétrocompatible avec les versions précédentes du plug-in !*
* Réarchitecture de la base de code interne pour améliorer les performances et la stabilité du plug-in
* Interface utilisateur remaniée pour améliorer l’expérience globale de l’utilisateur
* Ajout d’une interface utilisateur permettant de modifier la mosaïque par défaut
* Ajout de la prise en charge de la mise à jour des textures dans la vue de rendu des cycles
* Ajout de la gestion des erreurs dans la console pour notifier si une substance ne se charge pas
* Mise à jour du menu flottant avec des actions rapides

**Section Préférences : Ajoutée/Mise À Jour :**

* Paramètre Exporter le format d’image : lorsque des images générées dans Blender sont utilisées comme entrées d’image pour un matériau de Substance, ce format est utilisé pour enregistrer cette image dans le dossier Temporel.
* Chemin de la bibliothèque Sbsar ; spécifie le dossier qui est ouvert par défaut lorsque le bouton Charger est utilisé pour rechercher un fichier substance.
* Un chemin d’exportation de texture par défaut (dossier temporel) qui émule le chemin utilisé par Substance 3d Painter pour gérer les exportations de fichiers non enregistrées
* Chemin relatif de la texture identique à celui indiqué ci-dessus, avec la possibilité d’utiliser des touches telles que $matName pour créer des sous-dossiers
* Fichier sbsar relatif au chemin de création d&#39;un sous-dossier qui compresse les fichiers sbsar utilisés dans votre fichier de fusion lorsque vous enregistrez votre projet
* Possibilité de définir dynamiquement différents réseaux de nuanceurs dans les préférences : dans le réseau de nuanceurs, possibilité de définir différentes variables par nuanceur en fonction des besoins du nuanceur
* Dans la section Sorties du réseau de nuanceurs, vous avez la possibilité de définir si une sortie est activée par défaut
* Possibilité de définir l’espace colorimétrique (cela prendra en charge les workflows ACE, Linear Exr et Blender, pas seulement srvb)
* Sélection par défaut du format d’image et de la résolution
* Sortie générique permettant de définir les valeurs pour les utilisations de sortie non définies dans le shader, par exemple si vous avez une autre sortie qui n’est pas utilisée par défaut par le shader, par exemple un masque.
* Un filtre pour modifier le type de sorties(1 Uniquement les sorties activées, 2 Toutes les sorties qui se trouvent dans le shader et dans la Substance, 3 Toutes les sorties disponibles dans la Substance)
* Prise en charge des raccourcis personnalisés (modifié)

**Section Du Panneau Substance 3D : Ajoutée/Mise À Jour :**

* Possibilité d’ajuster et de verrouiller la valeur des paramètres de mosaïque et de résolution
* Mise à jour de l’interface utilisateur des paramètres prédéfinis : liste déroulante du type de nuanceur pour modifier le type de graphique souhaité par les utilisateurs.
* Modification du paramètre d’entrée d’image sur l’entrée d’image standard utilisée dans Blender. Vous pouvez désormais utiliser des images de mélangeur et pas seulement des fichiers
* Possibilité de travailler dans plusieurs instances de Blender à tout moment
* Prise en charge de la mise en surbrillance automatique des matériaux dans le panneau Substance 3D lorsque le matériau est sélectionné dans la clôture
