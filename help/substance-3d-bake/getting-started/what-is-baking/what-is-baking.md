---
helpx_url: 'https://helpx.adobe.com/substance-3d-bake/getting-started/what-is-baking.html'
breadcrumb-title: ''
description: Découvrez ce qu’est le baking et apprenez à enregistrer des informations de Maillage 3D dans des fichiers de texture pour améliorer vos matériaux de Substance.
helpx_creative_field: ''
helpx_description: 'bakers > Getting Started > What is Baking '
helpx_experience_level: ''
helpx_learn_topic: ''
helpx_tags: ''
title: 'Qu’est-ce que le Baking ? '
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0a948aa65b787c0f84e0af681dbe74021e878687
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 0%

---


# Qu&#39;est-ce que le Baking ?

![](https://upload.wikimedia.org/wikipedia/commons/3/36/Normal_map_example.png)

(Crédits : [Paolo Cignoni](https://commons.wikimedia.org/wiki/File:Normal_map_example.png) - [CC BY-SA 1.0](https://creativecommons.org/licenses/by-sa/1.0))

Baker est le nom du processus concernant l&#39;**enregistrement d&#39;informations** relatives à un **Maillage 3D** dans un fichier de **texture** ([bitmap](https://en.wikipedia.org/wiki/Raster_graphics)). La plupart du temps, ce processus implique un autre maillage. Dans ce cas, les informations du premier maillage sont transférées sur le deuxième maillage UVs puis sauvegardées dans une texture.

Bien que certaines applications puissent prendre en charge les informations de baking dans les propriétés du maillage (telles que les couleurs du vertex), Substance Bakers permet uniquement de baker les informations jusqu’à une texture. Cependant, ils peuvent lire les propriétés du maillage et les baker en textures (comme les couleurs du vertex).

## Le baking est-il nécessaire ?

Les logiciels de Substance génèrent des textures qui peuvent être améliorées en utilisant des informations relatives à la géométrie du maillage.\
De nombreux filtres et matériaux peuvent s’adapter à la géométrie spécifique d’un Maillage 3D en observant les textures bakées. Le Baking peut fournir des informations sur les ombres ambiantes, les contours de la géométrie, etc.

Par exemple : une vieille voiture peut avoir une rouille appliquée en bas parce qu&#39;elle n&#39;a pas bougé pendant un certain temps. Baker la carte de position permettra de savoir où se trouve le fond sur le maillage qui alimentera le générateur de rouille et produira la texture adaptée.

![](../../assets/examples.jpg){width="500px"}

## Comment fonctionne le baking ?

Chaque baker effectue des actions spécifiques afin de générer son propre baking, mais en général le processus de traitement implique deux méthodes possibles :

* **Baker sur un seul maillage** : s&#39;appuie sur le maillage actif pour générer des informations.
* **Baking d&#39;un maillage à un autre** : calcul des informations d&#39;un maillage source et transfert du résultat à un autre.

Ce processus de baking repose sur les propriétés du maillage, c&#39;est pourquoi le maillage doit être propre et exempt de tout défaut possible dans sa géométrie.

## Quel type d&#39;information pouvez-vous baker ?

De nombreux types d&#39;informations peuvent être bakés. Cependant, en général, seul un ensemble spécifique est nécessaire, car ils peuvent être extrapolés pour créer un résultat plus avancé ultérieurement. C&#39;est pourquoi il existe un type commun de processus de baking qui peut être trouvé dans plusieurs logiciels.

A titre d&#39;exemple, un logiciel de Substance peut générer les informations suivantes :

* **Ambient occlusion** (ombres ambiantes)
* Informations sur la **normale** (variations des détails de surface stockées sous forme de directions vectorielles)
* **Direction** (haut ou bas, gauche ou droite, etc.)
* **Courbure** (arêtes et cavités de la géométrie)
* **Position** (position relative de la géométrie dans un cube normalisé)

Reportez-vous à la [documentation de chaque baker](../../bakers-settings/bakers-settings.md) pour plus d&#39;informations.

## Différence entre « normal » et « provenant des Bakers du maillage »

Selon le processus, les bakers utilisent différentes implémentations. En règle générale, les bakers **de maillage** s&#39;appuient sur des techniques de raytracing pour extraire et projeter des données d&#39;un modèle à l&#39;autre.
