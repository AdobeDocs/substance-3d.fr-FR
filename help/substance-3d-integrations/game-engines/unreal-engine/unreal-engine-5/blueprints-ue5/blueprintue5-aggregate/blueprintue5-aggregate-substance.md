---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-integrations/game-engines/unreal-engine/unreal-engine-5/blueprints-ue5/blueprintue5-aggregate-substance.html"
breadcrumb-title: ''
description: Combinez plusieurs matériaux de Substance lors de l’exécution dans Unreal Engine 5 à l’aide des nœuds d’agrégation Blueprint pour les workflows avancés.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unreal Engine > Unreal Engine 5 > Blueprints - UE5 > Blueprint(UE5) Aggregate Substance
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Blueprint(UE5) Aggregate Substance
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 0%

---


# Blueprint(UE5) : Substance globale

1. Utilisez le nœud Créer une fabrique de Substances d&#39;agrégat et définissez la fabrique de sortie et d&#39;entrée. La fabrique de sortie doit avoir une texture plaquée qui sera utilisée comme image d’entrée dans les paramètres de la fabrique d’entrée.
1. Créez des objets SubstanceConnection pour chaque texture de sortie utilisée comme entrée avec les noms des valeurs correspondantes (nom de la sortie dans le graphique de sortie et nom du paramètre d’entrée dans le graphique d’entrée)
1. Ajoutez un nœud Créer une instance de graphe et branchez le nœud Créer une fabrique de Substances agrégées dans l&#39;entrée Usine avec un matériau parent servant de modèle (il peut s&#39;agir de l&#39;un des matériaux par défaut\_substance inclus avec le module externe).
1. Créer une variable Instance de Graphe Substance et stocker le résultat du nœud précédent.
1. Facultatif : définissez les paramètres Substance souhaités (cet exemple montre comment définir une nouvelle résolution pour les sorties graphiques).
1. Créez un nœud de rendu Async ou Sync et connectez les instances à Render à la variable d’instance de Graphe Substance.
1. Utilisez la fonction « Obtenir une instance de matériau dynamique » à partir de l’instance de graphe pour créer ou obtenir une instance de matériau existante. Si vous laissez Nom et Dans matériau parent vides, les paramètres utilisés lors de la génération de l&#39;instance à l&#39;étape 3 seront utilisés.
1. Ajoutez un nœud Définir matière et définissez la valeur de la variable MID comme entrée matière. Pour la cible, définissez-la sur l’objet auquel vous souhaitez appliquer la matière.
