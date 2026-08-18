---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/3d-applications/3ds-max/3ds-max-plugin-release-notes/3ds-max-2-3-1.html"
breadcrumb-title: ''
description: Consultez les notes de mise à jour du module externe 3ds Max version 2.3.1 pour en savoir plus sur les nouvelles fonctionnalités, les améliorations et les correctifs de bogues.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > 3ds Max > 3ds Max Plugin Release Notes > 3ds Max 2.3.1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3ds Max 2.3.1
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '362'
ht-degree: 0%

---


# 3ds Max 2.3.1

Publié le 13 février 2020

Le module externe s’installe désormais en dehors du répertoire 3ds Max dans C:\ProgramData\Autodesk\ApplicationPlugins\SubstanceIn3dsMax. Il devrait désormais fonctionner partout où 3ds Max est invité à rechercher des plug-ins, il devrait donc maintenant fonctionner sur un lecteur réseau, etc.\
Notez que le passage au plug-in d’application et la modification du répertoire d’installation font en sorte qu’une mise à niveau à partir de la version 2.1.1 et des versions antérieures ne fonctionnera pas correctement. Ils doivent être supprimés manuellement pour 3ds Max 2018 et 2019. La version 2.2.0 doit être mise à niveau correctement.\
Pour certains problèmes non résolus dans cette version, un autre est prévu prochainement pour les résoudre, ainsi que tout autre problème pouvant survenir.

Cette version est actuellement disponible pour 3ds Max 2018, 2019, 2020 et 2021.

* Chargez d’abord les looks sbsar dans le dossier des images du projet
* La boîte de dialogue de compatibilité du système de rendu s’affiche désormais uniquement pour VRay RT et VUE File Renderer
* Glisser-déposer pour l’éditeur de matériaux Slate désactivé pour supprimer les problèmes avec le lot Max
* La boîte de dialogue de rendu ne s’affiche plus en mode silencieux 3ds Max
* Des scripts Python plus petits sont désormais compatibles avec Python 3
* Ajout de la prise en charge du lanceur de Substances pour envoyer des ressources de Substance Source à 3ds Max. Cela nécessitera des modifications dans le lanceur, mais la prise en charge du plug-in sera disponible au fur et à mesure de l’ajout de la fonctionnalité.
* Le script de rendu Redshift utilise désormais les nouveaux noms de nœuds définis dans Redshift 2.6.24
* Max ne se bloque plus lorsqu’un chemin vide est attribué au Substance 2 SubstanceFilePath
* Supprimer la collision de nom du type SubstanceOutput avec l’ancien plug-in
* Classe SubstanceOutput renommée en Substance 2Output
* Classe du Gestionnaire de menus de Substance renommée en Substance 2MenuManager
* Les ID de bloc de paramètre sont désormais effacés de force lorsqu’une scène est ouverte, ce qui supprime les collisions entre les fichiers de scène. Cela devrait résoudre les problèmes de blocs de paramètres non valides lors de la charge lors de l’alternance entre les scènes. L’importation peut encore présenter des problèmes, car elle nécessite des modifications plus complexes
* Le plug-in est maintenant installé en dehors de 3ds Max. Tous les chemins ont été remplacés par des chemins relatifs à partir de l’emplacement de chargement.
* Le plug-in utilise désormais le système de plug-in d&#39;application Autodesk.
