---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-bake/common-issues/baking-failed-with-color-map-from-mesh.html"
breadcrumb-title: ''
description: Résolvez les problèmes de baking des Maps de couleur à partir du maillage en vérifiant les propriétés de couleur du maillage et en UV du mappage.
helpx_creative_field: ""
helpx_description: bakers > Common Issues > Baking failed with Color Map from Mesh
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Échec du Baking avec la Map de couleur à partir du maillage
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 0%

---


# Échec du Baking avec la Map de couleur à partir du maillage

>[!WARNING]
>
> **Problème**
> 
> Message d’erreur possible :
> 
> &#x200B;> > > 
> 
> [ Baking ] Échec du Baking (Map de couleur à partir du maillage)\
> Couleurs de vertex introuvables

>[!NOTE]
>
> **Explication**
> 
> Les paramètres par défaut de la [Map de couleur à partir du maillage](../../bakers-settings/color-map-from-mesh/color-map-from-mesh.md) consistent à baker les couleurs du vertex du maillage à polychromie élevé en une texture en fonction des UV du maillage. Cependant, c’est souvent le cas lorsque le maillage à haut niveau de concurrence ne dispose d’aucune information sur les couleurs du vertex. Par conséquent, le baker ne peut pas écrire d&#39;informations qui n&#39;existent pas.

>[!NOTE]
>
> **Solution**
> 
> Différentes solutions sont disponibles pour éviter ce message d’erreur :
> 
> * Utilisez un maillage à polychromie intense avec des couleurs vertex
> * Définition du baker de Map de couleur à partir du maillage avec différents paramètres
> * N&#39;utilisez pas le baker de Map de couleur à partir du maillage si vous n&#39;en avez pas besoin
