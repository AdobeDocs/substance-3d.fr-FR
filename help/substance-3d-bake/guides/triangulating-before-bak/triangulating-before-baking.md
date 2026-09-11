---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-bake/guides/triangulating-before-baking.html"
breadcrumb-title: ''
description: Découvrez comment la triangulation de maillage affecte les résultats de baking et les meilleures pratiques pour préparer votre géométrie.
helpx_creative_field: ""
helpx_description: bakers > Guides > Triangulating before baking
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Triangulation avant baking
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 0%

---


# Triangulation avant baking

Les Maillages 3D peuvent être définis avec des polygones avec plusieurs bords de bordure par face. Habituellement par quads (4 bords), parfois plus (n-gons).\
Cependant, les logiciels transforment ces polygones en triangles ultérieurement, car il est plus facile de gérer et d’effectuer des calculs avec (en particulier sur le GPU).

## Comment la triangulation peut-elle affecter un maillage ?

![](../../assets/triangulation.jpg)

Il n&#39;existe **aucune solution standard** pour convertir les Quad/N-Gons en triangles. Comme le montre l’image ci-dessus, plusieurs choix sont possibles.\
Il est peu probable que les bakers triangulent les maillages comme un moteur de jeu le ferait parce que nous choisissons un algorithme spécifique plutôt qu&#39;un autre.

## Pourquoi trianguler avant de baker ?

Le processus de baking lira la géométrie, puis encodera les informations dans des textures.\
Comme ces informations sont basées sur les UV et parfois sur la topologie du maillage, d&#39;autres logiciels pourraient décoder les informations de manière incorrecte s&#39;ils ne lisent pas la géométrie de la même manière que lorsqu&#39;ils appliquent la texture.

Sur l’image ci-dessous, vous pouvez voir le maillage en bas à gauche et le maillage en haut à droite.\
En bas se trouve le low-poly avec la map normal bakée du high-poly. Le maillage de gauche utilise une triangulation identique à celle utilisée par la Substance Painter lors du baking. Le maillage de droite n’affiche pas d’artefacts noirs. En effet, il existe une incohérence entre la façon dont la map normal a été bakée et la façon dont le maillage est actuellement triangulé. Cela peut être corrigé en **mettant à jour le maillage et/ou en le réorganisant**.

![](../../assets/example-triangulation-artifact.jpg)
