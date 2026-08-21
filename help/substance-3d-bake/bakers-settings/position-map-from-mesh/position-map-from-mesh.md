---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-bake/bakers-settings/position-map-from-mesh.html"
breadcrumb-title: ''
description: Calculer des cartes de position précises à partir de maillages à polyplexes élevés pour capturer des informations d'emplacement de géométrie précises.
helpx_creative_field: ""
helpx_description: bakers > Bakers Settings > Position map from Mesh
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Carte de position à partir du maillage
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 0%

---


# Carte de position à partir du maillage

La carte Position de mesh baker calcule l&#39;emplacement de la géométrie de maillage à polypole élevé et enregistre dans une texture. Il est similaire au boulanger de position de base, mais peut produire des résultats plus précis.

**Disponible en :**

* Concepteur de substance
* Boîte à outils d&#39;automatisation des substances

## Paramètres

| *Paramètre* | *Description* |
| --- | --- |
| **Mode** | Contrôle les informations qui seront calculées dans la texture de position.Valeurs possibles :<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Tous les axes :</strong> incorpore la position des axes X, Y et Z dans les canaux RGB de la texture de sortie.</li><li data-preserve-html="true"><strong>Un axe :</strong> incorpore un seul axe dans la texture de sortie sous forme d’image en niveaux de gris.</li></ul> |
| **Axe** | Définit l’axe à calculer si le paramètre **Mode** est défini sur **Un axe**. |
| **Type de normalisation** | Définit comment mettre à l’échelle les valeurs de position par axe.Valeurs possibles :<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Box :</strong> normalise chaque axe en fonction du volume de maillage (longueur du cadre de délimitation).</li><li data-preserve-html="true"><strong>BSphere:</strong> normalise tous les axes en fonction du rayon du volume de maillage (sphère de délimitation).</li></ul> |
| **Échelle de normalisation** | Définit comment mettre à l&#39;échelle les valeurs de position en fonction du maillage.Valeurs possibles :<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Par matériau</strong> : les valeurs sont mises à l&#39;échelle pour être comprises entre 0 et 1 pour chaque matériau (jeu de textures).</li><li data-preserve-html="true"><strong>Scène complète</strong> (par défaut) : les valeurs sont mises à l’échelle pour prendre en compte l’ensemble du maillage. Cela permet d&#39;obtenir des valeurs de position continues entre les objets et les matériaux (ensembles de textures).</li></ul> |
