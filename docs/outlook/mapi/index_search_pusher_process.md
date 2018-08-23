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
# <a name="indexsearchpusherprocess"></a><span data-ttu-id="58961-103">INDEX_SEARCH_PUSHER_PROCESS</span><span class="sxs-lookup"><span data-stu-id="58961-103">INDEX_SEARCH_PUSHER_PROCESS</span></span>

  
  
<span data-ttu-id="58961-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="58961-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="58961-105">Spécifie le processus qui envoie une notification pour le Gestionnaire de protocole MAPI qu’un objet de cette banque est prêt pour l’indexation.</span><span class="sxs-lookup"><span data-stu-id="58961-105">Specifies the process that is sending a notification to the MAPI Protocol Handler that an object in that store is ready for indexing.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="58961-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="58961-106">Quick info</span></span>

```cpp
typedef struct _INDEX_SEARCH_PUSHER_PROCESS {  
    DWORD dwPID;  
} INDEX_SEARCH_PUSHER_PROCESS; 
```

## <a name="members"></a><span data-ttu-id="58961-107">Members</span><span class="sxs-lookup"><span data-stu-id="58961-107">Members</span></span>

 <span data-ttu-id="58961-108">*dwPID*</span><span class="sxs-lookup"><span data-stu-id="58961-108">*dwPID*</span></span> 
  
>  <span data-ttu-id="58961-109">ID de processus pour le processus qui envoie une notification d’indexation à l’indexeur du Gestionnaire de protocole MAPI.</span><span class="sxs-lookup"><span data-stu-id="58961-109">Process ID for the process that is sending an indexing notification to the indexer of the MAPI Protocol Handler.</span></span> 
    

