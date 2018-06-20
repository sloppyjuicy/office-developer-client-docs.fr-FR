---
title: INDEX_SEARCH_PUSHER_PROCESS
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6b39504f-6eed-2605-048d-2707f38a7d9a
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: ada6d4127d503aae0b068d40d2bb48cb6b833ea0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784305"
---
# <a name="indexsearchpusherprocess"></a>INDEX_SEARCH_PUSHER_PROCESS

  
  
**S’applique à**: Outlook 
  
Spécifie le processus qui envoie une notification pour le Gestionnaire de protocole MAPI qu’un objet de cette banque est prêt pour l’indexation.
  
## <a name="quick-info"></a>Informations rapides

```cpp
typedef struct _INDEX_SEARCH_PUSHER_PROCESS {  
    DWORD dwPID;  
} INDEX_SEARCH_PUSHER_PROCESS; 
```

## <a name="members"></a>Membres

 *dwPID* 
  
>  ID de processus pour le processus qui envoie une notification d’indexation à l’indexeur du Gestionnaire de protocole MAPI. 
    

