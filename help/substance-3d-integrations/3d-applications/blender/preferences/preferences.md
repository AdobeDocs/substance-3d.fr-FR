---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/3d-applications/blender/preferences.html"
breadcrumb-title: ''
description: Configurez les préférences du module complémentaire Substance 3D dans Blender pour personnaliser le comportement et les paramètres du plug-in.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > Blender > Preferences
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Préférences
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '845'
ht-degree: 0%

---


# Préférences

Les préférences du module complémentaire se trouvent dans la fenêtre des préférences de Blender. Accédez à Modifier > Préférences > Modules complémentaires et recherchez Node : module complémentaire Substance 3D Adobe pour Blender.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Première moitié du menu des préférences du module complémentaire.](../../../assets/blender-prefs-1.png)

</td>
<td style="border: 0;" valign="top">

![Deuxième moitié du menu des préférences du module complémentaire.](../../../assets/blender-prefs-2-b.png)

</td>
</tr>
</table>

<b>Désinstaller</b> : supprime le module complémentaire du système et le supprime de la liste des modules complémentaires dans Blender.

<b>Signaler un bogue</b> : ouvre Substance 3D pour Blender Discord.

<b>Accepter le dossier d&#39;outils</b> : ouvre le navigateur de fichiers Blender pour choisir le chemin d&#39;installation des outils d&#39;intégration de Substance.

<b>Ouvrir les outils </b> : ouvrez le navigateur de fichiers système à l&#39;emplacement du dossier Outils d&#39;intégration.

<b>Réinitialiser le chemin</b> : réinitialise le chemin du dossier Outils d&#39;intégration à l&#39;emplacement par défaut.

<b>Outils de désinstallation</b> : supprime la version installée des outils d’intégration Substance 3D.

<b>Outils de mise à jour</b> : ouvre le navigateur de fichiers pour sélectionner le fichier zip des outils et les mettre à jour.

<b>Documentation</b> : ouvre la page de documentation sur l’écosystème et les plug-ins dans le navigateur.

<b>Forums</b> : ouvre les forums de la communauté Adobe dans le navigateur.

<b>Discord Server</b> : ouvre le serveur Discord Ecosystem et Plug-ins dans le navigateur.

<b>Répétition</b> : ajustez les répétitions X, Y et Z du matériau. Le verrou peut être utilisé pour dissocier les valeurs et les ajuster individuellement.

<b>Résolution</b> : résolution par défaut pour les textures générées. Le verrou peut être utilisé pour dissocier afin de définir leurs résolutions indépendamment.

<b>Appliquer le type </b> : définit le comportement du bouton Appliquer : <b>Insérer </b> remplacera le matériau actif par le matériau de Substance sélectionné, et <b>Ajouter</b> ajoutera le matériau à l&#39;objet dans un nouvel emplacement de matériau.

<b>Format d&#39;exportation d&#39;image</b> : lorsque des images générées dans Blender sont utilisées comme entrées d&#39;image pour un matériau de Substance, ce format est utilisé pour enregistrer cette image dans le dossier temporel.

<b>Groupes d&#39;entrée réduits par défaut</b> : les groupes d&#39;entrée du matériau de Substance sont développés ou réduits par défaut.

<b>Mettre à jour uniquement les textures par défaut</b> : active/désactive les paramètres de Substance de mise à jour météorologique qui n&#39;affectent que les textures de sortie dans le réseau d&#39;Ombrages du mélangeur. La désactivation de cette option réinitialise les connexions de nœuds après le réglage des paramètres. Il est recommandé d&#39;activer cette option lors de l&#39;ajout de nœuds supplémentaires à un matériau, sinon ils seront déconnectés après le réglage des paramètres.

<b>Moteur distant de Substances </b> : définit le matériel utilisé par le moteur distant de Substances.

<b>Appliquer automatiquement la matière</b> : lorsqu&#39;un matériau de Substance est créé, attachez automatiquement le matériau aux objets sélectionnés dans un nouvel emplacement de matériau.

<b>Mettre automatiquement en surbrillance la matière des objets sélectionnés</b> : modifiez la matière en surbrillance dans le panneau Substance 3D si un objet avec cette matière est sélectionné.

<b>Cycles : mise à jour automatique des textures</b> : force la texture à se mettre à jour dans la fenêtre 3D lors de l’utilisation de la vue de rendu Cycles.

<b>Supprimer la confirmation de suppression de préconfiguration</b> : supprime la fenêtre de confirmation qui apparaît lors de la suppression des préconfigurations de matériau.

<b>Créer un matériau avec l’option Faux utilisateur activée</b> : selon le temps, le matériau est créé avec l’option « Faux utilisateur » activée ou désactivée. Les données du mélangeur marquées comme faux utilisateur ne sont pas vidées après la fermeture, même lorsque les données ne sont pas utilisées.

<b>Démarrer automatiquement le moteur distant de Substance de données </b> : basculez si le moteur distant de Substance de données est initialisé au démarrage de Blender. Si cette option est désactivée, le moteur distant démarrera uniquement lorsqu&#39;un utilisateur chargera un bouton ou utilisera le raccourci de chargement.

>[!NOTE]
>
> REMARQUE : si vous utilisez Substance Connector, le SRE doit être actif pour que l’application expéditrice détecte Blender comme point de terminaison.

<b>Chemin de bibliothèque SBSAR</b> : dossier ouvert par défaut lorsque vous cliquez sur le bouton Charger pour rechercher un fichier substance.

<b>Dossier temporaire </b> : ce dossier sera l’emplacement par défaut où les textures seront stockées avant qu’un fichier ne soit enregistré pour la première fois.

<b>Copier les fichiers .sbsar lors de l&#39;enregistrement dans</b> : lorsque cette option est activée, les fichiers .sbsar sont copiés dans le chemin relatif spécifié lors de l&#39;enregistrement du fichier. Cela peut faciliter le partage de projets entre appareils.

<b>Lors de l&#39;enregistrement, copier les textures dans</b> : lorsqu&#39;un fichier est enregistré pour la première fois, les textures du dossier temporaire sont copiées à cet emplacement. La variable $matname est utilisée pour créer des sous-dossiers pour chaque matière.

<b>Paramètre prédéfini de shader</b> : définit le paramètre prédéfini de shader par défaut utilisé lors de la création de matériaux Blender à partir de fichiers de substances. Peut être défini sur Standard pour la projection basée sur les UV ou la projection pour la projection basée sur les boîtes, sphères et cylindres.

<b>Niveau intermédiaire du Displacement</b> : la valeur par défaut est la base du displacement dans le nœud de Displacement. Les valeurs supérieures à la valeur par défaut déplacent les surfaces vers l&#39;extérieur et les valeurs inférieures à la valeur par défaut les déplacent vers l&#39;intérieur.

<b>Échelle de Displacement</b> : valeur d&#39;échelle par défaut dans le nœud de Displacement.

<b>Intensité d&#39;émission</b> : valeur par défaut de la force d&#39;émission dans le nœud BSDF basé sur des principes.

<b>Fusion de projection</b> : définit la quantité de fusion entre les angles pour les ombrages de méthode de projection.

<b>Mélange AO</b> - Lorsque l&#39;Occlusion ambiante est activée en tant que sortie, cette valeur détermine la valeur de facteur par défaut du nœud MixRGB utilisé pour combiner la couleur de base et les textures de l&#39;Occlusion ambiante.

<b>Sorties</b> : les sorties individuelles des matériaux peuvent être activées ou désactivées. L’espace colorimétrique, le format de fichier et la profondeur des couleurs par défaut des sorties individuelles peuvent également être ajustés.

<b>Raccourcis </b> : personnalisez les touches de raccourci utilisées pour afficher un menu flottant, charger un matériau de Substance et appliquer le matériau actif. Les mises à jour de raccourcis nécessitent un redémarrage pour prendre effet.
