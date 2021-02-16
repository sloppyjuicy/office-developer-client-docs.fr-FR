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
# <a name="index_search_pusher_process"></a><span data-ttu-id="322a0-103">INDEX_SEARCH_PUSHER_PROCESS</span><span class="sxs-lookup"><span data-stu-id="322a0-103">INDEX_SEARCH_PUSHER_PROCESS</span></span>

  
  
<span data-ttu-id="322a0-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="322a0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="322a0-105">Spécifie le processus qui envoie une notification au responsable du protocole MAPI qu’un objet de ce magasin est prêt pour l’indexation.</span><span class="sxs-lookup"><span data-stu-id="322a0-105">Specifies the process that is sending a notification to the MAPI Protocol Handler that an object in that store is ready for indexing.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="322a0-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="322a0-106">Quick info</span></span>

```cpp
typedef struct _INDEX_SEARCH_PUSHER_PROCESS {  
    DWORD dwPID;  
} INDEX_SEARCH_PUSHER_PROCESS; 
```

## <a name="members"></a><span data-ttu-id="322a0-107">Membres</span><span class="sxs-lookup"><span data-stu-id="322a0-107">Members</span></span>

 <span data-ttu-id="322a0-108">*dwPID*</span><span class="sxs-lookup"><span data-stu-id="322a0-108">*dwPID*</span></span> 
  
>  <span data-ttu-id="322a0-109">ID de processus pour le processus qui envoie une notification d’indexation à l’indexeur du handler de protocole MAPI.</span><span class="sxs-lookup"><span data-stu-id="322a0-109">Process ID for the process that is sending an indexing notification to the indexer of the MAPI Protocol Handler.</span></span> 
    

