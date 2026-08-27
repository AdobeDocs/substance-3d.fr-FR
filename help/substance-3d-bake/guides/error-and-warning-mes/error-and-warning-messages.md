---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-bake/guides/error-and-warning-messages.html"
breadcrumb-title: ''
description: Guide de référence pour tous les messages d’erreur et d’avertissement qui peuvent apparaître lors de la cuisson avec un logiciel de Substance.
helpx_creative_field: ""
helpx_description: bakers > Guides > Error and Warning Messages
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Messages d’erreur et d’avertissement
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '502'
ht-degree: 0%

---


# Messages d’erreur et d’avertissement

Vous trouverez ci-dessous la liste de tous les messages d’erreur qui peuvent s’afficher lors de l’utilisation d’un logiciel de Substance.

## Tous les boulangers

| *Message* | *Description* |
| --- | --- |
| Baker non disponible. | Ce message d’erreur est généralement suivi de messages d’erreur supplémentaires, souvent liés à des problèmes de GPU. Cela peut se produire si le GPU est trop ancien et ne répond pas aux [exigences techniques](https://www.allegorithmic.com/products/tech-specs) du logiciel. |
| Le jeu UV [X] n&#39;existe pas. | Le Baker a essayé de travailler avec un ensemble UV donné qui n&#39;est pas présent dans le maillage de bas-poly. |
| Impossible de charger la scène à partir de l’URL. | Ce message signifie que le boulanger n&#39;a pas pu charger le fichier mesh, généralement le mesh high poly. Ce message peut provenir de plusieurs raisons :<ul data-preserve-html="true"><li data-preserve-html="true">Le fichier de maillage référencé n&#39;existe plus.</li><li data-preserve-html="true">Le fichier de filet est corrompu ou endommagé et ne peut pas être lu.</li><li data-preserve-html="true">Le filet est en cours de modification par une autre application et ne peut pas être lu.</li></ul> |

## Baker UV à SVG

| *Message* | *Description* |
| --- | --- |
| Impossible de trouver des UV pour le filet [nom du filet]. | Aucun UV n&#39;a été trouvé pour un maillage spécifique. Cela peut se produire si plusieurs maillages sont importés, mais que seuls quelques-uns d’entre eux ont des UV. |
| La scène n&#39;a pas d&#39;UV. Annulation du bake. | Si aucun maillage de la scène n’a d’UV, le processus de bake est annulé. |

## Baker de position

| *Message* | *Description* |
| --- | --- |
| Le maillage [nom du maillage] n’a pas de postes. | Le maillage low poly n&#39;a pas de positions sur le vertex. |
| Le maillage [nom du maillage] n&#39;a pas d&#39;UV pour le jeu d&#39;UV [X]. | Le Baker a tenté de travailler avec un Ensemble d&#39;UV donné qui n&#39;est pas présent dans le maillage à faible niveau de poly. |

## Tout Baker « Du Maillage »

| *Message* | *Description* |
| --- | --- |
| Normales du vertex introuvables dans le maillage [nom du maillage]. | Aucune normale de vertex n&#39;a été trouvée dans le maillage donné. Normalement, cela ne se produit jamais, car les normales de vertex sont recalculées si le maillage ne les a pas. Cela pourrait peut-être se produire en raison d&#39;un plugin de repère tangent personnalisé défectueux. |
| Tangentes de vertex introuvables dans le maillage [nom du maillage]. | Comme ci-dessus. |
| Impossible de trouver des valeurs binormales de vertex dans le maillage [nom du maillage]. | Comme ci-dessus. |
| Couleurs de vertex introuvables dans le maillage [nom du maillage]. | Aucune couleur de vertex n&#39;a été trouvée dans le maillage donné. Cela peut se produire si au moins un sous-maillage du maillage High-poly n’a pas de couleurs de vertex définies. |
| Données insuffisantes dans le poly élevé pour utiliser le baker sélectionné. Abandon de la cuisson. | précédée d&#39;au moins un des messages ci-dessus. Normalement, si seule une partie des données est manquante dans la scène (par exemple : un seul filet dans une scène High poly n&#39;a pas de couleurs de sommet), le processus de cuisson remplit les données manquantes avec des zéros, et continue la cuisson. Si trop de données sont manquantes, ce message est généré et le processus de boulangerie est arrêté. |

## Texture Transférée À Partir Du Filet

| *Message* | *Description* |
| --- | --- |
| Échec du chargement de la texture détaillée. | Impossible de charger la texture définie dans les paramètres du boulanger. Cela peut être dû au fait que le fichier est manquant sur le disque ou qu’il est corrompu et illisible. |
