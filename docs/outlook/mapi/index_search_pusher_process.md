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
ms.openlocfilehash: 9495caecd514656f6fd62fb5db6cd8ac2faf4b50
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581740"
---
# <a name="indexsearchpusherprocess"></a>INDEX_SEARCH_PUSHER_PROCESS

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Spécifie le processus qui envoie une notification pour le Gestionnaire de protocole MAPI qu’un objet de cette banque est prêt pour l’indexation.
  
## <a name="quick-info"></a>Informations rapides

```cpp
typedef struct _INDEX_SEARCH_PUSHER_PROCESS {  
    DWORD dwPID;  
} INDEX_SEARCH_PUSHER_PROCESS; 
```

## <a name="members"></a>Members

 *dwPID* 
  
>  ID de processus pour le processus qui envoie une notification d’indexation à l’indexeur du Gestionnaire de protocole MAPI. 
    

