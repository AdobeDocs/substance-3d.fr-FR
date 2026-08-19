---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/getting-started/compatible-3d-software.html"
breadcrumb-title: ''
description: Découvrez quel logiciel 3D est compatible avec Substance Bakers et apprenez à préparer des maillages pour des résultats de cuisson optimaux.
helpx_creative_field: ""
helpx_description: bakers > Getting Started > Compatible 3D software
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Logiciels 3D compatibles
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '391'
ht-degree: 2%

---


# Logiciels 3D compatibles

La plupart des logiciels 3D sont compatibles avec Substance Bakers à condition qu&#39;ils exportent la géométrie maillée sous forme de polygones dans des formats de fichiers pris en charge par les applications.

Cependant, tous les logiciels ne sont pas du même niveau en termes de fonctionnalité et de qualité lors de l’exportation de ces maillages. C&#39;est pourquoi il est important de nettoyer correctement un maillage et de s&#39;assurer qu&#39;il sera compatible avec les boulangers. Pour plus d&#39;informations sur la préparation d&#39;un maillage, consultez les différents [guides](../../guides/performances-and-opt/performances-and-optimizations.md).

## Compatibilité logicielle

Voici une liste des logiciels 3D connus et leur compatibilité avec les boulangers :

| *Nom* | *Statut* |
| --- | --- |
| **Blender** | Compatible : nécessite d’aplatir les modificateurs avant l’exportation. |
| **Maya** | Compatible : nécessite une transformation par gel et un historique de suppression avant exportation. |
| **3DS max** | Compatible : nécessite un xForm réinitialisé avant l&#39;export. |
| **MODO** | Compatible : recommandé d’utiliser l’exportateur d’onglet Jeu défini sur « Maillage statique irréel ». |
| **** | Compatible : nécessite d’aplatir les modificateurs avant l’exportation. |
| **zBrush** | Non compatible : les maillages bas-poly doivent d&#39;abord être traités et nettoyés dans une autre application 3D. Compatible : mailles en poly pour la cuisson. |

## Format du fichier

Lors de la cuisson de la géométrie, il est important de prendre également en compte le format de fichier utilisé. Le format de fichier définit la quantité d&#39;informations qui seront enregistrées dans le maillage.

Avoir trop d&#39;informations peut parfois être préjudiciable et conduire à des erreurs. Nous vous recommandons généralement d’essayer différents formats de fichiers en cas d’erreur, car il peut s’agir d’un moyen facile de résoudre les problèmes et de déterminer si le coupable est le boulanger lui-même ou le logiciel 3D.

Voici un aperçu rapide des deux formats de fichier les plus courants pris en charge par les boulangers :

| Format du fichier | Informations |
| --- | --- |
| **** | Autodesk FBX (Filmbox) est le format de fichier principal utilisé par le logiciel Autodesk. Il peut être écrit en texte ou en binaire.  Il prend en charge les éléments suivants :<ul data-preserve-html="true"><li data-preserve-html="true">UV (ensembles multiples)</li><li data-preserve-html="true">Vertex, tangente et binormales</li><li data-preserve-html="true">Couleurs des vertex</li><li data-preserve-html="true">Triangle face, Quad face et N-Gon face</li><li data-preserve-html="true">Caméras</li><li data-preserve-html="true">Lumières</li><li data-preserve-html="true">Subdivisions de maillage</li><li data-preserve-html="true">Lissage de groupes</li><li data-preserve-html="true">Informations sur le matériau (telles que la couleur)</li><li data-preserve-html="true">Bitmap</li></ul> |
| **** | Wavefront OBJ est un format de fichier texte très simple qui prend en charge :<ul data-preserve-html="true"><li data-preserve-html="true">UV (un seul ensemble)</li><li data-preserve-html="true">Normales de sommet</li><li data-preserve-html="true">Couleurs de sommet (uniquement si exportées à partir de Pixological zBrush)</li><li data-preserve-html="true">Face triangulaire, face quadruple et face N-Gon</li><li data-preserve-html="true">Couleur du matériau (si un fichier <strong>mtl</strong> est présent)</li></ul> |
