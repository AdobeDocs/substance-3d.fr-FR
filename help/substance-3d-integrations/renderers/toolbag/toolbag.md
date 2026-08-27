---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-integrations/renderers/toolbag.html"
breadcrumb-title: ''
description: Utilisez la rugosité de la Substance et les sorties métalliques dans Toolbag 2 pour un aperçu et un rendu de la matière en temps réel.
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

Cette page explique comment utiliser les sorties Rugosité/Métal pour Toolbag 2.

Toolbag prend en charge les workflows specular/brillance et métallique/rugosité.

Substance 3D Painter utilise l’ombrage PBR métallique par défaut, mais vous pouvez également l’utiliser avec l’ombrage specular/brillance. Ce workflow explique comment utiliser les sorties métalliques pour Toolbag 2. Toolbag prend en charge le workflow métallique.

[Télécharger un exemple de scène](https://www.dropbox.com/s/qyed3un2zhtuibj/toolbag.zip?dl=0)

## Exporter depuis Painter

1. Lors de l’utilisation de l’ombrage PBR métallique par défaut, nous pouvons exporter à l’aide du paramètre prédéfini d’exportation Couches du document + Normal + AO par défaut.  ***\*Les canaux du document exportent le mappage normal en fonction de la configuration du projet. Toolbag requiert OGL Mappage normal. Vous pouvez changer le format normal dans la configuration du projet.***
1. Vous pouvez également créer une configuration d’exportation personnalisée qui utilise la brillance

   ![](../../assets/settings-export.png){width="600px"}
1. Vous pouvez modifier le format normal en OpenGL avant l’exportation.  **Modifier>Configuration du projet**

   ![](../../assets/settings-normal-format.png)

## Configuration des matériaux

1. Définir la Réflectivité sur Métal
1. Définir la réflexion sur GGX
1. Ajoutez les textures aux couches appropriées comme indiqué dans le graphique suivant :

   | Texture Substance 3D Painter | Espace colorimétrique | Matériau de la trousse à outils |
   | --- | --- | --- |
   | Couleur de base | sRVB | Albédo |
   | Rugosité | sRGB désactivé | Microsurface - Lissage - Clic sur Inverser |
   | Métallique | sRGB désactivé | Réflectivité - Métallisation |
   | Normale | sRGB désactivé | Normale |
   | Occlusion ambiante | sRGB désactivé | Occlusion |

![](../../assets/settings-toolbag.jpg){width="600px"}
