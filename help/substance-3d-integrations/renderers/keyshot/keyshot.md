---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/renderers/keyshot.html"
breadcrumb-title: ''
description: Utilisez des matériaux de Substance dans le rendu Keyshot pour la visualisation du produit avec les textures graphiques exportées.
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

*Keyshot 6.1.72*[&#x200B; Télécharger Un Exemple De Scène](https://www.dropbox.com/s/rvjsbbcx7c74aah/keyshot.zip?dl=0)

## Exportation de Substance Painter

1. Pour Keyshot, vous devrez configurer un paramètre prédéfini d’exportation en utilisant Diffus, Réflexion, Métallique, Rugosité et Normal (X direct).

   ![](https://helpx-prod.scene7.com/is/image/HelpxProd/key-01?$png$&jpegSize=300&wid=1794)

## Configuration avancée des matériaux

Vous utiliserez 2 matériaux avancés. L&#39;un sera pour métallique et l&#39;autre pour diélectrique.

1. Définissez la matière sur Avancé et dessinez un graphique de la matière.

   **Métallique :**\
   a. Réglez l’indice de réfraction sur 10\
   b. Définissez les mappages comme indiqué dans le tableau ci-dessous

   | texture Substance Painter | Canal de matériau avancé |
   | --- | --- |
   | Diffuse | Diffuse |
   | Métallique | Opacité |
   | Normale | Saut \*Normal Activé |
   | Rugosité | Rugosité |
   | Réflexion | Spéculaire |

1. Créer un matériau avancé

   **Diélectrique :**\
   a. Réglez l’indice de réfraction sur 1,5\
   b. Définissez les mappages comme indiqué dans le tableau ci-dessous

   | texture Substance Painter | Canal de matériau avancé |
   | --- | --- |
   | Diffuse | Diffuse |
   | Normale | Saut \*Normal Activé |
   | Rugosité | Rugosité |
   | Réflexion | Spéculaire |

1. Prenez la sortie du matériau avancé métallique et ajoutez-la au + du matériau avancé diélectrique. Cela créera un champ Étiquette sur le matériau.

   ![](../../assets/key-02.png)
