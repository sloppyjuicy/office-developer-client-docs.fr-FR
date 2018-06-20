---
title: MAPIOFFLINE_AGGREGATEINFO
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2e502d28-ae09-49d9-a35a-5d77acdcd6f4
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 24e16aeb1bbee1c35cf8fbd5813fb3e83b762187
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784750"
---
# <a name="mapiofflineaggregateinfo"></a><span data-ttu-id="c1a1f-103">MAPIOFFLINE_AGGREGATEINFO</span><span class="sxs-lookup"><span data-stu-id="c1a1f-103">MAPIOFFLINE_AGGREGATEINFO</span></span>

  
  
<span data-ttu-id="c1a1f-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c1a1f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c1a1f-105">La structure est utilisée avec [HrCreateOfflineObj](hrcreateofflineobj.md).</span><span class="sxs-lookup"><span data-stu-id="c1a1f-105">The structure is used with [HrCreateOfflineObj](hrcreateofflineobj.md).</span></span> 
  
```cpp
typedef struct
{
  ULONG            ulSize;
  IUnknown*          pOuterObj;
  IUnknown*          pRefTrackRoot;
} MAPIOFFLINE_AGGREGATEINFO;
```

## <a name="members"></a><span data-ttu-id="c1a1f-106">Membres</span><span class="sxs-lookup"><span data-stu-id="c1a1f-106">Members</span></span>

 <span data-ttu-id="c1a1f-107">**ulSize**</span><span class="sxs-lookup"><span data-stu-id="c1a1f-107">**ulSize**</span></span>
  
> <span data-ttu-id="c1a1f-108">La taille de la structure.</span><span class="sxs-lookup"><span data-stu-id="c1a1f-108">The size of the structure.</span></span>
    
 <span data-ttu-id="c1a1f-109">**pOuterObj**</span><span class="sxs-lookup"><span data-stu-id="c1a1f-109">**pOuterObj**</span></span>
  
> <span data-ttu-id="c1a1f-110">Pointeur vers l’objet IUnknown sur lequel cet objet est en cours d’agrégation.</span><span class="sxs-lookup"><span data-stu-id="c1a1f-110">A pointer to the IUnknown object onto which this object is being aggregated.</span></span> <span data-ttu-id="c1a1f-111">Ainsi, les appels QueryInterface à transmettre à l’objet créé.</span><span class="sxs-lookup"><span data-stu-id="c1a1f-111">This allows any QueryInterface calls to pass through to the created object.</span></span>
    
 <span data-ttu-id="c1a1f-112">**pRefTrackRoot**</span><span class="sxs-lookup"><span data-stu-id="c1a1f-112">**pRefTrackRoot**</span></span>
  
> <span data-ttu-id="c1a1f-113">Doit être NULL.</span><span class="sxs-lookup"><span data-stu-id="c1a1f-113">Must be NULL.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c1a1f-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c1a1f-114">See also</span></span>



[<span data-ttu-id="c1a1f-115">HrCreateOfflineObj</span><span class="sxs-lookup"><span data-stu-id="c1a1f-115">HrCreateOfflineObj</span></span>](hrcreateofflineobj.md)
  
[<span data-ttu-id="c1a1f-116">MAPIOFFLINE_CREATEINFO</span><span class="sxs-lookup"><span data-stu-id="c1a1f-116">MAPIOFFLINE_CREATEINFO</span></span>](mapioffline_createinfo.md)

