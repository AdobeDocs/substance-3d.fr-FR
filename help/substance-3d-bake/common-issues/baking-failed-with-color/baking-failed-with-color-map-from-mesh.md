---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/common-issues/baking-failed-with-color-map-from-mesh.html"
breadcrumb-title: ''
description: Résolvez les problèmes de correspondance des couleurs des filets en vérifiant les propriétés des couleurs des filets et la correspondance UV.
helpx_creative_field: ""
helpx_description: bakers > Common Issues > Baking failed with Color Map from Mesh
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Échec de la cuisson avec la table des couleurs à partir du filet
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 0%

---


# Échec de la cuisson avec la table des couleurs à partir du filet

>[!WARNING]
>
> **Problème**
> 
> Message d’erreur possible :
> 
> &#x200B;> > > 
> 
> [ Cuisson ] Échec de la cuisson (table des couleurs à partir du filet)\
> Couleurs de sommet introuvables

>[!NOTE]
>
> **Explication**
> 
> Les paramètres par défaut de la [table des couleurs du filet](../../bakers-settings/color-map-from-mesh/color-map-from-mesh.md) consistent à transformer les couleurs des sommets du filet en une texture basée sur les UV du filet. Cependant, c’est souvent le cas lorsque le filet à polygone élevé ne dispose d’aucune information sur les couleurs des sommets. Par conséquent, le boulanger ne peut pas écrire des informations qui n&#39;existent pas.

>[!NOTE]
>
> **Solution**
> 
> Différentes solutions sont disponibles pour éviter ce message d’erreur :
> 
> * Utiliser un filet à haute densité polychrome avec des couleurs de sommets
> * Définition de la table des couleurs de Mesh Baker avec différents paramètres
> * N’utilisez pas la table des couleurs de Mesh Baker si vous n’en avez pas besoin
