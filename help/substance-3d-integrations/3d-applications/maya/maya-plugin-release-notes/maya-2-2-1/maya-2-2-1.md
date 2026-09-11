---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/3d-applications/maya/maya-plugin-release-notes/maya-2-2-1.html"
breadcrumb-title: ''
description: Consultez les notes de mise à jour pour le plug-in Maya version 2.2.1 pour en savoir plus sur les nouvelles fonctionnalités, les améliorations et les correctifs de bogues.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > Maya > Maya Plugin Release Notes > Maya 2.2.1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Maya 2.2.1
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---


# Maya 2.2.1

Version 2.2.1 de Maya :

* Mettre à jour la Substance Engine vers la version 8.3.0
* Ajout d’une prise en charge native pour Arnold, ce qui rend inutile la mise en cache sur disque
* Cela peut être utilisé après avoir activé les extensions de rendu dans les paramètres et redémarré Maya
* Les versions prises en charge sont les suivantes :
* Maya 2017 - MtoA 3.1.0/Arnold 5.2.0
* Maya 2018 - MtoA 4.0.0/Arnold 6.0.0, MtoA 4.2.0/Arnold 6.2.0
* Maya 2019 - MtoA 4.0.0/Arnold 6.0.0, MtoA 4.2.0/Arnold 6.2.0, MtoA 5.0.0/Arnold 7.0.0
* Maya 2020 - MtoA 4.0.0/Arnold 6.0.0, MtoA 4.2.0/Arnold 6.2.0, MtoA 5.0.0/Arnold 7.0.0
* Maya 2022 - MtoA 4.2.1/Arnold 6.2.0, MtoA 5.0.0/Arnold 7.0.0
* Répertoire d’installation mis à jour sous Windows et MacOS
* Les fichiers binaires sous MacOS/Windows sont désormais signés à l’aide de certificats Adobes
* Les basculements de canal sont désormais masqués lorsque l’auteur du fichier sbsar est Allegorithmic ou Adobe, au lieu de simplement Allegorithmic
* Ajout d’une nouvelle interface utilisateur de workflow, avec des fonctionnalités supplémentaires pour dupliquer, écraser, renommer et supprimer des workflows

Ajout des nouvelles commandes de script suivantes :

substance

substanceGetEnableRenderingExtensions

substanceSetEnableRenderingExtensions

substanceWorkflow.py

substanceWorkflowIsReadOnly

substanceWorkflowRenameWorkflow

substanceWorkflowDuplicateWorkflow

substanceWorkflowOverwriteWorkflow

substanceWorkflowRemoveWorkflow

Correctifs de bogues :

* Correction de l’erreur lors de l’ouverture de la boîte de dialogue Paramètres
* Les fonctions de workflow n’échouent plus lorsqu’un pyc est généré

Cette version est publiée pour Maya 2017, 2018, 2019, 2020 et 2022 sur Linux, MacOS et Windows, et Maya LT 2018, 2019 et 2020 sur MacOS et Windows
