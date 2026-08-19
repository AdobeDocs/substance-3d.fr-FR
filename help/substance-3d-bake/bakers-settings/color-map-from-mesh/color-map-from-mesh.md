---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/bakers-settings/color-map-from-mesh.html"
breadcrumb-title: ''
description: Projetez les propriétés de couleur des filets à polypoles élevés dans les textures pour faire de la polypeinture ou des identifiants de matériau pour les masques de sélection.
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

Cette Map de couleur de mesh baker projette les propriétés de couleur d&#39;un maillage haute définition dans une texture. Il peut être utilisé pour fabriquer de la polypeinture ou des identifiants de matériau pour créer des masques de sélection.

**Disponible en :**

* Concepteur de substance
* Boîte à outils d&#39;automatisation des substances
* Substance Painter

## Paramètres

| *Paramètre* | *Description* |
| --- | --- |
| Source des couleurs **&#x200B;**&#x200B;| Contrôle à partir de quelle propriété du maillage à poly élevé la génération de couleur doit être basée.Valeurs possibles :<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Couleur du sommet</strong> : lit la couleur du sommet et l’enregistre dans la texture. Les couleurs sont interpolées de sommet en sommet.</li><li data-preserve-html="true"><strong>Couleur du matériau</strong> : permet de lire la couleur de matériau affectée à une face de polygone.</li><li data-preserve-html="true"><strong>ID de maillage</strong> : attribuez une couleur à chaque objet trouvé.</li><li data-preserve-html="true"><strong>Polygroup/ID de sous-maillage</strong> : attribuez une couleur par sous-objet (également appelé élément).</li></ul> |
| **Générateur de couleurs** | Définit la manière dont la couleur est générée lorsque la Source de couleur **est définie sur** ID de maillage **ou** ID de polygroupe/sous-maillage **. Valeurs possibles :**<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Aléatoire</strong> : chaque objet ou sous-objet est coloré par une couleur générée de manière aléatoire.</li><li data-preserve-html="true"><strong>Décalage de teinte</strong> : chaque objet ou sous-objet est coloré par une couleur unique basée sur une teinte.</li><li data-preserve-html="true"><strong>Niveaux de gris</strong> : chaque objet ou sous-objet est coloré par une valeur de niveaux de gris unique.</li></ul> |
