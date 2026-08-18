---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/3d-applications/maya/using-workflows.html"
breadcrumb-title: ''
description: Créez et utilisez des paramètres prédéfinis de rendu pour les sorties de Substance dans Maya afin de générer automatiquement des réseaux de nuanceurs pour différents systèmes de rendu.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > Maya > Using Workflows
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Utilisation des workflows
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '250'
ht-degree: 0%

---


# Utilisation des workflows

Sous Workflows, vous pouvez choisir ou créer des paramètres prédéfinis de rendu pour les sorties de Substance. Ces paramètres prédéfinis sont des réseaux de nuanceurs pour un moteur de rendu tel qu’Arnold ou Vray.

>[!NOTE]
>
> **Emplacements des paramètres prédéfinis de workflow**
> 
> **Windows** :\
> C:\Users\\Documents\maya\2022\substance\workflows\generated\
> **MacOS** :\
> /Users//Library/Preferences/Autodesk/maya//substance/workflows/generated\
> **Linux** :\
> /home//maya//substance/workflows/generated

![](../../../assets/workflows-4.png)

Pour utiliser un workflow, il vous suffit de choisir le paramètre prédéfini dans la liste déroulante, puis de cliquer sur le bouton Créer un réseau de nuanceurs.

![](../../../assets/workflow.gif)

## Création d’un workflow

Vous pouvez créer votre propre workflow et l’ajouter à la liste Workflow de rendu. Lors de l’ajout d’un nouveau workflow, tous les nœuds créés après le nœud de Substance de données sont enregistrés dans le workflow. Cela vous permet de créer un nombre illimité de nœuds ombrages pour créer un réseau de nuanceurs personnalisé complet qui peut être enregistré comme flux de travail prédéfini.

## ![](../../../assets/saved-workflow.png) Gestion des workflows

### Enregistrement de workflows personnalisés

1. Créez manuellement des sorties de Substance et connectez-les à un matériau tel que aiStandardSurface.
   1. Vous pouvez utiliser n&#39;importe quel Maya ou rendre des nœuds spécifiques pour construire le réseau de nuanceurs.
1. Cliquez sur le bouton **Créer un workflow** et saisissez un nom pour le paramètre prédéfini de workflow.

### Duplication de workflows

Vous pouvez dupliquer un workflow en cliquant sur le bouton **Dupliquer le workflow**.

### Renommer et remplacer des workflows

Vous pouvez renommer les workflows existants et les remplacer par des données mises à jour à l&#39;aide des boutons **Renommer** et **Remplacer** sélectionnés.

### Suppression de workflows

Vous pouvez supprimer des workflows existants à l’aide du bouton Supprimer le workflow.
