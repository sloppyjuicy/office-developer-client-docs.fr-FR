---
title: IsEqualMAPIUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.IsEqualMAPIUID
api_type:
- COM
ms.assetid: 85d71b73-0630-4c5d-b0e3-b48d27a300d0
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 44e3613338c8932bc80dd1150392033dfa3cd050
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426932"
---
# <a name="isequalmapiuid"></a><span data-ttu-id="7e3e7-103">IsEqualMAPIUID</span><span class="sxs-lookup"><span data-stu-id="7e3e7-103">IsEqualMAPIUID</span></span>

  
  
<span data-ttu-id="7e3e7-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7e3e7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7e3e7-105">Teste deux structures [MAPIUID](mapiuid.md) pour déterminer si elles contiennent le même identificateur.</span><span class="sxs-lookup"><span data-stu-id="7e3e7-105">Tests two [MAPIUID](mapiuid.md) structures to determine whether they contain the same identifier.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7e3e7-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="7e3e7-106">Header file:</span></span>  <br/> |<span data-ttu-id="7e3e7-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7e3e7-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="7e3e7-108">Structure connexe :</span><span class="sxs-lookup"><span data-stu-id="7e3e7-108">Related structure:</span></span>  <br/> |<span data-ttu-id="7e3e7-109">**MAPIUID**</span><span class="sxs-lookup"><span data-stu-id="7e3e7-109">**MAPIUID**</span></span> <br/> |
   
```cpp
IsEqualMAPIUID(lpuid1, lpuid2)
```

## <a name="parameters"></a><span data-ttu-id="7e3e7-110">Parameters</span><span class="sxs-lookup"><span data-stu-id="7e3e7-110">Parameters</span></span>

 <span data-ttu-id="7e3e7-111">_lpuid1_</span><span class="sxs-lookup"><span data-stu-id="7e3e7-111">_lpuid1_</span></span>
  
> <span data-ttu-id="7e3e7-112">Pointeur vers la première structure **MAPIUID** à tester.</span><span class="sxs-lookup"><span data-stu-id="7e3e7-112">Pointer to the first **MAPIUID** structure to be tested.</span></span> 
    
 <span data-ttu-id="7e3e7-113">_lpuid2_</span><span class="sxs-lookup"><span data-stu-id="7e3e7-113">_lpuid2_</span></span>
  
> <span data-ttu-id="7e3e7-114">Pointeur vers la deuxième structure **MAPIUID** à tester.</span><span class="sxs-lookup"><span data-stu-id="7e3e7-114">Pointer to the second **MAPIUID** structure to be tested.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="7e3e7-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="7e3e7-115">Remarks</span></span>

<span data-ttu-id="7e3e7-116">La macro **IsEqualMAPIUID** renvoie true si les deux structures **MAPIUID** contiennent le même identificateur et FALSE si ce n’est pas le cas.</span><span class="sxs-lookup"><span data-stu-id="7e3e7-116">The **IsEqualMAPIUID** macro returns TRUE if the two **MAPIUID** structures contain the same identifier and FALSE if they do not.</span></span> 
  
<span data-ttu-id="7e3e7-117">La macro **IsEqualMAPIUID nécessite** que le fichier d’en-tête Memory.h soit inclus.</span><span class="sxs-lookup"><span data-stu-id="7e3e7-117">The **IsEqualMAPIUID** macro requires that the header file Memory.h be included.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7e3e7-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7e3e7-118">See also</span></span>



[<span data-ttu-id="7e3e7-119">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="7e3e7-119">MAPIUID</span></span>](mapiuid.md)


[<span data-ttu-id="7e3e7-120">Macros liées aux structures</span><span class="sxs-lookup"><span data-stu-id="7e3e7-120">Macros Related to Structures</span></span>](macros-related-to-structures.md)

