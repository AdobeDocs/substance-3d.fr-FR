---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-integrations/3d-applications/blender/the-substance-3d-panel.html"
breadcrumb-title: ''
description: Découvrez comment utiliser le panneau Substance 3D dans Blender pour gérer les matériaux, les paramètres et les sorties.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > Blender > The Substance 3D Panel
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Panneau Substance 3D
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4a060ee1aaa1731c04e70d5512e3271cd63d0381
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 0%

---


# Panneau Substance 3D

![](../../../assets/blender-substance3dpanel.png)

## Commandes du panneau

**Créer** : ouvre l&#39;explorateur de fichiers pour sélectionner un matériau Substance 3D. Par défaut, un matériau mélangeur est créé à l’aide des textures générées à partir du fichier .fichier sbsar.

**Appliquer** : associez le matériau Substance 3D sélectionné aux objets sélectionnés dans un nouvel emplacement de matériau. Cela ne remplace pas les affectations de matériau précédentes sur l’objet.

**Ressources des communautés Substance 3D** : ouvre la page Ressources des communautés Substance 3D dans le navigateur web.

**Substance 3D Assets** : ouvre la page source Substance 3D Assets dans le navigateur web.

**Dupliquer le Matériau Substance 3D sélectionné** : chargez une nouvelle instance du matériau Substance 3D sélectionné. Les paramètres de différentes instances d&#39;un même matériau de Substance peuvent être ajustés indépendamment les uns des autres.

**Actualiser** : recharge le matériau Substance 3D

>[!WARNING]
>
> **Avertissement :**
> 
> L’utilisation du bouton Actualiser annule toutes les modifications apportées par l’utilisateur au graphe shader. Copiez tous les nœuds ajoutés par l’utilisateur avant l’actualisation pour les coller dans le graphe après l’actualisation.

**Supprimer** : supprime le matériau Substance 3D sélectionné du panneau.

>[!NOTE]
>
> Le matériau mélangeur créé à partir du matériau Substance restera dans le projet. Il peut être supprimé ou retiré manuellement d’objets.

**Matériaux de Substance 3D chargés** : affiche une liste des Matériaux de Substance qui ont été chargés dans le fichier .blend.

## Paramètres de graphe

**Résolution de sortie** : listes déroulantes pour la résolution avec et height. Vous pouvez dissocier ces éléments pour ajuster les valeurs indépendamment.

**Aléatoire et générateur aléatoire** : le bouton Aléatoire génère une nouvelle valeur de générateur aléatoire pour modifier les paramètres qui peuvent utiliser des valeurs aléatoires. Le générateur aléatoire peut également être défini manuellement.

## Utilisation des paramètres prédéfinis

Les fichiers SBSAR peuvent être publiés avec des paramètres prédéfinis, qui se trouvent dans la liste déroulante des paramètres prédéfinis. Pour créer vos propres paramètres prédéfinis, ajustez les paramètres comme vous le souhaitez et utilisez le bouton **Enregistrer**. Des options supplémentaires permettent d’exporter le paramètre prédéfini sélectionné dans un fichier .sbsprs et de supprimer le paramètre prédéfini sélectionné de la liste déroulante. Le bouton **Charger** peut être utilisé pour importer des paramètres prédéfinis à partir de fichiers .sbsprs.

## Paramètres de Substance

Les paramètres exposés dans la Substance Designer peuvent être ajustés à l&#39;aide des commandes Paramètre de Substance. Ces paramètres sont définis par le créateur du Matériau Substances et varient d’un matériau à l’autre. Le réglage de ces paramètres met à jour les textures générées, comme indiqué par l’icône de traitement en regard du nom du matériau dans la section Matériaux de Substance 3D chargés.

Le format de fichier des textures de sortie peut être changé via les listes déroulantes.

Pour plus d&#39;informations, voir [Exposer un paramètre](https://experienceleague.adobe.com/fr/docs/substance-3d-designer/using/substance-graphs/manage-parameters/exposing-a-parameter) sur la page de documentation Designer.

## Paramètres techniques

Les Matériaux de Substance peuvent avoir un ensemble de paramètres techniques. Il s’agit de commandes supplémentaires pour la correction colorimétrique et d’autres réglages de matériau.
