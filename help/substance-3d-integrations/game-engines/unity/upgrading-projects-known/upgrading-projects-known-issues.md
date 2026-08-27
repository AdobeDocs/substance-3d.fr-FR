---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unity/upgrading-projects-known-issues.html"
breadcrumb-title: ''
description: Découvrez comment mettre à niveau les projets Unity avec des supports de Substance et les problèmes connus à éviter pendant la migration.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unity > Upgrading ProjectsKnown Issues
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Problèmes connus de mise à niveau des projets
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 1%

---


# Mise à niveau des projets/problèmes connus

>[!WARNING]
>
> Le plug-in Substance 3D pour Unity 3.0.0 ne prend pas en charge la rétrocompatibilité. Assurez-vous donc d’utiliser Unity 2020.3.27x et versions ultérieures.
> 
> Unity a modifié l&#39;architecture de build par défaut en x86 au lieu de x86\_64.\
> Les scripts ne s’exécutent pas s’ils font référence à des Substances. Vous devrez revenir à x86\_64 et la build fonctionnera.

## Problèmes connus

* Erreur « *Échec de l’assertion sur l’expression » lors de la navigation dans les dossiers du panneau.*
  * Il s’agit d’une erreur qui se produit du côté d’Unity lorsque des modifications sont apportées à l’interface utilisateur, généralement des modifications de vignettes, qui doivent être un message inoffensif.
* *Les entrées d&#39;image semblent verrouillées sur 8 bits*
  * Ce problème est résolu dans la version 3.8.0-3. Le flux de travail correct serait que les utilisateurs changent le format par défaut d&#39;Unity pour la texture en RGBA64. Le plug-in s’occupera d’envoyer correctement ces informations à la Substance Engine.
