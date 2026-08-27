---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/renderers/arnold/arnold-substance-painter.html"
breadcrumb-title: ''
description: Utilisez des modèles de sortie de Substance Painter pour le moteur de rendu Arnold avec aiStandard matériau pour le rendu physique.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Renderers > Arnold > Arnold - Substance Painter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Arnold - Substance Painter
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4a060ee1aaa1731c04e70d5512e3271cd63d0381
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 3%

---


# Arnold - Substance Painter

Substance Painter 2020.1 (6.1.0) est livré avec [Modèles de sortie](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/getting-started/export/output-templates/export-presets) pour Arnold à l’aide du [matériau aiStandard](https://docs.arnoldrenderer.com/display/A5AFMUG/Standard+Surface).

![](../../../assets/arnold-export.png){width="800px"}

## Arnold Standard Shader (Arnold 5 et versions ultérieures)

| Exportation de Substance Painter | Arnold AiStandardSurface |
| --- | --- |
| Couleur de base | Base/Couleur |
| Rugosité | SPECULAR / RUGOSITÉ |
| Metalness | Base/Métal |
| Normale | (**Maya**) Géométrie/Mappage de relief/bump2d (Utiliser comme normales de Repère tangent) (**3ds** **Max**) Bitmap → Normal |
| Hauteur | (**Maya**) Shader/displacement Displacement (**3ds** **Max**) Modificateur d&#39;objet → Propriétés Arnold → Displacement → Utiliser la carte |
| Émissif | Émission/ Couleur (Poids des émissions = 1,0) |
| Anisotropy level (non incluse dans le Modèle de sortie Arnold par défaut) | (**Maya**) Manteau/Anisotropie (**3ds** **Max**) Manteau/Anisotropie |
| Anisotropy level (non incluse dans le Modèle de sortie Arnold par défaut) | (**Maya**) Couche/Rotation (**3ds** **Max**) Couche/Rotation |

>[!NOTE]
>
> Les cartes qui représentent des données devront être interprétées correctement. Pour plus d&#39;informations, consultez la page [Gestion des couleurs](../../../renderers/color-management/color-management.md).
