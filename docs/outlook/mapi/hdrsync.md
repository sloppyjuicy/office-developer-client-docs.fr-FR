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
ms.openlocfilehash: 2131197ca24804eec74270100fa70c05c47a27cc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410251"
---
# <a name="hdrsync"></a><span data-ttu-id="81d65-103">HDRSYNC</span><span class="sxs-lookup"><span data-stu-id="81d65-103">HDRSYNC</span></span>

  
  
<span data-ttu-id="81d65-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="81d65-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="81d65-105">Informations pour la synchronisation d’un en-tête de message pendant [l’état d’en-tête du message de téléchargement.](download-message-header-state.md)</span><span class="sxs-lookup"><span data-stu-id="81d65-105">Information for synchronizing a message header during the [download message header state](download-message-header-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="81d65-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="81d65-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="81d65-107">Membres</span><span class="sxs-lookup"><span data-stu-id="81d65-107">Members</span></span>

 <span data-ttu-id="81d65-108">_pupmsg_</span><span class="sxs-lookup"><span data-stu-id="81d65-108">_pupmsg_</span></span>
  
- <span data-ttu-id="81d65-109">[out] Informations pour l’en-tête de message actuel dans la boutique locale.</span><span class="sxs-lookup"><span data-stu-id="81d65-109">[out] Information for the current message header in the local store.</span></span>
    
 <span data-ttu-id="81d65-110">_pare-vie_</span><span class="sxs-lookup"><span data-stu-id="81d65-110">_feidPar_</span></span>
  
- <span data-ttu-id="81d65-111">[out] ID d’entrée pour le dossier parent de l’élément de message.</span><span class="sxs-lookup"><span data-stu-id="81d65-111">[out] Entry ID for the parent folder of the message item.</span></span>
    
 <span data-ttu-id="81d65-112">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="81d65-112">_pstmReserved_</span></span>
  
- <span data-ttu-id="81d65-113">[sortant] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="81d65-113">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
 <span data-ttu-id="81d65-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="81d65-114">_ulFlags_</span></span>
  
- <span data-ttu-id="81d65-115">[in] Indicateurs pour modifier le comportement :</span><span class="sxs-lookup"><span data-stu-id="81d65-115">[in] Flags to modify behavior:</span></span>
    
- <span data-ttu-id="81d65-116">HSF_LOCAL</span><span class="sxs-lookup"><span data-stu-id="81d65-116">HSF_LOCAL</span></span>
    
  - <span data-ttu-id="81d65-117">[in] L’élément complet réside dans la même boutique locale que l’élément d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="81d65-117">[in] Full item resides in the same local store as the header item.</span></span>
    
- <span data-ttu-id="81d65-118">HSF_COPYDESTRUCTIVE</span><span class="sxs-lookup"><span data-stu-id="81d65-118">HSF_COPYDESTRUCTIVE</span></span>
    
  -  <span data-ttu-id="81d65-119">[in] Optimiser les opérations de copie interne.</span><span class="sxs-lookup"><span data-stu-id="81d65-119">[in] Optimize internal copy operations.</span></span> <span data-ttu-id="81d65-120">Cela peut entraîner une perte de données.</span><span class="sxs-lookup"><span data-stu-id="81d65-120">This might cause data loss.</span></span> <span data-ttu-id="81d65-121">**HSF_LOCAL** doit être définie.</span><span class="sxs-lookup"><span data-stu-id="81d65-121">**HSF_LOCAL** must be set.</span></span> 
    
- <span data-ttu-id="81d65-122">HSF_OK</span><span class="sxs-lookup"><span data-stu-id="81d65-122">HSF_OK</span></span>
    
  - <span data-ttu-id="81d65-123">[in] La synchronisation d’en-tête a réussi.</span><span class="sxs-lookup"><span data-stu-id="81d65-123">[in] Header synchronization was successful.</span></span> <span data-ttu-id="81d65-124">Le client définit cet élément après avoir téléchargé des informations à partir du serveur.</span><span class="sxs-lookup"><span data-stu-id="81d65-124">The client sets this after downloading information from the server.</span></span>
    
     <span data-ttu-id="81d65-125">_pmsgFull_</span><span class="sxs-lookup"><span data-stu-id="81d65-125">_pmsgFull_</span></span>
    
  - <span data-ttu-id="81d65-126">[in] L’élément de message complet, y compris l’en-tête de message téléchargé à partir du serveur.</span><span class="sxs-lookup"><span data-stu-id="81d65-126">[in] The full message item including the message header downloaded from the server.</span></span> <span data-ttu-id="81d65-127">Voir mapidefs.h pour la définition de type **de LPMESSAGE**.</span><span class="sxs-lookup"><span data-stu-id="81d65-127">See mapidefs.h for the type definition of **LPMESSAGE**.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="81d65-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="81d65-128">See also</span></span>



[<span data-ttu-id="81d65-129">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="81d65-129">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="81d65-130">À propos de la machine à états de réplication</span><span class="sxs-lookup"><span data-stu-id="81d65-130">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="81d65-131">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="81d65-131">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="81d65-132">FEID</span><span class="sxs-lookup"><span data-stu-id="81d65-132">FEID</span></span>](feid.md)

