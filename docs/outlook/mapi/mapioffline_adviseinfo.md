---
title: MAPIOFFLINE_ADVISEINFO
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 20a46c69-d6ae-7d17-f8af-12952867d342
ms.openlocfilehash: ee185026e4502c8ddcf36395f9650417783dc25e
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63378505"
---
# <a name="mapioffline_adviseinfo"></a>MAPIOFFLINE_ADVISEINFO

**S’applique à** : Outlook 2013 | Outlook 2016
  
Fournit des informations **[à IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)** to register callback for an offline object.
  
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

_ulSize :_ taille des **MAPIOFFLINE_ADVISEINFO**.

_ulClientToken_ : jeton défini par le client à propos d’un rappel. Il s’agit _du membre ulClientToken_ de la structure **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)** transmise à **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)**.

_CallbackType_ : type de rappel à effectuer.

- MAPIOFFLINE_CALLBACK_TYPE_NOTIFY

- Le type de rappel est par notification. Il s’agit du seul type de rappel pris en charge. _pCallback doit_  indiquer l’interface **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.

_pCallback :_ interface à utiliser pour le rappel. Il s’agit de l’implémentation du client **[d’IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.

_ulAdviseTypes_ : types de conseils, tels qu’identifiés par la condition de conseil. Le seul type pris en charge est MAPIOFFLINE_ADVISE_TYPE_STATECHANGE.

_ulStateMask_ : le seul état pris en charge est MAPIOFFLINE_STATE_ALL.

## <a name="see-also"></a>Voir aussi

- [IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)
- [À propos de l’API d’état hors connexion](about-the-offline-state-api.md)
- [Constantes MAPI](mapi-constants.md)
- [MAPIOFFLINE_CALLBACK_TYPE](mapioffline_callback_type.md)
