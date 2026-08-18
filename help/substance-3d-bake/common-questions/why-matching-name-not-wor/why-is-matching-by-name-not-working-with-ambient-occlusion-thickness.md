---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/common-questions/why-is-matching-by-name-not-working-with-ambient-occlusion-thickness.html"
breadcrumb-title: ''
description: Découvrez pourquoi la correspondance par nom ne fonctionne pas avec Ambient Occlusion et les boulangers de Thickness et trouvez des alternatives.
helpx_creative_field: ""
helpx_description: "bakers > Common Questions > Why is Matching by Name not working with Ambient OcclusionThickness "
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 'Pourquoi la correspondance par nom ne fonctionne pas avec l’épaisseur d’occlusion ambiante. '
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 0%

---


# Pourquoi la correspondance par nom ne fonctionne-t-elle pas avec Occlusion/Thickness ambiant ?

>[!WARNING]
>
> **Question**
> 
> J&#39;ai activé [Correspondance par nom](../../features/matching-by-name/matching-by-name.md) dans les [paramètres communs](../../bakers-settings/common-parameters/common-parameters.md) pour filtrer et trier mes maillages poly bas et haut. Pourquoi Ambient Occlusion baker l&#39;ignore-t-il ?

>[!NOTE]
>
> **Explication**
> 
> Le boulanger Occlusion ambiante, Thickness et Courbures normales lance les rayons secondaires lorsqu’ils calculent leurs textures. Ces rayons possèdent leur propre paramètre Correspondance par nom.

>[!NOTE]
>
> **Solution : Substance Painter**
> 
> Solution : activez le filtrage de correspondance par nom pour les rayons secondaires dans les paramètres baker.
