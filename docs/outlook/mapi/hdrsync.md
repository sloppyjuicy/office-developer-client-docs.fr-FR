---
title: HDRSYNC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bf6892d0-a923-e926-5361-59efa49ebdc0
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 261a59e628320f384deeb760ba71c9c0386cfde6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576042"
---
# <a name="hdrsync"></a><span data-ttu-id="2e2de-103">HDRSYNC</span><span class="sxs-lookup"><span data-stu-id="2e2de-103">HDRSYNC</span></span>

  
  
<span data-ttu-id="2e2de-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2e2de-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2e2de-105">Informations pour la synchronisation d’un en-tête de message au cours de l' [état d’en-tête de message du téléchargement](download-message-header-state.md).</span><span class="sxs-lookup"><span data-stu-id="2e2de-105">Information for synchronizing a message header during the [download message header state](download-message-header-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="2e2de-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="2e2de-106">Quick info</span></span>

```cpp
struct HDRSYNC 
{ 
    UPMSG *pupmsg; 
    FEID feidPar; 
    LPSTREAM pstmReserved; 
    ULONG ulFlags; 
    LPMESSAGE pmsgFull; 
};
```

## <a name="members"></a><span data-ttu-id="2e2de-107">Members</span><span class="sxs-lookup"><span data-stu-id="2e2de-107">Members</span></span>

 <span data-ttu-id="2e2de-108">_pupmsg_</span><span class="sxs-lookup"><span data-stu-id="2e2de-108">_pupmsg_</span></span>
  
- <span data-ttu-id="2e2de-109">[out] Informations de l’en-tête du message en cours dans le magasin local.</span><span class="sxs-lookup"><span data-stu-id="2e2de-109">[out] Information for the current message header in the local store.</span></span>
    
 <span data-ttu-id="2e2de-110">_feidPar_</span><span class="sxs-lookup"><span data-stu-id="2e2de-110">_feidPar_</span></span>
  
- <span data-ttu-id="2e2de-111">[out] ID d’entrée pour le dossier parent de l’élément de message.</span><span class="sxs-lookup"><span data-stu-id="2e2de-111">[out] Entry ID for the parent folder of the message item.</span></span>
    
 <span data-ttu-id="2e2de-112">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="2e2de-112">_pstmReserved_</span></span>
  
- <span data-ttu-id="2e2de-113">[out] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="2e2de-113">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
 <span data-ttu-id="2e2de-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2e2de-114">_ulFlags_</span></span>
  
- <span data-ttu-id="2e2de-115">[in] Indicateurs pour modifier le comportement :</span><span class="sxs-lookup"><span data-stu-id="2e2de-115">[in] Flags to modify behavior:</span></span>
    
- <span data-ttu-id="2e2de-116">HSF_LOCAL</span><span class="sxs-lookup"><span data-stu-id="2e2de-116">HSF_LOCAL</span></span>
    
  - <span data-ttu-id="2e2de-117">[in] Élément complet réside dans le même magasin local en tant que l’élément d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="2e2de-117">[in] Full item resides in the same local store as the header item.</span></span>
    
- <span data-ttu-id="2e2de-118">HSF_COPYDESTRUCTIVE</span><span class="sxs-lookup"><span data-stu-id="2e2de-118">HSF_COPYDESTRUCTIVE</span></span>
    
  -  <span data-ttu-id="2e2de-119">[in] Optimiser les opérations de copie interne.</span><span class="sxs-lookup"><span data-stu-id="2e2de-119">[in] Optimize internal copy operations.</span></span> <span data-ttu-id="2e2de-120">Cela peut entraîner une perte de données.</span><span class="sxs-lookup"><span data-stu-id="2e2de-120">This might cause data loss.</span></span> <span data-ttu-id="2e2de-121">**HSF_LOCAL** doit être défini.</span><span class="sxs-lookup"><span data-stu-id="2e2de-121">**HSF_LOCAL** must be set.</span></span> 
    
- <span data-ttu-id="2e2de-122">HSF_OK</span><span class="sxs-lookup"><span data-stu-id="2e2de-122">HSF_OK</span></span>
    
  - <span data-ttu-id="2e2de-123">[in] La réussite de la synchronisation d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="2e2de-123">[in] Header synchronization was successful.</span></span> <span data-ttu-id="2e2de-124">Le client définit après le téléchargement des informations à partir du serveur.</span><span class="sxs-lookup"><span data-stu-id="2e2de-124">The client sets this after downloading information from the server.</span></span>
    
     <span data-ttu-id="2e2de-125">_pmsgFull_</span><span class="sxs-lookup"><span data-stu-id="2e2de-125">_pmsgFull_</span></span>
    
  - <span data-ttu-id="2e2de-126">[in] L’élément complet y compris l’en-tête de message téléchargé à partir du serveur.</span><span class="sxs-lookup"><span data-stu-id="2e2de-126">[in] The full message item including the message header downloaded from the server.</span></span> <span data-ttu-id="2e2de-127">Voir mapidefs.h pour la définition du type de **LPMESSAGE**.</span><span class="sxs-lookup"><span data-stu-id="2e2de-127">See mapidefs.h for the type definition of **LPMESSAGE**.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="2e2de-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2e2de-128">See also</span></span>



[<span data-ttu-id="2e2de-129">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="2e2de-129">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="2e2de-130">À propos de la machine à états de réplication</span><span class="sxs-lookup"><span data-stu-id="2e2de-130">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="2e2de-131">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="2e2de-131">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="2e2de-132">FEID</span><span class="sxs-lookup"><span data-stu-id="2e2de-132">FEID</span></span>](feid.md)

