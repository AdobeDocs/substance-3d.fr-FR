---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unreal-engine/unreal-engine-5/plugin-settings-ue5.html"
breadcrumb-title: ''
description: Configurez les paramètres du plug-in Substance dans Unreal Engine 5 via les paramètres du projet pour personnaliser le comportement du plug-in.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unreal Engine > Unreal Engine 5 > Plugin Settings - UE5
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Paramètres du plug-in - UE5
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 0%

---


# Paramètres du plug-in - UE5

Pour accéder aux paramètres, accédez à Modifier > Paramètres du projet, faites défiler jusqu’à la catégorie Plug-ins et cliquez sur Substance.

![](../../../../assets/screen-shot-2022-03-31-at-5-50-29-pm.png)

## Budget matériel

Le budget mémoire est la quantité maximale de mémoire à utiliser pour le moteur de Substance de données. Peut être augmenté pour améliorer la vitesse de traitement des Substances, mais consommera plus de ressources système. (Pas toujours une augmentation utile au niveau du projet).

Les cœurs du processeur déterminent le nombre de cœurs que le moteur de Substance de données peut utiliser. Cela inclut les cœurs physiques et les hyper-threads. (Si le nombre attribué est supérieur aux cœurs disponibles sur un système, tous les cœurs disponibles seront utilisés par défaut.

## Cuisiner

Le comptage des niveaux de mélange supprimé pendant la cuisson modifiera la façon dont les textures sont créées pour un pack. Ce paramètre peut considérablement améliorer les temps de chargement et réduire la taille du package, car les niveaux de texture plus élevés n’auront plus besoin d’être chargés. La plus faible résolution / plus petite LOD sera chargée et la plus élevée sera définie par défaut par UE5. Les Substances sont ensuite traitées par le moteur de Substance et mises à jour au moment de l&#39;exécution avec les LOD haute résolution.

La Substance Engine peut être CPU ou GPU. Le moteur GPU vous permettra de créer des textures 4K. Le moteur CPU est limité à 2 K.

## Optimisation :

Cela limite le nombre de substances asynchrones pouvant être transmises au moteur Substance par lot. Des valeurs basses accélèrent la rapidité d’exécution d’une tâche asynchrone et sa mise à jour, les valeurs élevées effectuant des rendus par lots et traitant plusieurs Substances à la fois. Plus le nombre de mises à jour est élevé, plus la texture devient saccadée, car l’intervalle de temps entre les mises à jour est long.

## Rendu asynchrone/synchronisé

Le rendu de synchronisation est un appel de rendu bloquant. Une instance de graphique de Substance est alors transmise au moteur de Substance de données pour être recalculée, mais l’exécution s’arrête jusqu’à ce que le moteur de Substance de données ait terminé de traiter la Substance de données avant de poursuivre l’exécution du code. Le résultat sera également mis à jour sur votre écran dès que le processus sera terminé.

Async ajoute votre graphique à une file d’attente et envoie plusieurs graphiques au moteur de Substance de données à la fois (définis dans les paramètres de Substance de données) dans la mise à jour du plug-in. Contrairement au rendu de synchronisation, dès qu’ils sont envoyés, le programme continue de fonctionner comme d’habitude au lieu d’attendre que le moteur de Substance de données soit terminé. Lorsque le moteur de Substance a terminé ce lot, il renvoie les résultats, nous les appliquons aux sorties et nous lançons un autre lot.
