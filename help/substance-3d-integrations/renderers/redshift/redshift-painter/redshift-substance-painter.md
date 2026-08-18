---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-integrations/renderers/redshift/redshift-substance-painter.html"
breadcrumb-title: ''
description: Exportez les textures de Substance Painter pour le rendu Redshift à l’aide des modèles de sortie et des paramètres de matière appropriés.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Renderers > Redshift > Redshift - Substance Painter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Redshift - Substance Painter
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 2%

---


# Redshift - Substance Painter

Substance Painter 2020.1 (6.1.0) prend en charge Redshift [Modèles de sortie](https://docs.substance3d.com/display/SPDOC/Export) pour la rugosité métallique (rsMaterial). Vous pouvez simplement exporter à l’aide du modèle Redshift pour produire des textures compatibles avec les matériaux Redshift.

![](../../../assets/rs-export.png)

## Configuration de la matière Redshift

| Exportation de Substance Painter | Matière Redshift |
| --- | --- |
| Couleur | Diffus/Couleur |
| Rugosité | Réflexion/Rugosité (BRDF = GGX) |
| Metalness | Réflexion/Métallique (Type de Fresnel = Métallique) |
| Normale | Globale / Carte de relief / rsBumpMap (Type de carte d&#39;entrée = Espace tangent normal - Échelle d&#39;Height = 1,0) |
| DisplaceHeightField | Displacement Shader / rsDisplacement TexMap (Codage de mappage = Champ Height) |
| EmissionColor | Total/Émissions (Poids des émissions = 1,0) |

>[!NOTE]
>
> Les cartes qui représentent des données devront être interprétées correctement. Pour plus d&#39;informations, consultez la page [Gestion des couleurs](../../../renderers/color-management/color-management.md).

## Exemple Maya/Redshift

![](https://helpx-prod.scene7.com/is/image/HelpxProd/maya-example?$pjpeg$&jpegSize=300&wid=1583){width="800px"}
