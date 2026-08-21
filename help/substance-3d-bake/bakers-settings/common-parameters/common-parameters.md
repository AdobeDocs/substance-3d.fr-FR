---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-bake/bakers-settings/common-parameters.html"
breadcrumb-title: ''
description: Découvrez les paramètres communs qui s’appliquent à tous les boulangers et comment les configurer pour une génération de texture optimale.
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

Les paramètres communs s&#39;appliquent à tous les boulangers. Ces paramètres définissent généralement la façon dont les boulangers se comporteront et travailleront avec des maillages à polyplis élevés, mais comment les textures finales seront générées. Certains de ces paramètres peuvent être remplacés par des boulangers spécifiques.

Bien que la plupart de ces paramètres soient disponibles dans tous les logiciels (y compris Substance Automation Toolkit), leur comportement peut être légèrement différent ; ou certains peuvent ne pas être disponibles selon le workflow et la mise en œuvre du logiciel.

## Paramètres généraux

Ces paramètres affectent la façon dont les boulangers génèrent des textures.

| *Nom* | *Description* |
| --- | --- |
| **Size**(Default Size ou Output Size) | Contrôle la résolution de la texture de sortie au four (en pixels). Valeurs disponibles :<ul data-preserve-html="true"><li data-preserve-html="true"><strong>32</strong></li><li data-preserve-html="true"><strong>64</strong></li><li data-preserve-html="true"><strong>128</strong></li><li data-preserve-html="true"><strong>256</strong></li><li data-preserve-html="true"><strong>512</strong></li><li data-preserve-html="true"><strong>1024</strong></li><li data-preserve-html="true"><strong>2048</strong> (par défaut)</li><li data-preserve-html="true"><strong>4096</strong></li><li data-preserve-html="true"><strong>8192</strong></li></ul>Les résolutions autres que carrées sont également prises en charge, par exemple : 2 048 x 1 024 (rapport 2:1). Dans Substance Designer, ce paramètre peut être remplacé par le boulanger lui-même. |
| **Format** | Format du fichier des textures cuites.*Non disponible dans Substance Painter.* Voir : [&#x200B; Comment exporter les cartes cuites &#x200B;](../../common-questions/how-export-the-baked-maps/how-to-export-the-baked-maps.md). |
| **Anti-crénelage** | Contrôle le lissage qui peut améliorer la qualité des textures cuites et réduire le lissage là où différentes géométries se connectent.Pour en savoir plus sur les alias, consultez [Aliasing sur les coutures UV](../../common-issues/aliasing-on-uv-seams/aliasing-on-uv-seams.md) et [Aliasing sur Wikipedia](https://en.wikipedia.org/wiki/Aliasing).Valeurs disponibles :<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Aucun</strong> (par défaut)</li><li data-preserve-html="true"><strong>Sous-échantillonnage 2x2</strong></li><li data-preserve-html="true"><strong>Sous-échantillonnage 4x4</strong></li><li data-preserve-html="true"><strong>Sous-échantillonnage 8x8</strong></li></ul>  **Remarque :** l&#39;activation de l&#39;anti-crénelage peut augmenter considérablement le temps de cuisson, car l&#39;anti-crénelage fonctionne en calculant la texture à une résolution plus élevée, puis en la réduisant à la taille sélectionnée à l&#39;origine. Cela signifie qu&#39;une texture 2K avec un sous-échantillonnage 2x2 calculera en fait une texture 4K.Il est parfois préférable d&#39;augmenter le nombre de rayons dans le boulanger plutôt que d&#39;augmenter le sous-échantillonnage. Il pourrait obtenir de meilleurs résultats sans attendre trop longtemps. |
| **Ensemble UV** | Contrôle quels UV du maillage à faible poly seront utilisés pour calculer les textures cuites.*Non disponible dans Substance Painter.* |
|  |  |
| **Dilatation (px)** | Dilatez/étendez les pixels des UV à l&#39;extérieur ou à leur bordure selon la quantité de pixels donnée. Cette opération permet d’éviter les jointures aux bordures UV lorsque ces bordures ne sont pas parfaitement alignées avec les pixels de texture ou lorsque la résolution de la texture est réduite (par exemple : mipmaps). Il s&#39;agit d&#39;un post-traitement appliqué après le processus de cuisson. Elle peut également être appelée « remplissage ».Pour en savoir plus sur la dilatation, voir [Aliasage sur coutures UV](../../common-issues/aliasing-on-uv-seams/aliasing-on-uv-seams.md) et [Marge intérieure](https://helpx.adobe.com/fr/substance-3d/unlisted/documentation/spdoc/padding-134643719.html). |
| **Appliquer la diffusion** | Si cette option est activée, l’extérieur des UV est rempli de couleurs de dégradé lissées en fonction des bordures UV. Ce processus garantit que lorsque la taille de la texture est réduite, elle reste stable et ne crée pas de jointures trop visibles (par exemple : mipmap). Il s&#39;agit d&#39;un post-traitement appliqué après le processus de cuisson. |
| **Normales moyennes** | Si cette option est activée, calcule la normale moyenne d&#39;un sommet pour savoir dans quelle direction envoyer les rayons pendant le processus de correspondance de maillage de la cuisson. Si cette option est désactivée, les rayons suivent les normales de sommet d&#39;origine du maillage. |

## Paramètres High-Poly

Les paramètres suivants régissent la cuisson des filets de haut-poly à bas-poly (« à partir de la cuisson des filets »).

| *Nom* | *Description* |
| --- | --- |
| **Maillages haute définition** | Une liste de fichiers (ou de ressources de package Substance) qui contient des maillages à poly élevé. Ils sont chargés en mémoire par les boulangers lorsque le processus de cuisson commence à calculer différentes informations et à enregistrer ces informations de maillage dans les textures. Cette liste est ignorée si l’option « **Utiliser une basse définition** » est activée. |
| **Utiliser un maillage bas comme haute définition** ou **Utiliser un maillage bas comme un maillage haut** | Si cette option est activée, la liste des maillages à polygone élevé fournie aux boulangers sera ignorée et le maillage à faible polygone sera cuit sur lui-même à la place.Ce paramètre est utile lorsque vous travaillez directement avec un maillage à poly élevé. Par exemple, lors de la cuisson d&#39;une texture d&#39;occlusion ambiante pour une voiture à polyvalence élevée avec ce paramètre activé, la distance de rayon est ignorée et le boulanger produira une cuisson parfaite (pas de défauts de rayon ou de discordance de géométrie). |
|  |  |
| **Définir la distance avec la cage** ou **Utiliser la cage** | Indique s&#39;il faut utiliser un fichier de maillage cage dans le processus de cuisson au lieu d&#39;utiliser des valeurs de distance de rayon. La cage contrôle la distance et la direction maximales du rayon. |
| **Fichier Cage** | Chemin d&#39;accès au fichier de maillage contenant la cage. |
| **Valeur frontale** ou **Distance frontale maximale** | Contrôle la distance au-dessus de la surface à faible poly le rayon doit commencer à trouver une géométrie à poly élevé le long de son chemin.*Ce paramètre n’a aucun effet lorsqu’une cage est utilisée.* |
| **Valeur arrière** ou **Distance arrière maximale** | Contrôle la distance au-dessous de la surface à faible poly que le rayon doit s&#39;arrêter pour trouver une géométrie à poly élevé le long de son chemin.*Ce paramètre n’a aucun effet lorsqu’une cage est utilisée.* |
| **Relatif au cadre de sélection** | Si cette option est activée, la distance des rayons et d&#39;autres calculs basés sur la taille sont basés sur l&#39;espace normalisé du maillage à faible polygone. Si cette option est désactivée, le calcul de la distance de rayon est basé sur les unités spécifiées dans le maillage low-poly lors de son exportation (mètres, centimètres, etc.). Il peut parfois être utile de désactiver ce paramètre et de saisir manuellement la distance de rayon lorsqu&#39;un objet possède des mesures précises. |
|  |  |
| **Correspondance** | Indique comment les boulangers doivent correspondre à une géométrie de poly faible et élevé. Il peut être utilisé pour filtrer le processus de cuisson sans avoir à séparer manuellement les maillages (éclater).Valeurs possibles :<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Always</strong> (par défaut) : un maillage low-poly est mis en correspondance avec chaque maillage high-poly.</li><li data-preserve-html="true"><strong>Par nom de maillage</strong> : filtrez les maillages en fonction de leur nom pour éviter toute correspondance avec une géométrie indésirable.</li></ul>Pour en savoir plus sur la correspondance de géométries, voir : [Correspondance par nom](../../features/matching-by-name/matching-by-name.md). |
| **Suffixes de correspondance** ou **Suffixe de maillage poly élevé** **suffixe de maillage poly faible** | Suffixes de nom de maillage pour identifier et regrouper la géométrie lors de l&#39;utilisation de la fonction Correspondance par nom. Suffixes disponibles :<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Faible maillage poly</strong> : suffixe pour identifier les faibles maillages poly dans la scène</li><li data-preserve-html="true"><strong>Maillage poly élevé</strong> : suffixe pour identifier les mailles poly élevées dans la scène</li><li data-preserve-html="true"><strong>Ignorer les faces arrière</strong> : suffixe pour identifier les maillages qui doivent être ignorés par des boulangers spécifiques (comme le [Occlusion ambiante à partir du maillage](../../bakers-settings/ambient-occlusion-from/ambient-occlusion-from-mesh.md))</li></ul>Pour en savoir plus sur la correspondance de géométries, voir : [Correspondance par nom](../../features/matching-by-name/matching-by-name.md) . |
|  |  |
| **Utiliser la correction de biais** | Si cette option est activée, la direction du rayon est calculée à partir de **Normale moyenne** ou de la normale de la géométrie d&#39;origine en fonction de la texture d&#39;entrée. Les valeurs noires de la texture utilisent la normale moyenne calculée, tandis que les valeurs blanches utilisent la normale du maillage d&#39;origine.*Non disponible dans Substance Painter.* |
| **Carte inclinée** | Chemin d&#39;accès au fichier de texture utilisé pour obvier la projection des rayons. |
| **Inverser la correction de biais** | Inversez la lecture de la texture d&#39;entrée (le noir devient blanc et le blanc devient noir). |
