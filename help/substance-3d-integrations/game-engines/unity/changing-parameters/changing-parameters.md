---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-integrations/game-engines/unity/changing-parameters.html"
breadcrumb-title: ''
description: Modifiez les paramètres du matériau de Substance dans Unity pour personnaliser l’apparence et les propriétés du matériau lors de l’exécution.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unity > Changing parameters
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Modification des paramètres
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 0%

---


# Modification des paramètres

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

Les paramètres du matériau de Substance sont accessibles sur l’objet de Graphe Substance (SGO).

1. Dans la fenêtre Projet, sélectionnez le logo du fichier sbsar correspondant au graphique à personnaliser. Le sbsar a le logo vert « SBSAR ».

   ![](../../../assets/screen-shot-2022-03-29-at-2-27-56-pm.png)

## Propriétés procédurales

1. **Générer toutes les sorties** : génère toutes les sorties du fichier sbsar de la Substance de données. Par défaut, seules les sorties utilisées par les shaders standard sont créées.
1. **Générer des mappages MIP** : génère des textures MIP pour chaque sortie de Substance.
1. **Générateur aléatoire** : ce bouton modifie la génératrice aléatoire utilisée par le graphique de Substance pour générer les textures. La modification de cette valeur crée un nouveau résultat pour la texture calculée en fonction de la valeur de départ.
1. Les paramètres exposés dans le fichier de Substance sont disponibles dans Unity. Le contrôle Editor est basé sur le type de paramètre qui a été créé pour la Substance.
1. **Gestion des paramètres prédéfinis :** vous pouvez exporter ou importer des fichiers de paramètres prédéfinis de Substance de données (sbsars). L’exportation d’un paramètre prédéfini entraîne la création d’un fichier de paramètre prédéfini en fonction des paramètres de la Substance. Vous pouvez exporter des fichiers de paramètres prédéfinis à partir de Substance Designer et Substance Player, qui peuvent ensuite être importés à l’aide du bouton Importer les paramètres prédéfinis. Cela permet de partager des paramètres prédéfinis de Substance entre applications et équipes.

</td>
<td style="border: 0;" valign="top">

![](../../../assets/changing-parameters.png)

</td>
</tr>
</table>
