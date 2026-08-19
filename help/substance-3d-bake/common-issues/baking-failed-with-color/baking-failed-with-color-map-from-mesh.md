---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/common-issues/baking-failed-with-color-map-from-mesh.html"
breadcrumb-title: ''
description: Résolvez les problèmes de couleur du maillage en vérifiant les propriétés de couleur du maillage et le mappage UV.
helpx_creative_field: ""
helpx_description: bakers > Common Issues > Baking failed with Color Map from Mesh
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Échec du cuisson avec Color Map de Mesh
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 0%

---


# Échec du cuisson avec Color Map de Mesh

>[!WARNING]
>
> **Problème**
> 
> Message d’erreur possible :
> 
> > > > 
> 
> [ Cuisson ] Échec de la cuisson (Carte des couleurs du maillage)\
> Couleurs de sommet introuvables

>[!NOTE]
>
> **Explication**
> 
> Les paramètres par défaut de la [Map de couleurs du maillage](../../bakers-settings/color-map-from-mesh/color-map-from-mesh.md) consistent à transformer les couleurs de sommet de maillage à polyvalence élevée en une texture basée sur les UV du maillage. Cependant, c&#39;est souvent le cas lorsque le maillage à poly élevé ne contient aucune information sur les couleurs de sommet. Par conséquent, le boulanger ne peut pas écrire des informations qui n&#39;existent pas.

>[!NOTE]
>
> **Solution**
> 
> Différentes solutions sont disponibles pour éviter ce message d&#39;erreur :
> 
> * Utilisez un maillage polyvalent aux couleurs de sommet
> * Définissez la Carte des couleurs de Mesh baker avec différents paramètres
> * N&#39;utilisez pas la Carte des couleurs de Mesh baker si vous n&#39;en avez pas besoin
