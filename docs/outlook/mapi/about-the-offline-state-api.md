---
title: À propos de l’API d’état hors connexion
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 18b0d284-c224-a022-47d9-b2d82a32f996
description: 'Dernière modification : 25 juin 2012'
ms.openlocfilehash: aa30a173251193d74d6560c8dce2663463a18e36
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565983"
---
# <a name="about-the-offline-state-api"></a>À propos de l’API d’état hors connexion

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
L’API d’état en mode hors connexion prend en charge les rappels indiquant les modifications de l’état de connexion d’un utilisateur dans Microsoft Outlook 2013 et Microsoft Outlook 2010 — par exemple, d’en cours en ligne dans Outlook 2013 ou Outlook 2010 pour en cours en mode hors connexion. L’API utilise un objet global en mode hors connexion dans Outlook 2013 ou Outlook 2010 pour le suivi des modifications pour un profil de compte d’utilisateur donné. Notification est la seule forme prises en charge de rappel. Comme des clients de cette API, les fournisseurs de messagerie qui vous souhaitez être averti de ces changements d’état de connexion procédez comme suit :
  
1. Mettre en œuvre **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**. 
    
2. Ouvrez un objet existant en mode hors connexion pour un profil spécifique à l’aide de **[HrOpenOfflineObj](hropenofflineobj.md)**. 
    
3. Déterminer si l’objet est en mesure de fournir des notifications en ligne ou hors connexion à l’aide de **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)**. 
    
4. Enregistrer l’objet pour les notifications en ligne ou hors connexion à l’aide de **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**. Désormais, les fournisseurs de messagerie peuvent recevoir des notifications que Outlook 2013 ou Outlook 2010 envoyer à l’aide de **IMAPIOfflineNotify**. 
    
5. Lors de l’arrêt, supprimez l’enregistrement pour les notifications en ligne et hors connexion à l’aide de **[IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md)**. 
    
> [!NOTE]
> En règle générale, Outlook 2013 et Outlook 2010 peuvent informer un client de modifications en ligne/hors ligne ainsi que d’autres modifications, mais l’API d’état en mode hors connexion prend en charge uniquement les notifications pour les modifications en ligne/hors connexion. Le client doit ignorer toutes les autres notifications. Pour plus d’informations, voir **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)** et **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**. 
  
 Pour obtenir un exemple d’un client qui utilise l’API de l’état en mode hors connexion, consultez la rubrique [sur l’exemple en mode hors connexion état Add-in](about-the-sample-offline-state-add-in.md). Le complément exemple hors connexion état est un complément COM qui utilise l’API de l’état en mode hors connexion pour surveiller et modifier l’état de connexion.
  
Cette API fournit les fonctionnalités suivantes :
  
Définitions :
  
- [Constantes MAPI](mapi-constants.md)
    
Types de données :
  
- **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)**
    
- **[MAPIOFFLINE_CALLBACK_TYPE](mapioffline_callback_type.md)**
    
- **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**
    
Fonctions :
  
- **[HrOpenOfflineObj](hropenofflineobj.md)**
    
Interfaces :
  
- **[IMAPIOffline](imapiofflineiunknown.md)**
    
- **[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**
    
- **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**
    

