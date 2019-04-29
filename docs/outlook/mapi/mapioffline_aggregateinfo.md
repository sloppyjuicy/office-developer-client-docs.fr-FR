---
title: MAPIOFFLINE_AGGREGATEINFO
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2e502d28-ae09-49d9-a35a-5d77acdcd6f4
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 4775de0707eb90549f07525e3aa54ec5842f6050
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438161"
---
# <a name="mapiofflineaggregateinfo"></a><span data-ttu-id="9a34a-103">MAPIOFFLINE_AGGREGATEINFO</span><span class="sxs-lookup"><span data-stu-id="9a34a-103">MAPIOFFLINE_AGGREGATEINFO</span></span>

  
  
<span data-ttu-id="9a34a-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9a34a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9a34a-105">La structure est utilisée avec [HrCreateOfflineObj](hrcreateofflineobj.md).</span><span class="sxs-lookup"><span data-stu-id="9a34a-105">The structure is used with [HrCreateOfflineObj](hrcreateofflineobj.md).</span></span> 
  
```cpp
typedef struct
{
  ULONG            ulSize;
  IUnknown*          pOuterObj;
  IUnknown*          pRefTrackRoot;
} MAPIOFFLINE_AGGREGATEINFO;
```

## <a name="members"></a><span data-ttu-id="9a34a-106">Members</span><span class="sxs-lookup"><span data-stu-id="9a34a-106">Members</span></span>

 <span data-ttu-id="9a34a-107">**ulSize**</span><span class="sxs-lookup"><span data-stu-id="9a34a-107">**ulSize**</span></span>
  
> <span data-ttu-id="9a34a-108">Taille de la structure.</span><span class="sxs-lookup"><span data-stu-id="9a34a-108">The size of the structure.</span></span>
    
 <span data-ttu-id="9a34a-109">**pOuterObj**</span><span class="sxs-lookup"><span data-stu-id="9a34a-109">**pOuterObj**</span></span>
  
> <span data-ttu-id="9a34a-110">Pointeur vers l'objet IUnknown sur lequel cet objet est regroupé.</span><span class="sxs-lookup"><span data-stu-id="9a34a-110">A pointer to the IUnknown object onto which this object is being aggregated.</span></span> <span data-ttu-id="9a34a-111">Cela permet aux appels QueryInterface de passer par l'objet créé.</span><span class="sxs-lookup"><span data-stu-id="9a34a-111">This allows any QueryInterface calls to pass through to the created object.</span></span>
    
 <span data-ttu-id="9a34a-112">**pRefTrackRoot**</span><span class="sxs-lookup"><span data-stu-id="9a34a-112">**pRefTrackRoot**</span></span>
  
> <span data-ttu-id="9a34a-113">Doit être NULL.</span><span class="sxs-lookup"><span data-stu-id="9a34a-113">Must be NULL.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9a34a-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9a34a-114">See also</span></span>



[<span data-ttu-id="9a34a-115">HrCreateOfflineObj</span><span class="sxs-lookup"><span data-stu-id="9a34a-115">HrCreateOfflineObj</span></span>](hrcreateofflineobj.md)
  
[<span data-ttu-id="9a34a-116">MAPIOFFLINE_CREATEINFO</span><span class="sxs-lookup"><span data-stu-id="9a34a-116">MAPIOFFLINE_CREATEINFO</span></span>](mapioffline_createinfo.md)

