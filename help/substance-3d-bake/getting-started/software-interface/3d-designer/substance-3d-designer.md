---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/getting-started/software-interface/substance-3d-designer.html"
breadcrumb-title: ''
description: Découvrez comment accéder à la fenêtre de baking de Substance 3D Designer et l’utiliser pour baker des informations sur le mannequin dans des textures.
helpx_creative_field: ""
helpx_description: bakers > Getting Started > Software Interface > Substance 3D Designer
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Substance 3D Designer
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '496'
ht-degree: 2%

---


# Substance 3D Designer

![](../../../assets/sd-mesh-right-click.png)

La fenêtre de baking est accessible via le fichier de maillage dans la fenêtre [Explorateur](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/the-explorer-129368147.html). Cliquez avec le bouton droit de la souris sur le nom du maillage et sélectionnez « **Informations sur le modèle Baker** » pour  la fenêtre de baking.

## Vue d’ensemble

![](../../../assets/sd-window-overview.png){width="500px"}

La fenêtre de baking de est divisée en plusieurs panneaux qui sont décrits ci-dessous.

### Élément à Baker

![](../../../assets/sd-mesh-selection.png)

Ce panneau contrôle la partie du maillage à faible poly qui sera utilisée pour effectuer le baking.

Ce panneau répertorie la géométrie du fichier de maillage low-poly. Par défaut, la liste est basée sur les matériaux individuels trouvés dans le fichier, mais elle peut être basculée vers des sous-maillages à la place, le cas échéant. Vous pouvez décocher les éléments qui doivent être ignorés pendant le processus de baking.

### Sortie

![](../../../assets/sd-output.png)

Ce panneau contrôle l’emplacement de la texture bakée.

| *Paramètre* | *Description* |
| --- | --- |
| **Méthode** | Contrôle la façon dont les textures bakées seront stockées avec le package de Substance.Valeurs possibles :<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Incorporé</strong> : les textures bakées sont stockées dans un sous-dossier en regard du package de Substances avec un nom spécifique.</li><li data-preserve-html="true"><strong>Lié</strong> (par défaut) : les textures bakées sont stockées dans le dossier défini, puis référencées dans le package de Substances.</li></ul> |
| **Dossier** | Emplacement des textures bakées lors de l’enregistrement. Cliquez sur le bouton à trois points pour ouvrir une boîte de dialogue de fichier et choisissez le dossier d’exportation. Une coche sera visible à droite pour indiquer si le dossier existe réellement ou non. |
| **Nom** | Convention de dénomination des textures bakées. Cliquez sur les trois points pour ouvrir une liste déroulante et insérer d’autres espaces réservés (nom de pain, personnalisé, matériau, maillage). |
| **Exemple** | Simuler un nom de fichier pour tester la convention de dénomination. |
| **Placer la ressource dans un dossier spécifique au Maillage** | Si cette option est activée, les textures bakées sont enregistrées dans un dossier nommé par fichier de maillage. |

### Maillages haute définition

![](../../../assets/sd-high.png)

Ce panneau contrôle la liste des maillages à haut niveau de concurrence et les paramètres associés. Voir les [paramètres communs](../../../bakers-settings/common-parameters/common-parameters.md) pour plus d&#39;informations.

### Valeurs par défaut

![](../../../assets/sd-default-values.png)

Voir les [paramètres communs](../../../bakers-settings/common-parameters/common-parameters.md) pour plus d&#39;informations.

### Liste de bakers et paramètres

![](../../../assets/sd-baker-list.png)

Par baker, vous pouvez choisir la texture bakée que vous souhaitez générer. Par défaut, la liste est vide.

* **Ajout d&#39;un nouveau baker :** Cliquez sur le bouton « Ajouter un Baker ».
* **Suppression d&#39;un baker :** sélectionnez le baker dans la liste, puis cliquez sur le bouton « Supprimer le baker ».
* **Déplacement d&#39;un baker vers le haut :** sélectionnez le baker dans la liste, puis cliquez sur le bouton « Déplacer vers le haut ».
* **Descente d&#39;un baker :**Sélectionnez le baker dans la liste, puis cliquez sur le bouton « Push down ».

Par défaut, chaque baker hérite des valeurs par défaut (voir ci-dessus). La taille (résolution) peut par exemple être remplacée en cliquant sur la cellule sur la ligne du baker. Cela est vrai pour les autres paramètres de la ligne.

Lorsque vous cliquez sur un baker dans la liste, la vue Paramètres de Baker est mise à jour avec ses paramètres spécifiques.

Pour en savoir plus sur les paramètres spécifiques, voir : [Paramètres de Bakers](../../../bakers-settings/bakers-settings.md).
