---
helpx_url: 'https://helpx.adobe.com/substance-3d-bake/features/matching-by-name.html'
breadcrumb-title: ''
description: Utilisez la fonction Correspondance par nom pour isoler les maillages à faible et à fort polygone et empêcher le saignement de la géométrie pendant la cuisson.
helpx_creative_field: ''
helpx_description: bakers > Features > Matching by Name
helpx_experience_level: ''
helpx_learn_topic: ''
helpx_tags: ''
title: Correspondance par nom
user-guide-description: ''
user-guide-title: ''
source-git-commit: d57629bee333101dd9f40f30ed24ff84b6b8c6f1
workflow-type: tm+mt
source-wordcount: '739'
ht-degree: 0%

---


# Correspondance par nom

![](../../assets/banner-matching-by-name.jpg)

Correspondance par nom est le nom d’une méthode de filtrage qui peut être utilisée dans Substance Bakers pour isoler les maillages low poly et high poly en fonction de leur nom.

Cette fonctionnalité est très utile pour éviter le débordement de la géométrie au cours du processus de cuisson afin d&#39;obtenir des textures propres. Il évite d&#39;avoir à déplacer les mailles (souvent appelées « éclatement ») pour obtenir le même résultat.

## Quand utiliser la correspondance par nom

### Cuisson normale de cartes avec saignement de maille

Dans cet exemple, le casque au-dessus de la tête du personnage s&#39;immisce dans la face du personnage.

En activant Correspondance par nom, nous pouvons ignorer le casque et cuire le visage correctement. *Ce résultat est basé sur le paramètre Correspondance principal.*

| *Maillage* | *Correspondance Par Nom Désactivée* | *Correspondance Par Nom Le* |
| --- | --- | --- |
| ![](../../assets/baking-demo-vela.png){width="250px"} | ![](../../assets/baking-demo-vela-normal-nomatch.png){width="250px"} | ![](../../assets/baking-demo-vela-normal-withmatch.png){width="250px"} |

### Ignorer la face arrière de la géométrie flottante

Dans cet exemple, les « boutons » situés en haut de la boîte sont une géométrie flottante, ils ne sont pas reliés au maillage poly élevé. Par conséquent, ils projetteront des ombres par défaut sur la zone située en dessous, qui affichera la bordure de la géométrie.

En activant l’option Correspondance par nom pour le paramètre **Ignorer la face arrière**, nous pouvons masquer l’occlusion ambiante tout en ignorant la zone sous les boutons pour qu’elle ressemble à une seule zone.*Ce résultat est basé sur l’utilisation du paramètre Ignorer la face arrière.*

| *Maillage* | *Correspondance Par Nom Désactivée* | *Correspondance Par Nom Le* |
| --- | --- | --- |
| ![](../../assets/ignorebf-mesh.png){width="250px"} | ![](../../assets/ignorebf-off.png){width="250px"} | ![](../../assets/ignorebf-on.png){width="250px"} |

## Fonctionnement De La Correspondance Par Nom

Le système Correspondance par nom fonctionne en lisant le nom de la géométrie dans les maillages poly bas et haut et en utilisant un mot-clé (le suffixe) pour identifier/faire correspondre les noms. Par défaut, les boulangers utilisent le suffixe spécifique mais ils peuvent être modifiés (voir ci-dessous).

Les suffixes actuellement pris en charge sont les suivants :

| *Type de suffixe* | *Valeur par défaut* | *Utilisation* |
| --- | --- | --- |
| Poly Élevée | *\_high* | Utilisé pour isoler le nom du maillage poly élevé pour le comparer au maillage poly faible. |
| Poly faible | *\_low* | Utilisé pour isoler le nom du maillage en poly bas pour correspondre au maillage en poly élevé. |
| Ignorer les faces arrière | *\_ignorebf* | Utilisé pour ignorer les faces arrière pour les boulangers utilisant des rayons secondaires, comme l’occlusion ambiante.*Ce suffixe ne doit être présent que sur les maillages poly élevés, par exemple :**mesh\_high\_ignorebf*** |

Certaines règles à prendre en compte pour que cette fonctionnalité fonctionne correctement :

* La correspondance par nom doit être activée dans [Paramètres communs](../../bakers-settings/common-parameters/common-parameters.md), car elle est **désactivée par défaut**.
* Un paramètre de correspondance secondaire par nom peut être activé dans certains boulangers (comme [Occlusion ambiante](../../bakers-settings/ambient-occlusion-from/ambient-occlusion-from-mesh.md)), car ils produisent des rayons secondaires.
* La correspondance est sensible à la casse. Cela signifie qu&#39;un maillage nommé « **vela** » ne correspond pas à un autre nommé « **vela** ».
* Plusieurs maillages peuvent être associés en fonction de l&#39;emplacement du suffixe dans le nom de la géométrie.

Vous trouverez ci-dessous des exemples de la manière dont la correspondance peut fonctionner (à l’aide du suffixe par défaut) :

| Nom de stratégie faible | Correspondra À Une Stratégie Élevée | Ne Correspondra Pas À Une Stratégie Élevée |
| --- | --- | --- |
| <ul data-preserve-html="true"><li data-preserve-html="true">body_low</li></ul> | <ul data-preserve-html="true"><li data-preserve-html="true">body_high</li><li data-preserve-html="true">body_high_top</li><li data-preserve-html="true">body_high_1</li><li data-preserve-html="true">body_high_2</li></ul> | <ul data-preserve-html="true"><li data-preserve-html="true">de haut niveau</li><li data-preserve-html="true">body_top_high</li></ul> |
| <ul data-preserve-html="true"><li data-preserve-html="true">Head_low</li></ul> | <ul data-preserve-html="true"><li data-preserve-html="true">Head_high</li></ul> | <ul data-preserve-html="true"><li data-preserve-html="true">head_high</li></ul> |
| <ul data-preserve-html="true"><li data-preserve-html="true">Leg_low_top</li></ul> | <ul data-preserve-html="true"><li data-preserve-html="true">Jambe_haute</li><li data-preserve-html="true">Leg_high_top</li><li data-preserve-html="true">Leg_high_high_top</li></ul> | <ul data-preserve-html="true"><li data-preserve-html="true">Leg_top_high</li></ul> |

## Comment installer les boulangers

### Activation De La Correspondance Par Nom

La correspondance par nom peut être activée dans les [paramètres communs](../../bakers-settings/common-parameters/common-parameters.md) des paramètres Baker :

| *Logiciel* | *Définition de la configuration* |
| --- | --- |
| **Peintre de substance** | <ol class="steps" data-preserve-html="true"> <li class="step" data-preserve-html="true">     Ouvrez la fenêtre de cuisson (via les paramètres d&#39;ensemble de texture).    </li> <li class="step" data-preserve-html="true">     Afficher les paramètres communs.    </li> <li class="step" data-preserve-html="true">     Remplacez le paramètre <strong>Correspondance</strong> de « Toujours » par « Par nom de maillage ».<br/> <img data-preserve-html="true" src="../../assets/baking-match-setting-sp.png"/>    </li> </ol> |
| **Concepteur de substance** | <ol class="steps" data-preserve-html="true"> <li class="step" data-preserve-html="true">     Ouvrez la fenêtre de cuisson (en cliquant avec le bouton droit de la souris sur un maillage lié dans la fenêtre de l’explorateur).    </li> <li class="step" data-preserve-html="true">     Remplacez le paramètre <strong>Correspondance</strong> de « Toujours » par « Par nom de maillage ». <br/> <br/>    </li> </ol> |

### Modification des noms des suffixes

Les suffixes par défaut sont \_low et \_high et peuvent être modifiés comme suit :

* **Substance Painter** : dans la fenêtre [Baking](../../getting-started/software-interface/3d-painter/substance-3d-painter.md), dans les paramètres communs.
* **Concepteur de substance** : dans les paramètres [Projet](https://experienceleague.adobe.com/en/docs/substance-3d-designer/using/workspace/preferences/project-settings), sous les paramètres Cuisson.

## Filets à haute teneur en poly de zBrush

Les maillages à polygone élevé exportés depuis zBrush peuvent être utilisés pour la cuisson avec la fonction Correspondance par nom, mais certains paramètres peuvent être suivis :

| *Format du fichier* | *Description* |
| --- | --- |
| **&#x200B;**&#x200B;| Aucun paramètre spécifique à activer/désactiver, les fichiers de maillage peuvent être utilisés en l’état. |
| **&#x200B;**&#x200B;| Les fichiers OBJ exportés par zBrush ne fonctionneront pas avec **Correspondance par nom** par défaut. Au lieu de cela, il est possible d&#39;indiquer à Substance Painter d&#39;utiliser le nom de fichier du maillage pour qu&#39;il corresponde au maillage par nom.Pour ce faire, veillez à :<ol data-preserve-html="true"><li data-preserve-html="true"><strong>Désactiver</strong> le paramètre group (Grp) pour le sous-outil <strong>each</strong>.</li><li data-preserve-html="true"><strong>Nommez</strong> le fichier OBJ de manière appropriée (par exemple : <strong>body_high.obj</strong>).</li></ol> ![](../../assets/zbrush-setting.png) |
