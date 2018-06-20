---
title: IOSTXInitSync
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.InitSync
api_type:
- COM
ms.assetid: e22244a2-ac5f-910a-501f-4483ea0667c2
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 07305f712fd925b206ce18a32f8f5a24f199ccbf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784330"
---
# <a name="iostxinitsync"></a><span data-ttu-id="36f4e-103">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="36f4e-103">IOSTX::InitSync</span></span>

  
  
<span data-ttu-id="36f4e-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="36f4e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="36f4e-105">Informe la banque de messages local que la synchronisation est prêt à démarrer.</span><span class="sxs-lookup"><span data-stu-id="36f4e-105">Informs the local message store that synchronization is about to start.</span></span>
  
```cpp
HRESULT InitSync( 
    ULONG ulFlags 
);
```

## <a name="parameters"></a><span data-ttu-id="36f4e-106">Param�tres</span><span class="sxs-lookup"><span data-stu-id="36f4e-106">Parameters</span></span>

 <span data-ttu-id="36f4e-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="36f4e-107">_ulFlags_</span></span>
  
> <span data-ttu-id="36f4e-108">[in] Indicateurs pour déterminer le comportement approprié lors de la synchronisation.</span><span class="sxs-lookup"><span data-stu-id="36f4e-108">[in] Flags to determine appropriate behavior during synchronization.</span></span> <span data-ttu-id="36f4e-109">Outlook utilise ces indicateurs dans chaque état de l’ordinateur d’état de réplication pour déterminer les informations qu’il doit fournir pour le client.</span><span class="sxs-lookup"><span data-stu-id="36f4e-109">Outlook uses these flags in each state of the replication state machine to determine the information that it should provide for the client.</span></span> <span data-ttu-id="36f4e-110">Par exemple, si le client transmet **SYNC_ONLY_ASSOCIATED**, Outlook renvoie uniquement les informations relatives aux éléments associés (ou masqués).</span><span class="sxs-lookup"><span data-stu-id="36f4e-110">For example, if the client passes **SYNC_ONLY_ASSOCIATED**, Outlook will only return information related to associated (or hidden) items.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="36f4e-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="36f4e-111">See also</span></span>



[<span data-ttu-id="36f4e-112">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="36f4e-112">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="36f4e-113">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="36f4e-113">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="36f4e-114">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="36f4e-114">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="36f4e-115">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="36f4e-115">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="36f4e-116">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="36f4e-116">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="36f4e-117">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="36f4e-117">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)
  
[<span data-ttu-id="36f4e-118">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="36f4e-118">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="36f4e-119">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="36f4e-119">MAPI Constants</span></span>](mapi-constants.md)

