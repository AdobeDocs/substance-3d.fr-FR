---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-bake/getting-started/compatible-3d-software.html"
breadcrumb-title: ''
description: Découvrez quel logiciel 3D est compatible avec Substance Bakers et apprenez à préparer des maillages pour des résultats de cuisson optimaux.
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

La plupart des logiciels 3D sont compatibles avec Substance Bakers à condition qu’ils exportent la géométrie de maillage sous forme de polygones dans des formats de fichiers pris en charge par les applications.

Cependant, tous les logiciels ne sont pas sur un pied d’égalité en termes de fonctionnalités et de qualité lors de l’exportation de ces maillages. C&#39;est pourquoi il est important de bien nettoyer un filet et de s&#39;assurer qu&#39;il sera compatible avec les boulangers. Pour plus d&#39;informations sur la préparation d&#39;un filet, consultez les différents [guides](../../guides/performances-and-opt/performances-and-optimizations.md).

## Compatibilité logicielle

Vous trouverez ci-dessous une liste des logiciels 3D communément connus et de leur compatibilité avec les boulangers :

| *Nom* | *État* |
| --- | --- |
| **Mélangeur** | Compatible : aplatit les modificateurs avant l’exportation. |
| **Maya** | Compatible : nécessite une transformation par blocage et un historique des suppressions avant l’exportation. |
| **3DS Max** | Compatible : nécessite une xForm réinitialisée avant l’exportation. |
| **MODO** | Compatible : recommandé d’utiliser l’exportateur Game Tab défini sur « Maillage statique irréel ». |
| **Cinema 4D** | Compatible : aplatit les modificateurs avant l’exportation. |
| **zBrush** | Non compatible : les maillages à faible poly doivent d’abord être traités et nettoyés dans une autre application 3D. Compatible : mailles en poly élevé pour la cuisson. |

## Format du fichier

Lors de la cuisson de la géométrie, il est important de prendre en compte le format de fichier utilisé également. Le format de fichier définit la quantité d&#39;informations qui seront enregistrées dans le maillage.

Le fait d&#39;avoir trop d&#39;informations peut parfois être préjudiciable et entraîner des erreurs. Nous vous recommandons généralement d’essayer différents formats de fichiers lorsque des erreurs se produisent, car cela peut être un moyen facile de résoudre les problèmes et de déterminer si le coupable est dans le boulanger lui-même ou provient du logiciel 3D.

Voici un aperçu rapide des deux formats de fichiers les plus courants pris en charge par les boulangers :

| Format du fichier | Informations |
| --- | --- |
| **FBX** | Autodesk FBX (Filmbox) est le format de fichier principal utilisé par Autodesk Software. Il peut être écrit sous forme de texte ou de binaire.  Il prend en charge :<ul data-preserve-html="true"><li data-preserve-html="true">UV (jeux multiples)</li><li data-preserve-html="true">Vertex, tangente et binormales</li><li data-preserve-html="true">Couleurs des vertex</li><li data-preserve-html="true">Triangle, quatre faces et N-Gon face</li><li data-preserve-html="true">Caméras</li><li data-preserve-html="true">Lumières</li><li data-preserve-html="true">Subdivisions de maillage</li><li data-preserve-html="true">Lissage de groupes</li><li data-preserve-html="true">Informations sur la matière (comme la couleur)</li><li data-preserve-html="true">Bitmap</li></ul> |
| **OBJ** | Wavefront OBJ est un format de fichier texte très simple qui prend en charge :<ul data-preserve-html="true"><li data-preserve-html="true">UV (un seul jeu)</li><li data-preserve-html="true">Normales aux sommets</li><li data-preserve-html="true">Couleurs des sommets (uniquement si exportées à partir de l’outil Pinceau pixellisé)</li><li data-preserve-html="true">Triangle, Quad et N-Gon</li><li data-preserve-html="true">Couleur du matériau (si le fichier <strong>mtl</strong> est présent)</li></ul> |
