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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 30ec82788e46ca07c6529ce74872e0a0c7c012a1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784427"
---
# <a name="ipstx2setspoolsuspendstate"></a><span data-ttu-id="7c968-103">IPSTX2::SetSpoolSuspendState</span><span class="sxs-lookup"><span data-stu-id="7c968-103">IPSTX2::SetSpoolSuspendState</span></span>

  
  
<span data-ttu-id="7c968-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7c968-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7c968-105">Définit l’état suspendu sur le spouleur.</span><span class="sxs-lookup"><span data-stu-id="7c968-105">Sets the suspended state on the spooler.</span></span>
  
```cpp
void SetSpoolSuspendState( 
    ULONG ulState 
);
```

## <a name="parameters"></a><span data-ttu-id="7c968-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7c968-106">Parameters</span></span>

 <span data-ttu-id="7c968-107">_ulState_</span><span class="sxs-lookup"><span data-stu-id="7c968-107">_ulState_</span></span>
  
> <span data-ttu-id="7c968-108">[in] L’état pour définir le spouleur.</span><span class="sxs-lookup"><span data-stu-id="7c968-108">[in] The state to set the spooler to.</span></span> <span data-ttu-id="7c968-109">Il doit être une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="7c968-109">It must be one of the following values:</span></span>
    
 <span data-ttu-id="7c968-110">**SS_ACTIVE**</span><span class="sxs-lookup"><span data-stu-id="7c968-110">**SS_ACTIVE**</span></span>
  
> 
    
 <span data-ttu-id="7c968-111">**SS_SUSPENDED**</span><span class="sxs-lookup"><span data-stu-id="7c968-111">**SS_SUSPENDED**</span></span>
  
> 
    
## <a name="see-also"></a><span data-ttu-id="7c968-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7c968-112">See also</span></span>



[<span data-ttu-id="7c968-113">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="7c968-113">MAPI Constants</span></span>](mapi-constants.md)

