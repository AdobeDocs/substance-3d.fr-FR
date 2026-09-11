---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-bake/getting-started/compatible-3d-software.html"
breadcrumb-title: ''
description: Découvrez quel logiciel 3D est compatible avec Substance Bakers et apprenez à préparer des maillages pour un baking optimal.
helpx_creative_field: ""
helpx_description: bakers > Getting Started > Compatible 3D software
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Logiciel 3D compatible
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '391'
ht-degree: 2%

---


# Logiciel 3D compatible

La plupart des logiciels 3D sont compatibles avec Substance Bakers à condition qu’ils exportent la géométrie du maillage sous forme de polygones dans des formats de fichiers pris en charge par les applications.

Cependant, tous les logiciels ne sont pas sur un pied d’égalité en termes de fonctionnalités et de qualité lors de l’exportation de ces maillages. C&#39;est pourquoi il est important de bien nettoyer un maillage et de s&#39;assurer qu&#39;il sera compatible avec les bakers. Pour plus d&#39;informations sur la préparation d&#39;un maillage, consultez les différents [guides](../../guides/performances-and-opt/performances-and-optimizations.md).

## Compatibilité logicielle

Vous trouverez ci-dessous une liste des logiciels 3D connus et de leur compatibilité avec les bakers :

| *Nom* | *État* |
| --- | --- |
| **Mélangeur** | Compatible : aplatit les modificateurs avant l’exportation. |
| **Maya** | Compatible : nécessite un transforme de blocage et un historique des suppressions avant l’exportation. |
| **3DS Max** | Compatible : nécessite une xForm réinitialisée avant l’exportation. |
| **MODO** | Compatible : recommandé d&#39;utiliser l&#39;exporteur de l&#39;onglet Jeu défini sur « Maillage statique irréel ». |
| **Cinema 4D** | Compatible : aplatit les modificateurs avant l’exportation. |
| **zBrush** | Non compatible : les maillages à faible poly doivent d’abord être traités et nettoyés dans une autre application 3D. Compatible : maillages à poly élevé pour le baking. |

## Format du fichier

Lors du baking de la géométrie, il est important de prendre en compte le format de fichier utilisé. Le format de fichier définit la quantité d’informations qui seront enregistrées dans le maillage.

Le fait d&#39;avoir trop d&#39;informations peut parfois être préjudiciable et entraîner des erreurs. Nous vous recommandons généralement d’essayer différents formats de fichiers lorsque des erreurs se produisent, car cela peut être un moyen facile de résoudre les problèmes et de déterminer si le coupable est dans le baker lui-même ou provient du logiciel 3D.

Vous trouverez ci-dessous un aperçu des deux formats de fichier les plus courants pris en charge par les bakers :

| Format du fichier | Informations |
| --- | --- |
| **FBX** | Autodesk FBX (Filmbox) est le format de fichier principal utilisé par Autodesk Software. Il peut être écrit sous forme de texte ou de binaire.  Il prend en charge :<ul data-preserve-html="true"><li data-preserve-html="true">UV (jeux multiples)</li><li data-preserve-html="true">Vertex, Tangente et binormaux</li><li data-preserve-html="true">Couleurs des vertex</li><li data-preserve-html="true">Face triangulaire, face quadruple et face N-Gon</li><li data-preserve-html="true">Caméras</li><li data-preserve-html="true">Lumières</li><li data-preserve-html="true">subdivisions de maillage</li><li data-preserve-html="true">Lissage de groupes</li><li data-preserve-html="true">Informations de matériau (telles que la couleur)</li><li data-preserve-html="true">Bitmap</li></ul> |
| **OBJ** | Wavefront OBJ est un format de fichier texte très simple qui prend en charge :<ul data-preserve-html="true"><li data-preserve-html="true">UV (un seul jeu)</li><li data-preserve-html="true">Normales vertex</li><li data-preserve-html="true">Couleurs par vertex (uniquement si exportées à partir de Pixologic zBrush)</li><li data-preserve-html="true">Face triangulaire, face quadruple et face N-Gon</li><li data-preserve-html="true">Couleur du matériau (si le fichier <strong>mtl</strong> est présent)</li></ul> |
