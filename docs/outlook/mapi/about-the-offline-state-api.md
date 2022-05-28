---
title: À propos de l’API d’état hors connexion
description: Décrit l’API d’état hors connexion, qui prend en charge les rappels indiquant les modifications apportées à l’état de connexion d’un utilisateur dans Microsoft Outlook 2013 et 2010.
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 18b0d284-c224-a022-47d9-b2d82a32f996
ms.openlocfilehash: e3d502af3086e6d6f8cc2e09d667326fb06aa0b6
ms.sourcegitcommit: 8c8e4ac05a6612dd5c815ab18ba40e56a6ba839d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2022
ms.locfileid: "65769822"
---
# <a name="about-the-offline-state-api"></a>À propos de l’API d’état hors connexion

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
L’API d’état hors connexion prend en charge les rappels indiquant les modifications apportées à l’état de connexion d’un utilisateur dans Microsoft Outlook 2013 et Microsoft Outlook 2010, par exemple, d’être en ligne dans Outlook 2013 ou Outlook 2010 à être hors connexion. L’API utilise un objet hors connexion global dans Outlook 2013 ou Outlook 2010 pour suivre ces modifications pour un profil de compte d’utilisateur donné. La notification est la seule forme de rappel prise en charge. En tant que clients de cette API, les fournisseurs de messagerie qui souhaitent être avertis de ces changements d’état de connexion effectuent les opérations suivantes :
  
1. Implémentez **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**. 
    
2. Ouvrez un objet hors connexion existant pour un profil spécifique à l’aide de **[HrOpenOfflineObj](hropenofflineobj.md)**. 
    
3. Déterminez si l’objet peut fournir des notifications en ligne ou hors connexion à l’aide **[d’IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)**. 
    
4. Inscrivez l’objet pour les notifications en ligne ou hors connexion à l’aide **[d’IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**. Les fournisseurs de messagerie peuvent désormais recevoir des notifications que Outlook 2013 ou Outlook 2010 envoient à l’aide **d’IMAPIOfflineNotify**. 
    
5. À l’arrêt, supprimez l’inscription pour les notifications en ligne et hors connexion à l’aide **[d’IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md)**. 
    
> [!NOTE]
> En général, Outlook 2013 et Outlook 2010 peuvent informer un client des modifications en ligne/hors connexion, ainsi que d’autres modifications, mais l’API d’état hors connexion prend uniquement en charge les notifications pour les modifications en ligne/hors connexion. Le client doit ignorer toutes les autres notifications. Pour plus d’informations, consultez **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)** et **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**. 
  
 Pour obtenir un exemple de client qui utilise l’API d’état hors connexion, consultez [À propos de l’exemple de complément d’état hors connexion](about-the-sample-offline-state-add-in.md). L’exemple de complément d’état hors connexion est un complément COM qui utilise l’API d’état hors connexion pour surveiller et modifier l’état de connexion.
  
Cette API fournit les éléments suivants :
  
Définitions :
  
- [Constantes MAPI](mapi-constants.md)
    
Types de données :
  
- **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)**
    
- **[MAPIOFFLINE_CALLBACK_TYPE](mapioffline_callback_type.md)**
    
- **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**
    
Fonctions :
  
- **[HrOpenOfflineObj](hropenofflineobj.md)**
    
Interfaces :
  
- **[IMAPIOffline](imapiofflineiunknown.md)**
    
- **[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**
    
- **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**
    

