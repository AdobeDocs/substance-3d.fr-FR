---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/renderers/corona.html"
breadcrumb-title: ''
description: Utilisez des matériaux de Substance avec le rendu Corona dans 3ds Max à l’aide du workflow Specular/brillance et des mappages requis.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Renderers > Corona
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Corona
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 1%

---


# Corona

Pour le rendu avec Corona, vous pouvez utiliser des mappages exportés à partir de Substance Painter ou du plug-in Substance. Corona utilise le workflow Specular/brillance avec une carte 1/IOR. Vous aurez besoin des mappages suivants :

* Diffuse
* Réflexion (Specular)
* Brillance
* 1/IOR (Converti)

La texture 1/IOR ne peut être convertie qu&#39;à partir du flux Métallique/Rugosité, qui est le flux par défaut à la fois dans Substance Designer et Substance Painter.

1. Exportez des mappages depuis Substance Painter à l’aide du paramètre prédéfini Corona.
1. Pour les Substances personnalisées, vous pouvez utiliser le nœud converti couleur de base\_métallique\_rugosité défini sur le paramètre prédéfini Vray pour créer les sorties personnalisées.
1. Pour 3ds Max et Cinema 4D, vous utilisez un matériau Corona multicalque pour manipuler les matériaux métalliques et diélectriques et éviter ainsi de convertir une carte 1/IOR.

## Table des matières

* [Corona pour 3ds Max](../../renderers/corona/corona-for-3ds-max/corona-for-3ds-max.md)
* [Corona - Substance Painter](../../renderers/corona/corona-painter/corona-substance-painter.md)
