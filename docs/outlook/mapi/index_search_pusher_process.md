---
title: INDEX_SEARCH_PUSHER_PROCESS
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 6b39504f-6eed-2605-048d-2707f38a7d9a
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 34c7f5f2a17ce4b1fb4ed18bf7c3ab89a18cb658
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556356"
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
  
>  ID de processus pour le processus qui envoie une notification d’indexation à l’indexeur du handler de protocole MAPI. 
    

