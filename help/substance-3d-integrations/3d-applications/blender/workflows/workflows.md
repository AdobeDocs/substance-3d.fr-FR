---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-integrations/3d-applications/blender/workflows.html"
breadcrumb-title: ''
description: Apprenez à utiliser les matériaux de Substance avec les cycles du mélangeur et les moteurs de rendu Eevee pour différents workflows.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > Blender > Workflows
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Workflows
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '595'
ht-degree: 0%

---


# Workflows

## Utilisation des cycles

Par défaut, les modifications de paramètres ne sont pas automatiquement mises à jour dans le viewport 3D lorsqu’elles sont affichées dans la vue de rendu Cycles. Pour afficher les mises à jour dans la vue Rendu des cycles, activez **textures de mise à jour automatique des cycles** dans Préférences pour forcer la mise à jour.

## Fichiers .sbsar multigraphiques

Le module complémentaire prend en charge les fichiers .sbrar avec plusieurs graphes substance. Lors du chargement d’un fichier contenant plusieurs graphes, une nouvelle liste déroulante Graphes s’affiche dans le panneau Substance 3D. Contrairement aux autres modifications de paramètres, le changement de graphe ne met pas automatiquement à jour le matériau. Pour cette raison, le bouton **Appliquer** doit être utilisé pour réattribuer le matériau après avoir modifié les graphes.

>[!NOTE]
>
> Par défaut, le bouton Appliquer ajoute le matériau dans un nouvel emplacement sans remplacer les affectations de matériau précédentes. Supprimez les matériaux précédents ou utilisez la liste déroulante matériau pour réattribuer les matériaux nouvellement appliqués.

![](https://helpx-prod.scene7.com/is/image/HelpxProd/blender-workflows-multigraphs?$png$&jpegSize=100&wid=168)

## Utilisation des entrées d’image

Lorsque vous utilisez un matériau de Substance de données qui permet des entrées d’image personnalisées, un paramètre de sélection d’image Panneau Substance 3D vous permet d’ouvrir le navigateur de fichiers pour une image (icône de dossier) ou de sélectionner une image qui existe dans votre projet (liste déroulante de l’icône d’image).

La préférence Exporter le format d’image peut être utilisée pour enregistrer les entrées d’image générées dans Blender dans le dossier temporaire. Consultez la page [Préférences](../../../3d-applications/blender/preferences/preferences.md) pour plus de détails.

![](../../../assets/blender-workflows-image-inputs-steps.png)

## Paramètres prédéfinis de réseau shader.

Le paramètre prédéfini shader peut être rapidement ajusté via le menu déroulant dans la section Sorties du panneau Substance 3D. Ces paramètres prédéfinis de shader permettent d’ajuster la façon dont les textures d’image sont appliquées. Cycles/Eevee Standard utilise le mappage de coordonnées d’UV régulier. Les trois autres paramètres prédéfinis Cycles/Projection d’œil utilisent le mappage des coordonnées de texture générées pour les méthodes de projection de boîte, de sphère ou de cylindre.

Le paramètre prédéfini shader par défaut utilisé par les matériaux peut être sélectionné dans le module complémentaire [Préférences](../../../3d-applications/blender/preferences/preferences.md).

![](../../../assets/2022-08-12-12-12-33-adobeexpress-1.gif)

## Filtrage et réglage des sorties

La section Sorties du panneau Substance 3D propose également des options pour les sorties filtrage. Trois boutons en regard de la liste déroulante des paramètres prédéfinis shader peuvent être utilisés pour filtrer les sorties activées (coche), les sorties shader (sphère) et toutes les sorties disponibles (lignes).

Les sorties peuvent être activées individuellement en cochant la case. Lorsqu’une sortie est activée, une sortie correspondante dans le groupe de nœuds de texture est créée. Si cette sortie est prise en charge par le nœud de matériau Principled BSDF, elle y est automatiquement connectée. L&#39;Height se connecte à un nœud de displacement et l&#39;Occlusion ambiante se combine avec la couleur de base dans un nœud MixRGB.\
Le menu déroulant Format de fichier en regard de la coche peut être utilisé pour définir le type de fichier sous lequel la texture de sortie est enregistrée.

En outre, les préférences de sortie de fichier par défaut peuvent être modifiées dans le module complémentaire [Préférences](../../../3d-applications/blender/preferences/preferences.md).

## Permutation de matériaux sur des objets

Cliquez sur l&#39;icône en forme de sphère dans le panneau des propriétés de matériau de Blender pour ouvrir une liste de matériaux dans votre projet Blender. Les matériaux de Substance qui ont été créés dans le panneau apparaîtront également dans la liste. La sélection d&#39;un matériau dans cette liste remplace le matériau actif dans cet emplacement de matériau.

## Displacement

Displacement du filet à partir des textures pris en charge dans le moteur de rendu Cycles, mais pas dans Eevee. Pour voir le displacement, assurez-vous que la sortie Height est activée. Le module complémentaire définit automatiquement le paramètre de displacement du matériau sur **Displacement et relief**. L’affichage de la matière sur un objet affiche désormais le displacement dans la vue de rendu. L’échelle du displacement peut être ajustée dans le panneau Matériau ou sur le nœud de displacement.

Pour obtenir de meilleurs résultats, utilisez des niveaux de subdivision supérieurs ou des maillages à poly élevé pour les matériaux présentant des détails de displacement complexes.
