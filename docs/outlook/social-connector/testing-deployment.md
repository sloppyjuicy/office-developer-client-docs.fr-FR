---
title: Test de déploiement
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8b585200-33e7-4607-a603-0c7e52a6b09d
description: Cette rubrique décrit certains scénarios que vous devez tester concernant l'installation et la désinstallation d'un fournisseur Outlook Social Connector (OSC).
ms.openlocfilehash: 9c811683097a08b9f6e575d4ea2fee29cdd545d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329161"
---
# <a name="testing-deployment"></a>Test de déploiement

Cette rubrique décrit certains scénarios que vous devez tester concernant l'installation et la désinstallation d'un fournisseur Outlook Social Connector (OSC).

<a name="olosc_TestingDeployment_PresenceOfOutlook"> </a>

## <a name="presence-of-outlook-and-the-osc-on-client-computer"></a>Présence d'Outlook et de l'utilisateur OSC sur un ordinateur client

Facteurs l'installation d'un fournisseur OSC inclut le nombre de bits du système d'exploitation, la présence et le nombre de bits d'Outlook, et le OSC activé dans Outlook.
  
Un fournisseur OSC peut être écrit pour une version 32 bits ou 64 bits du OSC. Outlook 2010 et Outlook 2013 sont disponibles dans les versions 32 bits et 64 bits, et Office Outlook 2003 et Office Outlook 2007 sont disponibles uniquement dans les versions 32 bits. Sur un système d'exploitation Windows 64 bits, vous pouvez installer Outlook bits ou 64 bits. Sur un système d'exploitation 32 bits, vous pouvez installer uniquement 32 bits, mais pas 64 bits, Outlook. En fonction du nombre de bits de la version installée d'Outlook et du fournisseur OSC lui-même, l'utilisateur doit utiliser le programme d'installation approprié pour installer un fournisseur OSC du nombre de bits approprié. Par exemple, si Outlook 64 bits est installé et que le fournisseur OSC est un composant COM natif, un fournisseur OSC 32 bits ne fonctionnera pas et l'utilisateur doit utiliser le programme d'installation approprié pour installer un fournisseur OSC 64 bits.
  
Le code de déploiement de votre fournisseur OSC peut supposer que l'utilisateur dispose d'une version prise en charge d'Outlook sur l'ordinateur. Toutefois, si la version actuelle de OSC ne se trouve pas sur l'ordinateur client, votre code de déploiement peut télécharger et installer une version appropriée du OSC à l'aide d'URL g- https://g.live.comLink spécialement construites sur. Ces liens g-Link dépendent de la version et du nombre de bits d'Outlook et des paramètres régionaux de l'ordinateur client. Pour plus d'informations sur l'utilisation de g-Links pour installer ou mettre à jour le OSC, consultez la rubrique [Installation Checklist](installation-checklist.md).
  
Avant d'installer un fournisseur OSC, l'utilisateur Outlook doit s'assurer que le complément OSC est activé dans Outlook.
  
La méthode recommandée pour le déploiement d'un fournisseur OSC consiste à utiliser un package Windows Installer (. msi). Testez chacun des scénarios suivants pour vérifier que le déploiement fonctionne correctement pour le fournisseur.
  
|**Scénario**|**Comportement attendu**|
|:-----|:-----|
|Outlook n'est pas présent-Outlook 2003 ou Outlook 2007 n'est pas installé, et Outlook 2010 ou Microsoft Outlook 2013 n'est pas installé et n'a pas été remis par «démarrer en un clic».  <br/> |Le déploiement échoue.  <br/> |
|Outlook 2003 ou Outlook 2007 n'est pas installé, mais Outlook 2010 ou Microsoft Outlook 2013 a été fourni par «démarrer en un clic».  <br/> |Le fournisseur 32 bits est déployé.  <br/> |
|Outlook 2003 ou Outlook 2007 est installé, mais le OSC n'est pas installé.  <br/> |Le programme d'installation installe OSC et tous les correctifs. Une fois que OSC a été installé correctement, le programme d'installation déploie le fournisseur.  <br/> |
|Outlook 2003 ou Outlook 2007 est installé, et une version antérieure du OSC est installée.  <br/> |Le programme d'installation met à jour le OSC, via un lien g-Link vers les correctifs, puis déploie le fournisseur.  <br/> |
|Outlook 2003 ou 2007 est installé et le OSC est à jour.  <br/> |Le programme d'installation déploie le fournisseur 32 bits.  <br/> |
|Outlook 2010 ou Microsoft Outlook 2013 est installé, mais le OSC n'est pas installé.  <br/> |Le programme d'installation échoue avec un message d'erreur approprié.  <br/> |
|Outlook 2010 ou Microsoft Outlook 2013 est installé et une version plus ancienne du OSC est installée.  <br/> |Le programme d'installation qui est approprié pour le nombre de bits de l'installation d'Outlook 2010 ou de Microsoft Outlook 2013, met à jour le OSC via le lien g-Link vers les correctifs, puis déploie le fournisseur approprié.  <br/> |
|Outlook 2010 ou Microsoft Outlook 2013 est installé et le OSC est à jour.  <br/> |Le programme d'installation approprié pour le nombre de bits de l'installation d'Outlook 2010 ou de Microsoft Outlook 2013 (32 bits ou 64 bits) déploie le fournisseur approprié.  <br/> |

<a name="olosc_TestingDeployment_PresenceOfOutlook"> </a>

## <a name="installed-location-and-registry-keys"></a>Emplacement d'installation et clés de Registre

Vérifiez l'emplacement du fichier dans lequel votre fournisseur OSC a été déployé, ainsi que les emplacements dans le Registre Windows où les clés de Registre pour votre fournisseur sont créées.
  
### <a name="file-location-for-osc-provider-dlls"></a>Emplacement de fichier pour les dll du fournisseur OSC

Testez les scénarios comme décrit dans le tableau suivant. Notez que le tableau répertorie les chemins d'installation par défaut pour les dll du fournisseur OSC. Les utilisateurs peuvent personnaliser l'emplacement où ils installent ces dll.
  
|**Scénario**|**Comportement attendu**|
|:-----|:-----|
|Microsoft Outlook 2013 est installé sur l'ordinateur client.  <br/> |Les dll de fournisseur sont déployées dans le dossier Office15 Si le système d'exploitation est 64 bits et que Microsoft Outlook 2013 est 32 bits, les dll 32 bits sont déployées sous C:\Program Files (x86) \Microsoft Office\Office15. Si le système d'exploitation est 64 bits et que Microsoft Outlook 2013 est 64 bits, les dll 64 bits sont déployées sous C:\Program Files\Microsoft Office\Office15. Si le système d'exploitation est 32 bits, les dll sont déployées sous C:\Program Files\Microsoft Office\Office15.  <br/> |
|Outlook 2010 est installé sur l'ordinateur client.  <br/> |Les dll de fournisseur sont déployées dans le dossier Office14 Si le système d'exploitation est 64 bits et qu'Outlook 2010 est 32 bits, les dll 32 bits sont déployées sous C:\Program Files (x86) \Microsoft Office\Office14. Si le système d'exploitation est 64 bits et qu'Outlook 2010 est 64 bits, les dll 64 bits sont déployées sous C:\Program Files\Microsoft Office\Office14. Si le système d'exploitation est 32 bits, les dll sont déployées sous C:\Program Files\Microsoft Office\Office14.  <br/> |
|Outlook 2007 est installé sur l'ordinateur client.  <br/> |Les dll de fournisseur sont déployées sous C:\Program Files\Microsoft Office\Office14. L'installation de l'OSC crée le dossier Office14 et le OSC doit être installé avant toute DLL de fournisseur. Consultez la section précédente [sur la présence d'Outlook et de l'utilisateur OSC sur l'ordinateur client](#olosc_TestingDeployment_PresenceOfOutlook).  <br/> |
|Outlook 2003 est installé sur l'ordinateur client.  <br/> |Les dll de fournisseur sont déployées sous C:\Program Files\Microsoft Office\Office14. L'installation de l'OSC crée le dossier Office14 et le OSC doit être installé avant toute DLL de fournisseur. Consultez la section précédente [sur la présence d'Outlook et de l'utilisateur OSC sur l'ordinateur client](#olosc_TestingDeployment_PresenceOfOutlook).  <br/> |
|Microsoft Outlook 2013 n'est pas installé mais fourni par «démarrer en un clic» sur l'ordinateur client.  <br/> |Les dll de fournisseur sont déployées dans le dossier Office15 Si le système d'exploitation est 64 bits, les dll 32 bits sont déployées sous C:\Program Files (x86) \Microsoft Office\Office15 ou C:\Program Files\Microsoft Office\Office15. Si le système d'exploitation est 32 bits, les dll sont déployées sous C:\Program Files\Microsoft Office\Office15. Si le dossier Office15 n'existe pas, l'installation crée le dossier.  <br/> |
|Outlook 2010 n'est pas installé mais il est fourni par «démarrer en un clic» sur l'ordinateur client.  <br/> |Les dll de fournisseur sont déployées dans le dossier Office14 Si le système d'exploitation est 64 bits, les dll 32 bits sont déployées sous C:\Program Files (x86) \Microsoft Office\Office14 ou C:\Program Files\Microsoft Office\Office14. Si le système d'exploitation est 32 bits, les dll sont déployées sous C:\Program Files\Microsoft Office\Office14. Si le dossier Office14 n'existe pas, l'installation crée le dossier.  <br/> |
   
### <a name="windows-registry-locations"></a>Emplacements du Registre Windows

Vérifiez les éléments suivants :
  
- Le programme d'installation du fournisseur OSC crée une valeur ProgID pour le fournisseur OSC dans le Registre Windows `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders` , `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`soit dans ou. 
    
- L'exception est si l'ordinateur client dispose d'Outlook 32 bits s'exécutant sur un système d'exploitation Windows 64 bits. Dans ce cas, le ProgID est créé dans `HKEY_CURRENT_USER\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders` ou. `HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
- Les clés de Registre doivent être identiques et au même emplacement si, au lieu de cela, les dll sont inscrites par regsvr32. exe.

<a name="olosc_TestingDeployment_PresenceOfOutlook"> </a>

## <a name="removing-the-installation"></a>Suppression de l'installation

Voici quelques tests permettant de vérifier que le processus de désinstallation fonctionne correctement pour votre fournisseur OSC.
  
|**Scénario**|**Comportement attendu**|
|:-----|:-----|
|L'utilisateur choisit de désinstaller le fournisseur.  <br/> |Le fournisseur désinstalle les dll et efface le registre.  <br/> |
|L'utilisateur choisit d'annuler le processus de désinstallation du fournisseur.  <br/> |Le fournisseur annule le processus de désinstallation et remet l'utilisateur à l'état avant le démarrage du processus de désinstallation.  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [Inscription d'un fournisseur](registering-a-provider.md)  
- [Liste de vérification de l'installation](installation-checklist.md)
- [Prise en main de la publication d'un fournisseur OSC](getting-ready-to-release-an-osc-provider.md)

