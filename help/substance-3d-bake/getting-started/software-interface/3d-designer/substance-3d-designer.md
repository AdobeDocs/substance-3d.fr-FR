---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/getting-started/software-interface/substance-3d-designer.html"
breadcrumb-title: ''
description: Découvrez comment accéder à la fenêtre de cuisson dans Substance 3D Designer et l’utiliser pour transformer les informations de modèle en textures.
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

La fenêtre de cuisson est accessible à partir du fichier de maillage dans la fenêtre [Explorateur](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/the-explorer-129368147.html). Cliquez avec le bouton droit de la souris sur le nom du maillage et choisissez « **Informations sur le modèle de cuisson** » pour ouvrir la fenêtre de cuisson.

## Vue d’ensemble

![](../../../assets/sd-window-overview.png){width="500px"}

La fenêtre de cuisson de est divisée en plusieurs panneaux qui sont décrits ci-dessous.

### Élément à cuire

![](../../../assets/sd-mesh-selection.png)

Ce panneau contrôle la partie du maillage low-poly qui sera utilisée pour effectuer la cuisson.

Ce panneau répertorie la géométrie présente dans le fichier de maillage low-poly. Par défaut, la liste est basée sur les différents matériaux trouvés dans le fichier, mais elle peut être changée en sous-maillages si nécessaire. Vous pouvez décocher les éléments qui doivent être ignorés pendant le processus de cuisson.

### Sortie

![](../../../assets/sd-output.png)

Ce panneau contrôle l’emplacement de la texture cuite.

| *Paramètre* | *Description* |
| --- | --- |
| **Méthode** | Contrôle la façon dont les textures cuites seront stockées avec l&#39;emballage Substance.Valeurs possibles :<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Incorporé</strong> : la texture cuite est stockée dans un sous-dossier à côté du package Substance avec un nom spécifique.</li><li data-preserve-html="true"><strong>Lié</strong> (par défaut) : la texture cuite est stockée dans le dossier défini, puis référencée dans le package Substance .</li></ul> |
| **Dossier** | Emplacement des textures cuites lors de l’enregistrement. Cliquez sur le bouton des trois petits points pour ouvrir une boîte de dialogue de fichier et choisir le dossier d&#39;exportation. Une coche apparaît à droite pour indiquer si le dossier existe réellement ou non. |
| **Nom** | Convention d’affectation des noms des textures cuites. Cliquez sur le bouton des trois petits points pour ouvrir une liste déroulante et insérer d’autres espaces réservés (nom de fichier, personnalisé, matériau, maillage). |
| **Exemple** | Simulez un nom de fichier pour tester la convention d’affectation des noms. |
| **Placer la ressource dans un dossier spécifique au maillage** | Si cette option est activée, les textures ancrées sont enregistrées dans un dossier nommé fichier de maillage. |

### Maillages haute définition

![](../../../assets/sd-high.png)

Ce panneau contrôle la liste des maillages à polyvalence élevée et les paramètres associés. Pour plus d’informations](../../../bakers-settings/common-parameters/common-parameters.md) voir les [paramètres communs.

### Valeurs par défaut

![](../../../assets/sd-default-values.png)

Pour plus d’informations](../../../bakers-settings/common-parameters/common-parameters.md) voir les [paramètres communs.

### Liste et paramètres Baker

![](../../../assets/sd-baker-list.png)

Le boulanger est l&#39;endroit où vous pouvez choisir la texture de cuisson que vous voulez générer. Par défaut, la liste est vide.

* **Ajouter un nouveau boulanger :** Cliquez sur le bouton « Ajouter un boulanger ».
* **Retrait d&#39;un boulanger :** Sélectionnez le boulanger dans la liste, puis cliquez sur le bouton « Supprimer le boulanger ».
* **Déplacer un boulanger en haut :** Sélectionnez le boulanger dans la liste, puis cliquez sur le bouton « Tirer en haut ».
* **Déplacer vers le bas d&#39;un boulanger :**Sélectionnez le boulanger dans la liste, puis cliquez sur le bouton « Push down ».

Chaque boulanger dans le hérite par défaut des valeurs par défaut (voir ci-dessus). La taille (résolution) peut par exemple être remplacée en cliquant sur la cellule sur la ligne du boulanger. C&#39;est vrai pour les autres paramètres de la ligne.

Lorsque vous cliquez sur un boulanger dans la liste, la vue Paramètres Baker est mise à jour avec ses paramètres spécifiques.

Pour en savoir plus sur les paramètres spécifiques, voir : [Bakers Settings](../../../bakers-settings/bakers-settings.md).
