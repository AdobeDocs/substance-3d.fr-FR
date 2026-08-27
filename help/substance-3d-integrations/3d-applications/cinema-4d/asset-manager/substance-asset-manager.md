---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/3d-applications/cinema-4d/substance-asset-manager.html"
breadcrumb-title: ''
description: Utilisez le Gestionnaire d’actifs de Substance de données dans Cinema 4D pour ajouter, supprimer et organiser des matériaux de Substance de données dans votre scène.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > Cinema 4D > Substance Asset Manager
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Gestionnaire d’actifs de Substance
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '651'
ht-degree: 0%

---


# Gestionnaire d’actifs de Substance

La fenêtre Gestionnaire d&#39;actifs de Substance répertorie toutes les Substances chargées dans une scène. Vous pouvez y ajouter, supprimer et réorganiser des Substances.

La sélection (clic gauche) d’une Substance dans le Gestionnaire d’actifs de Substance ouvre la Substance dans le Gestionnaire d’attributs de Cinema 4D. Vous pouvez y modifier les paramètres et les entrées de Substance des images clés comme tout autre paramètre dans Cinema 4D.

>[!NOTE]
>
> Le Gestionnaire d’attributs dispose d’un mode Substance/actif spécial, pratique pour disposer d’un Gestionnaire d’attributs dédié aux Substances dans votre mise en page de Cinema 4D.

![](../../../assets/cinema-4d-4.png){width="500px"}

## Menu Fichier

## Charger la ressource...

Chargez une nouvelle Substance dans la scène (comme dans le menu Plug-ins ).

Fermer

Ferme le Gestionnaire d&#39;actifs de Substance. Les Substances chargées resteront bien sûr dans la scène.

## Menu Modifier

## Sélectionner toutes les Substances

Sélectionne toutes les Substances répertoriées dans le Gestionnaire d’actifs. Il est possible d’obtenir le même résultat en appuyant sur Ctrl+a, pendant que la souris survole le Gestionnaire d’actifs.

## Désélectionner toutes les Substances

Désélectionne toutes les Substances répertoriées dans Asset Manager. Il est possible d’obtenir le même résultat en appuyant sur les touches Maj+Ctrl+a, pendant que la souris survole le Gestionnaire d’actifs.

## Sélectionner à partir du ou des Matériaux sélectionnés

Sélectionne toutes les Substances référencées par les matériaux actuellement *sélectionnés*.

## Sélectionner parmi les Matériaux marqués

Sélectionne toutes les Substances référencées par les matériaux *marqués* actuels. Dans Cinema 4D, un matériau est marqué si un objet ou une balise utilisant ce matériau est sélectionné.

## Sélectionner un ou plusieurs Matériaux

Sélectionne tous les matériaux qui font référence aux Substances actuellement sélectionnées.

## Menu Actions

## Créer un ou plusieurs Matériaux

Créez de nouveaux Cinema 4D à partir des Substances actuellement sélectionnées. Les canaux de matériau seront automatiquement initialisés avec des shaders de Substance se référant aux canaux de sortie respectifs des Substances.

## Substance(s) en double

Dupliquez les Substances actuellement sélectionnées. Cela peut être utile pour utiliser la même Substance avec différents jeux de paramètres sur plusieurs matériaux.

## Réimporter la ou les Substances

Cette fonction peut être utilisée pour revenir aux valeurs par défaut d&#39;une Substance ou pour intégrer des modifications externes (par exemple, à partir de la Substance Designer).\
Remarque : **Toutes les modifications de paramètre** sur les entrées de Substance seront perdues.

## Supprimer la ou les Substances

Supprime les Substances actuellement sélectionnées de la scène. Il est possible d’obtenir le même résultat en appuyant sur la touche Suppr lorsque la souris survole le Gestionnaire d’actifs.

## Supprimer les Substances inutilisées

Supprime toutes les Substances actuellement non référencées par un matériau.

## menu Substance Engine

Le contenu de ce menu dépend du système d’exploitation sur lequel le Cinema 4D est exécuté. La modification de la Substance Engine ne prendra effet qu’après un redémarrage de la Cinema 4D.

## Menu contextuel

En cliquant avec le bouton droit de la souris sur une Substance sélectionnée, le menu contextuel s’affiche. Leur fonctionnalité est identique aux fonctions portant le même nom dans les menus susmentionnés :

* Supprimer
* Créer un ou plusieurs Matériaux
* Dupliquer la Substance
* Substance de réimportation
* Sélectionner toutes les Substances
* Désélectionner toutes les Substances
* Sélectionner une ou plusieurs matières

## Glisser-déposer

Vous pouvez interagir avec le Gestionnaire d’actifs de Substance de données par glisser-déposer. Plusieurs options sont disponibles :

* Chargez des Substances dans la scène par glisser-déposer à partir de l’Explorateur ou du Finder en les déposant simplement sur le Gestionnaire d’actifs de Substance.
* Vous pouvez faire glisser des Substances dans le champ de lien des shaders de Substance pour connecter un shader et un actif de Substance.
* Si vous êtes en mode Non trié (voir ci-dessous), vous pouvez réorganiser les Substances dans le Gestionnaire d’actifs en les faisant glisser vers un nouvel emplacement.


## Tri dans Substance Asset Manager

## Mode non trié

## Le Gestionnaire d&#39;actifs de Substance de données est en **mode non trié par défaut**. La cellule d’en-tête de la colonne Nom n’affiche pas de flèche à droite. Vous pouvez utiliser le glisser-déposer pour réorganiser les substances à votre convenance.

![](../../../assets/cinema-4d-3.png){width="500px"}

![](../../../assets/cinema-4d-5.png){width="500px"}

## Aperçus dans Substance Asset Manager

## Substance Asset Manager affiche de petites icônes avec des aperçus des canaux disponibles pour chaque Substance.

## Les aperçus s’affichent simplement dans l’ordre des canaux de sortie dans la Substance. La colonne dans laquelle un aperçu est affiché n’a aucune signification.
