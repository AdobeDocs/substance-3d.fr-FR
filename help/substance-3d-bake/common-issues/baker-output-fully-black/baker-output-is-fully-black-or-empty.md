---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/common-issues/baker-output-is-fully-black-or-empty.html"
breadcrumb-title: ''
description: Dépannez les raisons pour lesquelles les sorties baker sont entièrement noires ou vides et apprenez à résoudre les problèmes de maillage et d’UV.
helpx_creative_field: ""
helpx_description: bakers > Common Issues > Baker output is fully black or empty
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: La sortie du baker est entièrement noire ou vide
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 0%

---


# La sortie du baker est entièrement noire ou vide

>[!WARNING]
>
> **Problème**
> 
> Le résultat d’un baker est une texture noire ou vide :
> 
> ![](../../assets/black.png)

>[!NOTE]
>
> **Explication**
> 
> Une texture noire signifie que le baker n’a pas pu trouver les informations requises pour générer un résultat. Par exemple, le processus de baking n&#39;a pas permis de trouver un maillage à haut niveau de concurrence correspondant à celui à bas niveau de concurrence, ce qui n&#39;a pas donné lieu à une comparaison.

>[!NOTE]
>
> **Solution**
> 
> * Vérifiez si le maillage de haute qualité nécessaire au baker a été chargé correctement (reportez-vous au fichier journal/à la fenêtre pour les éventuelles erreurs).
> * Vérifier que les maillages à faible ou à fort poly ne sont pas trop grands (plus d&#39;un kilomètre) ou trop petits (moins d&#39;un centimètre).
> * Vérifiez si le baker a pu lire/traiter le maillage (reportez-vous au fichier journal/à la fenêtre pour les éventuelles erreurs).
> * Vérifiez si la fonctionnalité [Correspondance par nom](../../features/matching-by-name/matching-by-name.md) n&#39;a pas été correctement configurée (certains objets peuvent s&#39;exclure les uns les autres et ne jamais se chevaucher).
> * Vérifiez que les UV à faible poly se situent dans la plage 0-1.
