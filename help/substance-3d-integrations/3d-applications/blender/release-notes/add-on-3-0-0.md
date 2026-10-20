---
title: Module complémentaire Blender 3.0.0+
description: Liste des notes de mise à jour concernant le module externe Substance 3D pour Blender.
source-git-commit: aa5acd016cd1a55ab230d36352c4d3aa5514012a
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 0%
---

# Module complémentaire 3.0.0+

**Module complémentaire 3.1.0**.*Publié le : 12 octobre 2026*

**Module Complémentaire Blender :**

* &amp;lbrack ;Bug&amp;rbrack ; Le chemin de bibliothèque fixe ne fonctionne pas
* &amp;lbrack ; Bug&amp;rbrack ; Correction d&#39;un problème de contexte dans le multithreading, qui empêche le chargement/la mise à jour de SBSAR
* &amp;lbrack ;Bug&amp;rbrack ; Le format d&#39;exportation de Texture fixe est ignoré
* &amp;lbrack ; Performance&amp;rbrack ; Amélioration multiple des performances

**Outils d&#39;intégration de Substances (Moteur Substance à distance) :**

* &amp;lbrack ; Feature&amp;rbrack ; Mis à jour vers la Substance Engine 9.6.1
* &amp;lbrack ; Performance&amp;rbrack ; Dépendances mises à jour et plusieurs améliorations des performances

**Module complémentaire 3.0.1**.*Publié le : février 2026*

**Module complémentaire Blender :**

* Les valeurs min/max des paramètres &amp;lbrack ; Fixed&amp;rbrack ; ne fonctionnent pas
* La Taille physique &amp;lbrack ; Fixed&amp;rbrack ; ne fonctionne pas avec l&#39;échelle de scène personnalisée
* La Taille physique &amp;lbrack ; Fixed&amp;rbrack ; ne fonctionne pas avec des unités système non métriques
* &amp;lbrack ;Fixed&amp;rbrack ; Les cartes Clearcoat ne fonctionnent pas avec le mélangeur 4+
* &amp;lbrack ;Fixed&amp;rbrack ; La carte colorimétrique Clearcoat est manquante dans shader
* &amp;lbrack ; Fixed&amp;rbrack ; Mauvais libellé dans la définition du module complémentaire
* La Substance &amp;lbrack ;Fixed&amp;rbrack ; crash aléatoirement le SRE ( avec des valeurs de couleur float4)
* &amp;lbrack ; Fixe&amp;rbrack ; Les entrées d&#39;image ne s&#39;affichent pas dans la liste des paramètres
* &amp;lbrack ; Fixe&amp;lbrack ; Les entrées d&#39;image ne fonctionnent pas après la fermeture et la réouverture du mélangeur

**Outils d&#39;intégration de Substances (Moteur Substance à distance) :**

* Mettre à niveau à la version 3.0.1
* Suppression de l&#39;interface ABI C++11 pour la nouvelle compilation Linux