---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/3d-applications/3ds-max/3ds-max-scripting-api.html"
breadcrumb-title: ''
description: Documentation de référence de l’API de script Substance 3ds Max pour l’automatisation des opérations sur le matériel.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > 3ds Max > 3ds MAX Scripting API
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: API de scripts 3ds MAX
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '895'
ht-degree: 2%

---


# API de scripts 3ds MAX

Vous trouverez ci-dessous la liste des commandes et des propriétés du nœud Substance 2.

## Propriétés :

| Propriété | Description | Type |
| --- | --- | --- |
| nom | Nom du nœud Substance 2. La valeur par défaut est « Substance 2 » | Chaîne |

## Commandes :

| Commande | Description | Renvoyer | Type de valeur renvoyé : | Paramètre |
| --- | --- | --- | --- | --- |
| getCurrentPackageName | Obtient le nom de fichier de base du package chargé (fichier sbsar chargé dans le nœud de graphe) | Nom de fichier (sans le répertoire de préfixe) du package chargé (fichier sbsar) | Chaîne |  |
| getCurrentGraphName | Obtenir le nom du graphique actuel | identifiant de l&#39;instance de graphe actuelle | Chaîne |  |
| getOutoutputsNamesFromCurrentGraph | Obtenir la liste des noms d&#39;utilisation des sorties pour les sorties activées | Tableau contenant la liste des noms de canal pour les sorties activées | Liste |  |
| getPresetIdentifiers | Obtenir la liste des paramètres prédéfinis à partir du graphique de Substance | Tableau contenant la liste des identificateurs de chaîne pour tous les paramètres prédéfinis | Liste |  |
| setPackageAndGraphNames | Chargement d’un fichier sbsar à partir du disque dans le nœud de graphe | Vrai en cas de réussite, faux en cas d&#39;échec | Booléen | ***Paramètre de chaîne*** : **substancePackageFilePath** Chemin d&#39;accès au fichier sbsar sur le disque ***Paramètre de chaîne*** : **graphInstanceNameToSelect** Identificateur de chaîne du graphique |
| setInputInt | Définir une entrée entière avec une nouvelle valeur |  |  | ***Paramètre entier*** : **valeur** Valeur entière pour définir l&#39;entrée sur ***Paramètre String*** : **inputIdentifier** Identificateur de chaîne unique de l&#39;entrée |
| setInputFloat | Définir une entrée flottante avec une nouvelle valeur |  |  | ***Paramètre Float*** : **valeur** Valeur float pour définir l&#39;entrée sur ***Paramètre String*** : **inputIdentifier** Identificateur de chaîne unique de l&#39;entrée |
| setInputString | Définir une entrée de chaîne avec une nouvelle valeur |  |  | ***Paramètre de chaîne*** : **valeur** Valeur de chaîne pour définir l&#39;entrée sur ***Paramètre de chaîne*** : **inputIdentifier** Identificateur de chaîne unique de l&#39;entrée |
| setInputBool | Définir une entrée booléenne avec une nouvelle valeur |  |  | ***Paramètre booléen :* valeur &#x200B;** Valeur booléenne pour définir l&#39;entrée sur&#x200B;***Paramètre String &#x200B;*** : **inputIdentifier** Identificateur de chaîne unique de l&#39;entrée |
| setInputVec2 | Définir une entrée vectorielle avec deux éléments |  |  | Paramètre ***Point2 :**&#x200B;***valeur** Valeur maximale de point2 pour définir l&#39;entrée sur ***Paramètre String &#x200B;*** : **inputIdentifier** Identificateur de chaîne unique de l&#39;entrée |
| setInputVec3 | Définition d’une entrée vectorielle avec trois éléments |  |  | Paramètre ***Point3 :* valeur &#x200B;** valeur maximale de point3 pour définir l&#39;entrée sur le paramètre&#x200B;***String &#x200B;*** : **inputIdentifier** identificateur de chaîne unique de l&#39;entrée |
| setInputVec4 | Définition d’une entrée vectorielle avec quatre éléments |  |  | Paramètre ***Point4*** : **valeur** valeur maximale de point4 pour définir l&#39;entrée sur ***Paramètre de chaîne :* inputIdentifier &#x200B;** Identificateur de chaîne unique de l&#39;entrée |
| setInputColor | Définir une entrée de couleur avec une nouvelle valeur |  |  | ***Paramètre de couleur*** : **valeur** valeur de couleur maximale pour définir l&#39;entrée sur ***Paramètre de chaîne :* inputIdentifier &#x200B;** Identificateur de chaîne unique de l&#39;entrée |
| setInputComboSelection | Définir la valeur actuellement sélectionnée dans une entrée de zone de liste déroulante |  |  | ***Paramètre entier*** : **valeur** Index du widget de zone de liste déroulante ***Paramètre String*** : **inputIdentifier** Identificateur de chaîne unique de l&#39;entrée |
| getInputInt | Obtention de la valeur d&#39;entrée d&#39;un type d&#39;entrée entier | Valeur entière actuelle de l&#39;entrée | Entier | ***Paramètre de chaîne :* inputIdentifier &#x200B;** Identificateur de chaîne unique de l&#39;entrée |
| getInputFloat | Obtention de la valeur d’entrée pour un type d’entrée flottante | Valeur flottante actuelle de l&#39;entrée | Flottant | ***Paramètre de chaîne :* inputIdentifier &#x200B;** Identificateur de chaîne unique de l&#39;entrée |
| getInputString | Obtention de la valeur d&#39;entrée pour un type d&#39;entrée de chaîne | Valeur de chaîne actuelle de l&#39;entrée | Chaîne | ***Paramètre de chaîne :* inputIdentifier &#x200B;** Identificateur de chaîne unique de l&#39;entrée |
| getInputBool | Obtention de la valeur d&#39;entrée d&#39;un type d&#39;entrée booléen | Valeur booléenne actuelle de l&#39;entrée | Booléen | ***Paramètre de chaîne :* inputIdentifier &#x200B;** Identificateur de chaîne unique de l&#39;entrée |
| getInputVec2 | Obtention de la valeur d’entrée pour un type d’entrée point2 | Valeur maximale actuelle de point2 de l’entrée | Point2 | ***Paramètre de chaîne :* inputIdentifier &#x200B;** Identificateur de chaîne unique de l&#39;entrée |
| getInputVec3 | Obtention de la valeur d’entrée pour un type d’entrée point3 | Valeur maximale actuelle de point3 de l’entrée | Point3 | ***Paramètre de chaîne :* inputIdentifier &#x200B;** Identificateur de chaîne unique de l&#39;entrée |
| getInputVec4 | Obtient la valeur d&#39;entrée pour un type d&#39;entrée point4 | Valeur maximale actuelle de point4 de l’entrée | Point4 | ***Paramètre de chaîne :* inputIdentifier &#x200B;** Identificateur de chaîne unique de l&#39;entrée |
| getInputColor | Obtention de la valeur d’entrée d’un type d’entrée de couleur | Valeur actuelle de l’entrée en tant que couleur | Couleur | ***Paramètre de chaîne :* inputIdentifier &#x200B;** Identificateur de chaîne unique de l&#39;entrée |
| getInputComboSelection | Obtenir l&#39;index de la sélection de la zone de liste déroulante en fonction de l&#39;identificateur | Index de l’élément de zone de liste déroulante sélectionné | Entier | ***Paramètre de chaîne :* inputIdentifier &#x200B;** Identificateur de chaîne unique de l&#39;entrée |
| getMaterialDependentCount | Obtention du nombre de dépendances de matière | Nombre de références dépendantes d&#39;un type de matière | Entier |  |
| ApplyValuesToSelectedPreset | Remplace le paramètre prédéfini actuellement sélectionné par les valeurs d’entrée actuelles |  |  |  |
| RemoveAllPresets | Supprime tous les paramètres prédéfinis du nœud de graphe actuel |  |  |  |
| Créer un paramètre prédéfini | Créer un nouveau paramètre prédéfini à partir des entrées actuelles |  |  | ***Paramètre de chaîne :* newPresetName &#x200B;** Nom d&#39;affichage du nouveau paramètre prédéfini |
| RemoveOnePreset | Supprimer le paramètre prédéfini portant le nom donné |  |  | ***Paramètre de chaîne :* selectedPresetName &#x200B;** Nom du paramètre prédéfini à supprimer |
| Importer le paramètre prédéfini | Importez le fichier sbsprs dans les paramètres prédéfinis actuels |  |  | ***Paramètre de chaîne :**&#x200B;***filePath** Chaîne contenant le chemin du fichier à partir duquel importer le paramètre prédéfini |
| ExportPreset&#x200B;**\*deprecated** À supprimer dans 2.5.0\* | Exporter le paramètre prédéfini actuellement sélectionné vers un fichier sbsprs |  |  | ***Paramètre de chaîne*** : chaîne **filePath** contenant le chemin du fichier vers lequel exporter le paramètre prédéfini |
| exportPresetList | Exporter les paramètres prédéfinis donnés dans un seul fichier de paramètres prédéfinis |  |  | ***Paramètre de chaîne*** : **filePath** chaîne contenant le chemin du fichier pour exporter les paramètres prédéfinis vers le paramètre *** liste*** : **paramètres prédéfinis** liste contenant les noms des paramètres prédéfinis à exporter |
| BakeOutoutputsOfSelectedGraph | Convertir en disque les bitmaps de l’instance de graphique sélectionnée |  |  | ***Paramètre de chaîne :* filePath &#x200B;** Le répertoire du chemin racine dans lequel écrire les images dans le paramètre&#x200B;***String &#x200B;*** : **imageFormatExtension** L&#39;extension/le format de fichier dans lequel écrire les images |
