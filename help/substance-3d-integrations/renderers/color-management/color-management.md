---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/renderers/color-management.html"
breadcrumb-title: ''
description: Découvrez la gestion des couleurs et la correction gamma lors de l’utilisation de matériaux de Substance avec différents systèmes de rendu.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Renderers > Color Management
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Gestion des couleurs
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '683'
ht-degree: 2%

---


# Gestion des couleurs

Nous adopterons une approche simpliste en affirmant que le rendu d&#39;espace linéaire fournit les calculs corrects pour les calculs d&#39;éclairage. Il crée un environnement qui permet aux interactions lumineuses d’être représentées de manière crédible dans le monde réel. Pour une discussion sur le rendu d’espace linéaire, nous devons introduire le concept de correction gamma. Lors du codage d’images à des fins d’affichage et de stockage, la correction gamma est le processus d’optimisation consistant à réduire la bande passante et l’allocation de bits. Ce processus exploite la perception de la luminosité par l’œil humain, qui suit approximativement la racine cubique de la luminance.

>[!NOTE]
>
> Le rendu d’espace linéaire est un sujet très complexe. Pour plus d&#39;informations, consultez le [GUIDE PBR VOLUME ONE](https://academy.substance3d.com/courses/the-pbr-guide-part-1) disponible gratuitement sur [Substance Academy](https://academy.substance3d.com/).

## Gestion des couleurs

L&#39;objectif de ce document est de détailler le processus de travail avec les textures exportées à partir de **Substance Painter** et de **Substance Designer** dans le [logiciel 3D](https://www.adobe.com/products/substance3d/3d-augmented-reality.html) et les moteurs de rendu.

La bonne façon d’interpréter une image utilisée comme entrée dans une couche de matériau dépend de la façon dont l’image est utilisée dans la scène. L&#39;espace colorimétrique, le codage et le fait que les valeurs de couleur soient proportionnelles à la **luminance à référence scène** ou à la **luminance à référence affichage** jouent également un rôle important.

* Les images utilisées pour représenter des **données non colorées** ne doivent pas être transformées. Il s&#39;agit généralement de cartes **normales**, **de rugosité**, **métalliques**, **de displacement** et **ambiantes** **d&#39;occlusion**.
* Les images qui représentent les couleurs que nous voyons peuvent avoir plusieurs scénarios. Par exemple, les images déjà **linéaires de scène** n&#39;ont généralement pas besoin d&#39;être converties, telles que les images **HDR** stockées dans des formats tels que **OpenEXR** et **HDR**.
* Les images créées pour l&#39;affichage (**référencées pour l&#39;affichage**) devront être supprimées de leur gamma. Il s&#39;agit notamment de la plupart des formats tels que **PNG**, **JPEG** et **BMP**. Ces images sont **de base** **couleur**, **diffuses**, **specular** et **émissives**.

Bien qu&#39;il s&#39;agisse d&#39;une simplification excessive, il peut être utile de considérer le processus comme suit :

* « référencé par la scène (ex. linear) » : n’applique pas de conversion
* « référencé (ex. sRGB) » : appliquer la transformation inverse pour « linéariser » l&#39;image pour un calcul correct

>[!NOTE]
>
> La fonction de décodage sRVB (EOTF), convertissant l&#39;espace gamma en espace linéaire, est utilisée en Substance Painter et en Substance Designer et est définie par la norme IEC 61966-2-1:1999

La Substance Designer peut être configurée pour utiliser [OpenColorIO](https://opencolorio.org/) pour la gestion des couleurs. Cela vous permet d&#39;avoir des transformations de couleur *cohérentes* et un affichage des images dans plusieurs applications. Dans ce mode, la Substance Designer fonctionnera en interne avec des couleurs **RGB linéaires**. Étant donné que 8 nombres de bits par pixel ne sont généralement pas suffisants pour représenter des couleurs linéaires, il est recommandé d&#39;utiliser la profondeur *au moins* **16 bits** pour les textures de couleur dans le [graphique](https://docs.substance3d.com/display/SDDOC/Graph+View).

![](https://helpx-prod.scene7.com/is/image/HelpxProd/sd-cm?$png$&jpegSize=200&wid=686)

Lorsque nous avons introduit [ACES](https://www.oscars.org/science-technology/sci-tech-projects/aces), nous disposons désormais de deux espaces colorimétriques différents : le sRVB linéaire (la version sans gamma de sRVB) et le [ACEScg](https://acescolorspace.com/), qui est un espace colorimétrique à large gamme (« référencé scène » ou linéaire) mieux adapté au rendu CG.

*Graphique de tracé de gamme -<https://acescolorspace.com/>*

La Substance Designer prend également en charge **Adobe Color Engine (ACE)**. Avec **ACE**, vous pouvez choisir votre espace colorimétrique de travail entre **sRGB**, **sRGB linéaire** et **ACEScg**. Lors de l&#39;utilisation de **sRGB**, **ACE** est quasiment identique au mode hérité. Lorsque vous utilisez un espace colorimétrique linéaire, **ACE** ressemble plus ou moins à [OpenColorIO](https://opencolorio.org/index.html).

## Plug-ins Substance

Lors de l’utilisation de matériaux de Substance via le module externe d’intégration de Substance, les sorties sont automatiquement marquées pour la valeur linéaire/gamma via l’intégration et la gestion des couleurs de l’application hôte. Toutefois, il est important de bien comprendre le processus : lorsque des cartes de Substance sont utilisées comme images bitmap exportées plutôt que comme matériaux de Substance, vous devrez peut-être marquer manuellement les textures comme **gamma-encodées** ou **brutes** en fonction du moteur de rendu que vous utilisez. Les fichiers .png, .jpg, .tga ou .tif 8 ou 16 bits sont généralement codés en gamma, tandis que les fichiers **sRGB OETF** et .exr sont linéaires.

## Applications 3D

### Utilisation des textures

* [Textures de Substance en maya](../../renderers/color-management/textures-in-maya/substance-textures-in-maya.md)
* [Textures de Substance dans 3ds Max](../../renderers/color-management/textures-in-3ds-max/substance-textures-in-3ds-max.md)
