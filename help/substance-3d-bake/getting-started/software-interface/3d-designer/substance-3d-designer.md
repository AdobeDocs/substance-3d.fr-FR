---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-bake/getting-started/software-interface/substance-3d-designer.html"
breadcrumb-title: ''
description: Apprenez à transformer des informations de mannequin en textures à l’aide de la fenêtre de création de baking de Substance 3D Designer.
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

La fenêtre de cuisson est accessible via le fichier de maillage dans la fenêtre [Explorateur](https://helpx.adobe.com/fr/substance-3d/unlisted/documentation/sddoc/the-explorer-129368147.html). Cliquez avec le bouton droit de la souris sur le nom du maillage et sélectionnez « **Informations sur le modèle de cuisson** » pour ouvrir la fenêtre de cuisson.

## Vue d’ensemble

![](../../../assets/sd-window-overview.png){width="500px"}

La fenêtre de cuisson de est divisée en plusieurs panneaux qui sont décrits ci-dessous.

### Elément à cuire

![](../../../assets/sd-mesh-selection.png)

Ce panneau contrôle la partie du maillage en bas-poly qui sera utilisée pour effectuer la cuisson.

Ce panneau répertorie la géométrie trouvée dans le fichier de maillage low-poly. Par défaut, la liste est basée sur les matériaux individuels trouvés dans le fichier, mais elle peut être commutée en sous-maillages à la place lorsque cela est pertinent. Vous pouvez décocher les éléments qui doivent être ignorés pendant le processus de cuisson.

### Sortie

![](../../../assets/sd-output.png)

Ce panneau contrôle l’emplacement de la texture cuite.

| *Paramètre* | *Description* |
| --- | --- |
| **Méthode** | Contrôle la façon dont les textures cuites seront stockées avec le package de Substance.Valeurs possibles :<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Incorporé</strong> : la texture cuite est stockée dans un sous-dossier en regard du package de Substance avec un nom spécifique.</li><li data-preserve-html="true"><strong>Lié</strong> (par défaut) : la texture cuite est stockée dans le dossier défini, puis référencée dans le pack de Substances.</li></ul> |
| **Dossier** | Emplacement des textures cuites lors de l’enregistrement. Cliquez sur le bouton à trois points pour ouvrir une boîte de dialogue de fichier et choisissez le dossier d’exportation. Une coche sera visible à droite pour indiquer si le dossier existe réellement ou non. |
| **Nom** | Convention de dénomination des textures cuites. Cliquez sur le bouton à trois points pour ouvrir une liste déroulante et insérer d’autres espaces réservés (nom de pain, personnalisé, matière, filet). |
| **Exemple** | Simuler un nom de fichier pour tester la convention de dénomination. |
| **Placer la ressource dans un dossier spécifique au maillage** | Si cette option est activée, les textures cuites sont enregistrées dans un dossier nommé fichier de filet. |

### Maillages haute définition

![](../../../assets/sd-high.png)

Ce panneau contrôle la liste des maillages à haute densité de polices et les paramètres associés. Voir les [paramètres communs](../../../bakers-settings/common-parameters/common-parameters.md) pour plus d&#39;informations.

### Valeurs par défaut

![](../../../assets/sd-default-values.png)

Voir les [paramètres communs](../../../bakers-settings/common-parameters/common-parameters.md) pour plus d&#39;informations.

### Baker List and Settings

![](../../../assets/sd-baker-list.png)

Le boulanger est l’endroit où vous pouvez choisir la texture cuite que vous souhaitez générer. Par défaut, la liste est vide.

* **Ajout d&#39;un nouveau boulanger :** Cliquez sur le bouton « Ajouter un boulanger ».
* **Suppression d&#39;un boulanger :** sélectionnez le boulanger dans la liste, puis cliquez sur le bouton « Supprimer le boulanger ».
* **Placement d&#39;un boulanger en haut :** sélectionnez le boulanger dans la liste, puis cliquez sur le bouton « Placer en haut ».
* **Descendre un boulanger :**&#x200B;Sélectionnez le boulanger dans la liste, puis cliquez sur le bouton « Push down ».

Chaque boulanger hérite par défaut des valeurs par défaut (voir ci-dessus). La taille (résolution) peut par exemple être remplacée en cliquant sur la cellule sur la ligne du boulanger. Cela est vrai pour les autres paramètres de la ligne.

Lorsque vous cliquez sur un boulanger dans la liste, la vue Baker Parameters est mise à jour avec ses paramètres spécifiques.

Pour en savoir plus sur les paramètres spécifiques, voir : [Paramètres Bakers](../../../bakers-settings/bakers-settings.md).
