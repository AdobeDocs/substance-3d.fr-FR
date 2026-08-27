---
helpx_url: 'https://helpx.adobe.com/substance-3d-bake/features/matching-by-name.html'
breadcrumb-title: ''
description: Utilisez la fonction Correspondance par nom (Matching by Name) pour isoler les maillages bas-poly et haut-poly et empêcher le saignement de la géométrie pendant la cuisson.
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

La correspondance par nom est le nom d’une méthode de filtrage qui peut être utilisée dans Substance Bakers pour isoler les maillages en poly bas et en poly haut en fonction de leur nom.

Cette fonctionnalité est très utile pour éviter le débordement de la géométrie les unes sur les autres pendant le processus de cuisson afin d&#39;obtenir des textures propres. Elle évite d&#39;avoir à écarter les mailles (souvent appelées « explosives ») pour obtenir le même résultat.

## Quand utiliser la correspondance par nom

### Cuisson de cartes normales avec débordement du maillage

Dans cet exemple, le casque au-dessus de la tête du personnage se fond sur le visage du personnage.

En activant l&#39;option Assortir par nom, nous pouvons ignorer le casque et cuire le visage correctement. *Ce résultat est basé sur le paramètre de correspondance principal.*

| *Maillage* | *Correspondance Par Nom Désactivée* | *Correspondance Par Nom Le* |
| --- | --- | --- |
| ![](../../assets/baking-demo-vela.png){width="250px"} | ![](../../assets/baking-demo-vela-normal-nomatch.png){width="250px"} | ![](../../assets/baking-demo-vela-normal-withmatch.png){width="250px"} |

### Ignorer la face arrière de la géométrie flottante

Dans cet exemple, les « boutons » en haut de la boîte sont à géométrie flottante, ils ne sont pas connectés au maillage poly élevé. Par conséquent, ils projetteront des ombres par défaut sur la boîte sous eux qui affichera la bordure de la géométrie.

En activant l&#39;option Correspondance par nom pour le paramètre **Ignorer l&#39;arrière-plan**, nous sommes en mesure de transformer l&#39;occlusion ambiante tout en ignorant la zone sous les boutons pour lui donner l&#39;aspect d&#39;une boîte singulière.*Ce résultat est basé sur l’utilisation du paramètre Ignorer l’arrière-plan.*

| *Maillage* | *Correspondance Par Nom Désactivée* | *Correspondance Par Nom Le* |
| --- | --- | --- |
| ![](../../assets/ignorebf-mesh.png){width="250px"} | ![](../../assets/ignorebf-off.png){width="250px"} | ![](../../assets/ignorebf-on.png){width="250px"} |

## Fonctionnement De La Correspondance Par Nom

Le système de correspondance par nom fonctionne en lisant le nom de la géométrie dans les maillages poly bas et haut et en utilisant un mot-clé (suffixe) pour identifier/faire correspondre les noms. Par défaut, les boulangers utilisent le suffixe spécifique mais ils peuvent être modifiés (voir ci-dessous).

Les suffixes actuellement pris en charge sont :

| *Type de suffixe* | *Valeur par défaut* | *Utilisation* |
| --- | --- | --- |
| Poly élevé | *\_high* | Utilisé pour isoler le nom du maillage en poly élevé afin de le comparer au maillage en poly faible. |
| Poly faible | *\_low* | Utilisé pour isoler le nom du maillage poly bas pour le comparer au maillage poly haut. |
| Ignorer les faces arrière | *\_ignorebf* | Utilisé pour ignorer les faces arrière pour les boulangers utilisant des rayons secondaires, tels que l&#39;Occlusion Ambient.*Ce suffixe doit être présent sur les maillages poly élevés uniquement, par exemple :**mesh\_high\_ignorebf*** |

Voici quelques règles à prendre en compte pour que cette fonctionnalité fonctionne correctement :

* La correspondance par nom doit être activée dans [Paramètres communs](../../bakers-settings/common-parameters/common-parameters.md), car elle est **désactivée par défaut**.
* Un paramètre de correspondance secondaire par nom peut être activé dans certains boulangers (tels que [Occlusion ambiante](../../bakers-settings/ambient-occlusion-from/ambient-occlusion-from-mesh.md)), car ils produisent des rayons secondaires.
* La correspondance est sensible à la casse, ce qui signifie qu&#39;un maillage nommé « **Vela** » ne correspondra pas à un autre nommé « **vela** ».
* Plusieurs maillages peuvent être mis en correspondance en fonction de l&#39;emplacement du suffixe dans le nom de la géométrie.

Vous trouverez ci-dessous des exemples de fonctionnement de la correspondance (à l’aide du suffixe par défaut) :

| Nom du poly faible | Correspondra À High Poly | Ne Correspond Pas À High Poly |
| --- | --- | --- |
| <ul data-preserve-html="true"><li data-preserve-html="true">body_low</li></ul> | <ul data-preserve-html="true"><li data-preserve-html="true">body_high</li><li data-preserve-html="true">body_high_top</li><li data-preserve-html="true">body_high_1</li><li data-preserve-html="true">body_high_2</li></ul> | <ul data-preserve-html="true"><li data-preserve-html="true">corps-haut</li><li data-preserve-html="true">body_top_high</li></ul> |
| <ul data-preserve-html="true"><li data-preserve-html="true">Head_low</li></ul> | <ul data-preserve-html="true"><li data-preserve-html="true">Head_high</li></ul> | <ul data-preserve-html="true"><li data-preserve-html="true">head_high</li></ul> |
| <ul data-preserve-html="true"><li data-preserve-html="true">Leg_low_top</li></ul> | <ul data-preserve-html="true"><li data-preserve-html="true">Jambe_haut</li><li data-preserve-html="true">Leg_high_top</li><li data-preserve-html="true">Leg_high_high_top</li></ul> | <ul data-preserve-html="true"><li data-preserve-html="true">Leg_top_high</li></ul> |

## Configuration des bakers

### Activation de la correspondance par nom

La correspondance par nom peut être activée dans les [paramètres communs](../../bakers-settings/common-parameters/common-parameters.md) des paramètres de Baker :

| *Logiciel* | *Configuration* |
| --- | --- |
| **Substance Painter** | <ol class="steps" data-preserve-html="true"> <li class="step" data-preserve-html="true">     Ouvrez la fenêtre de Bake (via les paramètres de Jeu de textures).    </li> <li class="step" data-preserve-html="true">     Affichez les paramètres communs.    </li> <li class="step" data-preserve-html="true">     Modifiez le paramètre <strong>Correspondance</strong> de « Toujours » à « Par nom de Maillage ».<br/> <img data-preserve-html="true" src="../../assets/baking-match-setting-sp.png"/>    </li> </ol> |
| **Substance Designer** | <ol class="steps" data-preserve-html="true"> <li class="step" data-preserve-html="true">     Ouvrez la fenêtre de Bake (en cliquant avec le bouton droit de la souris sur un maillage lié dans la fenêtre de l’Explorateur).    </li> <li class="step" data-preserve-html="true">     Modifiez le paramètre <strong>Correspondance</strong> de « Toujours » à « Par nom de Maillage ». <br/> <br/>    </li> </ol> |

### Modification des noms des suffixes

Les suffixes par défaut sont \_low et \_high et peuvent être modifiés comme suit :

* **Substance Painter** : dans la [fenêtre de cuisson](../../getting-started/software-interface/3d-painter/substance-3d-painter.md), dans les paramètres courants.
* **Substance Designer** : dans les [paramètres du projet](https://experienceleague.adobe.com/en/docs/substance-3d-designer/using/workspace/preferences/project-settings), sous les paramètres de cuisson.

## Filets en polypropylène de zBrush

Les maillages polychromes exportés à partir de zBrush peuvent être utilisés pour la cuisson avec la fonction Correspondance par nom, mais certains paramètres peuvent être suivis :

| *Format de fichier* | *Description* |
| --- | --- |
| **FBX** | Aucun paramètre spécifique à activer/désactiver, les fichiers de maillage peuvent être utilisés tels quels. |
| **OBJ** | Les fichiers OBJ exportés par zBrush ne fonctionneront pas par défaut avec **Correspondance par nom**. Il est possible d’indiquer à la Substance Painter d’utiliser le nom du fichier de maillage pour faire correspondre les maillages par nom.Pour ce faire, assurez-vous de :<ol data-preserve-html="true"><li data-preserve-html="true"><strong>Désactivez</strong> le paramètre de groupe (Grp) pour le sous-outil <strong>each</strong>.</li><li data-preserve-html="true"><strong>Nommez</strong> le fichier OBJ de manière appropriée (ex : <strong>body_high.obj</strong>).</li></ol> ![](../../assets/zbrush-setting.png) |
