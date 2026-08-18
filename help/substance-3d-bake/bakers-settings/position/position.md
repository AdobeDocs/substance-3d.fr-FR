---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-bake/bakers-settings/position.html"
breadcrumb-title: ''
description: Calculez et enregistrez l’emplacement de la géométrie du maillage dans les textures pour créer des effets basés sur le volume et des masques de dégradé.
helpx_creative_field: ""
helpx_description: bakers > Bakers Settings > Position
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Position
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 2%

---


# Position

Le boulanger de position calcule l’emplacement de la géométrie du maillage et l’enregistre dans une texture. La position est utile pour calculer les informations dans le volume de l’objet ou pour créer des masques de dégradé.

**Disponible dans :**

* Substance Painter
* Substance Designer
* Substance Automation Toolkit

## Paramètres

| *Paramètre* | *Description* |
| --- | --- |
| **Mode** | Détermine les informations à calculer dans la texture de position.Valeurs possibles :<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Tous les axes :</strong> insère la position des axes X, Y et Z dans les couches RGB de la texture de sortie.</li><li data-preserve-html="true"><strong>Un axe :</strong> insère un seul axe dans la texture de sortie sous forme d&#39;image en niveaux de gris.</li></ul> |
| **Axe** | Définit l&#39;axe à calculer si le paramètre **Mode** est défini sur **Un axe**. |
| **Type de normalisation** | Définit la mise à l’échelle des valeurs de position par axe.Valeurs possibles :<ul data-preserve-html="true"><li data-preserve-html="true"><strong>BBox :</strong> normalisez chaque axe en fonction du volume du maillage (longueur du cadre de sélection).</li><li data-preserve-html="true"><strong>BSphere :</strong> normalisez tous les axes en fonction du rayon du volume du maillage (sphère de délimitation).</li></ul> |
| **Échelle de normalisation** | Définit la mise à l’échelle des valeurs de position en fonction du maillage.Valeurs possibles :<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Par matière</strong> : les valeurs sont mises à l&#39;échelle pour être comprises entre 0 et 1 pour chaque matière (ensemble de textures).</li><li data-preserve-html="true"><strong>Scène complète</strong> (par défaut) : les valeurs sont mises à l’échelle pour prendre en compte l’ensemble du filet. Cela permet d’appliquer des valeurs de position continues sur les objets et les matières (ensembles de textures).</li></ul> |
