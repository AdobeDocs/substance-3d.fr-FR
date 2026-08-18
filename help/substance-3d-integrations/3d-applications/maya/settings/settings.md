---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/3d-applications/maya/settings.html"
breadcrumb-title: ''
description: Configurez les paramètres du plug-in de Substance dans Maya via l’étagère de Substance ou le menu pour personnaliser le comportement.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > Maya > Settings
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Paramètres
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 1%

---


# Paramètres

Le menu des paramètres de Substance est accessible via le panneau Substance ou le menu Substance. Les paramètres de ce menu sont stockés dans un fichier de configuration modifiable « substance.cfg ».

>[!NOTE]
>
> **Emplacements des fichiers de configuration**
> 
> **Windows** :\
> C:\Users\\Documents\maya\\substance\\
> **MacOS** :\
> /Users//Library/Preferences/Autodesk/maya//substance/\
> **Linux** :\
> /home//maya//substance/

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Résolution par défaut

Définit la résolution par défaut pour un nœud de Substance lorsque le fichier sbsar est chargé.

## Workflow de rendu

Définit le processus de rendu par défaut à utiliser sur le nœud de Substance.

## Substance Engine

Définition de préférences spécifiques à la Substance Engine et globales à tous les nœuds de Substance. Le moteur de Substance est utilisé pour calculer les textures de Substance.

### Type de moteur

La Substance Engine est disponible en tant que CPU et GPU Engine. Le changement de moteur nécessitera le redémarrage de Maya. Le moteur GPU permet des résolutions plus élevées que le moteur CPU.

>[!WARNING]
>
> Il peut y avoir des différences de calcul entre le processeur et le GPU. Pour obtenir des résultats cohérents, il est donc préférable de définir le type sur le même moteur utilisé dans la Substance Designer.

Les cœurs du processeur et la mémoire du moteur sont des paramètres pour la quantité de ressources que le moteur de Substance de données est autorisé à utiliser.

### Blocage des rendus

Cette option vous permet de définir si le calcul du moteur de Substance de données bloquera les processus de l&#39;interface utilisateur Maya. Lorsque cette option est activée, le moteur de Substance de données est prioritaire et bloque les processus de l’interface utilisateur Maya. Lorsque cette option est désactivée, les processus de l’interface utilisateur Maya ne sont pas bloqués par les calculs du moteur de Substance.

## Sorties du cache sur le disque

Définit l&#39;emplacement du cache, le type de fichier et le dossier de cache par défaut pour tous les nœuds de Substance nouvellement créés dans un projet.

## Extensions de rendu

Activez les extensions de rendu pour utiliser les sorties de Substance directement avec les nuanceurs Arnold.

## Taille physique

Activez cette option si la Taille physique doit être utilisée par défaut lors du chargement des fichiers sbsar et si elle doit être recalculée lors du rechargement du fichier sbsar.

</td>
<td style="border: 0;" valign="top">

![](../../../assets/settings-35.png)

</td>
</tr>
</table>
