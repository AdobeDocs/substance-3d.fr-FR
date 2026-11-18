---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-integrations/3d-applications/maya/using-workflows.html"
breadcrumb-title: ""
description: Créez et utilisez des paramètres prédéfinis de rendu pour les sorties de Substance dans Maya afin de générer automatiquement des réseaux de shader pour différents systèmes de rendu.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > Maya > Using Workflows
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Utilisation des workflows
user-guide-description: ""
user-guide-title: ""
source-git-commit: 28a9d8cf7a4eed4163f99e8158c9cb8f9da88302
workflow-type: tm+mt
source-wordcount: '568'
ht-degree: 0%
---

# Utilisation des workflows

Sous Workflows, vous pouvez choisir ou créer des paramètres prédéfinis de rendu pour les sorties de Substance. Ces paramètres prédéfinis sont des réseaux shader pour un moteur de rendu tel qu’Arnold ou Vray.

>[!NOTE]
>
> **Emplacements des paramètres prédéfinis de workflow**
>
> **Windows** :
> C:\Users\\Documents\maya\2022\substance\workflows\generated
> **MacOS** :
> /Users//Library/Preferences/Autodesk/maya//substance/workflows/generated
> **Linux** :
> /home//maya//substance/workflows/generated

![](../../../assets/maya-max-v3-1/maya-all-presets.png)

Pour utiliser un workflow, il vous suffit de choisir le paramètre prédéfini dans la liste, puis de cliquer sur le bouton Créer un réseau.

![](../../../assets/workflow.gif)

## Création d’un workflow

Vous pouvez créer votre propre workflow et l’ajouter à la liste Workflow de rendu. Lors de l’ajout d’un nouveau workflow, tous les nœuds créés après le nœud de Substance de données sont enregistrés dans le workflow. Cela vous permet de créer un nombre illimité de nœuds d’ombrage pour créer un réseau de shader personnalisé complet qui peut être enregistré en tant que workflow prédéfini.

![](../../../assets/saved-workflow.png)

## Gestion des workflows

### Enregistrement de workflows personnalisés

1. Créez manuellement des sorties de Substance et connectez-les à un matériau tel que aiStandardSurface.
   1. Vous pouvez utiliser n’importe quel Maya ou effectuer le rendu de nœuds spécifiques pour créer le réseau shader.
1. Cliquez sur le bouton **Créer un workflow** et saisissez un nom pour le paramètre prédéfini de workflow.

### Duplication de workflows

Vous pouvez dupliquer un workflow en cliquant sur le bouton **Dupliquer le workflow**.

### Renommer et remplacer des workflows

Vous pouvez renommer les workflows existants et les remplacer par des données mises à jour à l&#39;aide des boutons **Renommer** et **Remplacer** sélectionnés.

### Suppression de workflows

Vous pouvez supprimer des workflows existants à l’aide du bouton Supprimer le workflow.

## Workflows d’OpenPBR

Deux workflows OpenPBR sont disponibles dans la liste des workflows : **OpenPBR** et **OpenPBR - V-Ray**. Ces workflows sont conçus pour être utilisés avec des fichiers SBSAR créés à l’aide de l’OpenPBR dans Substance 3D Designer ou Sampler (OpenPBR est le modèle par défaut depuis Designer V16.0+ et Sampler V6.0+).

### Qu’est-ce que l’OpenPBR ?

OpenPBR est un modèle d&#39;ombrage de matériau physique ouvert développé par Adobe et Autodesk et contribué à l&#39;Academy Software Foundation (ASWF). Elle fournit une définition de matériau unifiée compatible entre les systèmes de rendu. Pour plus d&#39;informations, consultez la [documentation OpenPBR](https://experienceleague.adobe.com/fr/docs/substance-3d/general-knowledge/openpbr/openpbr-overview).

### Quand utiliser un workflow OpenPBR

Utilisez un workflow OpenPBR lorsque votre Fichier sbsar a été créé à l’aide de l’modèle de matériau dans Substance 3D Designer ou Substance 3D Sampler. Si votre SBSAR a été créé à l’aide d’un modèle de matériau standard d’Adobe (ASM), utilisez le workflow hérité compatible avec votre système de rendu (Arnold, V-Ray ou V-Ray 6).

>[!NOTE]
>
> Si vous appliquez un workflow OpenPBR à un matériau ASM, ou un workflow standard à un OpenPBR SBSAR, le module externe connectera uniquement les sorties communes aux deux modèles de matériau. Le résultat peut être incomplet.

### Workflows d’OpenPBR disponibles

**OpenPBR**

Utilise le nœud Maya openPBRSurface natif. Compatible avec Arnold et V-Ray. Il s’agit du workflow recommandé pour la plupart des utilisateurs qui travaillent avec des OpenPBR dans Maya.

**OpenPBR - V-Ray**

Utilise le matériau V-Ray (VRayMtl) en mode OpenPBR. Recommandé pour les utilisateurs dont le pipeline est spécifiquement construit autour des configurations de matériau V-Ray.

### Application d’un workflow OpenPBR

1. Chargez votre Fichier sbsar dans le plug-in à l’aide du bouton Charger la Substance.
1. Dans la liste Workflows, sélectionnez **OpenPBR** ou **OpenPBR - V-Ray**.
1. Cliquez sur **Créer un réseau** pour créer le réseau shader dans l&#39;**Éditeur de Matériau Hypershade**.
1. Le plug-in connecte automatiquement les sorties SBSAR aux entrées correspondantes de l&#39;OpenPBR.
1. Attribuez le matériau à votre maillage comme d’habitude.

![](../../../assets/maya-max-v3-1/maya-openpbr-overview.png)
