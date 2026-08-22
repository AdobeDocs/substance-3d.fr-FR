---
title: Foire aux questions
description: Découvrez les réponses aux questions courantes sur OpenPBR et Substance 3D.
source-git-commit: a3ceb4df30f08099799bc2caecc5446d3832fc06
workflow-type: tm+mt
source-wordcount: '1424'
ht-degree: 0%

---


# OpenPBR - Foire aux questions

## Le modèle d’OpenPBR

+++Qu’est-ce qu’OpenPBR et quelle version Painter prend-il en charge ?

OpenPBR est une spécification de matériau ouvert hébergée par l’Academy Software Foundation, définissant un modèle d’ombrage standardisé conçu pour fonctionner de manière cohérente entre les applications. La documentation de [Painter contient plus d&#39;informations sur l&#39;utilisation d&#39;OpenPBR](https://experienceleague.adobe.com/fr/docs/substance-3d-painter/using/home).

+++

+++Qu&#39;est-ce que cela signifie lorsqu&#39;une application prétend « appuyer l&#39;OpenPBR », et comment puis-je savoir dans quelle mesure une application particulière appuie cette demande ?

Il n&#39;y a pas de processus de certification officiel, alors la revendication peut signifier différentes choses. Dans la pratique, les implémentations varient : certaines couvrent l’intégralité de la spécification technique, d’autres uniquement un sous-ensemble, laissant de côté des fonctionnalités telles que le film mince, la dispersion ou certains comportements de sous-surface. Notez également que « Support MaterialX » et « Support OpenPBR » ne sont pas la même chose ; une application peut prendre en charge l&#39;un sans mettre pleinement en œuvre l&#39;autre.

Pour savoir ce qu&#39;une application spécifique prend réellement en charge, utilisez une combinaison d&#39;approches : vérifiez les notes de mise à jour (la prise en charge est souvent ajoutée de manière incrémentielle) ; chargez le terrain de jeu OpenPBR Shader de l&#39;ASWF et comparez-le rapidement à un rendu de référence aux espaces de surface ; ou, pour les studios avec un investissement important dans le pipeline, interrogez directement le fournisseur sur les fonctionnalités prises en charge et leur feuille de route.

+++

+++L’OpenPBR peut-elle garantir des résultats identiques entre différentes applications et systèmes de rendu ?

Pas tout à fait, et c&#39;est par dessein. L’OpenPBR définit un modèle de matériau partagé, mais l’aspect final est également façonné par l’éclairage, les algorithmes de rendu, la gestion des couleurs et le degré de conformité de chaque implémentation à la spécification des tuyauteries.

En pratique, maximiser cette garantie signifie : exporter en USD avec l&#39;intégration de MaterialX ; valider le aller-retour tôt en utilisant le terrain de jeu OpenPBR Shader d&#39;ASWF plutôt qu&#39;à la fin de la production ; confirmer les niveaux de support de vos fournisseurs pour toutes les fonctionnalités avancées que vous utilisez ; et s&#39;entendre dès le départ sur les fonctionnalités qui seront utilisées ou non dans les matériaux partagés. La transférabilité doit être validée activement et non pas supposée.

+++

+++Existe-t-il des matériaux que l’OpenPBR ne peut pas représenter avec précision ?

Oui. OpenPBR est un modèle paramétrique. Les paramètres tels que la rugosité, la métallisation et l&#39;IOR couvrent la grande majorité des cas d&#39;utilisation en production, mais ne peuvent pas reproduire la précision des formats de matériau mesurés tels que X-Rite AxF, qui capturent des données optiques réelles à partir d&#39;un échantillon physique. Pour les travaux de production en général, l&#39;OpenPBR convient bien ; pour les applications nécessitant une mise en correspondance exacte des échantillons, un format mesuré peut être plus approprié.

La peinture de voiture est une illustration utile. Il est possible de peindre une voiture en OpenPBR avec quelques avertissements. L’OpenPBR ne comprend pas d’ombrage de peinture automobile spécialisé, il peut donc être insuffisant pour certaines utilisations dans l’industrie automobile. En outre, cela dépend simplement du type de peinture de voiture - certaines peintures de voiture auront toujours des propriétés qui sortent du cadre d&#39;un nuanceur donné. Mais en gardant ces points à l&#39;esprit, la peinture de voiture s&#39;adapte naturellement à l&#39;architecture en couches de l&#39;OpenPBR.

+++

## Configuration et conversion

+++Dois-je apprendre OpenUSD ou MaterialX pour utiliser OpenPBR ?

Non. Pour la plupart des artistes, l’OpenPBR est simplement le modèle de matériau intégré aux outils qu’ils utilisent déjà. Substance 3D Painter, Maya 2025.3 et 3ds Max 2026 utilisent tous OpenPBR comme matériau par défaut. Travailler avec ce matériau signifie simplement travailler avec le shader standard. USD et MaterialX ne deviennent pertinents que lorsque les matériaux doivent passer d&#39;une application à une autre. Pour les workflows à application unique, la prise en charge native est suffisante ; pour les pipelines multi-DCC, USD et MaterialX fournissent l’infrastructure d’échange, mais en grande partie en coulisses.

Cela dit, le chemin d’exchange le plus robuste pour les bibliothèques de matériaux partagées est via USD avec l’intégration MaterialX, qui fournit un conteneur standardisé et indépendant du moteur de rendu pour les descriptions de matériaux. Les workflows d’exportation de matériaux sous forme de ressources autonomes (sans modèle associé, à utiliser dans une bibliothèque partagée) sont toujours en cours de développement et ne sont pas encore entièrement pris en charge partout. Avant de vous engager dans une architecture de bibliothèque qui en dépend, validez votre pipeline spécifique par rapport aux capacités actuelles.

+++

+++Comment créer un projet OpenPBR dans Substance 3D Painter ?

Un projet créé sans modèle utilise le nuanceur d’OpenPBR par défaut. Le nuanceur d’OpenPBR est désormais la première option de la nouvelle fenêtre de projet, en remplacement d’ASM. Des modèles dédiés sont également disponibles pour des workflows spécifiques (Anisotropie, Couche, Fuzz, Dispersion de sous-surface). L’importation d’un fichier USD contenant un matériau OpenPBR configurera automatiquement le projet. Les exemples de projets fournis avec Substance 3D Painter ont également été mis à jour pour utiliser le workflow OpenPBR. Ils constituent un bon point de départ pour se familiariser avec son fonctionnement pratique.

+++

+++Puis-je convertir un projet Adobe Standard Material (ASM) existant en projet OpenPBR ?

Il n’y a pas de conversion automatique. Les projets ASM existants conservent leur nuanceur actuel lorsqu’ils sont ouverts, et les modèles ASM restent disponibles pour les nouveaux projets.

Pour migrer vers OpenPBR manuellement, sélectionnez l’ombrage de l’OpenPBR dans la fenêtre Paramètres de l’ombrage, puis ajoutez les couches OpenPBR appropriées via Paramètres du jeu de textures > Ajouter ou supprimer des couches. Une fois cela fait, passez en revue vos calques existants pour vous assurer que leur contenu cible les canaux prévus.

+++

+++Mes nuanceurs personnalisés doivent-ils être mis à jour pour l’OpenPBR ?

Non : les nuanceurs personnalisés existants continuent de fonctionner, car les bibliothèques de nuanceurs pertinentes sont obsolètes au lieu d’être supprimées. Cependant, il est recommandé de migrer vers les nouvelles bibliothèques de nuanceurs, car elles sont plus propres et plus faciles à utiliser. Consultez le journal des modifications de API de shader dans le menu Aide pour plus de détails.

+++

## Utilisation dans l’application

+++Avec autant de paramètres disponibles en OpenPBR, où dois-je me concentrer ?

Commencez simplement. Pour la plupart des surfaces opaques, la couleur de base, la rugosité au Specular et le métal représentent la majorité des différences visibles entre les matériaux. Ajoutez l&#39;IOR si la précision de la réflectivité est importante ; affinez la couleur du Specular si la matière présente une teinte d&#39;angle de pâturage. Activez la transmission, le sous-sol, la couche, le flou, le film mince et la dispersion uniquement lorsque vous avez une raison claire et basée sur les références de le faire, car chaque canal supplémentaire ajoute de la complexité et un coût de rendu potentiel. Le masquage ou la réduction des groupes de paramètres inutilisés permet de concentrer votre espace de travail et réduit le risque d&#39;effets inattendus.

+++

+++J’ai une carte de rugosité. Dois-je la connecter à Rugosité diffuse de base ou Rugosité au Specular ?

Rugosité du specular : contrôle la netteté de la réflexion et est l’équivalent direct de la rugosité saisie dans d’autres workflows PBR. La rugosité diffuse de base est un paramètre spécialisé distinct qui affecte uniquement la diffusion diffuse. Elle peut rester sa valeur par défaut pour la plupart des workflows.

+++

+++Pourquoi la modification de la couleur de base n’a-t-elle aucun effet lorsque j’utilise la diffusion de sous-surface ?

Il existe une «hiérarchie des priorités» qui détermine l&#39;influence de chaque paramètre sur l&#39;aspect final du matériau. Comme si :

* La métallisation vient en premier : lorsque la métallisation = 1, les parties Subsurface et Transmission sont désactivées.
* Le poids de transmission vient ensuite : si Poids de transmission = 1, Subsurface sera absent.
* Le poids de sous-surface vient après cela.
* La couleur de base diffuse vient en dernier : la diffusion de base ne contribue que lorsqu’aucune des options ci-dessus n’est définie sur 1.

Ainsi, dans l’exemple cité, si la propriété Subsurface Weight est définie sur 1 (sa valeur maximale), elle régit l’ensemble de l’aspect. La modification de la valeur Couleur de base n’a aucun effet, car la diffusion de base n’apporte pratiquement aucune contribution. Inversement, si l’option Métallique est définie sur la valeur maximale de 1, la modification des valeurs Poids transmission, Poids sous la surface et Couleur de base diffuse n’aura aucun effet sur l’aspect final du matériau. La transmission, le sous-sol et la diffusion sont tous diélectriques (non métalliques), donc régler la valeur Métallique sur 1 supprime toute contribution non métallique.

+++

+++Pourquoi la transmission se comporte-t-elle de manière inattendue ? Par exemple, pourquoi mon filet apparaît-il très sombre lorsque je l’active ?

Le coupable le plus courant est la Profondeur de transmission trop faible. Ce paramètre définit la distance parcourue par la lumière avant que la couleur de transmission n’atteigne sa pleine saturation. A des valeurs faibles, même une géométrie fine apparaît sombre et dense. Augmentez-la pour qu’elle corresponde à l’échelle physique approximative de votre objet. Si le matériau semble alors trop clair, réglez à la fois les options Couleur de transmission et Profondeur pour trouver le bon équilibre.

La diffusion peut ajouter une couche supplémentaire de complexité. La couleur de transmission n’est pas une simple teinte : son effet dépend de la distance parcourue par la lumière à travers l’objet, et est contrôlée par la Profondeur de transmission. La Couleur de la dispersion, quant à elle, contrôle une lumière de voyage distincte qui peut passer, rebondissant à l’intérieur du matériau plutôt que de passer directement à travers. La diffusion étant directionnelle, le résultat change également en fonction de l’emplacement de la source lumineuse. Ajuster l&#39;un sans tenir compte de l&#39;autre est une source courante de résultats inattendus.

+++

+++J’ai activé l’option Film fin, mais je ne vois aucun effet. Que me manque-t-il ?

Vérifiez d’abord la valeur par Thickness. Contre toutes attentes, les valeurs plus fines produisent une irisation plus visible, la plupart des effets se produisant entre 0 et 1 micromètre. Si l&#39;effet est encore subtil, ajustez l&#39;IOR, qui modifie à la fois l&#39;intensité et la couleur des interférences. Confirmez également que le poids du film mince est supérieur à zéro.

+++
