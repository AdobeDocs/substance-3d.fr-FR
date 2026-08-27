---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/bakers-settings/ambient-occlusion.html"
breadcrumb-title: ''
description: Découvrez comment utiliser le baker Ambient occlusion pour générer des textures d’ombre ambiante à l’aide d’algorithmes accélérés par GPU.
helpx_creative_field: ""
helpx_description: bakers > Bakers Settings > Ambient Occlusion
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Occlusion ambiante
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 4%

---


# Occlusion ambiante

Le baker Ambient occlusion permet de bake une texture d’ombre ambiante. Ce baker utilise un algorithme rapide exécuté sur le GPU.

**Disponible dans :**

* Substance Designer
* Substance Automation Toolkit

>[!WARNING]
>
> * Ce baker peut ne pas être pris en charge sur les anciens GPU.
> * Le bake à haute résolution sur les GPU bas de gamme/mobiles peut entraîner un crash.

## Paramètres

| *Nom* | *Description* |
| --- | --- |
| **Carte des normales** | Fichier de map normal d&#39;entrée qui peut être utilisé pour fournir des détails de géométrie supplémentaires sur la surface du maillage à prendre en compte pendant le calcul du baker. Ce paramètre est facultatif. |
| **Espace universel** | Si cette option est activée, spécifiez que la map normal d’entrée est en Espace monde (au lieu de Repère tangent). Si aucune map normal d’entrée n’est fournie, ces paramètres sont ignorés/désactivés. |
| **Inverser la normale** | Calculer la courbe d&#39;ambient occlusion avec des normales inversées (peut être utilisé pour générer une map thickness). |
| **Utiliser les parties de Maillage non sélectionnées** | Utilisez les parties de maillage non sélectionnées du maillage pour bake le mappage d’ambient occlusion. |
| **Qualité** | Choisissez la qualité de la carte des Ambients occlusion. Plus la qualité est élevée, plus le calcul est lent.Valeurs disponibles :<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Faible</strong> (3 passes)</li><li data-preserve-html="true"><strong>Moyen</strong> (par défaut, 5 passes)</li><li data-preserve-html="true"><strong>Élevé</strong> (10 passes)</li><li data-preserve-html="true"><strong>Très élevé</strong> (16 passes)</li></ul> |
| **Biais De Précision** | Précision de l&#39;occlusion ambiante. Une valeur inférieure donnera une plus grande précision, mais peut produire des artefacts plus grands. |
| **Atténuation de la distance** | Diffusion de l’occlusion ambiante. |
