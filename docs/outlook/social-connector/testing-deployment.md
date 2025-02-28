---
title: Test de déploiement
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 8b585200-33e7-4607-a603-0c7e52a6b09d
description: Cette rubrique décrit certains scénarios que vous devez tester concernant l’installation et la désinstallation d’un fournisseur OSC (Outlook Social Connector).
ms.openlocfilehash: 33c5bc8b7bc6b9360e66ed6cac01c1c1e7a42d2a
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63378169"
---
# <a name="testing-deployment"></a>Test de déploiement

Cette rubrique décrit certains scénarios que vous devez tester concernant l’installation et la désinstallation d’un fournisseur OSC (Outlook Social Connector).

<a name="olosc_TestingDeployment_PresenceOfOutlook"> </a>

## <a name="presence-of-outlook-and-the-osc-on-client-computer"></a>Présence de Outlook osc sur l’ordinateur client

Les facteurs qui affectent l’installation d’un fournisseur OSC incluent le nombre de bits du système d’exploitation, la présence et le nombre de bits de Outlook et l’OSC activé dans Outlook.
  
Un fournisseur OSC peut être écrit pour une version 32 bits ou 64 bits de l’OSC. Outlook 2010 et Outlook 2013 sont disponibles dans les versions 32 bits et 64 bits, et Office Outlook 2003 et Office Outlook 2007 sont disponibles uniquement dans les versions 32 bits. Sur un système d’exploitation Windows 64 bits, vous pouvez installer des Outlook 32 bits ou 64 bits. Sur un système d’exploitation 32 bits, vous ne pouvez installer que des Outlook 32 bits, mais pas 64 bits. En fonction du nombre de bits de la version installée de Outlook et du fournisseur OSC lui-même, l’utilisateur doit utiliser le programme d’installation approprié pour installer un fournisseur OSC du nombre de bits approprié. Par exemple, si le Outlook 64 bits est installé et que le fournisseur OSC est un composant COM natif, un fournisseur OSC 32 bits ne fonctionne pas et l’utilisateur doit utiliser le programme d’installation approprié pour installer un fournisseur OSC 64 bits.
  
Le code de déploiement de votre fournisseur OSC peut supposer que l’utilisateur dispose d’une version prise en charge de Outlook sur l’ordinateur. Toutefois, si la version actuelle d’OSC ne se trouve pas sur l’ordinateur client, votre code de déploiement peut télécharger et installer une version appropriée de l’OSC à l’aide d’URL de lien g <https://g.live.com>spécialement construites sur . Ces liens g dépendent de la version et du nombre de bits Outlook paramètres régionaux de l’ordinateur client. Pour plus d’informations sur l’utilisation des liens g pour installer ou mettre à jour OSC, consultez la liste de [contrôle d’installation](installation-checklist.md).
  
Avant d’installer un fournisseur OSC, l’Outlook utilisateur doit s’assurer que le module de mise en service d’OSC est activé dans Outlook.
  
La méthode recommandée pour déployer un fournisseur OSC consiste à utiliser un package Windows Installer (.msi). Testez chacun des scénarios suivants pour vérifier que le déploiement fonctionne correctement pour le fournisseur.
  
|**Scénario**|**Comportement attendu**|
|:-----|:-----|
|Outlook n’est pas présent : Outlook 2003 ou Outlook 2007 n’est pas installé et Outlook 2010 ou Microsoft Outlook 2013 n’est pas installé et n’a pas été remis par Click-to-Run. |Le déploiement échoue. |
|Outlook 2003 ou Outlook 2007 n’est pas installé, mais Outlook 2010 ou Microsoft Outlook 2013 a été remis par Click-to-Run. |Le fournisseur 32 bits est déployé. |
|Outlook 2003 ou Outlook 2007 est installé, mais l’OSC n’est pas installé. |Le programme d’installation installe OSC et tous les correctifs. Une fois l’OSC correctement installé, le programme d’installation déploie le fournisseur. |
|Outlook 2003 ou Outlook 2007 est installé et une version antérieure de l’OSC est installée. |Le programme d’installation met à jour OSC, via un lien g vers des correctifs, puis déploie le fournisseur. |
|Outlook 2003 ou 2007 est installé et l’OSC est à jour. |Le programme d’installation déploie le fournisseur 32 bits. |
|Outlook 2010 ou Microsoft Outlook 2013 est installé, mais l’OSC n’est pas installé. |Le programme d’installation échoue avec un message d’erreur approprié. |
|Outlook 2010 ou Microsoft Outlook 2013 est installé et une version antérieure d’OSC est installée. |Le programme d’installation approprié pour le nombre de bits du Outlook 2010 ou du Microsoft Outlook 2013 installé, met à jour l’OSC via le lien g vers des correctifs, puis déploie le fournisseur approprié. |
|Outlook 2010 ou Microsoft Outlook 2013 est installé et l’OSC est à jour. |Le programme d’installation approprié pour le nombre de bits de la Outlook 2010 ou de la Microsoft Outlook 2013 installée (32 bits ou 64 bits) déploie le fournisseur approprié. |

<a name="olosc_TestingDeployment_PresenceOfOutlook"> </a>

## <a name="installed-location-and-registry-keys"></a>Emplacement et clés de Registre installés

Vérifiez l’emplacement du fichier où votre fournisseur OSC a été déployé et les emplacements du Registre Windows où les clés de Registre de votre fournisseur sont créées.
  
### <a name="file-location-for-osc-provider-dlls"></a>Emplacement du fichier pour les DLLs de fournisseur OSC

Testez les scénarios répertoriés dans le tableau suivant. Notez que le tableau répertorie les chemins d’installation par défaut pour les DLL du fournisseur OSC. Les utilisateurs peuvent personnaliser l’endroit où ils installent ces DLL.
  
|**Scénario**|**Comportement attendu**|
|:-----|:-----|
|Microsoft Outlook 2013 est installé sur l’ordinateur client. |Les DLL de fournisseur sont déployées dans le dossier Office15. Si le système d’exploitation est 64 bits et Microsoft Outlook 2013 est 32 bits, les DLL 32 bits sont déployées sous C:\Program Files (x86)\Microsoft Office\Office15. Si le système d’exploitation est 64 bits et Microsoft Outlook 2013 est 64 bits, les DLL 64 bits sont déployées sous C:\Program Files\Microsoft Office\Office15. Si le système d’exploitation est 32 bits, les DLL sont déployées sous C:\Program Files\Microsoft Office\Office15. |
|Outlook 2010 est installé sur l’ordinateur client. |Les DLL de fournisseur sont déployées dans le dossier Office14. Si le système d’exploitation est 64 bits et Outlook 2010 est 32 bits, les DLL 32 bits sont déployées sous C:\Program Files (x86)\Microsoft Office\Office14. Si le système d’exploitation est 64 bits et Outlook 2010 est 64 bits, les DLL 64 bits sont déployées sous C:\Program Files\Microsoft Office\Office14. Si le système d’exploitation est 32 bits, les DLL sont déployées sous C:\Program Files\Microsoft Office\Office14. |
|Outlook 2007 est installé sur l’ordinateur client. |Les DLL de fournisseur sont déployées sous C:\Program Files\Microsoft Office\Office14. L’installation d’OSC crée le dossier Office14 et l’OSC doit être installé avant les DLL de fournisseur. Consultez la section [Précédente Présence de Outlook et OSC sur l’ordinateur client](#olosc_TestingDeployment_PresenceOfOutlook). |
|Outlook 2003 est installé sur l’ordinateur client. |Les DLL de fournisseur sont déployées sous C:\Program Files\Microsoft Office\Office14. L’installation d’OSC crée le dossier Office14 et l’OSC doit être installé avant les DLL de fournisseur. Consultez la section [Précédente Présence de Outlook et OSC sur l’ordinateur client](#olosc_TestingDeployment_PresenceOfOutlook). |
|Microsoft Outlook 2013 n’est pas installé, mais remis par l’outil « Click-to-Run » sur l’ordinateur client. |Les DLL de fournisseur sont déployées dans le dossier Office15. Si le système d’exploitation est 64 bits, les DLL 32 bits sont déployées sous C:\Program Files (x86)\Microsoft Office\Office15 ou C:\Program Files\Microsoft Office\Office15. Si le système d’exploitation est 32 bits, les DLL sont déployées sous C:\Program Files\Microsoft Office\Office15. Si le dossier Office15 n’existe pas, l’installation crée le dossier. |
|Outlook 2010 n’est pas installé, mais est remis par « En un clic » sur l’ordinateur client. |Les DLL de fournisseur sont déployées dans le dossier Office14. Si le système d’exploitation est 64 bits, les DLL 32 bits sont déployées sous C:\Program Files (x86)\Microsoft Office\Office14 ou C:\Program Files\Microsoft Office\Office14. Si le système d’exploitation est 32 bits, les DLL sont déployées sous C:\Program Files\Microsoft Office\Office14. Si le dossier Office14 n’existe pas, l’installation crée le dossier. |

### <a name="windows-registry-locations"></a>Windows de Registre

Vérifiez les éléments suivants :
  
- Le programme d’installation du fournisseur OSC crée une valeur ProgID pour le fournisseur OSC dans le Windows registre, dans l’une `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders` ou l’autre ou `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`.

- L’exception est si l’ordinateur client a des Outlook 32 bits en cours d’exécution sur un système d Windows d’exploitation 64 bits. Dans ce cas, le ProgID est créé dans l’un ou `HKEY_CURRENT_USER\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders` l’autre .`HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`

- Les clés de Registre doivent être identiques et se trouveront au même emplacement si, à la place, les DLL sont enregistrées par regsvr32.exe.

<a name="olosc_TestingDeployment_PresenceOfOutlook"> </a>

## <a name="removing-the-installation"></a>Suppression de l’installation

Voici quelques tests pour vérifier que le processus de désinstallation fonctionne correctement pour votre fournisseur OSC.
  
|**Scénario**|**Comportement attendu**|
|:-----|:-----|
|L’utilisateur choisit de désinstaller le fournisseur. |Le fournisseur désinstalle les DLL et désinstalle le Registre. |
|L’utilisateur choisit d’annuler le processus de désinstallation du fournisseur. |Le fournisseur annule le processus de désinstallation et place l’utilisateur à l’état avant le début du processus de désinstallation. |

## <a name="see-also"></a>Voir aussi

- [Inscription d’un fournisseur](registering-a-provider.md)  
- [Liste de vérification de l’installation](installation-checklist.md)
- [Prise en main de la publication d'un fournisseur OSC](getting-ready-to-release-an-osc-provider.md)
