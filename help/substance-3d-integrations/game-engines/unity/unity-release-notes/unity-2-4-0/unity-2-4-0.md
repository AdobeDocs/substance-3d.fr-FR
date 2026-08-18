---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unity/unity-release-notes/unity-2-4-0.html"
breadcrumb-title: ''
description: Consultez les notes de mise à jour du plug-in Unity version 2.4.0 pour en savoir plus sur les nouvelles fonctionnalités, les améliorations et les correctifs de bogues.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unity > Unity Release Notes > Unity 2.4.0
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Unity 2.4.0
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 0%

---


# Unity 2.4.0

>[!WARNING]
>
> Unity a modifié l&#39;architecture de build par défaut en x86 au lieu de x86\_64.\
> Les scripts ne s’exécutent pas s’ils font référence à des Substances. Vous devrez revenir à x86\_64 et la build fonctionnera.

## Nouvelles fonctionnalités :

* Prise en charge du projet HDRP ajoutée (aperçu)
* Ajout de préférences dans le menu Substance
* Possibilité de définir le paramètre d’importation de résolution de Substance par défaut ajoutée
* Possibilité de définir la compression Normale par défaut ajoutée
* Possibilité supplémentaire de générer toutes les sorties lors de l’importation d’une Substance
* Prise en charge des sorties personnalisées + sorties avec la même utilisation
* Paramètres de résolution de plate-forme ajoutés
* Correctifs de bugs de prise en charge de IL2CPP ajoutés

### Correctifs de bogues :

* Correction d’un bug en raison duquel l’ouverture de la Substance Source sur le système d’exploitation Mac donnait une erreur Linux
* Réduction du temps nécessaire pour changer de plate-forme. La conversion de texture pour les plates-formes mobiles est désormais effectuée sur build plutôt que lors du changement de plate-forme cible.
* Erreur d’échec d’assertion lors de l’importation de sbsar
* La mise à niveau de projets à l’aide de .NET 3.5 provoque la rupture des matériaux Substance
* Source de Substance non prise en charge dans la boîte de dialogue de Linux apparaissant sous OS X
* Le changement de nom du graphique détruit les préréglages et le fichier de scène en mode de sérialisation ForceText
* Les matériaux de Substance avec plusieurs sorties utilisant la même utilisation interrompront le plug-in ne prend pas en charge les sorties personnalisées dans sbsar

### Problèmes connus :

* Lors de la mise à niveau d’un projet entre 2017 et 2018/2019, une fois que l’utilisateur a importé le plug-in de Substance, Unity doit être redémarré pour que le projet soit mis à jour.\
  Solution : créez un pack contenant les actifs/le projet et importez ce pack dans un projet plus récent avec le plug-in 2.4.0. Les fichiers de Substance doivent être convertis correctement.
* Unity a modifié l’architecture de build par défaut en x86. Actuellement, le plug-in de Substance prend uniquement en charge x86\_64.

**Plus De Prise En Charge Complète :**

* Substance Live Link a été supprimé du package Asset Store. (Le pack peut toujours être téléchargé à partir de Substance share)
