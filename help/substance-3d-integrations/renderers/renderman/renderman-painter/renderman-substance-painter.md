---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/renderers/renderman/renderman-substance-painter.html"
breadcrumb-title: ''
description: Exportez les textures de Substance Painter pour Renderman en utilisant le matériau pxrSurface et les conversions de sortie appropriées.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Renderers > Renderman > Renderman - Substance Painter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Renderman - Substance Painter
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 1%

---


# Renderman - Substance Painter

Substance Painter 2020.1 (6.1.0) prend en charge [**pxrSurface**](https://rmanwiki.pixar.com/display/REN/PxrSurface) et pxrDisney [Modèles de sortie](https://docs.substance3d.com/display/SPDOC/Export).

![](../../../assets/renderman.png)

Il est recommandé d&#39;utiliser **pxrSurface** pour la sortie.

![](../../../assets/pxrsurface.png)

## Renderman Shader (Maya - RM 23.1)

| Exportation de Substance Painter | PxrSurface |
| --- | --- |
| DiffuseColor | Diffus/Couleur |
| RugositéSpéculaire | Specular primaire / Rugosité |
| SpecularFaceColor | Couleur primaire du Specular/du visage |
| Normale | Globals / Bump / PxrNormalMap → Orientation (Open GL) |
| Displacement | (canal rouge ) PxrDispTransform (Result F) → (disp scalar) PxrDisplace (Out Color) → (Displacement Shader) PxrSurfaceSG |
| GlowColor | Lueur / Couleur (Gain = 1,0) |
| Présence | Globals / Présence |

>[!NOTE]
>
> Les cartes qui représentent des données devront être interprétées correctement. Pour plus d&#39;informations, consultez la page [Gestion des couleurs](../../../renderers/color-management/color-management.md).
