---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/3d-applications/cinema-4d/visual-feedback-of-animated-substances.html"
breadcrumb-title: ''
description: Activez la prévisualisation animée dans Cinema 4D pour voir le retour visuel des matériaux de Substance animés dans la clôture.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > Cinema 4D > Visual Feedback of Animated Substances
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Commentaires visuels sur les Substances animées
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 3%

---


# Commentaires visuels sur les Substances animées

Pour avoir un retour visuel d’une Substance animée dans la fenêtre d’affichage de Cinema 4D, l’option Aperçu animé doit être activée pour ces matériaux.

Cette option se trouve dans l’éditeur de matériaux sous Éditeur (voir ci-dessous). Si un matériau a été créé à l&#39;aide de la commande Créer un(des) matériau(x) , cette option est activée par défaut.

![](../../../assets/cinema-4d-13.png){width="500px"}


## Création de matière(s)

La commande Créer des matériaux dans le Gestionnaire d&#39;actifs de Substance permet de créer facilement et rapidement des matériaux de Cinema 4D à l&#39;aide d&#39;une Substance.

Par conséquent, le mappage de canaux suivant sera utilisé :

|  |  |
| --- | --- |
| **Canal De Sortie De Substance** | **Canal de matériau Cinema 4D** |
| Diffuse | Couleur |
| Émissif | Luminance |
| Reflet | Réflectance |
| Environnement | Environnement |
| Relief | Relief |
| Opacité | Alpha |
| Spéculaire | Réflectance/Specular par défaut |
| Hauteur | Displacement |
| Normale | Normale |

Cette relation n&#39;est utilisée que pour la commande Créer matières et la matière qui a été créée peut être modifiée par la suite. Il peut être utile d’utiliser cette commande pour créer rapidement un matériau de base, que vous pourrez ensuite affiner en ne réglant que quelques couches.

Dans le nuanceur de Substances, vous n’êtes pas limité aux quelques canaux de sortie répertoriés ci-dessus, mais en fait vous pouvez utiliser n’importe quel canal de sortie fourni par une Substance.

## Création manuelle de matériau(x) de Substance

Au lieu d’utiliser la commande Créer une ou plusieurs matières, vous pouvez également créer des matières manuellement à l’aide de l’ombrage de Substance.

Sélectionnez simplement l’ombrage de Substance dans une couche de matériau et faites glisser la Substance à utiliser. L’étape suivante consiste à sélectionner le canal de sortie de la Substance à utiliser dans cet ombrage, et vous avez terminé.

Comme si :

![](../../../assets/cinema-4d-15.png){width="800px"}

Cette méthode offre une grande liberté de création et vous permet d’effectuer les opérations suivantes :

* Attribuez des canaux de sortie de Substance à des canaux de matériau Cinema 4D arbitraires. Il n&#39;est pas nécessaire de vous limiter à les utiliser uniquement dans les canaux prévus.
* Affectez une seule couche de sortie de Substance à plusieurs couches de matériau de Cinema 4D.
* Affectez des canaux de sortie de plusieurs Substances à un seul matériau de Cinema 4D.

## Restrictions

* Les images clés des paramètres d’entrée de Substance sont affichées dans le panneau Montage, mais pas dans le Powerslider de Cinema 4D (le curseur Montage sous les fenêtres).
* En raison d’une limitation, aucun profil colorimétrique personnalisé ne doit être utilisé sur les canaux de sortie de Substance.
* Dans certaines circonstances, les entrées d’image des Substances se rompent\
  La commande Fusionner... de Cinema 4D, qui combine deux scènes en une seule. Cela se produit si la scène à fusionner comporte des Substances situées dans son répertoire de projet avec des entrées d’image faisant référence à des images du répertoire de projet. Dans ce cas, les entrées d’image devront ensuite être réassociées manuellement.
* Si les Substances se trouvent dans le dossier du projet (ou ailleurs dans le chemin de recherche global), elles ne fonctionnent pas dans Cineware. Dans ce cas, ils sont rendus rouges, comme si la Substance était manquante. Pour contourner ce problème, les archives de Substance de données doivent être stockées en dehors du répertoire du projet, de sorte qu’elles soient référencées par un chemin absolu. Vous pouvez utiliser le paramètre Filename pour modifier l’emplacement du fichier, une fois que les fichiers ont été déplacés en dehors du chemin du projet.
