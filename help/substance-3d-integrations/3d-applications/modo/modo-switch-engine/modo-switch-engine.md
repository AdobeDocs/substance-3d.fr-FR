---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/3d-applications/modo/modo-switch-engine.html"
breadcrumb-title: ''
description: Basculez entre les moteurs de Substance CPU et GPU dans MODO pour optimiser les performances en fonction de votre matériel.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > MODO > Modo Switch Engine
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Modo Switch Engine
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 0%

---


# Modo Switch Engine

## Substance Engine de commutation

Il existe deux versions de la Substance Engine : le processeur et le GPU. Le moteur GPU est utilisé pour créer des textures supérieures à 2K. Le moteur CPU est uniquement capable de générer des textures jusqu’à 2K. Si vous avez besoin de textures en haute résolution, vous devez passer au moteur GPU.

Accédez à l’option Paramètres de Substance dans le menu Kit de Substance et choisissez Changer de Substance Engine. Vous devez redémarrer MODO pour que le moteur GPU soit activé. Ce paramètre agit comme une préférence globale. Le moteur GPU sera ensuite activé à chaque exécution de MODO jusqu’à ce qu’il soit commuté manuellement.

>[!NOTE]
>
> **L’utilisation du moteur GPU Substance nécessite un GPU avec une RAM vidéo dédiée de 1 Go ou plus. Les GPU intégrés ne sont pas pris en charge.**\
> Nvidia : GeForce 650M 1 Go ou plus\
> AMD : 6870M ou supérieur

![](../../../assets/switch.png)
