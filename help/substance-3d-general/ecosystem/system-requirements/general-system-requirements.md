---
helpx_url: 'https://helpx.adobe.com/substance-3d-general/ecosystem/general-system-requirements.html'
breadcrumb-title: ''
description: Vérifiez la configuration requise pour les applications Substance 3D pour vous assurer que votre matériel répond aux spécifications minimales, recommandées ou optimales.
helpx_creative_field: ''
helpx_description: General Knowledge > Ecosystem > General system requirements
helpx_experience_level: ''
helpx_learn_topic: ''
helpx_tags: ''
title: Configuration requise générale
user-guide-description: ''
user-guide-title: ''
source-git-commit: eef3d78f33034f2c24f4c4471d9ccac805184525
workflow-type: tm+mt
source-wordcount: '625'
ht-degree: 2%
---

# Configuration requise générale

## Configuration matérielle requise

+++Windows

|  | Minimum | Recommandé | Optimale |
| --- | --- | --- | --- |
| **SE** | Windows 11 64 bits version 23H2 | Windows 11 64 bits version 24H1 | Windows 11 64 bits version 24H2 |
| **CPU** | Intel Core i5 AMD Ryzen 5 | Intel Core i7 AMD Ryzen 7 | Intel Core i9 AMD Ryzen 9 |
| **GPU** | NVIDIA GeForce RTX 2060 Super NVIDIA Quadro RTX 4000 AMD Radeon RX 5700 XT AMD Radeon Pro W5700 | NVIDIA GeForce RTX 3080 NVIDIA Quadro A4000 AMD Radeon RX 6800 XT AMD Radeon Pro W7700 | NVIDIA GeForce RTX 4090 NVIDIA Quadro RTX 5000 Ada Generation AMD Radeon RX 7900 XTX AMD Radeon Pro W7800 |
| **VRAM** | 8 Go | 16 Go | 24 Go |
| **RAM** | 16 Go | 32 Go | 64 Go |
| **Stockage** | Disque SSD avec 30 Go d’espace disponible | Disque SSD avec 50 Go d’espace disponible | Disque SSD avec 70 Go d’espace disponible |

+++

+++macOS

|  | Minimum | Recommandé | Optimale |
| --- | --- | --- | --- |
| **SE** | macOS 15 Sequoia | macOS 27 Golden Gate | macOS 27 Golden Gate |
| **CPU** | Apple M1 | Apple M2 Pro | Apple M4 Pro |
| **GPU** | Apple M1 | Apple M2 Pro | Apple M4 Pro |
| **RAM** | 16 Go | 32 Go | 64 Go |
| **Stockage** | Disque SSD avec 30 Go d’espace disponible | Disque SSD avec 50 Go d’espace disponible | Disque SSD avec 70 Go d’espace disponible |

>[!WARNING]
>
> Pour les pipelines construits avec la [plateforme de référence VFX](https://vfxplatform.com/) en tête, les applications Substance 3D peuvent toujours être installées sur macOS 14 Sonoma. Cependant, les applications de Substance de données ne sont plus testées sur les versions du système d’exploitation inférieures à la configuration minimale requise, de sorte que la stabilité n’est pas garantie. La mise à jour vers une version plus récente du système d’exploitation est recommandée.

+++

+++Linux

|  | Minimum | Recommandé | Optimale |
| --- | --- | --- | --- |
| **SE** | **ETLA d’entreprise** RHEL 8.6 ou version ultérieure ou RHEL 9.2 ou version ultérieure **Steam** Ubuntu 22.04.1 LTS | **ETLA d’entreprise** RHEL 8.6 ou version ultérieure ou RHEL 9.4 ou version ultérieure **Steam** Ubuntu 22.04.1 LTS ou version ultérieure | **ETLA d’entreprise** RHEL 8.6 ou version ultérieure ou RHEL 9.4 ou version ultérieure **Steam** Ubuntu 22.04.1 LTS ou version ultérieure |

**Red Hat Enterprise Linux (RHEL) 9.x** : le package xcb-util-cursor requis par nos applications a été supprimé du référentiel EPEL 9 le 10 mai 2024. À partir de cette date, le package est pris en charge par le référentiel RHEL 9 par défaut, qui coïncide avec la version de RHEL 9.4. Les clients utilisant des versions de RHEL antérieures à la version 9.4 ne pourront plus s’approvisionner en package xcb-util-cursor à partir du référentiel EPEL 9 après le 10 mai 2024.

Pour plus d&#39;informations sur la disponibilité de ce package dans le référentiel RHEL 9 par défaut, consultez : [Red Hat Enterprise Linux 9 - Manifeste du package - Référentiel AppStream](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/9/html-single/package_manifest/index#AppStream-repository)

Pour plus d&#39;informations sur cette modification, consultez : [Red Hat Bugzilla - Bug 2238273](https://bugzilla.redhat.com/show_bug.cgi?id=2238273) , [Red Hat Bugzilla - Bug 2212302](https://bugzilla.redhat.com/show_bug.cgi?id=2212302)

+++

+++VR

| Marque | Modèles |
| --- | --- |
| Meta | Rift, Rift S, Quest, Quest 2 (avec lien), Quest Pro |

+++

Pour plus de détails, examinez les exigences de chaque application :

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../../assets/sa-appicon-noshadow-256.png" alt="Icône Substance 3D Sampler" width="64px"/><br><a href="https://experienceleague.adobe.com/en/docs/substance-3d-sampler/using/getting-started/system-requirements">Substance 3D Sampler</a></td>
    <td style="border: 0;" valign="top"><img src="../../assets/ds-appicon-noshadow-256.png" alt="Icône Substance 3D Designer" width="64px"/><br><a href="https://experienceleague.adobe.com/en/docs/substance-3d-designer/using/getting-started/system-requirements">Substance 3D</a> <a href="https://experienceleague.adobe.com/en/docs/substance-3d-designer/using/getting-started/system-requirements">Designer</a></td>
    <td style="border: 0;" valign="top"><img src="../../assets/pt-appicon-noshadow-256.png" alt="Icône Substance 3D Painter" width="64px"/><br><a href="https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/getting-started/system-requirements">Substance 3D Painter</a></td>
  </tr>
</table>

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../../assets/md-appicon-noshadow-256.png" alt="Icône Substance 3D Modeler" width="64px"/><br><a href="https://helpx.adobe.com/substance-3d-modeler/getting-started/system-requirements.html">Substance 3D Modeler</a></td>
    <td style="border: 0;" valign="top"><img src="../../assets/sg-appicon-noshadow-256.png" alt="Icône Substance 3D Stager" width="64px"/><br><a href="https://helpx.adobe.com/substance-3d-stager/getting-started/system-requirements.html">Substance 3D Stager</a></td>
    <td style="border: 0;" valign="top"></td>
  </tr>
</table>

## Remarques supplémentaires

### Configuration non prise en charge

* Les configurations d’ordinateur Apple avec les eGPU et les GPU installés par l’utilisateur ne sont pas prises en charge.
* Les ordinateurs virtuels Windows ne sont pas pris en charge.
* Le système d’exploitation du serveur Windows n’est pas pris en charge.
