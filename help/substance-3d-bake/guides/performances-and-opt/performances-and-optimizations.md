---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/guides/performances-and-optimizations.html"
breadcrumb-title: ''
description: Découvrez comment optimiser la configuration matérielle et la préparation du maillage pour obtenir des performances de cuisson plus rapides.
helpx_creative_field: ""
helpx_description: bakers > Guides > Performances and optimizations
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Performances et optimisations
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '612'
ht-degree: 0%

---


# Performances et optimisations

## Configuration matérielle minimale

Il n’existe aucune exigence minimale concernant l’utilisation de Substance Bakers, mais il est important de noter les points suivants :

* Un bon CPU offrira des temps de calcul réduits (plusieurs cœurs accéléreront le calcul de **à partir de maillage** boulangeries qui utilisent le lancer de rayons).
* Une quantité de mémoire décente (RAM) permettra de charger des maillages avec beaucoup de détails (polygones).
* Un bon GPU permettra de générer des textures à de grandes résolutions (comme 8K).

## Triangulation

Les boulangers travaillent en interne avec des mailles triangulées ; si les modèles 3D (low et high poly) ne sont pas triangulés, les boulangers triangulent eux-mêmes les mailles. Ce processus peut prendre beaucoup de temps et augmentera linéairement par rapport à la quantité de polygones contenus dans le modèle. Il est généralement conseillé de trianguler les mailles (en particulier la maille poly élevée) afin d&#39;éviter que ce processus ne se produise lors de la cuisson.

Si votre workflow est basé sur FBX, vous pouvez trianguler le maillage au moment de l’exportation à l’aide d’une option dans l’application DCC.

## Cache de géométrie

Pour plus d’informations, consultez la page suivante : [Geometry Cache](../../features/geometry-cache/geometry-cache.md)

## Anti-crénelage

Les boulangers peuvent utiliser le super échantillonnage pour effectuer l&#39;anti-repliement. Le sur-échantillonnage signifie que les boulangers vont projeter plus de rayons par pixel afin de lisser le résultat. Le temps de cuisson peut être considérablement affecté par ce paramètre ; ceci est particulièrement vrai pour les boulangers où beaucoup de rayons sont nécessaires, comme l&#39;occlusion ambiante du boulanger à mailles.

À titre d’exemple :

* un réglage AA de 2x2 signifie que le boulanger projettera 4 fois la quantité initiale de rayons. Pour une texture 2 048\*2 048 px, le calcul résultant équivaut à cuire une texture 4 096\*4 096 px et devrait prendre environ 4 fois plus de temps à calculer.
* un réglage AA de 8x8 signifie que le boulanger projettera 64 fois la quantité initiale de rayons. Pour une texture 2 048 **&#x200B; 2 048 px, le temps de calcul obtenu équivaut à cuire une texture 16384**&#x200B;16384px et devrait prendre environ 64 fois plus de temps à calculer.

**En tenant compte de ces chiffres, le paramètre 8x8 doit être utilisé avec précaution**.

Afin de réduire la présence de bruit, il est généralement conseillé d&#39;augmenter le nombre de rayons secondaires (pour l&#39;occlusion ambiante, l&#39;épaisseur et les normales courbées bakers) et de conserver un réglage 2x2 ou 4x4 AA plutôt que d&#39;utiliser une faible quantité de rayons secondaires et un réglage élevé AA.

>[!NOTE]
>
> Un bon réglage de performance/qualité pour l&#39;occlusion ambiante du maillage est d&#39;utiliser AA 2x2 et au moins 128 rayons secondaires.

## Format de fichier

L’exportation de fichiers sur le disque peut prendre un temps important en fonction du format de fichier, de la résolution, de la profondeur de bit et des paramètres de compression. Les paramètres de compression peuvent être modifiés dans les options Préférences / Projets / Général / Format de fichier . La désactivation de la compression peut réduire le temps d’exportation au détriment des fichiers plus volumineux.

## Blocages et TDR

Plusieurs facteurs peuvent être à l’origine des blocages, dont le TDR (Timeout Detection Recovery). La TDR est un mécanisme Windows conçu pour détecter et récupérer les situations où le GPU ne semble pas répondre. En raison d’une faible valeur par défaut pour la détection de délai TDR, des blocages peuvent se produire lors de l’utilisation de boulangers spécifiques dans certaines situations :

* lors de la cuisson de maillages denses avec le boulanger Ambient Occlusion
* lors de l&#39;utilisation des boulangers accélérés DXR avec des mailles très denses en poly élevé (plus de 60 millions de triangles)

Vous trouverez des informations supplémentaires sur le TDR et un guide détaillé sur la modification des paramètres associés ici : [Les pilotes de GPU se bloquent lors des longs calculs (blocage du TDR)](https://helpx.adobe.com/substance-3d/unlisted/documentation/spdoc/gpu-drivers-crash-with-long-computations-128745489.html)
