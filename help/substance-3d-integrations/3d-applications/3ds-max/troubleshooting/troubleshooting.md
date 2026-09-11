---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-integrations/3d-applications/3ds-max/troubleshooting.html"
breadcrumb-title: ''
description: Diagnostiquez et résolvez les problèmes avec le plug-in de Substance dans 3ds Max à l’aide de Script Listener pour les messages d’erreur.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > 3ds Max > Troubleshooting
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Dépannage
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 1%

---


# Dépannage

Le récepteur de scripts peut être utilisé pour diagnostiquer les erreurs rencontrées lors de l’utilisation du plug-in. Pour ouvrir l’écouteur de script, accédez à Menu Script > Écouteur de script. Lorsqu’une erreur se produit lors de l’utilisation du plug-in, un message d’erreur correspondant s’affiche dans cette fenêtre Script Listener. Pour plus d&#39;informations, consultez la [documentation officielle de Script Editor](https://help.autodesk.com/view/3DSMAX/2023/ENU/?guid=GUID-C8019A8A-207F-48A0-985E-18D47FAD8F36).

Pour signaler un bug, rejoignez le canal #3dsmax-plugin sur le [serveur Substance Discord](https://discord.com/invite/substance3d) ou visitez les [communautés d&#39;Adobes](https://community.adobe.com/t5/substance-3d-plugins/ct-p/ct-substance-3d-plugins?page=1&sort=latest_replies&lang=all&tabid=all&topics=label-autodesk3dsmax). Les informations pertinentes du journal de la console et les étapes de reproduction pour le problème peuvent être incluses dans les rapports.

## Problèmes connus

* *Le remplacement d&#39;un fichier .sbsar qui utilise une sortie diffuse par un fichier .sbsar qui n&#39;utilise pas de diffusion entraîne un rendu noir en raison de la déconnexion de la diffusion manquante.*
  * Ce comportement est attendu pour les nœuds à sorties multiples. Au lieu de charger ces fichiers .sbsars en utilisant le même nœud, il est recommandé d&#39;utiliser des nœuds de Substance différents pour chacun.
