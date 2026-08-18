---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-integrations/game-engines/unreal-engine/unreal-engine-5/physical-size-ue5.html"
breadcrumb-title: ''
description: Utilisez les paramètres de taille physique pour mettre à l’échelle les matériaux de Substance en fonction des dimensions réelles dans Unreal Engine 5.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unreal Engine > Unreal Engine 5 > Physical Size - UE5
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Taille physique - UE5
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 0%

---


# Taille physique - UE5

La taille physique des matériaux de Substance permet de les mettre à l’échelle en fonction de leur taille dans le monde. Cette valeur est définie en Substance Designer et lue dans Irréel via le système de gabarit de matériau.\
Le matériau [Substance\_triplanaire\_modèle](../../../../game-engines/unreal-engine/unreal-engine-5/material-template-usage/out-the-box-material-tem/out-of-the-box-material-templates.md) dans le parent contient un exemple d&#39;utilisation de la taille physique pour mettre à l&#39;échelle des matériaux irréels.



Quelles que soient les valeurs d&#39;agrandissement du maillage, les matériaux se divisent en mosaïques en fonction de la taille qu&#39;ils adoptent dans le monde en centimètres. Dans le cas du matériau rocheux (figure 1), il s&#39;agit de 1,8 m (180 cm) pour chaque mesure.

![](../../../../assets/rock-material-parameters.png)

Les valeurs des matériaux de Substance contenant des données de taille physique seront copiées dans n&#39;importe quel nœud de paramètre vectoriel de matériau existant nommé physicalsize.



Comme il n&#39;y a pas de valeur de displacement dans les matériaux dans UE5, le modèle de taille physique copie la valeur en tant que X, Y, X pour la carte triplanaire.
