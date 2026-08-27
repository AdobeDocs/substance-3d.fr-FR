---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-integrations/game-engines/unity/unity-release-notes/unity-2-2-0.html"
breadcrumb-title: ''
description: Consultez les notes de mise à jour du plug-in Unity version 2.2.0 pour en savoir plus sur les nouvelles fonctionnalités, les améliorations et les correctifs de bogues.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unity > Unity Release Notes > Unity 2.2.0
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Unity 2.2.0
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '674'
ht-degree: 0%

---


# Unity 2.2.0

## Notes de mise à jour 2.2.0

**date de publication : 1/10/2019**

### Plug-in principal :

* Substance Engine mise à jour
* Amélioration de la stabilité du code
* **Prise en charge d’Unity 2018.3**
* Prise en charge de **.NET 4.x**
* Prise en charge des Substances Sources en 2018.3
* Le problème de coloration de la Substance Source a été résolu
* Le graphe et le matériau correspondant portent désormais le même nom d’objet
* Ajout d’améliorations de la lisibilité de l’interface utilisateur graphique d’habillage d’Unity Pro
* Ajout de la prise en charge des affectations de sortie du matériau
* Correction d’un bug lié à la gestion sRVB
* Correction d’un bug en raison duquel un utilisateur pouvait supprimer toutes les instances d’un graphe.
* Correction d’un bug en raison duquel la tentative de rendu des Substances lors de la modification des paramètres à l’exécution n’entraînait que le rendu de deux éléments à la fois
* Lors de l’importation d’un pack contenant d’anciens fichiers de Substance de données, le plug-in informe désormais l’utilisateur qu’il contient d’anciennes données de Substance de données et supprime les fichiers du pack lorsqu’Unity tente de les importer (l’utilisateur n’a donc pas besoin de tout supprimer manuellement s’il est entré en panne)
* Ajout d’un bouton « À propos de » dans le menu Substance pour afficher les informations de build liées au plug-in Substance
* Ajout d’info-bulles de survol de la souris dans l’interface graphique de la Substance pour afficher les noms des paramètres de Substance exposés
* Ajout de boutons de navigation dans l&#39;interface graphique de Substance pour créer des liens vers le graphe et les matériaux de Substance
* Ajout de nouvelles icônes pour le graphe/matériau/textures de Substance dans l’Explorateur de contenu
* Mise à jour des vignettes de Substance dans le navigateur de contenu
* Suppression du fichier .mat au début des noms de matériau de Substance
* Possibilité de renommer les graphes et matériaux de Substance ajoutée
* Lorsque vous modifiez la résolution du graphe de Substance, la fenêtre contextuelle Appliquer/Rétablir n’apparaît plus, ce qui force l’utilisateur à valider la modification à ce moment-là
* Correction d’un bug en raison duquel le processus de réflexion utilisait uniquement la résolution de Substance par défaut, au lieu d’une résolution définie par l’utilisateur.
* Ajout d’un avertissement de passage de souris à l’interface graphique de la Substance informant l’utilisateur si l’espace colorimétrique est défini sur Gamma
* Fonctionnalité modifiée des instances de graphe de Substance de données : les utilisateurs peuvent désormais créer des instances de graphe dans une Substance de données sans être invités pour chaque instance créée dans l&#39;interface utilisateur du graphe de Substance de données

### Scripts :

* Nous avons masqué certaines fonctions non destinées à la prise en charge des scripts
* Fonction ajoutée pour dupliquer les instances de graphe de Substance via le script : Duplicate()
* Fonction ajoutée pour interroger des informations d&#39;entrée procédurales via C#, qui renvoie un tableau d&#39;éléments &#39;InputProperties&#39; : GetInputProperties()
* Fonction ajoutée pour vérifier si une entrée existe dans un graphe, retourne true/false : HasInput(string inputName)
* Fonction ajoutée pour vérifier si une entrée visible est visible, renvoie true/false : IsInputVisible(string inputName)
* Le schéma de rendu a été repensé. À ce titre, RenderSubstancesAsync() a été abandonné et remplacé par graphName.RenderAsync()

## Problèmes connus :

**Module externe Core Substance**

* L’utilisateur doit désactiver « Activer le code en bits » dans le menu Paramètres de génération de Xcode pour générer pour iOS.
* Les aperçus d’objet de Substance dans l’Explorateur de contenu s’affichent en noir lorsque la cible de la build est définie sur Android/iOS
* Le bouton d’Alpha et le curseur d’aperçu Mappage sont manquants dans l’interface graphique de la texture autre que la Substance après l’importation du module externe de Substance
* L’utilisateur doit utiliser des puissances de deux pour définir une résolution de graphe de Substance à l’aide d’un script
* Les matériaux de Substance ne sont pas persistants lorsqu’ils sont exportés/importés à l’aide d’un package Unity
* Les Substances ne fonctionnent pas avec les offres groupées de ressources
* Les icônes d’aperçu de Substance dans l’Explorateur d’actifs deviennent toutes l’icône Substance S après une réimportation
* Si vous renommez un graphe de Substance comportant un matériau dans la scène, ce matériau sera supprimé des objets sur lesquels il est placé
* (Mac uniquement) La mise à jour du plug-in sur Mac supprime les matériaux de Substance des préfabs dans la scène|

**Scripts**

* Les scripts ne fonctionnent pas à l’exécution si le projet est défini sur x86 dans les paramètres de génération
* Problèmes d’utilisation du back-end de script il2cpp avec certaines plateformes de build

**Substance Painter Live Link**

* La création d’un projet après avoir peint avec Substance Live Link rétablit le maillage peint à un matériau par défaut
* Canal AO non envoyé avec Painter Live Link
* Les maillages avec plusieurs matériaux ne fonctionnent pas dans Unity Live Link
* La façon dont Unity LiveLink utilise SimpleJson entre en conflit avec d’autres instances de SimpleJson dans un projet
