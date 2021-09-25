---
title: MAPIOFFLINE_NOTIFY_TYPE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: a111d7b7-6e87-4958-8f9b-0f2adbeb8b63
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: d97c88ee27fbe0b68c7495657c77fa2ca4734e81
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59604760"
---
# <a name="mapioffline_notify_type"></a>MAPIOFFLINE_NOTIFY_TYPE

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
La MAPIOFFLINE_NOTIFY_TYPE d’une notification identifie si un changement d’état de connexion va avoir lieu, est en cours ou est terminé. 
  
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

