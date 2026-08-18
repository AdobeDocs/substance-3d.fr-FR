---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-integrations/3d-applications/blender/troubleshooting.html"
breadcrumb-title: ''
description: Diagnostiquez et résolvez les problèmes courants avec le module complémentaire Substance 3D dans Blender à l’aide de la console système.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > Blender > Troubleshooting
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Dépannage
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '812'
ht-degree: 0%

---


# Dépannage

La console système peut être utilisée pour diagnostiquer les erreurs rencontrées lors de l’utilisation du module complémentaire. La fenêtre de la console système de Blender s&#39;ouvre différemment selon votre système d&#39;exploitation. Pour obtenir des instructions détaillées, suivez les étapes indiquées sur la [page de documentation](https://docs.blender.org/manual/en/2.79/advanced/command_line/introduction.html#console-window-status-and-error-messages) de la console système de Blender. La sortie de la console peut être utile en cas de problèmes inattendus, tels que des textures non chargées ou des matières bloquées dans le traitement.

Pour signaler un bug, rejoignez le canal #substance-blender-beta sur le [serveur Substance Discord](https://discord.com/invite/substance3d) ou visitez les [communautés d&#39;Adobes](https://community.adobe.com/t5/substance-3d-plugins/ct-p/ct-substance-3d-plugins?page=1&sort=latest_replies&lang=all&tabid=all&topics=label-blender). Les informations pertinentes du journal de la console et les étapes de reproduction pour le problème peuvent être incluses dans les rapports.

## Problèmes courants et solutions

* *Erreurs de console liées à WMIC.*
  * *Parfois, les installations Windows n&#39;incluent pas la ligne de commande WMI, ce qui est nécessaire dans ce cas. Voici comment résoudre ce problème manuellement :*
    * Accéder à Paramètres - Système - Fonctionnalités facultatives
    * Sélectionnez « Afficher les fonctionnalités », puis « Ajouter une fonctionnalité »
    * Cela fera apparaître une nouvelle fenêtre, fera défiler la liste pour trouver WMIC, cochera la case, puis appuyez sur Suivant, dans la fenêtre suivante appuyez sur Ajouter.
    * Vous devriez maintenant être dirigé vers une nouvelle fenêtre qui montre la progression de l&#39;installation de la WMIC sous les actions récentes.
    * *Notez que le téléchargement peut prendre quelques minutes. Réinitialisez ensuite votre ordinateur et redémarrez Blender et le module complémentaire. Lorsque vous cliquez sur le chargement dans le panneau Substance 3D, la fenêtre du navigateur de fichiers doit maintenant s&#39;afficher.*
  * Si cela ne résout pas le problème, vous devrez peut-être également définir WMIC dans vos variables PATH. Consultez la documentation de votre version spécifique de Windows.
* *Tous les paramètres n’apparaissent pas dans le panneau Substance 3D après la mise à jour du module complémentaire et le chargement d’un matériau.*
  * Cela peut se produire lors de la suppression d’une ancienne version du module complémentaire et de l’installation d’une nouvelle version dans la même session, car les anciens fichiers peuvent toujours être mis en cache dans le système.\
    Le redémarrage de Blender devrait permettre aux modifications de prendre effet.
* *Problèmes lors de l’installation du module complémentaire./ Le traitement des matériaux est bloqué entre les sessions. / Les matières ne génèrent pas de textures entre les sessions. / Erreurs lors du chargement des fichiers .sbsar.*
  * Cela peut être un problème avec l’installation des outils d’intégration et est généralement résolu en supprimant manuellement les outils. Consultez la page [Désinstallation du module complémentaire](../../../3d-applications/blender/uninstalling-the-add-on/uninstalling-the-add-on.md) pour obtenir des instructions sur la suppression manuelle.
* *Les matières ne sont pas mises à jour dans la vue de rendu Cycles*.
  * Par défaut, le module complémentaire ne met pas à jour les textures dans la vue de rendu Cycles. Cependant, ils peuvent être mis à jour de force en activant <b>Cycles mise à jour automatique des textures</b>dans les préférences du module complémentaire.
* Les paramètres semblent revenir en arrière après l’enregistrement dans la vue de rendu Cycles.
  * Il s’agit d’un problème de mise en cache connu du côté du mélangeur qui est uniquement visuel. Lors de l’enregistrement, aucun message n’est envoyé au moteur distant pour mettre à jour les fichiers de texture générés. Les textures apparaîtront normales après avoir quitté la vue de rendu Cycles et y être retournées.
* *Les matériaux ne sont plus mis à jour après l’annulation/la modification des paramètres.*
  * La mise à jour des matériaux peut échouer après l’annulation des actions. Même si les paramètres reviennent à l’état précédent, les textures ne sont pas annulées pour correspondre. Pour que la texture soit à nouveau mise à jour, utilisez le bouton Actualiser pour rétablir les paramètres par défaut et recharger les textures.
* *Les couleurs définies dans la Substance Designer apparaissent légèrement différemment dans le sélecteur de couleurs de Blender et les valeurs de couleur ne sont pas les mêmes.*
  * Le mélangeur applique une correction gamma aux couleurs uniquement pour le sélecteur de couleurs du mélangeur. Bien que cela entraîne une différence dans le sélecteur de couleurs, les couleurs qui apparaissent dans les textures sont exactes par rapport aux valeurs définies dans les applications de Substance.
* Erreur de console *« wmic non reconnu » lors du chargement d&#39;un matériau dans Windows.*
  * Ce problème se produit lorsque C:\Windows\System32\wbem\ n’est pas inclus dans les variables système PATH. Consultez la documentation de votre version spécifique de Windows.
* Erreur « Type de processeur incorrect est exécutable » *sur Mac.*
  * Ce problème se produit lorsque Rosetta n’est pas activé sur les ordinateurs ARM Mac. Voir [Page Apple Rosetta](https://support.apple.com/en-us/102527) pour plus d&#39;informations. Consultez également ce [guide d&#39;installation](https://medium.com/@jithmisha/fix-for-macbook-air-m1-m2-bad-cpu-type-in-executable-error-3719a0a1cb6) pour obtenir des instructions supplémentaires.
* *Les modifications apportées au graphique de nuanceur sont annulées lors de l&#39;utilisation du bouton Actualiser ou de la mise à jour des paramètres.*
  * Le module complémentaire a actualisé les connexions dans le graphique après les modifications ou les actualisations. Pour contourner ce problème, dupliquez le matériau du mélangeur créé à partir du fichier .sbsar et donnez-lui un nouveau nom de votre choix. Ajoutez vos nœuds uniquement au duplicata. Les textures seront mises à jour dans le groupe de nœuds tout en conservant les nœuds ajoutés par l’utilisateur. Lors de l’actualisation, copiez ces nœuds et collez-les de nouveau dans un nouveau graphique après l’actualisation.
