---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unity.html"
breadcrumb-title: ''
description: Importez et utilisez des matériaux de Substance dans le moteur de jeu Unity avec prise en charge des plug-ins natifs et contrôle des paramètres d’exécution.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unity
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Unité
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '743'
ht-degree: 0%

---


# Unité

![](../../assets/unity.png)

>[!NOTE]
>
> **Versions Prises En Charge Par Unity**
> 
> La version 3.0.0 du plug-in Adobe Substance 3D pour Unity prend actuellement en charge Unity 2020.3.27x et les versions ultérieures. Il peut être téléchargé à partir du [Unity Asset Store](https://assetstore.unity.com/packages/tools/utilities/substance-3d-for-unity-beta-213208).

>[!WARNING]
>
> Avant de mettre à niveau ou d&#39;utiliser le plug-in, vérifiez la [page du projet de mise à niveau](https://helpx.adobe.com/substance-3d/unlisted/documentation/integrations/upgrading-projects-182256244.html).

>[!WARNING]
>
> Assurez-vous de consulter la page [Directives d&#39;optimisation](../../game-engines/unity/optimization-guidelines/optimization-guidelines.md) avant de créer des documents de Substance personnalisés.

## Table des matières

* [Notes de mise à jour d’Unity](https://helpx.adobe.com/substance-3d/unlisted/documentation/integrations/beta-release-information-170460277.html) — Nouveautés de la Substance du plug-in Unity par version
* [Téléchargement du plug-in Substance 3D dans Unity](../../game-engines/unity/downloading-plugin-unity/downloading-substance-3d-plugin-in-unity.md) : Adobe Substance 3D pour Unity est disponible sur le site Unity Asset Store https://assetstore.unity.com/packages/tools/utilities/substance-in-unity-110555.
* [Présentation du plug-in Unity](../../game-engines/unity/unity-plugin-overview/unity-plugin-overview.md)
* [Préférences Unity](../../game-engines/unity/unity-preferences/unity-preferences.md) : la fenêtre des préférences de Substance de données vous permet de définir des options définies par l’utilisateur pour le plug-in.
* [Directives d&#39;optimisation](../../game-engines/unity/optimization-guidelines/optimization-guidelines.md) — Lorsque vous créez vos propres matériaux de Substance personnalisés, veillez à respecter les directives d&#39;optimisation ci-dessous.
* [Mise à niveau de projets/Problèmes connus](https://helpx.adobe.com/substance-3d/unlisted/documentation/integrations/upgrading-projects-182256244.html) — Problèmes connus avec la Substance dans le plug-in Unity
* [Gestion des Graphes Substance](https://helpx.adobe.com/substance-3d/unlisted/documentation/integrations/managing-and-navigating-substance-graphs-170459636.html) : vous pouvez créer de nouveaux matériaux à partir du matériau de Substance à l&#39;aide du Gestionnaire de Graphes Substance (SGM)
* [Modification des paramètres](../../game-engines/unity/changing-parameters/changing-parameters.md) : les paramètres du matériau de Substance sont accessibles sur l&#39;objet de Graphe Substance (SGO).
* [Textures générées (par Packing)](../../game-engines/unity/generated-textures-pac/generated-textures-packing.md) : les textures générées affichent les sorties de la Substance calculées par la Substance Engine de création des textures
* [Rendu de l&#39;espace colorimétrique](../../game-engines/unity/rendering-color-space/rendering-color-space.md) : pour obtenir de meilleurs résultats, vous devez définir l&#39;espace colorimétrique sur linéaire dans les paramètres d&#39;Unity Player.
* [Utilisation des entrées d’image](../../game-engines/unity/using-image-inputs/using-image-inputs.md)
* [Publication pour mobile](../../game-engines/unity/publishing-for-mobile/publishing-for-mobile.md) : directives de publication sur les plateformes mobiles
* [Substance 3D pour Unity Scripting](../../game-engines/unity/3d-for-unity-scripting/substance-3d-for-unity-scripting.md) : à l&#39;aide de l&#39;API de Substance de données, vous pouvez écrire des scripts pour mettre à jour et modifier les paramètres de Substance de données lors de l&#39;exécution.
* [Création de scripts dans Unity (obsolète)](https://helpx.adobe.com/substance-3d/unlisted/documentation/integrations/scripting-in-unity-170459644.html) : à l’aide de l’API de Substance de données, vous pouvez écrire des scripts pour mettre à jour et modifier les paramètres de Substance de données lors de l’exécution.
* [Utilisation de la bibliothèque Substance 3D Assets](https://helpx.adobe.com/substance-3d/unlisted/documentation/integrations/substance-3d-assets-library-225970070.html)
* [Suppression du plug-in de Substance](../../game-engines/unity/removing-plugin/removing-substance-plugin.md)
* [Substance 3D dans Unity Tutorials](../../game-engines/unity/3d-in-unity-tutorials/substance-3d-in-unity-tutorials.md)
* [Taille physique dans l’unité](../../game-engines/unity/physical-size-in-unity/physical-size-in-unity.md)
* [Partage de fichiers sbsar entre projets](https://helpx.adobe.com/sharing-sbsar-files-between-projects.html) [&#128279;](../../game-engines/unity/sharing-sbsar-files-bet/sharing-sbsar-files-between-projects.md)

**[FORMULAIRE TROUVÉ - RÈGLES REQUISES]**

>[!WARNING]
>
> Avant de mettre à niveau ou d&#39;utiliser le plug-in, vérifiez la [page du projet de mise à niveau](https://helpx.adobe.com/substance-3d/unlisted/documentation/integrations/upgrading-projects-182256244.html).

>[!WARNING]
>
> Assurez-vous de consulter la page [Directives d&#39;optimisation](../../game-engines/unity/optimization-guidelines/optimization-guidelines.md) avant de créer des documents de Substance personnalisés.

### Table des matières

* [Notes de mise à jour d’Unity](https://helpx.adobe.com/substance-3d/unlisted/documentation/integrations/beta-release-information-170460277.html) — Nouveautés de la Substance du plug-in Unity par version
* [Téléchargement du plug-in Substance 3D dans Unity](../../game-engines/unity/downloading-plugin-unity/downloading-substance-3d-plugin-in-unity.md) : Adobe Substance 3D pour Unity est disponible sur le site Unity Asset Store https://assetstore.unity.com/packages/tools/utilities/substance-in-unity-110555.
* [Présentation du plug-in Unity](../../game-engines/unity/unity-plugin-overview/unity-plugin-overview.md)
* [Préférences Unity](../../game-engines/unity/unity-preferences/unity-preferences.md) : la fenêtre des préférences de Substance de données vous permet de définir des options définies par l’utilisateur pour le plug-in.
* [Directives d&#39;optimisation](../../game-engines/unity/optimization-guidelines/optimization-guidelines.md) — Lorsque vous créez vos propres matériaux de Substance personnalisés, veillez à respecter les directives d&#39;optimisation ci-dessous.
* [Mise à niveau de projets/Problèmes connus](https://helpx.adobe.com/substance-3d/unlisted/documentation/integrations/upgrading-projects-182256244.html) — Problèmes connus avec la Substance dans le plug-in Unity
* [Gestion des Graphes Substance](https://helpx.adobe.com/substance-3d/unlisted/documentation/integrations/managing-and-navigating-substance-graphs-170459636.html) : vous pouvez créer de nouveaux matériaux à partir du matériau de Substance à l&#39;aide du Gestionnaire de Graphes Substance (SGM)
* [Modification des paramètres](../../game-engines/unity/changing-parameters/changing-parameters.md) : les paramètres du matériau de Substance sont accessibles sur l&#39;objet de Graphe Substance (SGO).
* [Textures générées (par Packing)](../../game-engines/unity/generated-textures-pac/generated-textures-packing.md) : les textures générées affichent les sorties de la Substance calculées par la Substance Engine de création des textures
* [Rendu de l&#39;espace colorimétrique](../../game-engines/unity/rendering-color-space/rendering-color-space.md) : pour obtenir de meilleurs résultats, vous devez définir l&#39;espace colorimétrique sur linéaire dans les paramètres d&#39;Unity Player.
* [Utilisation des entrées d’image](../../game-engines/unity/using-image-inputs/using-image-inputs.md)
* [Publication pour mobile](../../game-engines/unity/publishing-for-mobile/publishing-for-mobile.md) : directives de publication sur les plateformes mobiles
* [Substance 3D pour Unity Scripting](../../game-engines/unity/3d-for-unity-scripting/substance-3d-for-unity-scripting.md) : à l&#39;aide de l&#39;API de Substance de données, vous pouvez écrire des scripts pour mettre à jour et modifier les paramètres de Substance de données lors de l&#39;exécution.
* [Création de scripts dans Unity (obsolète)](https://helpx.adobe.com/substance-3d/unlisted/documentation/integrations/scripting-in-unity-170459644.html) : à l’aide de l’API de Substance de données, vous pouvez écrire des scripts pour mettre à jour et modifier les paramètres de Substance de données lors de l’exécution.
* [Utilisation de la bibliothèque Substance 3D Assets](https://helpx.adobe.com/substance-3d/unlisted/documentation/integrations/substance-3d-assets-library-225970070.html)
* [Suppression du plug-in de Substance](../../game-engines/unity/removing-plugin/removing-substance-plugin.md)
* [Substance 3D dans Unity Tutorials](../../game-engines/unity/3d-in-unity-tutorials/substance-3d-in-unity-tutorials.md)
* [Taille physique dans l’unité](../../game-engines/unity/physical-size-in-unity/physical-size-in-unity.md)
