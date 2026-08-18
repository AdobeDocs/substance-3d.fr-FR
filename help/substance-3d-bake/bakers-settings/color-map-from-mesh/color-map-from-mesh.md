---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-bake/bakers-settings/color-map-from-mesh.html"
breadcrumb-title: ''
description: Projetez les propriétés de couleur des filets en polychromie dans les textures pour cuire de la polypeinture ou des ID de matériau pour les masques de sélection.
helpx_creative_field: ""
helpx_description: bakers > Bakers Settings > Color Map from Mesh
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Map color à partir du maillage
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 5%

---


# Map color à partir du maillage

Cette table des couleurs de mesh baker projette les propriétés de couleur d&#39;un filet haute définition dans une texture. Il peut être utilisé pour cuire de la polypeinture ou des ID de matériau pour créer des masques de sélection.

**Disponible dans :**

* Substance Designer
* Substance Automation Toolkit
* Substance Painter

## Paramètres

| *Paramètre* | *Description* |
| --- | --- |
| **Source de couleur** | Détermine la propriété du maillage polychrome sur laquelle la génération de couleurs doit être basée.Valeurs possibles :<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Couleur du sommet</strong> : lit la couleur du sommet et l&#39;enregistre dans la texture. Les couleurs sont interpolées de sommet en sommet.</li><li data-preserve-html="true"><strong>Couleur du matériau</strong> : lit la couleur du matériau affectée à une face polygonale.</li><li data-preserve-html="true"><strong>ID de filet</strong> : attribuez une couleur par objet trouvé.</li><li data-preserve-html="true"><strong>ID de polygroupe/sous-maillage</strong> : attribuez une couleur par sous-objet (également appelé élément).</li></ul> |
| **Générateur de couleurs** | Définit la façon dont la couleur est générée lorsque la **source de couleur** est définie sur **ID de maillage** ou **ID de polygroupe/sous-maillage**. Valeurs possibles :<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Aléatoire</strong> : chaque objet ou sous-objet est coloré par une couleur générée de manière aléatoire.</li><li data-preserve-html="true"><strong>Décalage de teinte</strong> : chaque objet ou sous-objet est coloré par une couleur unique basée sur une teinte.</li><li data-preserve-html="true"><strong>Niveaux de gris</strong> : chaque objet ou sous-objet est coloré par une valeur de niveaux de gris unique.</li></ul> |
