---
description: Consultez les notes de mise à jour du module externe 3ds Max version 3.0.0 et ultérieure pour en savoir plus sur les nouvelles fonctionnalités, les améliorations et les correctifs de bogues.
title: 3Ds Max 3.1.0+
source-git-commit: 28a9d8cf7a4eed4163f99e8158c9cb8f9da88302
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 0%
---

# 3ds Max 3.1.0+

## 3ds Max 3.1.1

**Date de publication :** 18 novembre 2026

**Compatible avec :** 3ds Max 2025 et versions ultérieures

### Ajouté/Mis à jour

* Mise à jour de la Substance Engine (9.6.1.) y compris les correctifs de sécurité
* Prise en charge OpenPBR de 3ds Max 2025, 2026 et 2027 (Arnold et V-Ray)

### Limitations connues

* Poids d’émission : le paramètre poids_émission ne fait pas partie de la spécification de l’OpenPBR 1.1 et n’est pas connecté automatiquement. Après l&#39;application du flux de travail, définissez manuellement la valeur Poids d&#39;émission dans l&#39;OpenPBR si votre matériau utilise des émissions.
* Différences visuelles entre les systèmes de rendu : une certaine variation entre l’aperçu du matériau dans Substance 3D Designer et le rendu dans Arnold ou V-Ray est due à des différences dans l’implémentation de la spécification d’OpenPBR par chaque système de rendu et s’améliorera à mesure que les implémentations convergeront.
* Fichiers SBSAR exportés depuis Substance 3D Painter 12.2.0. ou une version antérieure peut ne pas se connecter correctement lors de l’utilisation d’un workflow OpenPBR

## 3ds Max 3.1.0

**Date de publication :** 18 novembre 2026

**Compatible avec :** 3ds Max 2024

### Ajouté/Mis à jour

* Mise à jour de la Substance Engine (9.6.1.) y compris les correctifs de sécurité
