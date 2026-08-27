---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/getting-started/what-is-baking.html"
breadcrumb-title: ''
description: Découvrez ce qu’est la cuisson et apprenez à enregistrer des informations de filet 3D dans des fichiers de texture pour améliorer vos matériaux de Substance.
helpx_creative_field: ""
helpx_description: "bakers > Getting Started > What is Baking "
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 'Qu''est-ce que la cuisson ? '
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4ba3396472c767b16a67daa489105093a6a20871
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 0%

---


# Qu&#39;est-ce que la cuisson ?

![](https://upload.wikimedia.org/wikipedia/commons/3/36/Normal_map_example.png)

&#x200B;>> 

(Crédits : [Paolo Cignoni](https://commons.wikimedia.org/wiki/File:Normal_map_example.png) - [CC BY-SA 1.0](https://creativecommons.org/licenses/by-sa/1.0))

La cuisson est le nom du processus d&#39;**enregistrement d&#39;informations** liées à un **filet 3D** dans un fichier de **texture** ([bitmap](https://en.wikipedia.org/wiki/Raster_graphics)). La plupart du temps, ce processus implique un autre maillage. Dans ce cas, les informations du premier maillage sont transférées sur les seconds UV de maillage puis sauvegardées dans une texture.

Bien que certaines applications puissent prendre en charge l’intégration d’informations d’ancrage dans les propriétés du filet (telles que les couleurs des sommets), Substance Bakers permet uniquement d’ancrer les informations jusqu’à une texture. Cependant, ils peuvent lire les propriétés du filet et les réduire à des textures (comme les couleurs des sommets).

## La cuisson est-elle nécessaire ?

Les logiciels de Substance génèrent des textures qui peuvent être améliorées à l&#39;aide des informations relatives à la géométrie du maillage.\
De nombreux filtres et matières peuvent s’adapter à la géométrie spécifique d’un filet 3D en examinant les textures cuites. La cuisson peut fournir des informations sur l&#39;emplacement possible des ombres ambiantes, des bords de la géométrie, etc.

Par exemple : une vieille voiture peut avoir une rouille appliquée en bas parce qu&#39;elle n&#39;a pas bougé pendant un certain temps. La cuisson de la carte de position permettra de savoir où se trouve le fond sur le maillage qui alimentera le générateur de rouille et produira la texture adaptée.

![](../../assets/examples.jpg){width="500px"}

## Comment la cuisson fonctionne-t-elle ?

Chaque boulanger effectue des actions spécifiques afin de générer son propre résultat, mais en général le processus de boulangerie implique deux méthodes possibles :

* **Baking sur un maillage** : repose sur le maillage actuel pour générer des informations.
* **Baking d&#39;un maillage à un autre** : calculez les informations à partir d&#39;un maillage source et transférez le résultat sur un autre.

Ce processus de cuisson repose sur les propriétés du maillage, c&#39;est pourquoi le maillage doit être propre et exempt de tout défaut possible dans sa géométrie.

## Quel type d’informations pouvez-vous créer ?

De nombreux types d&#39;informations peuvent être bake. Cependant, en général, seul un ensemble spécifique est nécessaire, car ils peuvent être extrapolés pour créer un résultat plus avancé ultérieurement. C&#39;est pourquoi il existe des types courants de processus de bake qui peuvent être trouvés dans plusieurs logiciels.

A titre d&#39;exemple, un logiciel de Substance peut générer les informations suivantes :

* **Ambient occlusion** (ombres ambiantes)
* Informations sur la **normale** (variations des détails de surface stockées sous forme de directions vectorielles)
* **Direction** (haut ou bas, gauche ou droite, etc.)
* **Courbure** (arêtes et cavités de la géométrie)
* **Position** (position relative de la géométrie dans un cube normalisé)

Reportez-vous à la [documentation de chaque baker](../../bakers-settings/bakers-settings.md) pour plus d&#39;informations.

## Différence entre « normal » et « provenant des Bakers du maillage »

Selon le processus, les bakers utilisent différentes implémentations. En règle générale, les bakers **de maillage** s&#39;appuient sur des techniques de raytracing pour extraire et projeter des données d&#39;un modèle à l&#39;autre.
