---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/renderers/keyshot.html"
breadcrumb-title: ''
description: Utilisez les matériaux de Substance dans le rendu Keyshot pour la visualisation du produit avec les cartes de texture exportées.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Renderers > Keyshot
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Keyshot
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 8%

---


# Keyshot

*Keyshot 6.1.72*[&#x200B; Téléchargez Un Exemple De Scène](https://www.dropbox.com/s/rvjsbbcx7c74aah/keyshot.zip?dl=0)

## Exportation de Substance Painter

1. Pour Keyshot, vous devrez configurer un paramètre prédéfini d’exportation à l’aide de Diffuse, Réflexion, Métallique, Rugosité et Normal (X direct).

   ![](https://helpx-prod.scene7.com/is/image/HelpxProd/key-01?$png$&jpegSize=300&wid=1794)

## Configuration avancée du Matériau

Vous utiliserez 2 matériaux avancés. L&#39;un sera pour métallique et l&#39;autre pour diélectrique.

1. Définissez le matériau sur Avancé et graphe le matériau.

   **Métallique :**\
   a. Réglez l’indice de réfraction sur 10\
   b. Définissez les mappages comme indiqué dans le tableau ci-dessous

   | texture de Substance Painter | Canal de Matériau avancé |
   | --- | --- |
   | Diffuse | Diffuse |
   | Métallique | Opacité |
   | Normale | Saut \*Normal Activé |
   | Rugosité | Rugosité |
   | Réflexion | Spéculaire |

1. Création d’un Matériau avancé

   **Diélectrique :**\
   a. Réglez l’indice de réfraction sur 1,5\
   b. Définissez les mappages comme indiqué dans le tableau ci-dessous

   | texture de Substance Painter | Canal de Matériau avancé |
   | --- | --- |
   | Diffuse | Diffuse |
   | Normale | Saut \*Normal Activé |
   | Rugosité | Rugosité |
   | Réflexion | Spéculaire |

1. Prenez la sortie du Matériau avancé Métallique et ajoutez-la au + du Matériau avancé diélectrique. Un champ Libellé est alors créé en matériau.

   ![](../../assets/key-02.png)
