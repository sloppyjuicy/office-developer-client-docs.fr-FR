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
# <a name="indexsearchpusherprocess"></a><span data-ttu-id="d32e7-103">INDEX_SEARCH_PUSHER_PROCESS</span><span class="sxs-lookup"><span data-stu-id="d32e7-103">INDEX_SEARCH_PUSHER_PROCESS</span></span>

  
  
<span data-ttu-id="d32e7-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d32e7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d32e7-105">Spécifie le processus qui envoie une notification pour le Gestionnaire de protocole MAPI qu’un objet de cette banque est prêt pour l’indexation.</span><span class="sxs-lookup"><span data-stu-id="d32e7-105">Specifies the process that is sending a notification to the MAPI Protocol Handler that an object in that store is ready for indexing.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="d32e7-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="d32e7-106">Quick info</span></span>

```cpp
typedef struct _INDEX_SEARCH_PUSHER_PROCESS {  
    DWORD dwPID;  
} INDEX_SEARCH_PUSHER_PROCESS; 
```

## <a name="members"></a><span data-ttu-id="d32e7-107">Membres</span><span class="sxs-lookup"><span data-stu-id="d32e7-107">Members</span></span>

 <span data-ttu-id="d32e7-108">*dwPID*</span><span class="sxs-lookup"><span data-stu-id="d32e7-108">*dwPID*</span></span> 
  
>  <span data-ttu-id="d32e7-109">ID de processus pour le processus qui envoie une notification d’indexation à l’indexeur du Gestionnaire de protocole MAPI.</span><span class="sxs-lookup"><span data-stu-id="d32e7-109">Process ID for the process that is sending an indexing notification to the indexer of the MAPI Protocol Handler.</span></span> 
    

