---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-bake/guides/performances-and-optimizations.html"
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

## Configuration matérielle minimale requise

Il n’y a pas d’exigences minimales pour l’utilisation de Substance Baker, mais il est important de noter les points suivants :

* Un bon processeur offre des temps de calcul réduits (plusieurs cœurs accélèrent le calcul de **à partir des boulangers de maillage** qui utilisent le lancer de rayons).
* Une quantité de mémoire décente (RAM) permettra de charger des maillages avec beaucoup de détails (polygones).
* Un bon GPU permettra de générer des textures à de grandes résolutions (comme 8K).

## Triangulation

Les boulangers travaillent en interne avec des maillages triangulés ; si les modèles 3D (low et high poly) ne sont pas triangulés, les boulangers trianguleront eux-mêmes les maillages. Ce processus peut prendre beaucoup de temps et augmentera linéairement en fonction de la quantité de polygones contenus dans le modèle. Il est généralement conseillé de trianguler les mailles (en particulier la maille poly élevée) afin d&#39;éviter que ce processus ne se produise lors de la cuisson.

Si votre workflow est basé sur FBX, vous pouvez trianguler le maillage au moment de l’exportation à l’aide d’une option dans l’application DCC.

## Cache de géométrie

Consultez la page suivante pour plus d&#39;informations : [Cache de géométrie](../../features/geometry-cache/geometry-cache.md)

## Anticrénelage

Les boulangers peuvent utiliser le super échantillonnage pour effectuer l&#39;anticrénelage. Le suréchantillonnage signifie que les boulangers projetteront plus de rayons par pixel afin de lisser le résultat. Le temps de cuisson peut être considérablement affecté par ce paramètre ; cela est particulièrement vrai pour les boulangers où beaucoup de rayons sont nécessaires, comme l&#39;occlusion ambiante de la boulangerie de treillis.

À titre d’exemple :

* un réglage AA de 2x2 signifie que le boulanger projettera 4 fois la quantité initiale de rayons. Pour une texture 2048\*2048 px, le calcul obtenu équivaut à la cuisson d&#39;une texture 4096\*4096px et devrait prendre environ 4 fois plus de temps pour le calcul.
* un réglage AA de 8x8 signifie que le boulanger projette 64 fois la quantité initiale de rayons. Pour une texture 2048\*2048 px, le temps de calcul obtenu équivaut à la cuisson d’une texture 16384\*16384px et devrait prendre environ 64 fois plus de temps pour le calcul.

**En tenant compte de ces chiffres, le paramètre 8x8 doit être utilisé avec précaution**.

Afin de réduire la présence de bruit, il est généralement conseillé d&#39;augmenter le nombre de rayons secondaires (pour les boulangers d&#39;occlusion ambiante, de thickness et de normales courbées) et de conserver un réglage AA 2x2 ou 4x4 plutôt que d&#39;utiliser une faible quantité de rayons secondaires et un réglage AA élevé.

>[!NOTE]
>
> Un bon paramètre de performance/qualité pour l&#39;occlusion ambiante à partir du maillage est d&#39;utiliser AA 2x2 et au moins 128 rayons secondaires.

## Format de fichier

L’exportation de fichiers sur disque peut prendre beaucoup de temps en fonction du format de fichier, de la résolution, de la résolution et des paramètres de compression. Les paramètres de compression peuvent être modifiés dans les options Préférences / Projets / Général / Format de fichier. La désactivation de la compression peut réduire le temps d’exportation au sein de fichiers plus volumineux.

## Blocages et TDR

Les blocages peuvent être causés par plusieurs facteurs, l’un d’eux étant le TDR (Timeout Detection Recovery). Le TDR est un mécanisme Windows conçu pour détecter et récupérer des situations où le GPU ne semble pas répondre. En raison d’une valeur par défaut faible pour la détection du retard TDR, des blocages peuvent se produire lors de l’utilisation de boulangers spécifiques dans certaines situations :

* lors de la cuisson de maillages denses avec le boulanger d&#39;Occlusion Ambient
* lors de l&#39;utilisation des boulangers accélérés DXR avec des mailles très denses en poly (plus de 60 millions de triangles)

Vous trouverez des informations supplémentaires sur le TDR et un guide étape par étape sur la façon de modifier ses paramètres associés ici : [Les pilotes GPU se bloquent lors de longs calculs (plantage du TDR)](https://helpx.adobe.com/fr/substance-3d/unlisted/documentation/spdoc/gpu-drivers-crash-with-long-computations-128745489.html)
