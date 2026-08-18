---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-integrations/game-engines/unity/unity-release-notes/unity-2-4-5.html"
breadcrumb-title: ''
description: Consultez les notes de mise à jour du plug-in Unity version 2.4.5 pour en savoir plus sur les nouvelles fonctionnalités, les améliorations et les correctifs de bogues.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unity > Unity Release Notes > Unity 2.4.5
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Unity 2.4.5
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 0%

---


# Unity 2.4.5

Publié le 6 avril 2020

* Ajouté : vérification des ressources HDRP à l’aide de l’API 2019.3
* Ajout : mise à jour de la Substance Engine 7.2 - corrige certains matériaux substance de la source qui ne fonctionnent pas
* Ajouté : mettre à jour les paramètres cibles pour qu’ils correspondent à la résolution du processeur
* Ajout : paramètre de résolution maximale du moteur du processeur (paramètre 4k ou 2k)
* Ajouté : conversion de Substances non HDRP dans un projet HDRP
* Correction : blocage lors de l’importation d’un grand nombre de Substances
* Correction : exception lors du clic sur la réimportation en mode de lecture après la modification des paramètres de Substance
* Correction : validez la résolution (texture) de la sortie ( API pour limiter le moteur CPU à 2K) préférence utilisateur pour définir la valeur par défaut sur 4K.
* Correction : cliquer sur « Générer des cartes mip » sur un graphique en Substance en mode Lecture, puis modifier les paramètres entraîne un blocage infini.
* Correction : lors de l’utilisation du plug-in Substance dans un projet HDRP, l’utilisation de la compression Brut définit les textures en niveaux de gris sur Alpha 8
* Fixe : GameObject désélectionné en mode Lecture
* Fixe : la texture de rugosité n’est pas mise à jour avec la modification des paramètres
* Correction : la sortie du masque n’est pas générée correctement pour certains fichiers de Substance dans HDRP
* Correction : blocage lors du basculement de la liste déroulante de mappage alpha compressée entre deux options
* Correction : la case à cocher Instance GPU est désactivée lorsque vous cliquez en dehors du matériau de Substance.
* Fixe : lorsque vous utilisez la fonction Duplicate() , le graphique de Substance dupliqué n’a pas le smoothness tassé dans l’alpha du métallique correctement.
* Correction : le basculement de la cible de construction vers Android entraîne le formatage incorrect des textures jusqu’à ce qu’elles soient réimportées manuellement.
* Correction : la suppression d’un fichier de Substance de données dans Unity entraîne une NullReferenceException.
* Correction : désactivez l’utilisation de l’API HDRP Unity 2019.3 pour les versions précédentes

Problèmes connus :

* La case à cocher d’émission n’est pas activée par défaut et la valeur HDR est définie sur noir lors de l’importation d’une Substance.
* Les propriétés de matériau des emballages contenant des matériaux Substance standard ne sont pas reportées lors de l’importation.
* La mise à jour de 2017-2019/2020 ne fonctionne pas dans HDRP
* Cliquer sur l’option de pince 2048 dans le menu des paramètres alors que 4096 est sélectionné dans les paramètres cibles (sans cliquer sur Appliquer) entraîne une erreur dans le journal de la console
