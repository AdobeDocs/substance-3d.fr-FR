---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-integrations/game-engines/unreal-engine/unreal-engine-5/blueprints-ue5/blueprintue5-dynamic-material-instance-skip-to-end-of-metadata.html"
breadcrumb-title: ''
description: Créez des instances de matériaux dynamiques à partir de matériaux de Substance lors de l’exécution dans Unreal Engine 5 à l’aide de Blueprints.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unreal Engine > Unreal Engine 5 > Blueprints - UE5 > Blueprint(UE5) Dynamic Material Instance Skip to end of metadata
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Blueprint(UE5) Dynamic Material Instance Passer à la fin des métadonnées
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '245'
ht-degree: 0%

---


# Blueprint(UE5) : instance de matériau dynamique Aller à la fin des métadonnées

1. Créez une variable de type Substance Instance Factory et définissez la valeur par défaut sur Imported Substance Factory.
1. Ajoutez un nœud Créer une instance de graphe et branchez l&#39;instance de Substance Factory dans l&#39;entrée Factory avec un matériau parent qui servira de modèle (il peut s&#39;agir de l&#39;un des matériaux par défaut\_substance inclus avec le plug-in).
1. Créez une autre variable pour stocker l’objet Instance de Graphe Substance créé à l’étape précédente.
1. Utilisez la fonction « Obtenir une instance de matériau dynamique » à partir de l’instance de graphe pour créer ou obtenir une instance de matériau existante. Si vous laissez Nom et Dans matériau parent vides, les paramètres utilisés lors de la génération de l&#39;instance à l&#39;étape 2 seront utilisés.
1. Créez une variable de type Matière. Il s&#39;agira de l&#39;instance de matériau dynamique (MID). Définissez la valeur renvoyée par « Get Dynamic Material Instance » sur la variable.

   ![](../../../../../assets/dynamic-material-annotated-1.png)
1. Ajoutez un nœud Définir matière et définissez la valeur de la variable MID comme entrée matière. Pour la cible, définissez-la sur l’objet auquel vous souhaitez appliquer la matière.
1. Facultatif : définissez les paramètres Substance souhaités (cet exemple utilise une instance de graphique Substance préexistante et copie les valeurs sur la nouvelle).
1. Créez un nœud de rendu Async ou Sync et connectez les instances à Render à la variable d’instance de Graphe Substance.
