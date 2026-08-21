---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-bake/common-issues/normal-map-has-strange-colorful-gradients.html"
breadcrumb-title: ''
description: Corrigez les dégradés de couleurs étranges dans les textures normales en vérifiant les normales du maillage, les groupes de lissage et le mappage UV.
helpx_creative_field: ""
helpx_description: bakers > Common Issues > Normal map has strange colorful gradients
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: La carte normale a d'étranges dégradés colorés
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 0%

---


# La carte normale a d&#39;étranges dégradés colorés

La sortie du boulanger est un ensemble de dégradés colorés très forts.

![](../../assets/color-gradient.png)


## Explication

Les dégradés colorés se produisent généralement lorsqu&#39;il y a une inadéquation entre le maillage à poly élevé et à poly faible au cours du processus de cuisson. Cette incohérence peut s’expliquer par la raison suivante :

* Les maillages à poly-élevé et à poly-faible-poly <b>ne se chevauchent pas</b> correctement l&#39;un l&#39;autre (voir l&#39;image ci-dessous).
* Le haut-poly est <b>géométrie manquante</b> que le bas-poly tente de couvrir.
* Le maillage à poly élevé ou à poly faible a des normales de vertex inversées.

Lorsque cela se produit, le processus de cuisson essaie de correspondre à une géométrie qui n&#39;existe pas, ce qui entraîne quelque chose de vide. Le boulanger remplit cette zone vide avec une couleur extraite des pixels voisins dans les textures qui crée le gradient coloré (sauf si <b>Diffusion</b> est désactivé).

## Solution

Etant donné les quelques raisons possibles qui conduisent à un non-recouvrement entre les mailles, quelques solutions doivent être envisagées :

* Veillez à figer/réinitialiser la transformation du maillage (réinitialiser x-form, etc.) pour vous assurer que tous les maillages sont cohérents
* Importez les maillages bas et haut-poly dans votre logiciel de modélisation 3D pour vérifier qu&#39;ils se chevauchent correctement
* Assurez-vous que votre convention de nommage est valide si vous utilisez la fonction [Correspondance par nom](../../features/matching-by-name/matching-by-name.md) (vous pouvez la vérifier en la cuisant au four, puis en consultant le fichier journal qui doit imprimer les noms de maillage).

### Exemple

Voici un exemple avec une sphère à poly élevé et à poly faible. À gauche, les maillages ne se chevauchent pas, car le haut-poly a été déplacé :

![](../../assets/baking-gradients.jpg)
