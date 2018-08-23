---
title: IPSTX2SetSpoolSuspendState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTX2.SetSpoolSuspendState
api_type:
- COM
ms.assetid: 396db029-1d4a-203d-2256-3353d03c6767
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: b6a36c1e0c3854342b627b6fddd6eb5459211f62
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590427"
---
# <a name="ipstx2setspoolsuspendstate"></a><span data-ttu-id="fd7fc-103">IPSTX2::SetSpoolSuspendState</span><span class="sxs-lookup"><span data-stu-id="fd7fc-103">IPSTX2::SetSpoolSuspendState</span></span>

  
  
<span data-ttu-id="fd7fc-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fd7fc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fd7fc-105">Définit l’état suspendu sur le spouleur.</span><span class="sxs-lookup"><span data-stu-id="fd7fc-105">Sets the suspended state on the spooler.</span></span>
  
```cpp
void SetSpoolSuspendState( 
    ULONG ulState 
);
```

## <a name="parameters"></a><span data-ttu-id="fd7fc-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fd7fc-106">Parameters</span></span>

 <span data-ttu-id="fd7fc-107">_ulState_</span><span class="sxs-lookup"><span data-stu-id="fd7fc-107">_ulState_</span></span>
  
> <span data-ttu-id="fd7fc-108">[in] L’état pour définir le spouleur.</span><span class="sxs-lookup"><span data-stu-id="fd7fc-108">[in] The state to set the spooler to.</span></span> <span data-ttu-id="fd7fc-109">Il doit être une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="fd7fc-109">It must be one of the following values:</span></span>
    
 <span data-ttu-id="fd7fc-110">**SS_ACTIVE**</span><span class="sxs-lookup"><span data-stu-id="fd7fc-110">**SS_ACTIVE**</span></span>
  
> 
    
 <span data-ttu-id="fd7fc-111">**SS_SUSPENDED**</span><span class="sxs-lookup"><span data-stu-id="fd7fc-111">**SS_SUSPENDED**</span></span>
  
> 
    
## <a name="see-also"></a><span data-ttu-id="fd7fc-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fd7fc-112">See also</span></span>



[<span data-ttu-id="fd7fc-113">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="fd7fc-113">MAPI Constants</span></span>](mapi-constants.md)

