---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-bake/bakers-settings/common-parameters.html"
breadcrumb-title: ''
description: Découvrez les paramètres courants qui s’appliquent à tous les boulangers et comment les configurer pour une génération de texture optimale.
helpx_creative_field: ""
helpx_description: bakers > Bakers Settings > Common Parameters
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Paramètres communs
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '1068'
ht-degree: 1%

---


# Paramètres communs

Les paramètres communs s&#39;appliquent à tous les boulangers. Ces paramètres définissent généralement comment les boulangers se comporteront et travailleront avec des maillages à haute teneur en poly, mais comment les textures finales seront générées. Certains de ces paramètres peuvent être remplacés par des boulangers spécifiques.

Bien que la plupart de ces paramètres soient disponibles dans tous les logiciels (y compris Substance Automation Toolkit), leur comportement peut différer légèrement ; certains peuvent ne pas être disponibles en fonction du workflow et de la mise en œuvre du logiciel.

## Paramètres généraux

Ces paramètres affectent la façon dont les boulangers génèrent des textures.

| *Nom* | *Description* |
| --- | --- |
| **Taille**(Taille par défaut ou Taille de sortie) | Contrôlez la résolution de la texture de sortie du baking (en pixels). Valeurs disponibles :<ul data-preserve-html="true"><li data-preserve-html="true"><strong>32</strong></li><li data-preserve-html="true"><strong>64</strong></li><li data-preserve-html="true"><strong>128</strong></li><li data-preserve-html="true"><strong>256</strong></li><li data-preserve-html="true"><strong>512</strong></li><li data-preserve-html="true"><strong>1024</strong></li><li data-preserve-html="true"><strong>2048</strong> (par défaut)</li><li data-preserve-html="true"><strong>4096</strong></li><li data-preserve-html="true"><strong>8192</strong></li></ul>Les résolutions non carrées sont également prises en charge, par exemple : 2 048 x 1 024 (rapport 2:1). En Substance Designer, ce paramètre peut être remplacé par le boulanger lui-même. |
| **Format** | Format de fichier des textures cuites.*Non disponible dans la Substance Painter.* Voir : [Exportation des maps bakées](../../common-questions/how-export-the-baked-maps/how-to-export-the-baked-maps.md). |
| **Anticrénelage** | Contrôle le lissage qui peut améliorer la qualité des textures cuites et réduire le lissage là où différentes géométries se connectent.Pour en savoir plus sur le crénelage, consultez : [Crénelage sur les coutures UV](../../common-issues/aliasing-on-uv-seams/aliasing-on-uv-seams.md) et [Crénelage sur Wikipedia](https://en.wikipedia.org/wiki/Aliasing).Valeurs disponibles :<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Aucun</strong> (par défaut)</li><li data-preserve-html="true"><strong>Sous-échantillonnage 2x2</strong></li><li data-preserve-html="true"><strong>Sous-échantillonnage 4x4</strong></li><li data-preserve-html="true"><strong>Sous-échantillonnage 8x8</strong></li></ul>  **Remarque :** l&#39;activation de l&#39;anticrénelage peut augmenter considérablement le temps de cuisson, car l&#39;anticrénelage fonctionne en calculant la texture à une résolution plus élevée, puis en la réduisant à la taille initialement sélectionnée. Cela signifie qu’une texture 2K avec un sous-échantillonnage 2x2 calculera en fait une texture 4K.Il est parfois préférable d&#39;augmenter le nombre de rayons dans le baker plutôt que d&#39;augmenter le sous-échantillonnage. Il pourrait obtenir de meilleurs résultats sans attendre trop longtemps. |
| **Ensemble UV** | Détermine les UV du maillage low-poly utilisés pour calculer les textures cuites.*Non disponible dans la Substance Painter.* |
|  |  |
| **Dilatation (px)** | Dilater/étendre les pixels des UV à l’extérieur ou à leur bordure de la quantité de pixels donnée. Cette opération permet d’éviter les coutures aux bordures UV lorsque ces bordures ne sont pas parfaitement alignées sur les pixels de texture ou lorsque la résolution de la texture est réduite (ex : mipmaps). Il s’agit d’un post-traitement appliqué après le processus de cuisson. On peut aussi parfois parler de « remplissage ».Pour en savoir plus sur la dilatation, voir : [Crénelage sur les coutures UV](../../common-issues/aliasing-on-uv-seams/aliasing-on-uv-seams.md) et [Remplissage](https://helpx.adobe.com/fr/substance-3d/unlisted/documentation/spdoc/padding-134643719.html). |
| **Appliquer la diffusion** | Si cette option est activée, l’extérieur des UV sera rempli avec des couleurs de dégradé lissées en fonction des bordures UV. Ce processus garantit que lorsque la taille de la texture est réduite, elle reste stable et ne crée pas de coutures trop visibles (ex : mipmaps). Il s’agit d’un post-traitement appliqué après le processus de cuisson. |
| **Normales moyennes** | Si cette option est activée, calcule la normale moyenne d&#39;un sommet pour savoir dans quelle direction envoyer les rayons pendant le processus de mise en correspondance du maillage de la cuisson. Si cette option est désactivée, les rayons suivent les normales des sommets d’origine du filet. |

## Paramètres High-Poly

Les paramètres suivants contrôlent la cuisson de maille de haut-poly à bas-poly (« à partir de boulangeries de maille »).

| *Nom* | *Description* |
| --- | --- |
| **Maillages haute définition** | Liste de fichiers (ou de Substances de package) contenant des maillages à polyvalence élevée. Ils sont chargés en mémoire par les boulangers lorsque le processus de boulangerie commence à calculer des informations différentes et à enregistrer ces informations de maillage dans les textures. Cette liste est ignorée si l&#39;option « **Utiliser basse comme haute définition** » est activée. |
| **Utiliser bas comme haute définition** ou **Utiliser bas maillage poly comme haut maillage poly** | Si cette option est activée, la liste de maillages en polypropylène fournie aux boulangers sera ignorée et le maillage en polychrome sera cuit sur lui-même à la place.Ce paramètre est utile lorsque vous travaillez directement avec un maillage à poly élevé. Par exemple, lorsque ce paramètre est activé pour la cuisson d&#39;une texture d&#39;occlusion ambiante pour une voiture en polypropylène, la distance de rayonnement est ignorée et le boulanger produit un cuisson impeccable (pas d&#39;erreur de rayonnement ni d&#39;incohérence de géométrie). |
|  |  |
| **Définir la distance avec la cage** ou **Utiliser la cage** | Indique s&#39;il est préférable d&#39;utiliser un fichier de filet de cage dans le processus de cuisson au lieu de valeurs de distance de rayon. La cage contrôle la distance et la direction maximales du rayon. |
| **Fichier Cage** | Chemin d&#39;accès au fichier de maillage contenant la cage. |
| **Valeur frontale** ou **Distance frontale maximale** | Détermine à quelle distance au-dessus de la surface à faible poly le rayon doit commencer à trouver une géométrie à fort poly le long de son chemin.*Ce paramètre n&#39;a aucun effet lorsqu&#39;une cage est utilisée.* |
| **Valeur arrière** ou **Distance arrière maximale** | Contrôle la distance sous la surface à faible polygone à laquelle le rayon doit s&#39;arrêter pour trouver une géométrie à polygone élevé le long de son chemin.*Ce paramètre n&#39;a aucun effet lorsqu&#39;une cage est utilisée.* |
| **Par rapport au cadre de sélection** | Si cette option est activée, les calculs de distance de rayon et autres calculs basés sur la taille sont basés sur l&#39;espace normalisé du maillage low-poly. Si cette option est désactivée, le calcul de la distance de rayon est basé sur les unités spécifiées dans le maillage low-poly lors de son exportation (mètres, centimètres, etc.). Il peut parfois être utile de désactiver ce paramètre et d&#39;entrer la distance de rayon manuellement lorsqu&#39;un objet a des mesures précises. |
|  |  |
| **Correspondance** | Indique comment les boulangers doivent correspondre à une géométrie de poly faible et élevé. Il peut être utilisé pour filtrer le processus de cuisson sans avoir besoin de séparer manuellement les maillages (éclater).Valeurs possibles :<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Toujours</strong> (par défaut) : le maillage low-poly est mis en correspondance avec chaque maillage high-poly.</li><li data-preserve-html="true"><strong>Par nom de maillage</strong> : filtrez les maillages par leur nom pour éviter toute correspondance avec une géométrie indésirable.</li></ul>Pour en savoir plus sur la correspondance de la géométrie, voir : [Correspondance par nom](../../features/matching-by-name/matching-by-name.md). |
| **Correspondance des suffixes** ou **Suffixe de maillage polychrome élevé** **Suffixe de maillage polychrome faible** | Suffixes de nom de maillage pour identifier et regrouper la géométrie lors de l&#39;utilisation de la fonction Correspondance par nom. Suffixes disponibles :<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Maillage poly bas</strong> : suffixe pour identifier les maillages poly bas dans la scène</li><li data-preserve-html="true"><strong>Maillage poly élevé</strong> : suffixe pour identifier les maillages poly élevés dans la scène</li><li data-preserve-html="true"><strong>Ignorer les faces arrière</strong> : suffixe pour identifier les maillages qui doivent être ignorés par des boulangers spécifiques (comme l&#39;[Occlusion ambiante à partir du maillage](../../bakers-settings/ambient-occlusion-from/ambient-occlusion-from-mesh.md))</li></ul>Pour en savoir plus sur la correspondance de la géométrie, voir : [Correspondance par nom](../../features/matching-by-name/matching-by-name.md) . |
|  |  |
| **Utiliser la correction de l&#39;inclinaison** | Si cette option est activée, la direction du rayon sera calculée à partir de la **normale moyenne** ou de la normale de la géométrie d&#39;origine en fonction de la texture d&#39;entrée. Les valeurs noires de la texture utilisent la normale moyenne calculée, tandis que les valeurs blanches utilisent la normale du maillage d’origine.*Non disponible dans la Substance Painter.* |
| **Mappage incliné** | Tracé du fichier de texture utilisé pour incliner la projection des rayons. |
| **Inverser la correction de l&#39;inclinaison** | Inversez la lecture de la texture d’entrée (le noir devient blanc et le blanc devient noir). |
