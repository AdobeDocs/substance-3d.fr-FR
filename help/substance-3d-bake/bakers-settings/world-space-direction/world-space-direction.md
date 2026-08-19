---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-bake/bakers-settings/world-space-direction.html"
breadcrumb-title: ''
description: Calculez les directions vectorielles dans l'espace univers et enregistrez-les dans les textures pour les effets directionnels et le masquage.
helpx_creative_field: ""
helpx_description: bakers > Bakers Settings > World Space Direction
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Direction dans l'espace monde
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 4%

---


# Direction dans l&#39;espace monde

Le boulanger World Space Direction permet de calculer une direction vectorielle dans l&#39;espace du monde en une texture.

**Disponible dans :**

* Concepteur de substance
* Boîte à outils d&#39;automatisation des substances

## Paramètres

| *Paramètre* | *Description* |
| --- | --- |
| **Direction d’entrée** | Définit à partir de quelle entrée la direction est calculée.Valeurs possibles :<ul data-preserve-html="true"><li data-preserve-html="true"><strong>De la texture</strong> : la direction du vecteur est définie par une texture d’entrée.</li><li data-preserve-html="true"><strong>Vecteur uniforme</strong> (valeur par défaut) : la direction du vecteur est définie avec les curseurs X, Y et Z.</li></ul> |
| **Orientation normale** | Définit si le format normal de la texture de sortie. Le canal vert est ainsi inversé en fonction du format.Valeurs possibles :<ul data-preserve-html="true"><li data-preserve-html="true"><strong>OpenGL </strong></li><li data-preserve-html="true"><strong>DirectX</strong> (par défaut)</li></ul> |
| **X Y Z** | Des curseurs pour définir les 3 composants du vecteur de direction, si **Direction d’entrée** est défini sur **Vecteur uniforme**. |
| **Fichier de direction** | Chemin d’accès au fichier de texture d’entrée pour définir le vecteur de direction, si **Direction d’entrée** est défini sur **De la texture**. |
