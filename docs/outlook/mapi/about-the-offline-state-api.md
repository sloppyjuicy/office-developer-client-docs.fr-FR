---
title: À propos de l’API d’état hors connexion
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 18b0d284-c224-a022-47d9-b2d82a32f996
description: 'Derni�re modification�: lundi 25 juin 2012'
ms.openlocfilehash: 56793ae0d2c2ce76c89c7cda4985618e3a40ccfd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410482"
---
# <a name="about-the-offline-state-api"></a>À propos de l’API d’état hors connexion

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
L'API d'État hors connexion prend en charge les rappels indiquant les modifications apportées à l'état de connexion d'un utilisateur dans Microsoft Outlook 2013 et Microsoft Outlook 2010, par exemple en étant en ligne dans Outlook 2013 ou Outlook 2010 en mode hors connexion. L'API utilise un objet hors connexion global dans Outlook 2013 ou Outlook 2010 pour suivre les modifications apportées à un profil de compte d'utilisateur donné. La notification est la seule forme de rappel prise en charge. En tant que clients de cette API, les fournisseurs de messagerie qui souhaitent être avertis de ces changements d'état de connexion effectuent les opérations suivantes:
  
1. Implémenter **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**. 
    
2. Ouvrez un objet hors connexion existant pour un profil spécifique à l'aide de **[HrOpenOfflineObj](hropenofflineobj.md)**. 
    
3. Déterminez si l'objet peut fournir des notifications en ligne ou hors ligne à l'aide de **[IMAPIOffline:: GetCapabilities](imapioffline-getcapabilities.md)**. 
    
4. Inscrivez l'objet pour les notifications en ligne ou hors connexion à l'aide de **[IMAPIOfflineMgr:: Advise](imapiofflinemgr-advise.md)**. Les fournisseurs de messagerie peuvent désormais recevoir des notifications qu'Outlook 2013 ou Outlook 2010 envoient à l'aide de **IMAPIOfflineNotify**. 
    
5. Lors de l'arrêt, supprimez l'inscription pour les notifications en ligne et hors connexion à l'aide de **[IMAPIOfflineMgr::](imapiofflinemgr-unadvise.md)** Unadvise. 
    
> [!NOTE]
> En règle générale, Outlook 2013 et Outlook 2010 peuvent informer un client des modifications en ligne/hors connexion, ainsi que d'autres modifications, mais l'API d'État hors connexion prend en charge uniquement les notifications pour les modifications en ligne et hors connexion. Le client doit ignorer toutes les autres notifications. Pour plus d'informations, voir **[IMAPIOfflineNotify:: Notify](imapiofflinenotify-notify.md)** et **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**. 
  
 Pour obtenir un exemple de client qui utilise l'API d'État hors connexion, voir [à propos de l'exemple de complément d'État hors connexion](about-the-sample-offline-state-add-in.md). L'exemple de complément d'État hors connexion est un complément COM qui utilise l'API d'État hors connexion pour surveiller et modifier l'état de connexion.
  
Cette API fournit les éléments suivants:
  
Définitions :
  
- [Constantes MAPI](mapi-constants.md)
    
Types de données:
  
- **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)**
    
- **[MAPIOFFLINE_CALLBACK_TYPE](mapioffline_callback_type.md)**
    
- **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**
    
Fonctions :
  
- **[HrOpenOfflineObj](hropenofflineobj.md)**
    
Interfaces :
  
- **[IMAPIOffline](imapiofflineiunknown.md)**
    
- **[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**
    
- **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**
    

