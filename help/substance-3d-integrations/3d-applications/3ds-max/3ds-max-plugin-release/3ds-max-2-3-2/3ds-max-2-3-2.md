---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/3d-applications/3ds-max/3ds-max-plugin-release-notes/3ds-max-2-3-2.html"
breadcrumb-title: ''
description: Consultez les notes de mise à jour du module externe 3ds Max version 2.3.2 pour en savoir plus sur les nouvelles fonctionnalités, les améliorations et les correctifs de bogues.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > 3ds Max > 3ds Max Plugin Release Notes > 3ds Max 2.3.2
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3ds Max 2.3.2
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '253'
ht-degree: 0%

---


# 3ds Max 2.3.2

Publié le 8 avril 2020

Aujourd’hui, nous avons publié la version 2.3.2 du plug-in, qui est principalement une version de correctif de bogue en plus de la version 2.3.1.

Version 2.3.2 :

* Substances Engine mises à jour de la section 7.2.9
* Résolution d’un problème de rendu suite au blocage de Redshift/VRay dans 3ds Max 2018, 2019 et 2020
* Les erreurs d’assertion de débogage n’apparaîtront plus
* Le nœud Substance 2 dispose désormais correctement des interfaces de script pour iMultipleOutputChannelsWithValues
* L’entrée Source de Substance de données du menu ouvre désormais le Lanceur de Substance de données dans l’onglet Source s’il est installé
* Les matériaux de Substance doivent désormais être mis à jour correctement lors de l’utilisation du rendu Corona
* Les sorties de Substance ne sont plus temporairement remplacées par des images lorsqu’elles sont utilisées avec VRay Next
* La boîte de dialogue de compatibilité de rendu a été supprimée de l’affichage automatique. Elle est toujours disponible dans la boîte de dialogue des paramètres si nécessaire
* Correction d’un problème possible lié à l’exportation d’un fichier fbx lorsque la matière Substance est appliquée dans 3ds Max 2021.

Problèmes connus :

* Dans 3ds Max 2018, l&#39;exportation d&#39;un fichier fbx avec un matériau de Substance attaché à l&#39;objet se bloque dans le module fbxmax.dlu. Nous discutons actuellement avec Autodesk pour voir s&#39;il y a quelque chose que nous pouvons faire ou s&#39;il s&#39;agit d&#39;une limitation de l&#39;ancienne version de l&#39;intégration fbx. La solution précédente n’était pas fiable et a été supprimée. Cela ne se produit pas dans 3ds Max 2019 ou version ultérieure.

Cette version est publiée pour 3ds Max 2018, 2019, 2020 et 2021.
