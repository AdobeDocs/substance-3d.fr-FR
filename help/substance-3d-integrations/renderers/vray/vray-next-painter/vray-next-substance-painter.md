---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-integrations/renderers/vray/vray-next-substance-painter.html"
breadcrumb-title: ''
description: Exportez les textures de Substance Painter pour le rendu V-Ray Next à l’aide de modèles de sortie et des paramètres de workflow appropriés.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Renderers > Vray > Vray Next - Substance Painter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Vray Next - Substance Painter
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 3%

---


# Vray Next - Substance Painter

Substance Painter 2020.1 (6.1.0) est livré avec des shaders [VrayMtl](https://docs.chaosgroup.com/display/VRAY4MAYA/VRayMtl) pour les workflows métallique et specular. Vous pouvez [configurer votre projet de Substance Painter](https://docs.substance3d.com/display/SPDOC/Project+Creation) à l&#39;aide du **modèle VrayMtl**, qui configurera votre shader de viewport.

![](../../../assets/template-16.jpg)

Sous les Paramètres de Shader, vous pouvez configurer le shader Vray pour travailler avec VrayMtl.

>[!NOTE]
>
> Si votre projet a été configuré pour utiliser l&#39;[UDIM de Tuiles UV hérité](https://helpx.adobe.com/fr/substance-3d/unlisted/documentation/spdoc/uv-tile-udim-legacy-144310352.html). Utilisez le modèle de sortie UDIM Vray Next.

![](../../../assets/vray-mtl-shader.png){width="800px"}

Pour exporter des textures de rendu dans Vray Next, choisissez le Modèle de sortie Vray Mtl.

![](../../../assets/template-project.jpg){width="800px"}

## Vray Matériau (Vray Next - Métallique/Rugosité)

| Exportation de Substance Painter | VRayHTML |
| --- | --- |
| Couleur de base | (**Maya**) Couleur Diffuse (Quantité = 1,0) (**3ds Max**) Diffuse |
| Rugosité | (**Maya**) Réflexion/Rugosité (BRDF = GGX) + (Utiliser la Rugosité activée)(**3ds Max**) Rugosité → BRDF/ Utiliser GGX et activer Utiliser la rugosité |
| Métallique | (**Maya**) Réflexion/Métallique (**3ds Max**) Métallique |
| Normale | (**Maya**) Mappage de relief et de normales / carte (Type de carte = Normal dans le Repère tangent)(**3ds** **Max**) bitmap → Normal |
| Hauteur | (**Maya**) Shader/displacement Displacement (**3ds** **Max**) Modificateur d&#39;objet → VrayDisplacementMod → Tex Map |
| Émissif | Auto-illumination |
| Transmissif | (**Maya**) Couleur de Subsurface scattering/Translucency (**3ds Max**) Couleur de Translucency → de face arrière |
| AnisotropyAngle | (**Maya**) Anisotropie/Rotation de l’Anisotropie (**3ds** **Max**) BRDF/Rotation |
| Niveau d&#39;anisotropie | (**Maya**) Anisotropie/Anisotropie (**3ds Max**) BRDF/Angle |

## Vray Matériau (Vray Next - Specular/Brillance

| Exportation de Substance Painter | VRayHTML |
| --- | --- |
| Diffuse | (**Maya**) Couleur Diffuse (Quantité = 1,0) (**3ds Max**) Diffuse |
| Spéculaire | (**Maya**) Réflexion/Couleur De Réflexion (Quantité = 1,0) (**3ds Max**) Réflexion |
| Brillance | (**Maya**) Réflexion/Rugosité (BRDF = GGX) + (Utiliser la Rugosité activée)(**3ds Max**) Brillance → BRDF/Utiliser GGX et activer Utiliser la brillance |
| Normale | (**Maya**) Mappage de relief et de normales / carte (Type de carte = Normal dans le Repère tangent)(**3ds** **Max**) bitmap → Normal |
| Hauteur | (**Maya**) Shader/displacement Displacement (**3ds** **Max**) Modificateur d&#39;objet → VrayDisplacementMod → Tex Map |
| Émissif | Auto-illumination |
| Transmissif | (**Maya**) Couleur de Subsurface scattering/Translucency (**3ds Max**) Couleur de Translucency → de face arrière |
| AnisotropyAngle | (**Maya**) Anisotropie/Rotation de l’Anisotropie (**3ds** **Max**) BRDF/Rotation |
| Niveau d&#39;anisotropie | (**Maya**) Anisotropie/Anisotropie (**3ds Max**) BRDF/Angle |

>[!NOTE]
>
> Les cartes qui représentent des données devront être interprétées correctement. Pour plus d&#39;informations, consultez la page [Gestion des couleurs](../../../renderers/color-management/color-management.md).

Cet exemple montre le viewport de Substance Painter utilisant le shader Vray Métallique/Rugosité et le rendu Vray utilisant Maya.

![](../../../assets/vray-maya.jpg){width="800px"}
