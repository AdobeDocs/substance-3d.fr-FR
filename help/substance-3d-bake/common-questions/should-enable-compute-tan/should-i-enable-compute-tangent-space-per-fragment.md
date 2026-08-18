---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-bake/common-questions/should-i-enable-compute-tangent-space-per-fragment.html"
breadcrumb-title: ''
description: Découvrez quand activer le calcul de l’espace tangent par fragment et comment cela affecte vos résultats d’ancrage.
helpx_creative_field: ""
helpx_description: bakers > Common Questions > Should I enable
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Dois-je activer
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 1%

---


# Dois-je activer « Calculer l’espace tangent par fragment » ?

>[!WARNING]
>
> **Question**
> 
> Que signifie le paramètre « Calculer l’espace tangent par fragment » et quelle est son utilisation ?

>[!NOTE]
>
> **Explication**
> 
> Lorsque cette option est activée, ce paramètre indique au boulanger d’effectuer le calcul de l’espace tangent dans l’ombrage de fragments (également appelé ombrage de pixels) au lieu de l’ombrage de sommets. Cela signifie que le calcul sera effectué par pixel au lieu d’être interpolé de sommet en sommet. Ces paramètres sont utilisés par le créateur de cartes standard pour savoir comment coder la texture. Il savait également lire la texture à l&#39;aide des ombrages.
> 
> L’activation ou la désactivation de ce paramètre nécessite généralement le recadrage des textures pour les synchroniser avec les fenêtres 3D et les moteurs de rendu (tels qu’Iray).

>[!NOTE]
>
> **Solution**
> 
> Selon le logiciel ou le moteur de jeu ciblé pour le rendu de la texture, ce paramètre peut être désactivé ou activé :
> 
> | *Logiciel* | *Calculer l&#39;espace tangent par fragment* |
> | --- | --- |
> | **Unreal Engine 4** | Activé |
> | **Unité** | Désactivé |
