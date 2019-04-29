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
# <a name="hdrsync"></a><span data-ttu-id="db523-103">HDRSYNC</span><span class="sxs-lookup"><span data-stu-id="db523-103">HDRSYNC</span></span>

  
  
<span data-ttu-id="db523-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="db523-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="db523-105">Informations pour la synchronisation d'un en-tête de message lors de l' [État d'en-tête de message de téléchargement](download-message-header-state.md).</span><span class="sxs-lookup"><span data-stu-id="db523-105">Information for synchronizing a message header during the [download message header state](download-message-header-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="db523-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="db523-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="db523-107">Membres</span><span class="sxs-lookup"><span data-stu-id="db523-107">Members</span></span>

 <span data-ttu-id="db523-108">_pupmsg_</span><span class="sxs-lookup"><span data-stu-id="db523-108">_pupmsg_</span></span>
  
- <span data-ttu-id="db523-109">remarquer Informations de l'en-tête de message actuel dans le magasin local.</span><span class="sxs-lookup"><span data-stu-id="db523-109">[out] Information for the current message header in the local store.</span></span>
    
 <span data-ttu-id="db523-110">_feidPar_</span><span class="sxs-lookup"><span data-stu-id="db523-110">_feidPar_</span></span>
  
- <span data-ttu-id="db523-111">remarquer ID d'entrée du dossier parent de l'élément de message.</span><span class="sxs-lookup"><span data-stu-id="db523-111">[out] Entry ID for the parent folder of the message item.</span></span>
    
 <span data-ttu-id="db523-112">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="db523-112">_pstmReserved_</span></span>
  
- <span data-ttu-id="db523-113">[sortant] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="db523-113">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
 <span data-ttu-id="db523-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="db523-114">_ulFlags_</span></span>
  
- <span data-ttu-id="db523-115">dans Indicateurs permettant de modifier le comportement:</span><span class="sxs-lookup"><span data-stu-id="db523-115">[in] Flags to modify behavior:</span></span>
    
- <span data-ttu-id="db523-116">HSF_LOCAL</span><span class="sxs-lookup"><span data-stu-id="db523-116">HSF_LOCAL</span></span>
    
  - <span data-ttu-id="db523-117">dans L'élément complet réside dans le même magasin local que l'élément d'en-tête.</span><span class="sxs-lookup"><span data-stu-id="db523-117">[in] Full item resides in the same local store as the header item.</span></span>
    
- <span data-ttu-id="db523-118">HSF_COPYDESTRUCTIVE</span><span class="sxs-lookup"><span data-stu-id="db523-118">HSF_COPYDESTRUCTIVE</span></span>
    
  -  <span data-ttu-id="db523-119">dans Optimiser les opérations de copie interne.</span><span class="sxs-lookup"><span data-stu-id="db523-119">[in] Optimize internal copy operations.</span></span> <span data-ttu-id="db523-120">Cela peut entraîner une perte de données.</span><span class="sxs-lookup"><span data-stu-id="db523-120">This might cause data loss.</span></span> <span data-ttu-id="db523-121">**HSF_LOCAL** doit être défini.</span><span class="sxs-lookup"><span data-stu-id="db523-121">**HSF_LOCAL** must be set.</span></span> 
    
- <span data-ttu-id="db523-122">HSF_OK</span><span class="sxs-lookup"><span data-stu-id="db523-122">HSF_OK</span></span>
    
  - <span data-ttu-id="db523-123">dans La synchronisation d'en-tête a réussi.</span><span class="sxs-lookup"><span data-stu-id="db523-123">[in] Header synchronization was successful.</span></span> <span data-ttu-id="db523-124">Le client définit cet élément après avoir téléchargé des informations à partir du serveur.</span><span class="sxs-lookup"><span data-stu-id="db523-124">The client sets this after downloading information from the server.</span></span>
    
     <span data-ttu-id="db523-125">_pmsgFull_</span><span class="sxs-lookup"><span data-stu-id="db523-125">_pmsgFull_</span></span>
    
  - <span data-ttu-id="db523-126">dans Élément de message complet incluant l'en-tête de message téléchargé à partir du serveur.</span><span class="sxs-lookup"><span data-stu-id="db523-126">[in] The full message item including the message header downloaded from the server.</span></span> <span data-ttu-id="db523-127">Voir mapidefs. h pour la définition de type de **LPMESSAGE**.</span><span class="sxs-lookup"><span data-stu-id="db523-127">See mapidefs.h for the type definition of **LPMESSAGE**.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="db523-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="db523-128">See also</span></span>



[<span data-ttu-id="db523-129">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="db523-129">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="db523-130">À propos de la machine à états de réplication</span><span class="sxs-lookup"><span data-stu-id="db523-130">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="db523-131">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="db523-131">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="db523-132">FEID</span><span class="sxs-lookup"><span data-stu-id="db523-132">FEID</span></span>](feid.md)

