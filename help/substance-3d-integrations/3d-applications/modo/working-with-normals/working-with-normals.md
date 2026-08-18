---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/3d-applications/modo/working-with-normals.html"
breadcrumb-title: ''
description: Configurez les paramètres d'orientation de la texture normale dans MODO pour vous assurer que le rendu de texture normale avec les matériaux de Substance est correct.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > MODO > Working with Normals
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Utilisation des normales
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 0%

---


# Utilisation des normales

Utilisation des données normales : définition de l’orientation correcte

Les Substances Stock sont conçues pour utiliser l’orientation normale DX. Cependant, MODO utilise OGL. Vous pouvez retourner la normale en définissant le paramètre Format normal sur 1,0. Le module externe de Substance interprète uniquement les paramètres définis dans la Substance. Vous pouvez rencontrer une Substance qui n&#39;a pas le paramètre « normal\_format », car il appartient à l&#39;auteur de la Substance d&#39;ajouter ce contrôle aux Substances personnalisées. Si vous rencontrez une Substance qui n’a pas ce paramètre, vous pouvez retourner la couche verte sur le calque Texture de la carte normale pour fixer l’orientation.

>[!NOTE]
>
> Le retournement de la couche verte n&#39;est possible que si la Substance n&#39;a pas la bonne orientation normale et que l&#39;auteur n&#39;a pas créé de contrôle pour retourner la normale dans les paramètres de la Substance

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../assets/normal-1.png)

</td>
<td style="border: 0;" valign="top">

![](../../../assets/invert-2.png)

</td>
</tr>
</table>
