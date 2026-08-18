---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unity/unity-release-notes/unity-3-0-0-plus.html"
breadcrumb-title: ''
description: Consultez les notes de mise à jour du plug-in Unity version 3.0.0 et ultérieure pour en savoir plus sur les nouvelles fonctionnalités et améliorations.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unity > Unity Release Notes > Unity 3.0.0
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Unity 3.0.0
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4a060ee1aaa1731c04e70d5512e3271cd63d0381
workflow-type: tm+mt
source-wordcount: '1384'
ht-degree: 0%

---


# Unity 3.0.0+

## Unity 3.12.0

<b>Ajouté/Mis À Jour :</b>

* Prise en charge de Substance 3D Connector dans Unity, activant la fonctionnalité Envoyer vers pour l’envoi de ressources entre Substance 3D Sampler et Unity.
* Prise en charge du renommage et de la republication des graphiques .sbsar de Designer vers Unity, garantissant que les modifications apportées dans Designer sont conservées lorsque le graphique mis à jour est réimporté dans le plug-in Unity.
* Documentation pour le partage de fichiers .sbsar entre projets Unity.
* Page de contribution de la communauté à la documentation du plug-in Unity : https://helpx.adobe.com/substance-3d-integrations/game-engines/unity/community-contributions.html.

<b>Fixe :</b>

* Problème en raison duquel la miniature de matériau dans le dossier Ressources du projet Unity ne se met pas à jour après la republication d’un fichier .sbsar, affichant le matériau précédent au lieu du matériau actuel.

## Unity 3.11.0

<b>Ajouté/Mis À Jour :</b>

* Amélioration des performances des projets avec plus de 1 000 graphiques de Substance, réduisant considérablement les temps de réponse de l’interface utilisateur lors de l’inspection des fichiers sbsar dans le dossier Assets.
* Ajout d’un bouton de réinitialisation pour rétablir les fichiers sbsar à leur état d’origine, améliorant ainsi l’efficacité du workflow.
* Documentation mise à jour avec une solution pour le problème « Entrées d’image verrouillées sur 8 bits », disponible à l’adresse : [Intégrations Substance 3D dans Unity - Mise à niveau des projets et problèmes connus](../../../../game-engines/unity/upgrading-projects-known/upgrading-projects-known-issues.md).
* Documentation mise à jour pour résoudre l’erreur « Échec de l’assertion sur l’expression » rencontrée lors de la navigation dans les dossiers des panneaux dans Unity : [Intégrations Substance 3D dans Unity - Mise à niveau des projets et problèmes connus](../../../../game-engines/unity/upgrading-projects-known/upgrading-projects-known-issues.md).

<b>Fixe :</b>

* Correction d’un problème qui provoquait la rupture du plug-in sur les plateformes Linux.
* Correction des problèmes de compatibilité avec le plug-in Unity dans la version 2023.

## Unity 3.10.1

<b>Fixe :</b>

* Correction d’un problème en raison duquel le chargement de la Substance Engine échouait en raison d’un problème avec sbsario.dll dans le plug-in Substance 3D pour Unity.

## Unity 3.10.0

<b>Ajouté/Mis À Jour :</b>

* Mise à jour de la section des commentaires pour l’API RenderInstanceAsync dans le plug-in

<b>Fixe :</b>

* Correction d’un problème de fuite de mémoire dans le code C++ du plug-in, garantissant une récupération complète de la mémoire lors de l’élimination des objets.
* Correction d’un problème sous Linux en raison duquel l’importation du package de plug-in Unity entraînait une erreur « SubstanceException : un argument non valide a été donné à l’API », ce qui permettait désormais l’importation réussie des fichiers SBSAR.
* Correction d’un problème en raison duquel SubstanceGraphSO.CurrentStatePreset ne fonctionnait pas correctement pour le chargement des paramètres prédéfinis avec un script de fenêtre d’éditeur personnalisé dans Unity. Un script correctif est désormais disponible sur notre page de documentation de la Substance de données (HelpX) : https://experienceleague.adobe.com/en/docs/substance-3d/ecosystem/game-engines/unity/substance-3d-for-unity-scripting/substance-3d-for-unity-scripting.
* Correction d’un bug en raison duquel les propriétés du graphique disparaissaient lors de la resélection dans l’éditeur Unity.
* Correction du problème « Type managé inconnu référencé » lié à SubstanceGraphSO dans le plug-in Unity, en améliorant la compatibilité et les fonctionnalités sur les plateformes Android, en particulier pour Unity 2022.1 et potentiellement pour toutes les versions d’Unity.
* Correction d’un problème en raison duquel la sélection « FORMAT NORMAL » dans la section PARAMÈTRES TECHNIQUES était incorrectement affichée en tant que champ de saisie numérique, au lieu de la liste déroulante prévue avec les options DirectX et OpenGL.

## Unity 3.9.0

<b>Ajouté/Mis À Jour :</b>

* Les fichiers Sbsar peuvent désormais être glissés et déposés dans le projet. L’objet .sbsar peut être appliqué à un filet comme prévu dans Unity 2022.3.
* Documentation améliorée du plug-in.

<b>Fixe :</b>

* Correction d’un problème en raison duquel le plug-in Unity ne fonctionnait pas sous Android.
* Correction des contraintes de dénomination dans le plug-in Unity. Lorsqu’un nom de fichier contenait un « . », le plug-in ne chargeait pas le fichier correctement.
* Correction d’un problème en raison duquel la désélection de « Générer toutes les sorties » ne supprimait pas automatiquement la texture supplémentaire.
* Correction de l’importation incorrecte de matériaux SBSAR dans les projets standard Unity 2021.3. Désormais, dans le projet de modèle standard, les matériaux SBSAR peuvent être importés dans le dossier assets et appliqués à un filet 3D sans erreurs.
* Correction de l’importation incorrecte de matériaux SBSAR dans les projets Unity 2021/2022 HDRP. Désormais, dans le projet de modèle HDRP, les matériaux SBSAR peuvent être importés dans le dossier assets et appliqués à un filet 3D sans erreurs.
* Correction d’une erreur de compilation lors de la génération de la build Android pour produire l’APK : « Échec de la compilation ; consultez la sortie de l’erreur du compilateur pour plus de détails. »
* Correction d’un problème en raison duquel le processus de projet de build échouait avec des erreurs sous Windows.
* Correction d’un problème en raison duquel le processus de projet de build échouait avec des erreurs sur Android : UnityEditor.BuildPlayerWindow+BuildMethodException.
* Correction de l’UnityException rencontrée lors de la modification des entrées SubstanceGraph lors de l’exécution. Auparavant, l’appel de SubstanceRuntimeGraph.SetTexturesResolution et de SubstanceRuntimeGraph.Render() entraînait le rendu de résultats incorrects dans SubstanceGraph.
* Correction d’une erreur typographique dans SubstanceEditorTools.cs.

## Unity 3.8.0

<b>Ajouté/Mis À Jour :</b>

* Prise en charge introduite des paramètres avec visibilité conditionnelle (fonction Visible si).
* Mise à niveau du moteur de Substance vers la version 9.
* Documentation mise à jour pour résoudre un problème avec NativeGraph.InRenderWork qui ne fonctionne pas dans un script de fenêtre d’éditeur personnalisé. Pour plus d&#39;informations, cliquez ici : [Substance 3D pour les scripts Unity - Documentation de la classe](../../../../game-engines/unity/3d-for-unity-scripting/class-documentation/substanceruntime-class/substanceruntime-class.md)

<b>Fixe :</b>

* Correction d’un problème affectant les mappages normaux dans les projets Android.
* Correction d’un bug en raison duquel le glissement d’un objet sbsar dans la vue de la scène entraînait par inadvertance le remplacement de la matière de tous les objets survolés par la matière de l’objet sbsar.
* Correction d’un bug qui provoquait une erreur lors de l’inspection d’une matière marquée comme Runtime uniquement en mode Runtime et de l’ouverture du mappage de texture de sortie.

## Unity 3.7.0

<b>Ajouté/Mis À Jour :</b>

* Prise en charge des paramètres prédéfinis intégrés et externes
* Compatibilité avec Unity 2022.2

<b>Fixe :</b>

* Erreur lors de la création d’un graphique pour un fichier sbsar à l’aide du bouton Copier le graphique : « Transfert récursif inattendu de la classe scriptée »
* Création d’un dossier matières supplémentaires dans Mac après la réouverture d’un projet
* Le tableau SubstanceFileSO ne se met pas à jour lors de la création/suppression d’instances de graphiques
* Affichage d’options de saisie incorrectes lors de la duplication d’une Substance
* Champs de libellé vides dans les exportations de fichiers .sbsprs
* Erreurs lors de l’exportation/l’importation de paramètres prédéfinis dans l’éditeur : EndLayoutGroup : BeginLayoutGroup doit être appelé en premier.

<b>Supprimé(e) :</b>

* Section Canaux du plug-in Unity en raison d’un manque de valeur utilisateur

## Unity 3.6.0

<b>Ajouté/Mis À Jour :</b>

* Possibilité de rendre des valeurs Int 4 individuelles modifiables indépendamment.

<b>Fixe :</b>

* Problème de matériaux qui revenaient à un état précédent lors de la réouverture d’un projet
* Erreur lors de l’affichage du message « Aucun graphique trouvé » lors de la tentative de modification du graphique Matériau
* Problème en raison duquel les valeurs d’entrée pour le paramètre Décalage de rotation dans la fonction de Taille physique n’étaient pas modifiées
* Problème de valeurs d’ID de graphique incorrectes pour les entrées des instances de graphique dupliquées
* Problème lors duquel le générateur de Substances ne s’initialisait pas correctement dans l’éditeur lors de l’utilisation de scripts de l’éditeur (fenêtre de l’éditeur personnalisé) pour modifier un graphique
* Problème lors de l’exportation d’un script de fenêtre d’éditeur personnalisé avec SubstanceGraphSO.CurrentStatePreset, qui exportait une version mise en cache du graphique.
* Un problème en raison duquel les modifications de paramètres n’étaient pas enregistrées lorsque la fenêtre de l’inspecteur était verrouillée
* Un problème en raison duquel la saisie manuelle au clavier dans la section Décalage de position des options de Taille physique n’avait aucun effet sur la matière en mode Éditeur
* Erreur lors de la saisie manuelle des valeurs de paramètre dans l&#39;objet SBSAR

## Unity 3.5.0

<b>Ajouté/Mis À Jour :</b>

* Prise en charge pour les utilisateurs de la modification de la façon dont les textures de sortie sont attribuées au matériau Unity
* Compatibilité des modules avec la dernière version d’Unity 2022.2

<b>Fixe :</b>

* Erreur de référence nulle lorsque les matériaux ont une entrée Int4
* Erreur avec les entrées Int4, la valeur W est affectée à Data2 au lieu de Data3
* Erreur de frappe dans le nom de fonction « \_OcclusionStrength »

## Unity 3.4.0

<b>Ajouté/Mis À Jour :</b>

* Contrôles de décalage de position pour appliquer la texture à la surface dans le panneau taille physique
* Liens pour télécharger les actifs de la communauté Adobe Substance 3D Assets et Substance dans les paramètres du projet

## Unity 3.3.0

<b>Ajouté/Mis À Jour :</b>

* La fonction de taille physique pour HDRP, qui permet d’appliquer les matériaux et de les mettre à l’échelle en fonction de leurs tailles réelles
* Interface utilisateur pour l’activation du GPU dans les paramètres du projet

<b>Supprimé(e) :</b>

* graphID de la plupart des appels API

## Unity 3.2.1

<b>Fixe :</b>

* Problème de mise à niveau du plug-in de 3.0.0 et 3.1.0 vers la dernière version.

## Unity 3.2.0

<b>Ajouté/Mis À Jour :</b>

* Amélioration des performances lors de la recompilation de scripts

<b>Fixe :</b>

* Échec de l’importation des ressources dans le plug-in Unity lors de l’importation de matériaux Sbsar personnalisés
* Erreur « ArgumentException : la valeur n’est pas comprise dans la plage attendue »
* Erreur « ArgumentOutOfRangeException : Index était hors limites »

## Unity 3.1.0

<b>Ajouté/Mis À Jour :</b>

* Amélioration des performances de 1,38x pour Mac
* Le moteur GPU sur Mac utilise Metal au lieu d’OpenGL

<b>Fixe :</b>

* Problème Mac où les canaux R et B des textures de sortie seront inversés

## Unity 3.0.0

<b>Ajouté/Mis À Jour :</b>

* Prise en charge d’Apple Silicon
* Nouveau tutoriel YouTube sur l’utilisation du plug-in
* Nouvelle documentation sur les scripts

<b>Fixe :</b>

* Bogue dans l’affichage de l’inspecteur lorsque vous appuyez plusieurs fois sur le bouton de sélection aléatoire
* Entrées de texture nulles interrompant les mises à jour de Substance
* Les boutons « Générer toutes les sorties », « Générer des mappages Mip » et « Exécution uniquement » ne fonctionnent pas
* Problèmes liés aux espaces de noms
* Erreur Référence nulle lors de l’entrée en mode de lecture avec l’élément de graphique sélectionné
* Problème avec HDRP et URP pour la dernière version LTS 2021.3 d’Unity lors de l’utilisation de matériaux uniquement à l’exécution
