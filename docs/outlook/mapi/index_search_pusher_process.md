---
title: INDEX_SEARCH_PUSHER_PROCESS
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6b39504f-6eed-2605-048d-2707f38a7d9a
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 64e5cf31dffdc794a22bcbd6d503a2b688f9c733
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423348"
---
# <a name="indexsearchpusherprocess"></a>INDEX_SEARCH_PUSHER_PROCESS

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie le processus qui envoie une notification au gestionnaire de protocole MAPI indiquant qu'un objet de ce magasin est prêt pour l'indexation.
  
## <a name="quick-info"></a>Informations rapides

```cpp
typedef struct _INDEX_SEARCH_PUSHER_PROCESS {  
    DWORD dwPID;  
} INDEX_SEARCH_PUSHER_PROCESS; 
```

## <a name="members"></a>Membres

 *dwPID* 
  
>  ID de processus pour le processus qui envoie une notification d'indexation à l'indexeur du gestionnaire de protocole MAPI. 
    

