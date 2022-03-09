---
title: MAPIOFFLINE_NOTIFY_TYPE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: a111d7b7-6e87-4958-8f9b-0f2adbeb8b63
ms.openlocfilehash: ca275445cf21abff53d72feb9e33f253a6c3a4ce
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63371456"
---
# <a name="mapioffline_notify_type"></a>MAPIOFFLINE_NOTIFY_TYPE

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
La MAPIOFFLINE_NOTIFY_TYPE d’une notification indique si un changement d’état de connexion va avoir lieu, est en cours ou est terminé. 
  
## <a name="quick-info"></a>Informations rapides

Voir **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**. 
  
```cpp
typedef enum { 
    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START = 1,  
    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE = 2,  
    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE = 3  
} MAPIOFFLINE_NOTIFY_TYPE;
```

## <a name="see-also"></a>Voir aussi



[À propos de l’API d’état hors connexion](about-the-offline-state-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)

