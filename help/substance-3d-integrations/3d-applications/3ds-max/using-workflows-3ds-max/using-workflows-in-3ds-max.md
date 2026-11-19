---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-integrations/3d-applications/3ds-max/using-workflows-in-3ds-max.html"
breadcrumb-title: ""
description: Utilisez les workflows de rendu de 3ds Max pour créer automatiquement des réseaux de shader pour différents systèmes de rendu à partir de matériaux de Substance.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > 3ds Max > Using Workflows in 3ds Max
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Utilisation des workflows dans 3ds Max
user-guide-description: ""
user-guide-title: ""
source-git-commit: 335f3107fb325bb769325bff8c150b3e8b7ff054
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 0%
---

# Utilisation des workflows dans 3ds Max

Le module externe Substance in 3ds Max contient des workflows pour la création automatique d’un réseau de shader afin de prendre en charge les systèmes de rendu. Les workflows de rendu se trouvent dans le menu Substance.

![](../../../assets/maya-max-v3-1/3dsmax-all-presets.png)

Pour utiliser un workflow, sélectionnez le nœud de Substance dans l’éditeur de matériau, puis choisissez le workflow dans le menu Substance.

![](../../../assets/max-workflow.gif)

## Workflows d’OpenPBR

Deux workflows OpenPBR sont disponibles dans la **liste des workflows** à partir du **menu Substance** : **Substance vers OpenPBR** et **Substance vers OpenPBR V-Ray**. Ces workflows sont conçus pour être utilisés avec des fichiers SBSAR créés à l’aide de l’OpenPBR dans Substance 3D Designer ou Sampler (OpenPBR est le modèle par défaut depuis Designer V16.0+ et Sampler V6.0+).

![](../../../assets/maya-max-v3-1/3ds-max-openpbr-node-preview.png)

### Qu’est-ce que l’OpenPBR ?

OpenPBR est un modèle d&#39;ombrage de matériau physique ouvert développé par Adobe et Autodesk et contribué à l&#39;Academy Software Foundation (ASWF). Elle fournit une définition de matériau unifiée compatible entre les systèmes de rendu. Pour plus d&#39;informations, consultez la [documentation OpenPBR](https://experienceleague.adobe.com/fr/docs/substance-3d/general-knowledge/openpbr/openpbr-overview).

### Quand utiliser un workflow OpenPBR

Utilisez un workflow OpenPBR lorsque votre Fichier sbsar a été créé à l’aide de l’modèle de matériau dans Substance 3D Designer ou Substance 3D Sampler. Si votre SBSAR a été créé à l’aide d’un modèle de matériau standard d’Adobe (ASM), utilisez le workflow hérité compatible avec votre système de rendu (Arnold, V-Ray ou V-Ray 6).

>[!NOTE]
>
> Si vous appliquez un workflow OpenPBR à un matériau ASM, ou un workflow standard à un OpenPBR SBSAR, le module externe connectera uniquement les sorties communes aux deux modèles de matériau. Le résultat peut être incomplet.

### Workflows d’OpenPBR disponibles

**OpenPBR**

Utilise le nœud openPBRSurface natif de 3ds Max. Compatible avec Arnold et V-Ray. Il s’agit du workflow recommandé pour la plupart des utilisateurs qui travaillent avec des OpenPBR dans 3ds Max.

**OpenPBR - V-Ray**

Utilise le matériau V-Ray (VRayMtl) en mode OpenPBR. Recommandé pour les utilisateurs dont le pipeline est spécifiquement construit autour des configurations de matériau V-Ray.

### Application d’un workflow OpenPBR

![](../../../assets/maya-max-v3-1/3dsmax-substance-to-openpbr.png)

1. Sélectionnez votre Fichier sbsar (OpenPBR) à l’aide du bouton Charger la Substance.
1. Dans le menu supérieur, sélectionnez OpenPBR ou OpenPBR - V-Ray.
1. Cliquez sur Créer un réseau pour créer le réseau shader dans l’éditeur de Matériau d’ardoise.
1. Le plug-in connecte automatiquement les sorties SBSAR aux entrées correspondantes de l&#39;OpenPBR.
1. Attribuez le matériau à votre maillage comme d’habitude.

![](../../../assets/maya-max-v3-1/3ds-max-openpbr-overview.png)
