---
title: INDEX_SEARCH_PUSHER_PROCESS
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 6b39504f-6eed-2605-048d-2707f38a7d9a
ms.openlocfilehash: 4aca18b7cf648dbeaf12663006fc5f6cbbc936b1
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63371498"
---
# <a name="index_search_pusher_process"></a>INDEX_SEARCH_PUSHER_PROCESS

**S’applique à** : Outlook 2013 | Outlook 2016
  
Spécifie le processus qui envoie une notification au responsable du protocole MAPI qu’un objet de ce magasin est prêt pour l’indexation.
  
## <a name="quick-info"></a>Informations rapides

```cpp
typedef struct _INDEX_SEARCH_PUSHER_PROCESS {  
    DWORD dwPID;  
} INDEX_SEARCH_PUSHER_PROCESS; 
```

## <a name="members"></a>Membres

 *dwPID*
  
> ID de processus pour le processus qui envoie une notification d’indexation à l’indexeur du handler de protocole MAPI.
