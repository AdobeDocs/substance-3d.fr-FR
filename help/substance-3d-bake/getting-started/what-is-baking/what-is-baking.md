---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/getting-started/what-is-baking.html"
breadcrumb-title: ''
description: Découvrez ce qu'est la cuisson et apprenez à enregistrer des informations de maillage 3D dans des fichiers de texture pour améliorer vos matériaux Substance.
helpx_creative_field: ""
helpx_description: "bakers > Getting Started > What is Baking "
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 'Qu’est-ce que la cuisson ? '
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4ba3396472c767b16a67daa489105093a6a20871
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 0%

---


# Qu&#39;est-ce que la cuisson ?

![](https://upload.wikimedia.org/wikipedia/commons/3/36/Normal_map_example.png)

>> 

(Crédits : [Paolo Cignoni](https://commons.wikimedia.org/wiki/File:Normal_map_example.png) - [CC BY-SA 1.0](https://creativecommons.org/licenses/by-sa/1.0))

La cuisson est le nom du processus d’**enregistrement d’informations** liées à un maillage **3D** dans un fichier **texture** ([bitmap](https://en.wikipedia.org/wiki/Raster_graphics)). La plupart du temps, ce processus implique un autre maillage. Dans ce cas, les informations du premier maillage sont transférées sur les deuxièmes UV de maillage puis sauvegardées dans une texture.

Bien que certaines applications puissent prendre en charge l’intégration d’informations dans les propriétés du maillage (telles que les couleurs de sommet), Substance Bakers permet uniquement d’intégrer des informations dans une texture. Toutefois, ils peuvent lire les propriétés du maillage et les transformer en textures (comme les couleurs de sommet).

## La cuisson est-elle nécessaire ?

Les logiciels de substance génèrent des textures qui peuvent être améliorées en utilisant des informations relatives à la géométrie du maillage.\
De nombreux filtres et matériaux peuvent s&#39;adapter à la géométrie spécifique d&#39;un maillage 3D en observant les textures cuites. La cuisson peut fournir des informations sur l&#39;emplacement des ombres ambiantes, les arêtes de la géométrie, etc.

Par exemple : une vieille voiture peut avoir de la rouille appliquée à son bas parce qu&#39;elle n&#39;a pas bougé pendant un certain temps. La réalisation de la carte de position permettra de savoir où se trouve le fond sur le maillage qui alimentera le générateur de rouille et produira la texture adaptée.

![](../../assets/examples.jpg){width="500px"}

## Comment la cuisson fonctionne-t-elle ?

Chaque boulanger effectue des actions spécifiques afin de générer son propre résultat, mais en général le processus de cuisson implique deux méthodes possibles :

* **Ancrage sur un maillage** : repose sur le maillage actuel pour générer des informations.
* **Cuisson d&#39;un maillage à un autre** : calculez les informations d&#39;un maillage source et transférez le résultat sur un autre.

Ce processus de cuisson repose sur les propriétés du maillage, c&#39;est pourquoi le maillage doit être propre et exempt de toute faille possible dans sa géométrie.

## Quel type d’informations pouvez-vous créer ?

De nombreux types d’informations peuvent être regroupés. Cependant, en général, seul un ensemble spécifique est nécessaire, car ils peuvent être extrapolés pour créer des résultats plus avancés ultérieurement. C&#39;est pourquoi il existe un type commun de processus de cuisson qui peut être trouvé dans plusieurs logiciels.

À titre d’exemple, un logiciel Substance peut générer le type d’informations suivant :

* **Occlusion ambiante** (ombres ambiantes)
* **Normale** informations (variations de détails de surface stockées sous forme de directions vectorielles)
* **Direction** (où est vers le haut ou vers le bas, vers la gauche ou la droite, etc.)
* **Courbure** (arêtes et cavités de la géométrie)
* **Position** (position relative de la géométrie dans un cube normalisé)

Pour plus d’informations, reportez-vous à la [documentation de chaque boulanger](../../bakers-settings/bakers-settings.md).

## Différence entre « standard » et « from mesh » Bakers

En fonction du processus, les boulangers utilisent diverses implémentations. De manière générale, les boulangers **à partir de mailles** s&#39;appuient sur des techniques de lancer de rayons pour extraire et projeter des données d&#39;un modèle à un autre.
