---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/common-issues/baker-output-is-fully-black-or-empty.html"
breadcrumb-title: ''
description: Dépannez les raisons pour lesquelles les sorties baker sont entièrement noires ou vides et apprenez à résoudre les problèmes de maillage et d’UV.
helpx_creative_field: ""
helpx_description: bakers > Common Issues > Baker output is fully black or empty
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: La sortie de Baker est entièrement noire ou vide
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 0%

---


# La sortie de Baker est entièrement noire ou vide

>[!WARNING]
>
> **Problème**
> 
> Le résultat d’un boulanger est une texture noire ou vide :
> 
> ![](../../assets/black.png)

>[!NOTE]
>
> **Explication**
> 
> Une texture noire signifie que le boulanger n’a pas pu trouver les informations nécessaires pour générer un résultat. Par exemple, le processus de boulangerie n&#39;a pas trouvé le maillage de haut-poly pour correspondre au maillage de bas-poly, ce qui n&#39;a rien donné à comparer.

>[!NOTE]
>
> **Solution**
> 
> * Vérifiez si le maillage polyvalent nécessaire au boulanger a été correctement chargé (reportez-vous au fichier journal/à la fenêtre pour les erreurs).
> * Vérifier que les mailles à faible ou à fort poly ne sont pas trop grandes (plus d&#39;un kilomètre) ou trop petites (moins d&#39;un centimètre).
> * Vérifiez si le boulanger a pu lire/traiter le maillage (reportez-vous au fichier journal/à la fenêtre pour les erreurs).
> * Vérifiez si la fonctionnalité [Correspondance par nom](../../features/matching-by-name/matching-by-name.md) n&#39;a pas été correctement configurée (certains objets peuvent s&#39;exclure les uns les autres et ne jamais se chevaucher).
> * Vérifiez que les UV à faible poly se situent dans la plage 0-1.
