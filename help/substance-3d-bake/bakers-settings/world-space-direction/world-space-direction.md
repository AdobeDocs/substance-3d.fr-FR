---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/bakers-settings/world-space-direction.html"
breadcrumb-title: ''
description: Calculez les directions des vecteurs dans l’espace monde et enregistrez-les dans des textures pour les effets directionnels et le masquage.
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

Le baker de Direction dans l&#39;espace monde permet de calculer une direction vectorielle dans l’espace monde d’une texture.

**Disponible dans :**

* Substance Designer
* Substance Automation Toolkit

## Paramètres

| *Paramètre* | *Description* |
| --- | --- |
| **Direction d&#39;entrée** | Définit à partir de quelle entrée la direction est calculée.Valeurs possibles :<ul data-preserve-html="true"><li data-preserve-html="true"><strong>De la Texture</strong> : la direction du vecteur est définie par une texture d&#39;entrée.</li><li data-preserve-html="true"><strong>À partir du vecteur uniforme</strong> (par défaut) : la direction du vecteur est définie avec les curseurs X, Y, Z.</li></ul> |
| **Orientation normale** | Définit si le format normal de la texture de sortie. La couche verte est inversée en fonction du format.Valeurs possibles :<ul data-preserve-html="true"><li data-preserve-html="true"><strong>OpenGL</strong></li><li data-preserve-html="true"><strong>DirectX</strong> (par défaut)</li></ul> |
| **X Y Z** | Curseurs pour définir les 3 composantes du vecteur de direction, si la **direction d&#39;entrée** est définie sur **à partir d&#39;un vecteur uniforme**. |
| **Fichier de direction** | Chemin d&#39;accès au fichier de texture d&#39;entrée pour définir le vecteur de direction, si **Direction d&#39;entrée** est définie sur **De la Texture**. |
