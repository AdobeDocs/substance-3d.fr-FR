---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/guides/error-and-warning-messages.html"
breadcrumb-title: ''
description: Guide de référence pour tous les messages d'erreur et d'avertissement qui peuvent apparaître lors de la cuisson avec le logiciel Substance.
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

Ci-dessous se trouve la liste de tous les messages d&#39;erreur qui peuvent apparaître lors de la cuisson avec le logiciel Substance.

## Tous boulangers

| *Message* | *Description* |
| --- | --- |
| Baker non disponible. | Ce message d’erreur est généralement suivi de messages d’erreur supplémentaires, souvent liés à des problèmes de GPU. Cela peut se produire si le GPU est trop ancien et ne répond pas aux [exigences techniques](https://www.allegorithmic.com/products/tech-specs) du logiciel. |
| L&#39;ensemble UV [X] n&#39;existe pas. | Le Baker a essayé de travailler avec un ensemble UV donné qui n&#39;est pas présent dans le maillage bas-poly. |
| Impossible de charger la scène à partir de l’URL. | Ce message signifie que le boulanger n&#39;a pas pu charger le fichier mesh, généralement le maillage poly élevé. Quelques raisons peuvent être à l’origine de ce message :<ul data-preserve-html="true"><li data-preserve-html="true">Le fichier de maillage référencé n&#39;existe plus.</li><li data-preserve-html="true">Le fichier maillé est endommagé ou endommagé et ne peut pas être lu.</li><li data-preserve-html="true">Le maillage est en cours de modification par une autre application et ne peut pas être lu.</li></ul> |

## UV à SVG Baker

| *Message* | *Description* |
| --- | --- |
| Impossible de trouver des UV pour le maillage [nom du maillage]. | Aucun UV n&#39;a été trouvé pour un maillage spécifique. Cela peut se produire si plusieurs filets sont importés, mais que seuls quelques-uns d&#39;entre eux ont des UV. |
| La scène n&#39;a pas d&#39;UV. Annulation de la cuisson. | Si aucun maillage de la scène ne comporte d&#39;UV, le processus de cuisson est annulé. |

## Position Baker

| *Message* | *Description* |
| --- | --- |
| Le maillage [nom du maillage] n&#39;a pas de position. | Le maillage poly bas n&#39;a pas de position de sommet. |
| Le maillage [nom du maillage] n&#39;a pas d&#39;UV pour le jeu d&#39;uv [X]. | Le Baker a essayé de travailler avec un ensemble UV donné qui n&#39;est pas présent dans le maillage bas-poly. |

## N&#39;importe quel boulanger « From Mesh »

| *Message* | *Description* |
| --- | --- |
| Impossible de trouver des normales de sommet dans le maillage [nom du maillage]. | Aucune normale de sommet n&#39;a été trouvée dans le maillage donné. Normalement, cela n&#39;arrive jamais car les normales de vertex sont recalculées si le maillage ne les contient pas. Cela peut se produire en raison d’un plug-in d’espace tangent personnalisé défectueux. |
| Impossible de trouver les tangentes de sommet dans le maillage [nom du maillage]. | Comme ci-dessus. |
| Impossible de trouver les binormales de vertex dans le maillage [nom du maillage]. | Comme ci-dessus. |
| Couleurs de sommet introuvables dans le maillage [nom du maillage]. | Aucune couleur de sommet n&#39;a été trouvée dans le maillage donné. Cela peut se produire si aucune couleur de sommet n&#39;est définie pour au moins un sous-maillage du maillage à polygone élevé. |
| Pas assez de données dans le poly élevé pour utiliser le boulanger sélectionné. Abandon de la cuisson. | Précédé d&#39;au moins un des messages ci-dessus. Normalement, si seulement un peu de données est manquant dans la scène (par exemple : un seul maillage de la scène high poly n&#39;a pas de couleurs de sommet), le processus de cuisson remplit les données manquantes avec des zéros, et continue la cuisson. S’il manque trop de données, ce message est généré et le processus de cuisson est arrêté. |

## Texture Transférée Du Maillage

| *Message* | *Description* |
| --- | --- |
| Échec du chargement de la texture du détail. | Impossible de charger la texture définie dans les paramètres de boulangerie. Cela peut être dû au fait que le fichier est manquant sur le disque ou qu’il est corrompu et non lisible. |
