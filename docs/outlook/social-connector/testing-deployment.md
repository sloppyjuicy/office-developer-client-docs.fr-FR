---
title: Test de déploiement
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8b585200-33e7-4607-a603-0c7e52a6b09d
description: Cette rubrique décrit des scénarios dans lesquels vous devez tester concernant l’installation et de désinstallation d’un fournisseur Outlook Social Connector (OSC).
ms.openlocfilehash: 9c811683097a08b9f6e575d4ea2fee29cdd545d6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383933"
---
# <a name="testing-deployment"></a>Test de déploiement

Cette rubrique décrit des scénarios dans lesquels vous devez tester concernant l’installation et de désinstallation d’un fournisseur Outlook Social Connector (OSC).

<a name="olosc_TestingDeployment_PresenceOfOutlook"> </a>

## <a name="presence-of-outlook-and-the-osc-on-client-computer"></a>Présence d’Outlook et la OSC sur l’ordinateur client

Facteurs de l’impact de l’installation d’un fournisseur OSC inclut le nombre de bits du système d’exploitation, la présence et nombre de bits d’Outlook et la OSC est activé dans Outlook.
  
Un fournisseur OSC peut être écrits pour une version 32 bits ou 64 bits de l’OSC. Outlook 2010 et Outlook 2013 sont disponibles en versions 32 bits et 64 bits, et Office Outlook 2003 et Office Outlook 2007 sont disponibles dans les versions 32 bits uniquement. Sur un système d’exploitation de Windows 64 bits, vous pouvez installer Outlook 32 bits ou 64 bits. Sur un système d’exploitation 32 bits, vous pouvez installer uniquement 32 bits, mais pas Outlook 64 bits. Selon le nombre de bits de la version installée d’Outlook et le fournisseur OSC lui-même, l’utilisateur doit utiliser le programme d’installation approprié pour installer un fournisseur OSC du nombre de bits approprié. Par exemple, si Outlook 64 bits est installé et que le fournisseur OSC est un composant COM natif, un fournisseur OSC de 32 bits ne fonctionneront pas et l’utilisateur doit utiliser le programme d’installation approprié pour installer un fournisseur OSC de 64 bits.
  
Le code de déploiement de votre fournisseur OSC pouvez supposer que l’utilisateur dispose d’une version prise en charge d’Outlook sur l’ordinateur. Toutefois, si la version actuelle de OSC n’est pas sur l’ordinateur client, le code de votre déploiement peut télécharger et installer une version appropriée de l’OSC à l’aide d’URL g-lien spéciale sur https://g.live.com. Ces liens g-dépendent de la version et le nombre de bits d’Outlook et les paramètres régionaux de l’ordinateur client. Pour plus d’informations sur l’utilisation de g-liens pour installer ou mettre à jour l’OSC, consultez la rubrique [Installation checklist](installation-checklist.md).
  
Avant d’installer un fournisseur OSC, l’utilisateur Outlook doit vous assurer que le complément OSC est activé dans Outlook.
  
La méthode de déploiement d’un fournisseur OSC recommandée consiste à utiliser un package Windows Installer (.msi). Tester chacune des scénarios suivants pour vérifier les travaux de déploiement appropriée pour le fournisseur.
  
|**Scénario**|**Comportement attendu**|
|:-----|:-----|
|Outlook n’est pas présent - Outlook 2003 ou Outlook 2007 n’est pas installé et Outlook 2010 ou Microsoft Outlook 2013 n’est pas installé ni a été remis par Click-to-Run.  <br/> |Le déploiement échoue.  <br/> |
|Outlook 2003 ou Outlook 2007 n’est pas installé, mais Outlook 2010 ou Microsoft Outlook 2013 a été remis par Click-to-Run.  <br/> |Le fournisseur de 32 bits est déployé.  <br/> |
|Outlook 2003 ou Outlook 2007 est installé, mais le OSC n’est pas installé.  <br/> |La ligne de programme d’installation installe l’OSC et tous les correctifs. Une fois l’OSC a été installé avec succès, le programme d’installation déploie le fournisseur.  <br/> |
|Outlook 2003 ou Outlook 2007 est installé, et une version antérieure de l’OSC est installée.  <br/> |Le programme d’installation met à jour l’OSC, via un lien g à des correctifs et puis déploie le fournisseur.  <br/> |
|Outlook 2003 ou 2007 est installé et l’OSC est mis à jour.  <br/> |Le programme d’installation déploie le fournisseur 32 bits.  <br/> |
|Outlook 2010 ou Microsoft Outlook 2013 est installé, mais le OSC n’est pas installé.  <br/> |Le programme d’installation échoue avec un message d’erreur.  <br/> |
|Outlook 2010 ou Microsoft Outlook 2013 est installé et une version antérieure de l’OSC est installée.  <br/> |Le programme d’installation qui est approprié pour le nombre de bits du installé Outlook 2010 ou Microsoft Outlook 2013, met à jour l’OSC via le lien de g correctifs, puis déploie le fournisseur approprié.  <br/> |
|Outlook 2010 ou Microsoft Outlook 2013 est installé et l’OSC est mis à jour.  <br/> |Le programme d’installation approprié pour le nombre de bits de la version Outlook 2010 ou Microsoft Outlook 2013 (32 bits ou 64 bits) installée déploie le fournisseur approprié.  <br/> |

<a name="olosc_TestingDeployment_PresenceOfOutlook"> </a>

## <a name="installed-location-and-registry-keys"></a>Installé emplacement et clés de Registre

Vérifiez l’emplacement du fichier où votre fournisseur OSC a été déployé et les emplacements dans le Registre Windows dans lequel les clés de Registre pour votre fournisseur sont créés.
  
### <a name="file-location-for-osc-provider-dlls"></a>Emplacement du fichier de la DLL de fournisseur OSC

Pour les scénarios de test comme indiqué dans le tableau suivant. Notez que le tableau répertorie les chemins d’installation par défaut pour les DLL de fournisseur OSC. Les utilisateurs peuvent personnaliser où ils installent ces DLL.
  
|**Scénario**|**Comportement attendu**|
|:-----|:-----|
|Microsoft Outlook 2013 est installé sur l’ordinateur client.  <br/> |DLL de fournisseur sont déployés dans le dossier Office15. Si le système d’exploitation 64 bits et que Microsoft Outlook 2013 est 32 bits, les DLL 32 bits sont déployés sous C:\Program Files (x86) \Microsoft Office\Office15. Si le système d’exploitation 64 bits et que Microsoft Outlook 2013 est 64 bits, les dll 64 bits sont déployés sous C:\Program Files\Microsoft Office\Office15. Si le système d’exploitation est de 32 bits, les DLL sont déployées sous C:\Program Files\Microsoft Office\Office15.  <br/> |
|Outlook 2010 est installé sur l’ordinateur client.  <br/> |DLL de fournisseur sont déployés dans le dossier Office14. Si le système d’exploitation est de 64 bits et Outlook 2010 est de 32 bits, les DLL 32 bits sont déployés sous C:\Program Files (x86) \Microsoft Office\Office14. Si le système d’exploitation est de 64 bits et Outlook 2010 est de 64 bits, les dll 64 bits sont déployés sous C:\Program Files\Microsoft Office\Office14. Si le système d’exploitation est de 32 bits, les DLL sont déployées sous C:\Program Files\Microsoft Office\Office14.  <br/> |
|Outlook 2007 est installé sur l’ordinateur client.  <br/> |DLL de fournisseur sont déployées sous C:\Program Files\Microsoft Office\Office14. L’installation de l’OSC crée le dossier Office14 et l’OSC doit être installé avant tout fournisseur de DLL. Voir la section précédente [présence d’Outlook et la OSC sur l’ordinateur Client](#olosc_TestingDeployment_PresenceOfOutlook).  <br/> |
|Outlook 2003 est installé sur l’ordinateur client.  <br/> |DLL de fournisseur sont déployées sous C:\Program Files\Microsoft Office\Office14. L’installation de l’OSC crée le dossier Office14 et l’OSC doit être installé avant tout fournisseur de DLL. Voir la section précédente [présence d’Outlook et la OSC sur l’ordinateur Client](#olosc_TestingDeployment_PresenceOfOutlook).  <br/> |
|Microsoft Outlook 2013 n’est pas installé mais livré par Click-to-Run sur l’ordinateur client.  <br/> |DLL de fournisseur sont déployés dans le dossier Office15. Si le système d’exploitation 32 bits, 64 bits DLL sont déployées sous C:\Program Files (x86) \Microsoft Office\Office15 ou C:\Program Files\Microsoft Office\Office15. Si le système d’exploitation est de 32 bits, les DLL sont déployées sous C:\Program Files\Microsoft Office\Office15. Si le dossier Office15 n’existe pas, l’installation crée le dossier.  <br/> |
|Outlook 2010 n’est pas installé mais livré par Click-to-Run sur l’ordinateur client.  <br/> |DLL de fournisseur sont déployés dans le dossier Office14. Si le système d’exploitation 32 bits, 64 bits DLL sont déployées sous C:\Program Files (x86) \Microsoft Office\Office14 ou C:\Program Files\Microsoft Office\Office14. Si le système d’exploitation est de 32 bits, les DLL sont déployées sous C:\Program Files\Microsoft Office\Office14. Si le dossier Office14 n’existe pas, l’installation crée le dossier.  <br/> |
   
### <a name="windows-registry-locations"></a>Emplacements du Registre Windows

Vérifiez les points suivants :
  
- Le programme d’installation du fournisseur OSC crée une valeur ProgID pour le fournisseur OSC dans le Registre Windows, soit `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders` ou `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`. 
    
- L’exception est si l’ordinateur client est Outlook 32 bits sur un système d’exploitation de Windows 64 bits. Dans ce cas, le ProgID est créé dans une `HKEY_CURRENT_USER\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders` ou `HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`.
    
- Les clés de Registre doivent être identiques et au même emplacement si, au lieu de cela, les DLL sont enregistrées par regsvr32.exe.

<a name="olosc_TestingDeployment_PresenceOfOutlook"> </a>

## <a name="removing-the-installation"></a>Suppression de l’installation

Voici quelques tests pour vérifier que le processus de désinstallation fonctionne correctement pour votre fournisseur OSC.
  
|**Scénario**|**Comportement attendu**|
|:-----|:-----|
|Utilisateur choisit désinstaller le fournisseur.  <br/> |Le fournisseur désinstalle les DLL et efface le Registre.  <br/> |
|Utilisateur choisit d’annuler le processus de désinstallation du fournisseur.  <br/> |Le fournisseur annule le processus de désinstallation et ramène l’utilisateur à l’état avant de démarrer le processus de désinstallation.  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [Inscription d’un fournisseur](registering-a-provider.md)  
- [Aide-mémoire d’installation](installation-checklist.md)
- [Prise en main de la publication d'un fournisseur OSC](getting-ready-to-release-an-osc-provider.md)

