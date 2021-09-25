---
title: À propos de l’API d’état hors connexion
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 18b0d284-c224-a022-47d9-b2d82a32f996
description: 'Derni�re modification�: lundi 25 juin 2012'
ms.openlocfilehash: 520ee2b76c851cfdb112f7be72fcb48ea9f38c01
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614324"
---
# <a name="about-the-offline-state-api"></a>À propos de l’API d’état hors connexion

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
L’API d’état hors connexion prend en charge les rappels indiquant les modifications apportées à l’état de connexion d’un utilisateur dans Microsoft Outlook 2013 et Microsoft Outlook 2010, par exemple, d’être en ligne dans Outlook 2013 ou Outlook 2010 jusqu’à être hors connexion. L’API utilise un objet hors connexion global dans Outlook 2013 ou Outlook 2010 pour suivre ces modifications pour un profil de compte d’utilisateur donné. La notification est la seule forme de rappel prise en charge. En tant que clients de cette API, les fournisseurs de messagerie qui souhaitent être avertis de ces changements d’état de connexion sont les suivants :
  
1. **[Implémenter IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**. 
    
2. Ouvrez un objet hors connexion existant pour un profil spécifique à l’aide **[de HrOpenOfflineObj](hropenofflineobj.md)**. 
    
3. Déterminez si l’objet a la possibilité de fournir des notifications en ligne ou hors connexion à l’aide **[d’IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)**. 
    
4. Inscrivez l’objet pour les notifications en ligne ou hors connexion à l’aide **[d’IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**. Les fournisseurs de messagerie peuvent désormais recevoir des notifications Outlook 2013 ou 2010 Outlook 2010 à l’aide **d’IMAPIOfflineNotify**. 
    
5. Lors de l’arrêt, supprimez l’inscription pour les notifications en ligne et hors connexion à l’aide **[d’IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md)**. 
    
> [!NOTE]
> En règle générale, Outlook 2013 et Outlook 2010 peuvent notifier un client de modifications en ligne/hors connexion ainsi que d’autres modifications, mais l’API d’état hors connexion prend en charge uniquement les notifications pour les modifications en ligne/hors connexion. Le client doit ignorer toutes les autres notifications. Pour plus d’informations, **[voir IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)** et **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**. 
  
 Pour obtenir un exemple de client qui utilise l’API d’état hors connexion, voir à propos de l’exemple [de add-in d’état hors connexion.](about-the-sample-offline-state-add-in.md) L’exemple de compl?ment d’état hors ligne est un compl?ment COM qui utilise l’API d’état hors connexion pour surveiller et modifier l’état de connexion.
  
Cette API fournit les informations suivantes :
  
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
    

