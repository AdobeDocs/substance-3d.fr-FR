---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unity/generated-textures-packing.html"
breadcrumb-title: ''
description: Découvrez comment Substance génère des textures dans Unity et configurez le packing de texture pour des entrées de nuanceur optimales.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unity > Generated Textures (Packing)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Textures générées (Packing)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '362'
ht-degree: 6%

---


# Textures générées (Packing)

Les textures générées affichent les sorties de la Substance calculées par la Substance Engine pour créer des textures. Ces textures sont entrées dans les entrées du nuanceur. Par défaut, seules les entrées de base utilisées par le shader sont créées. Si l’option « Générer toutes les sorties » est activée, toutes les textures seront affichées ici.

![](../../../assets/screen-shot-2022-03-29-at-1-24-16-pm-copy.png)

Lorsque « Générer toutes les sorties » est activé

![](../../../assets/screen-shot-2022-03-29-at-1-29-35-pm-copy.png)

## Utilisation

1. La sélection d’une icône de texture entraîne la sélection de la texture dans la fenêtre Projet. Cela ne fonctionne pas pour les matériaux d’exécution, car les textures ne sont pas générées dans le dossier du projet.
1. Le fonctionnement du bouton sRVB est similaire à celui de l’option sRVB (texture colorée) dans les Paramètres d’importation de texture. Elle permet de définir si une texture doit être interprétée en espace gamma (sRVB) ou linéairement. Le module externe Substance gère automatiquement cette interprétation, mais il peut être remplacé si nécessaire.

   | Sortie de Substance | sRVB |
   | --- | --- |
   | Base color | Activé |
   | Diffuse | Activé |
   | Spéculaire | Activé |
   | Normale | Désactivé |
   | Métallique | Désactivé |
   | Rugosité | Désactivé |
   | Brillance | Désactivé |
   | Hauteur | Désactivé |
   | Occlusion ambiante | Désactivé |

## Couches packings

Vous pouvez compresser une texture dans la couche alpha d’une autre texture à l’aide du menu déroulant. Chaque texture générée dispose d’un menu déroulant qui contient une liste de toutes les textures générées par les matériaux de Substance. Choisissez simplement une texture dans la liste pour la compresser dans la couche alpha de la texture. L’option Source correspond à la couche alpha de la texture.

Dans cette image, j’ai sélectionné le mappage d’height :

![](../../../assets/screen-shot-2022-03-29-at-2-48-33-pm.png)

Dans l’image ci-dessous, vous pouvez voir que la sortie height est compressée dans la couche alpha de la table de correspondance des couleurs de base.

![](https://helpx-prod.scene7.com/is/image/HelpxProd/screen-shot-2022-03-29-at-2-53-20-pm-copy?$png$&jpegSize=200&wid=1248)

## Mappage de texture de sortie

En outre, la texture de sortie peut être affectée individuellement aux entrées de surface des matériaux Unity via la section Correspondance de texture de sortie. Les textures de sortie générées par le fichier .sbsar seront affichées dans la colonne de gauche et les entrées Unity Surface disponibles apparaissent dans la colonne de droite. Ces dernières peuvent être modifiées via les listes déroulantes.

![](../../../assets/image2023-3-27-14-30-24.png)
