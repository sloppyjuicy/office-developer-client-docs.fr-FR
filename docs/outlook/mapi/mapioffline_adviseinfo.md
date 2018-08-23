---
title: MAPIOFFLINE_ADVISEINFO
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 20a46c69-d6ae-7d17-f8af-12952867d342
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 82869fa479ebe8a4d7b1881cec5d5c243b7d7957
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565094"
---
# <a name="mapiofflineadviseinfo"></a>MAPIOFFLINE_ADVISEINFO
 
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Fournit des informations à **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)** pour enregistrer le rappel pour un objet en mode hors connexion. 
  
## <a name="quick-info"></a>Informations rapides

Voir **IMAPIOfflineMgr::Advise**. 
  
```cpp
typedef struct 
{ 
      ULONG                   ulSize; 
      ULONG                   ulClientToken; 
      MAPIOFFLINE_CALLBACK_TYPE     CallbackType; 
      IUnknown*               pCallback; 
      ULONG                   ulAdviseTypes; 
      ULONG                   ulStateMask; 
} MAPIOFFLINE_ADVISEINFO;
```

## <a name="members"></a>Members

_ulSize_: la taille de **MAPIOFFLINE_ADVISEINFO**. 
    
_ulClientToken_: un jeton défini par le client sur un rappel. Il est membre de la structure **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)** transmis à **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)** *ulClientToken* . 
    
_CallbackType_: Type de rappel à effectuer.
    
   -  MAPIOFFLINE_CALLBACK_TYPE_NOTIFY 
    
   - Le type de rappel est par notification. Il s’agit du seul type pris en charge de rappel.  *pCallback* doit indiquer l’interface **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**. 
    
_pCallback_: Interface à utiliser pour le rappel. Il s’agit d’implémentation du client de **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**. 
    
_ulAdviseTypes_: les types de notifications, tels qu’identifiés par la condition pour conseiller. Le seul type pris en charge est MAPIOFFLINE_ADVISE_TYPE_STATECHANGE.
    
_ulStateMask_: le seul état pris en charge est MAPIOFFLINE_STATE_ALL.
    
## <a name="see-also"></a>Voir aussi

- [IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)
- [À propos de l’API d’état hors connexion](about-the-offline-state-api.md) 
- [Constantes MAPI](mapi-constants.md) 
- [MAPIOFFLINE_CALLBACK_TYPE](mapioffline_callback_type.md)

