---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-integrations/game-engines/unreal-engine/unreal-engine-5/material-template-usage-ue5.html"
breadcrumb-title: ''
description: Créez et utilisez des modèles de matériau dans Unreal Engine 5 pour définir la façon dont les nœuds de sortie de Substance se connectent aux entrées de matériau.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unreal Engine > Unreal Engine 5 > Material Template Usage - UE5
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Utilisation du modèle de matériau - UE5
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 0%

---


# Utilisation du modèle de matériau - UE5

Les modèles de matériau permettent à l&#39;utilisateur de créer un matériau de base pour les substances à utiliser comme modèle pour connecter leurs nœuds de sortie aux entrées dans le matériau.\
Les sorties partageant le même nom et le même type qu&#39;une entrée de matériau seront automatiquement utilisées. Cet exemple de matériau parent comporte un nœud d’échantillon de texture « baseColor » qui sera rempli si la Substance comporte une sortie de texture également nommée « baseColor ».\
![](../../../../assets/parent-material-sample.png)

Les sorties de Substance prennent en charge la mise à jour des textures, des valeurs scalaires int ou flottantes et des valeurs vectorielles (2-4). Pour utiliser des sorties float ou int à l&#39;exécution, vous devez obtenir dynamicMaterialInstance à partir du graphique, car constantMaterialInstances (tous les matériaux générés dans l&#39;éditeur) ne peut pas modifier les valeurs scalaires à l&#39;exécution.

![](https://helpx-prod.scene7.com/is/image/HelpxProd/scalar-value?$png$&jpegSize=100&wid=245)

L’instance de graphe de substance tente de renseigner toutes les valeurs de sortie pertinentes au moment de la création.

![](https://helpx-prod.scene7.com/is/image/HelpxProd/screen-shot-2022-04-01-at-4-38-31-pm?$png$&jpegSize=200&wid=1076)
