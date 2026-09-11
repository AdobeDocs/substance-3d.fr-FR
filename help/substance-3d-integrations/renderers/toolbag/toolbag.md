---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-integrations/renderers/toolbag.html"
breadcrumb-title: ''
description: Utilisez la rugosité de Substance et les sorties métallique dans la Boîte à outils 2 pour un aperçu et un rendu du matériau en temps réel.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Renderers > Toolbag
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Toolbag
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 5%

---


# Toolbag

Cette page explique comment utiliser les sorties rugosité/métallique pour Toolbag 2.

Toolbag prend en charge les workflows specular/brillance et métallique/rugosité.

Substance 3D Painter utilise le shader PBR métallique par défaut, mais vous pouvez également l’utiliser avec specular/brillance shader. Ce workflow explique comment utiliser les sorties métallique pour Toolbag 2. Toolbag prend en charge le workflow métallique.

[Télécharger un exemple de Scène](https://www.dropbox.com/s/qyed3un2zhtuibj/toolbag.zip?dl=0)

## Exporter depuis Painter

1. Lorsque vous utilisez le shader PBR métallique par défaut, nous pouvons exporter à l’aide du paramètre prédéfini d’exportation Couches du document + Normal + AO par défaut.  ***\*Les canaux du document exportent la Map normal en fonction de la configuration du projet. Toolbag requiert une Map normal OGL. Vous pouvez changer le format normal dans la configuration du projet.***
1. Vous pouvez également créer une configuration d’exportation personnalisée qui utilise la brillance

   ![](../../assets/settings-export.png){width="600px"}
1. Vous pouvez modifier le format normal en OpenGL avant l’exportation.  **Modifier>Configuration du projet**

   ![](../../assets/settings-normal-format.png)

## Configuration du matériau

1. Définir la Réflectivité sur Métal
1. Définir la réflexion sur GGX
1. Ajoutez les textures aux canaux appropriés comme indiqué dans le graphique ci-dessous :

   | Texture Substance 3D Painter | Espace colorimétrique | Matériau Toolbag |
   | --- | --- | --- |
   | Couleur de base | sRVB | Albédo |
   | Rugosité | sRGB désactivé | Microsurface - Lissage - Clic sur Inverser |
   | Métallique | sRGB désactivé | Réflectivité - Métallisation |
   | Normale | sRGB désactivé | Normale |
   | Occlusion ambiante | sRGB désactivé | Occlusion |

![](../../assets/settings-toolbag.jpg){width="600px"}
