---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-bake/common-questions/should-i-enable-compute-tangent-space-per-fragment.html"
breadcrumb-title: ''
description: Découvrez quand activer l’espace de tangente de calcul par fragment et comment cela affecte vos résultats de baking.
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


# Dois-je activer « Calculer l’espace de tangente par fragment » ?

>[!WARNING]
>
> **Question**
> 
> Que signifie le paramètre « Calculer l’espace de tangente par fragment » et quelle est son utilisation ?

>[!NOTE]
>
> **Explication**
> 
> Lorsque cette option est activée, ce paramètre indique au baker d’effectuer le calcul de Repère tangent dans le Shader de fragments (également appelé Shader de pixels) au lieu du Shader de Vertex. Cela signifie que le calcul sera effectué par pixel au lieu d’être interpolé de vertex en vertex. Ces paramètres sont utilisés par le baker de map normal pour savoir comment coder la texture. Il savait aussi lire la texture par les shaders.
> 
> L’activation ou la désactivation de ce paramètre nécessite généralement de redéfinir les textures pour les synchroniser avec les viewports et moteurs de rendu 3D (tels que Iray).

>[!NOTE]
>
> **Solution**
> 
> Selon le logiciel ou le moteur de jeu ciblé pour le rendu de la texture, ce paramètre peut être désactivé ou activé :
> 
> | *Logiciel* | *Calculer l&#39;espace de tangente par fragment* |
> | --- | --- |
> | **Moteur irréel 4** | Activé |
> | **Unité** | Désactivé |
