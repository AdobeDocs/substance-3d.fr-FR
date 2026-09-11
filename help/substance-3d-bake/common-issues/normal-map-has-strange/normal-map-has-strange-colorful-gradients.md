---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/common-issues/normal-map-has-strange-colorful-gradients.html"
breadcrumb-title: ''
description: Corrigez les dégradés colorés étranges dans les maps normal en vérifiant les normales du maillage, les groupes de lissage et le mappage UV.
helpx_creative_field: ""
helpx_description: bakers > Common Issues > Normal map has strange colorful gradients
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: La map normal a d’étranges dégradés colorés
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 0%

---


# La map normal a d’étranges dégradés colorés

Le résultat du baker est un ensemble de dégradés colorés très forts.

![](../../assets/color-gradient.png)


## Explication

Les dégradés colorés se produisent généralement lorsqu’il y a une incompatibilité entre le maillage à poly élevé et à poly faible au cours du processus de baking. Cette incompatibilité peut s’expliquer par la raison suivante :

* Les maillages en haut et en bas de gamme <b>ne se chevauchent pas</b> correctement (voir l&#39;image ci-dessous).
* Le polygone de niveau élevé est à <b>géométrie manquante</b> que le polygone de niveau inférieur tente de couvrir.
* Le maillage à poly élevé ou à poly faible a des normales de vertex inversées.

Lorsque cela se produit, le processus de baking tente de faire correspondre une géométrie qui n&#39;existe pas, ce qui crée quelque chose de vide. Le baker remplit cette zone vide avec une couleur extraite des pixels voisins dans les textures qui crée le dégradé coloré (sauf si <b>Diffusion</b> est désactivée).

## Solution

Étant donné les quelques raisons possibles qui conduisent à un non-chevauchement entre les maillages, quelques solutions doivent être envisagées :

* Assurez-vous de figer/réinitialiser la transformation du maillage (réinitialiser l’œil, etc.) pour vous assurer que tous les maillages sont cohérents
* Importez les maillages low et high-poly dans votre logiciel de modélisation 3D pour vérifier qu’ils se chevauchent correctement
* Assurez-vous que votre convention de dénomination est valide si vous utilisez la fonction [Correspondance par nom](../../features/matching-by-name/matching-by-name.md) (vous pouvez la vérifier en bakant, puis en examinant le fichier journal qui doit imprimer les noms de maillage).

### Exemple

Vous trouverez ci-dessous un exemple avec une sphère à poly élevé et une sphère à poly faible. Sur la gauche, les maillages ne se chevauchent pas car le high-poly a été déplacé :

![](../../assets/baking-gradients.jpg)
