---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/features/gpu-raytracing.html"
breadcrumb-title: ''
description: Activez le lancer de rayons du GPU accéléré par le matériel pour accélérer les calculs de baking de 25 fois ou plus pour des workflows plus rapides.
helpx_creative_field: ""
helpx_description: bakers > Features > GPU Raytracing
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Raytracing GPU
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 18%

---


# Raytracing GPU

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

Certains boulangers prennent en charge l&#39;accélération matérielle du lancer de rayons sur le GPU, ce qui augmente généralement la vitesse de calcul d&#39;un facteur de 25 ou plus.

## Configuration matérielle requise

Le lancer de rayons est automatiquement activé si le système répond aux exigences suivantes :

* Un GPU compatible est installé\* (série RTX, Titan V ou GeForce 10xx)
* Les pilotes GPU sont à jour
* Windows 10 « Créateur d’automne » / Mise à jour d’octobre (version 1809) ou ultérieure installée\*\*

</td>
<td style="border: 0;" valign="top">

![Comparaison d’activation/de désactivation du lancer de rayons GPU](../../assets/rtx-ao-demo.gif "Comparaison d’activation/de désactivation du lancer de rayons GPU"){zoomable="yes"}

</td>
</tr>
</table>

\* : les GPU NVIDIA compatibles incluent tous les GPU utilisant l’architecture Pascal ou une architecture plus récente. C’est-à-dire les séries GTX 10, Titan V, RTX 20 ou plus récentes.

\*\* : Pour vérifier votre version de Windows, cliquez sur le menu Démarrer, tapez &#39;winver&#39; et appuyez sur Entrée.\
Vous pouvez obtenir la mise à jour par le biais de la [page dédiée](https://support.microsoft.com/en-us/help/4028685/windows-10-get-the-update) sur le site web d’assistance Microsoft.

>[!TIP]
>
> En cas de problèmes, le lancer de rayons du GPU peut être désactivé dans les préférences de l’application.

## Boulangers pris en charge

Les tableaux ci-dessous répertorient la prise en charge du lancer de rayons GPU pour chaque boulanger, en fonction de la version Substance 3D bakers :

+++Version 3 et ultérieure

| Baker | Prend en charge le lancer de rayons du GPU |
| --- | --- |
| Occlusion ambiante | <div><img alt="(coche)&quot; data-preserve-html=&quot;true" src="../../assets/check.svg"/></div> |
| Bent normal | <div><img alt="(coche)&quot; data-preserve-html=&quot;true" src="../../assets/check.svg"/></div> |
| Couleur | <div><img alt="(coche)&quot; data-preserve-html=&quot;true" src="../../assets/check.svg"/></div> |
| Courbure | <div><img alt="(coche)&quot; data-preserve-html=&quot;true" src="../../assets/check.svg"/></div> |
| Hauteur | <div><img alt="(coche)&quot; data-preserve-html=&quot;true" src="../../assets/check.svg"/></div> |
| Normale | <div><img alt="(coche)&quot; data-preserve-html=&quot;true" src="../../assets/check.svg"/></div> |
| Espace monde normal | <div><img alt="(erreur)&quot; data-preserve-html=&quot;true" src="../../assets/error.svg"/></div> |



| Baker | Prend en charge le lancer de rayons du GPU |
| --- | --- |
| Masque d’opacité | <div><img alt="(coche)&quot; data-preserve-html=&quot;true" src="../../assets/check.svg"/></div> |
| Position | <div><img alt="(coche)&quot; data-preserve-html=&quot;true" src="../../assets/check.svg"/></div> |
| Position basse | <div><img alt="(erreur)&quot; data-preserve-html=&quot;true" src="../../assets/error.svg"/></div> |
| Épaisseur | <div><img alt="(coche)&quot; data-preserve-html=&quot;true" src="../../assets/check.svg"/></div> |
| Texture transférée | <div><img alt="(coche)&quot; data-preserve-html=&quot;true" src="../../assets/check.svg"/></div> |
| Monde à tangente | <div><img alt="(erreur)&quot; data-preserve-html=&quot;true" src="../../assets/error.svg"/></div> |


+++

+++Version 2

| Baker | Prend en charge le lancer de rayons du GPU |
| --- | --- |
| Occlusion ambiante | <div><img alt="(erreur)&quot; data-preserve-html=&quot;true" src="../../assets/error.svg"/></div> |
| Ambient occlusion à partir du maillage | <div><img alt="(coche)&quot; data-preserve-html=&quot;true" src="../../assets/check.svg"/></div> \* |
| Bent normals à partir du maillage | <div><img alt="(coche)&quot; data-preserve-html=&quot;true" src="../../assets/check.svg"/></div> \* |
| Color à partir du maillage | <div><img alt="(erreur)&quot; data-preserve-html=&quot;true" src="../../assets/error.svg"/></div> \* |
| Convertir UV en SVG | <div><img alt="(erreur)&quot; data-preserve-html=&quot;true" src="../../assets/error.svg"/></div> |
| Curvature à partir du maillage | <div><img alt="(coche)&quot; data-preserve-html=&quot;true" src="../../assets/check.svg"/></div> \* |
| Height à partir du maillage | <div><img alt="(erreur)&quot; data-preserve-html=&quot;true" src="../../assets/error.svg"/></div> \* |
| Normal à partir du maillage | <div><img alt="(erreur)&quot; data-preserve-html=&quot;true" src="../../assets/error.svg"/></div> \* |



| Baker | Prend en charge le lancer de rayons du GPU |
| --- | --- |
| Masque d’opacité du maillage | <div><img alt="(erreur)&quot; data-preserve-html=&quot;true" src="../../assets/error.svg"/></div> \* |
| Position à partir du maillage | <div><img alt="(erreur)&quot; data-preserve-html=&quot;true" src="../../assets/error.svg"/></div> \* |
| Position | <div><img alt="(erreur)&quot; data-preserve-html=&quot;true" src="../../assets/error.svg"/></div> |
| Thickness à partir du maillage | <div><img alt="(coche)&quot; data-preserve-html=&quot;true" src="../../assets/check.svg"/></div> \* |
| Texture transférée du maillage | <div><img alt="(erreur)&quot; data-preserve-html=&quot;true" src="../../assets/error.svg"/></div> \* |
| Sens de l&#39;espace dans le monde | <div><img alt="(erreur)&quot; data-preserve-html=&quot;true" src="../../assets/error.svg"/></div> |
| Normales de l&#39;espace mondial | <div><img alt="(erreur)&quot; data-preserve-html=&quot;true" src="../../assets/error.svg"/></div> |


\* : prend en charge le lancer de rayons CPU, beaucoup plus lent que le lancer de rayons GPU.

+++
