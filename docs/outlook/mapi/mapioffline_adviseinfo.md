---
title: MAPIOFFLINE_ADVISEINFO
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 20a46c69-d6ae-7d17-f8af-12952867d342
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 3cb110fdcbbd88e494c44ba2ed73cc26674638ca
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270034"
---
# <a name="mapiofflineadviseinfo"></a>MAPIOFFLINE_ADVISEINFO
 
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Fournit des informations à **[IMAPIOfflineMgr:: Advise](imapiofflinemgr-advise.md)** pour inscrire le rappel pour un objet hors connexion. 
  
## <a name="quick-info"></a>Informations rapides

Voir **IMAPIOfflineMgr:: Advise**. 
  
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

_ulSize_: taille de **MAPIOFFLINE_ADVISEINFO**. 
    
_ulClientToken_: jeton défini par le client à propos d'un rappel. Il s'agit du membre *ulClientToken* de la structure **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)** transmis à **[IMAPIOfflineNotify:: Notify](imapiofflinenotify-notify.md)**. 
    
_CallbackType_: type de rappel à effectuer.
    
   -  MAPIOFFLINE_CALLBACK_TYPE_NOTIFY 
    
   - Le type de rappel est par notification. Il s'agit du seul type de rappel pris en charge.  *pCallback* doit indiquer l'interface **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**. 
    
_pCallback_: interface à utiliser pour le rappel. Il s'agit de l'implémentation du client de **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**. 
    
_ulAdviseTypes_: type de notification, tel qu'identifié par la condition pour conseiller. Le seul type pris en charge est MAPIOFFLINE_ADVISE_TYPE_STATECHANGE.
    
_ulStateMask_: le seul État pris en charge est MAPIOFFLINE_STATE_ALL.
    
## <a name="see-also"></a>Voir aussi

- [IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)
- [À propos de l’API d’état hors connexion](about-the-offline-state-api.md) 
- [Constantes MAPI](mapi-constants.md) 
- [MAPIOFFLINE_CALLBACK_TYPE](mapioffline_callback_type.md)

