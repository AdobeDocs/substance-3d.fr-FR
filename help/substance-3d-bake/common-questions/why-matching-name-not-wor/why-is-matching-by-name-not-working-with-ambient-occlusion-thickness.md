---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-bake/common-questions/why-is-matching-by-name-not-working-with-ambient-occlusion-thickness.html"
breadcrumb-title: ''
description: Comprenez pourquoi le Matching by Name ne fonctionne pas avec Ambient Occlusion et les boulangers d'épaisseur et trouvez des alternatives.
helpx_creative_field: ""
helpx_description: "bakers > Common Questions > Why is Matching by Name not working with Ambient OcclusionThickness "
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 'Pourquoi la correspondance par nom ne fonctionne-t-elle pas avec l’épaisseur d’occlusion ambiante ? '
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 0%

---


# Pourquoi la correspondance par nom ne fonctionne-t-elle pas avec l’occlusion/épaisseur ambiante ?

>[!WARNING]
>
> **Question**
> 
> J&#39;ai activé [Correspondance par nom](../../features/matching-by-name/matching-by-name.md) dans les [paramètres communs](../../bakers-settings/common-parameters/common-parameters.md) pour filtrer et trier mes maillages bas et haut poly, pourquoi l&#39;Ambient Occlusion baker l&#39;ignore-t-il ?

>[!NOTE]
>
> **Explication**
> 
> Le boulanger Occlusion ambiante, Épaisseur et Courbure normales lance des rayons secondaires lorsqu&#39;ils calculent leurs textures. Ces rayons possèdent leur propre paramètre Correspondance par nom .

>[!NOTE]
>
> **Solution : Peintre De Substance**
> 
> Solution : activez le filtrage par nom correspondant aux rayons secondaires dans les paramètres baker.
