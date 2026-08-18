---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unreal-engine/unreal-engine-5/material-template-usage-ue5/out-of-the-box-material-templates.html"
breadcrumb-title: ''
description: Utilisez des modèles de matériaux préconfigurés lors de l’importation de matériaux SBSAR dans Unreal Engine 5 pour une configuration et des workflows rapides.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unreal Engine > Unreal Engine 5 > Material Template Usage - UE5 > Out-of-the-Box Material Templates
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Modèles de matériau prêts à l'emploi
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 0%

---


# Modèles de matériau prêts à l&#39;emploi

Lors de l’importation de matériaux SBSAR dans le navigateur de contenu, vous pouvez choisir les différents modèles de matériaux dans la liste déroulante qui sont prêts à l’emploi.

![](../../../../../assets/screen-shot-2022-05-10-at-8-58-45-pm-copy.png)

## Modèle standard de Substance

Il s’agit d’un modèle de matériau de base pour une expérience UV générique. Il fournit quelques commandes de base des quantités d’UV afin que vous puissiez mettre à l’échelle les UV pour étirer les textures. Vous pouvez diviser la mise à l’échelle UV en activant l’option Diviser les UV. Vous disposez également des options Quantité U, Quantité V, Décalage des UV et Angle de rotation UV. Cela vous permet de créer des mosaïques UV ainsi qu’une rotation UV.

![](../../../../../assets/screen-shot-2022-05-10-at-9-06-40-pm-copy.png)

## Modèle triplanaire de Substance

Le gabarit triplanaire effectue une correspondance triplanaire des angles ou faces X, Y et Z du maillage afin de fusionner trois projections différentes des textures pour fusionner facilement les angles. Le gabarit triplanaire permet aux matériaux de se fondre entre les différentes faces lors de la flexion de l’objet

![menu de détails pour un matériau triplanaire de Substance](../../../../../assets/triplanar-template.png)

Le modèle triplanaire prend en charge les tailles physiques. Ainsi, lorsque la taille physique est activée, le modèle triplanaire met à l’échelle les images en fonction de la taille physique du matériau. Quelle que soit la mise à l’échelle de l’objet, la texture restera toujours la même et aura un aspect uniforme. En savoir plus sur la Taille physique ici : [Taille physique - UE5](../../../../../game-engines/unreal-engine/unreal-engine-5/physical-size-ue5/physical-size-ue5.md)

## Modèle de réfraction de Substance

Le gabarit de réfraction est principalement utilisé pour les objets transparents, par exemple, les lunettes. Il vous permet de modifier la valeur IOR ou les textures standard d&#39;un matériau en verre ou transparent.

![](../../../../../assets/screen-shot-2022-05-10-at-9-07-38-pm.png)

## Modèle de peinture de voiture de Substance

Le template de peinture de voiture ajoute une prise en charge du revêtement transparent et inclut la prise en charge des valeurs et des carreaux UV réglables, des valeurs de rugosité du revêtement claires et des valeurs de puissance de Fresnel.

![menu de détails pour un matériau de peinture de voiture de Substance](../../../../../assets/car-paint-template.png)

## Configuration de modèles de Displacement

>[!IMPORTANT]
>
> Modèles expérimentaux
> 
> Avertissement : les modèles suivants sont expérimentaux et peuvent subir des modifications importantes entre les versions. Ces modèles utilisent la fonction Nanite d&#39;Epic, qui est elle-même expérimentale au moment de l&#39;écriture de cet article. Ils peuvent ne pas être stables à 100 % et il convient de faire preuve de prudence lors de leur utilisation dans des projets.

Suivez les étapes ci-dessous pour activer complètement la prise en charge du displacement Nanite dans vos projets et utiliser des matériaux displacements avec vos maillages.

1. Accédez à Dossier du projet > Configuration > DefaultEngine.ini et ouvrez-le
1. Ajoutez ce qui suit à la section [/Script/Engine.RendererSettings] :
   * r.Nanite.AllowTessellation=1
   * r.Nanite.Tessellation=1
1. Sélectionnez le maillage statique auquel vous souhaitez appliquer un modèle de displacement et ouvrez ses paramètres.
1. Activez l’option Activer la prise en charge Nanite.
1. Importez le fichier .sbsar souhaité dans le navigateur de contenu et sélectionnez la Substance\_Displacement\_Template ou Susbtance\_Triplanar\_Displacement\_Template
1. Pour modifier la quantité de displacement, accédez au modèle de matière et sélectionnez le nœud de sortie. Réglez ensuite l’amplitude sous la section Displacement.

## Modèle de Displacement de Substance

Similaire au modèle standard de Substance, ce modèle permet d&#39;ajuster les valeurs U et V tout en ajoutant la prise en charge du Displacement Nanite.

![menu de détails pour un matériau de Displacement de Substance](../../../../../assets/displacement-template.png)

## Modèle de Displacement triplanaire de Substance

Similaire au modèle de Displacement de Substance, ce modèle applique une projection triplanaire avec l&#39;option de prise en charge de Taille physique avec l&#39;ajout de la prise en charge de Displacement Nanite.

![menu de détails pour un matériau de Displacement triplanaire de Substance](../../../../../assets/triplanar-displacement-template.png)
