---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/features/geometry-cache.html"
breadcrumb-title: ''
description: Utilisez la mise en cache de la géométrie pour conserver les données de maillage prétraitées et accélérer considérablement les opérations de baking ultérieures.
helpx_creative_field: ""
helpx_description: bakers > Features > Geometry Cache
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Cache de géométrie
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---


# Cache de géométrie

Lors du baking, les maillages sont prétraités pour les nettoyer et convertis dans un format compatible avec le processus de baking. La mémoire cache de géométrie permet de conserver cette géométrie prétraitée d&#39;une manière rapide à recharger afin d&#39;éviter de refaire cette opération ultérieurement (sauf si le maillage source change).

* Dans la **Substance Designer**, le cache de géométrie est créé après l&#39;exécution d&#39;un premier baking. L&#39;antémémoire est alors conservée jusqu&#39;à la fermeture de la fenêtre de baker.
* Dans la **Substance Painter**, le cache de géométrie est enregistré en tant que fichier avec l&#39;extension **assbin** à côté du fichier source après le premier baking.

La réutilisation de la mémoire cache de géométrie accélère considérablement le processus de baking, en particulier lorsque vous ajustez les paramètres de baker pour obtenir un résultat parfait.
