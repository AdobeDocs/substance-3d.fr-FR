---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/guides/triangulating-before-baking.html"
breadcrumb-title: ''
description: Comprenez comment la triangulation du maillage affecte les résultats de cuisson et découvrez les bonnes pratiques pour préparer la géométrie.
helpx_creative_field: ""
helpx_description: bakers > Guides > Triangulating before baking
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Triangulation avant cuisson
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 0%

---


# Triangulation avant cuisson

Les filets 3D peuvent être définis avec des polygones avec plusieurs arêtes de bordure par face. Habituellement via des quads (4 bords), parfois plus (n-gons).\
Les logiciels transforment toutefois ces polygones en triangles plus tard, car il est plus facile de gérer et d&#39;effectuer des calculs avec (en particulier sur le GPU).

## Comment la triangulation peut-elle affecter un maillage ?

![](../../assets/triangulation.jpg)

Il n&#39;existe **pas de solutions standard** pour convertir les Quad/N-Gons en triangles. Comme illustré dans l’image ci-dessus, plusieurs choix sont possibles.\
Les boulangers sont peu susceptibles de trianguler les mailles comme le ferait un moteur de jeu parce que nous choisissons un algorithme spécifique plutôt qu&#39;un autre.

## Pourquoi trianguler avant de cuire ?

Le processus de cuisson lira la géométrie, puis codera les informations en textures.\
Comme ces informations sont basées sur les UV et parfois sur la topologie du maillage, d&#39;autres logiciels peuvent décoder les informations de manière incorrecte s&#39;ils ne lisent pas la géométrie de la même manière que lorsqu&#39;ils appliquent la texture.

Sur l’image ci-dessous, vous pouvez voir le maillage low-poly en haut à gauche et le maillage high-poly en haut à droite.\
En bas se trouve le bas-poly avec la carte normale préparée à partir du haut-poly. Le maillage à gauche utilise une triangulation identique à celle utilisée par Substance Painter lors de la cuisson. Le maillage de droite ne le fait pas et affiche des artefacts noirs. Ceci est dû au fait qu&#39;il existe une incohérence entre la façon dont la carte normale a été créée et la façon dont le maillage est actuellement triangulé. Ce problème peut être résolu en **actualisant le maillage et/ou en le reconcassant**.

![](../../assets/example-triangulation-artifact.jpg)
