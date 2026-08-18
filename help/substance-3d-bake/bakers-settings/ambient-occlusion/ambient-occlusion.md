---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/bakers-settings/ambient-occlusion.html"
breadcrumb-title: ''
description: Apprenez à utiliser Ambient Occlusion baker pour générer des textures d’ombre ambiante à l’aide d’algorithmes accélérés par GPU.
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

Le boulanger d&#39;Occlusion ambiante permet de cuire une texture d&#39;ombre ambiante. Ce boulanger utilise un algorithme rapide exécuté sur le GPU.

**Disponible dans :**

* Substance Designer
* Substance Automation Toolkit

>[!WARNING]
>
> * Ce boulanger n’est peut-être pas pris en charge sur les anciens GPU.
> * La cuisson à haute résolution sur des GPU bas de gamme/mobiles peut entraîner un blocage.

## Paramètres

| *Nom* | *Description* |
| --- | --- |
| **Carte des normales** | Saisissez un fichier de courbe de normales qui peut être utilisé pour fournir des détails de géométrie supplémentaires sur la surface du maillage à prendre en compte lors du calcul de Baker. Ce paramètre est facultatif. |
| **Espace universel** | Si cette option est activée, spécifiez que la carte normale d&#39;entrée est dans l&#39;espace universel (au lieu de l&#39;espace tangent). Si aucun mappage normal d&#39;entrée n&#39;est fourni, ces paramètres sont ignorés/désactivés. |
| **Inverser la normale** | Calculer la courbe d&#39;occlusion ambiante avec des normales inversées (peut être utilisé pour générer une courbe de thickness). |
| **Utiliser des parties de filet non sélectionnées** | Utilisez les parties de filet non sélectionnées du filet pour former la carte d’occlusion ambiante. |
| **Qualité** | Choisissez la qualité de la carte d’Occlusion ambiante. Plus la qualité est élevée, plus le calcul est lent.Valeurs disponibles :<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Faible</strong> (3 passes)</li><li data-preserve-html="true"><strong>Moyen</strong> (par défaut, 5 passes)</li><li data-preserve-html="true"><strong>Élevé</strong> (10 passes)</li><li data-preserve-html="true"><strong>Très élevé</strong> (16 passes)</li></ul> |
| **Biais De Précision** | Précision de l&#39;occlusion ambiante. Une valeur inférieure donnera une plus grande précision, mais peut produire des artefacts plus grands. |
| **Atténuation de la distance** | Diffusion de l’occlusion ambiante. |
