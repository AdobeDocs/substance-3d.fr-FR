---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-integrations/3d-applications/3ds-max/3ds-max-plugin-release-notes/3ds-max-2-8-0.html"
breadcrumb-title: ''
description: Consultez les notes de mise à jour du module externe 3ds Max version 2.8.0 pour en savoir plus sur les nouvelles fonctionnalités, les améliorations et les correctifs de bogues.
helpx_creative_field: ""
helpx_description: Substance 3D Integrations
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3ds Max 2.8.0
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 0%

---


# 3ds Max 2.8.0

<b>Ajouté/Mis à jour :
</b>

* Prise en charge de la visibilité conditionnelle des paramètres (« visible if ») ; les paramètres seront désormais masqués lorsque les conditions ne sont pas remplies, leurs groupes respectifs restant visibles.
* Mise à niveau du rendu Corona vers la version 10 dans le plug-in 3ds Max, améliorant les capacités de rendu et
* La dernière mise à jour améliore considérablement la vitesse de rendu et l’utilisation du processeur dans 3ds Max 2024 lors de l’utilisation de la Substance, alignant ses performances plus étroitement avec l’efficacité observée dans 3ds Max 2022.

<b>Fixe :</b>

* Amélioration du plug-in de Substance pour restreindre les valeurs d’entrée du clavier à la plage pratique pour chaque paramètre, évitant les problèmes de contrôle par curseur et de réglage manuel des valeurs.
* Correction d’un problème en raison duquel la copie de conversions de textures Substance 2 (.sbsar) dans l’éditeur de matériau Slate entraînait une instanciation involontaire du nœud copié, ce qui pouvait provoquer des blocages liés à d3d11.dll
* Résolution d’un problème de blocage dans 3ds Max lors du rendu de substances de matériau copiées personnalisées/modifiées (.sbsar) avec Corona Interactive
* Correction d’un problème dans le nœud Substance 2 de 3ds Max en raison duquel les curseurs des valeurs Entier 3 et 4 ne répondaient pas et seule la saisie numérique manuelle mettait à jour les valeurs. En outre, ces valeurs ne s’affichaient pas correctement au format flottant. Les curseurs sont désormais fonctionnels et reflètent avec précision les types de valeurs prévus.
* Correction d’un problème dans 3ds Max 2021 avec le rendu Corona en raison duquel les matériaux de Substance apparaissaient correctement dans la fenêtre d’affichage, mais étaient rendus en gris lorsque les fichiers étaient transférés vers un autre PC. Les utilisateurs n’ont plus besoin de configurer des matériaux à partir de zéro ou de charger des paramètres prédéfinis pour un rendu correct.
* Correction d’un problème de blocage dans le plug-in 3ds Max lors de la tentative de duplication des nœuds de Substance dans l’éditeur de matériaux Slate.
* Correction d’un problème en raison duquel le paramètre Limite des cœurs du processeur dans le plug-in de Substance de données n’était pas enregistré après le redémarrage de 3ds Max, garantissant ainsi que les valeurs configurées par l’utilisateur sont désormais conservées entre les sessions.

Cette version est publiée pour 3ds Max 2021, 2022 et 2023
