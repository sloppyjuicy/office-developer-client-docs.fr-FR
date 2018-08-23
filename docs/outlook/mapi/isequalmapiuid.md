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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 0c72164cac8a37d0372ac93f4ed6d3face966ddb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566662"
---
# <a name="isequalmapiuid"></a><span data-ttu-id="c6334-103">IsEqualMAPIUID</span><span class="sxs-lookup"><span data-stu-id="c6334-103">IsEqualMAPIUID</span></span>

  
  
<span data-ttu-id="c6334-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c6334-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c6334-105">Teste deux structures [MAPIUID](mapiuid.md) pour déterminer s’ils contiennent le même identificateur.</span><span class="sxs-lookup"><span data-stu-id="c6334-105">Tests two [MAPIUID](mapiuid.md) structures to determine whether they contain the same identifier.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c6334-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="c6334-106">Header file:</span></span>  <br/> |<span data-ttu-id="c6334-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c6334-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="c6334-108">Structure connexe :</span><span class="sxs-lookup"><span data-stu-id="c6334-108">Related structure:</span></span>  <br/> |<span data-ttu-id="c6334-109">**MAPIUID**</span><span class="sxs-lookup"><span data-stu-id="c6334-109">**MAPIUID**</span></span> <br/> |
   
```cpp
IsEqualMAPIUID(lpuid1, lpuid2)
```

## <a name="parameters"></a><span data-ttu-id="c6334-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c6334-110">Parameters</span></span>

 <span data-ttu-id="c6334-111">_lpuid1_</span><span class="sxs-lookup"><span data-stu-id="c6334-111">_lpuid1_</span></span>
  
> <span data-ttu-id="c6334-112">Pointeur vers la structure **MAPIUID** premier à tester.</span><span class="sxs-lookup"><span data-stu-id="c6334-112">Pointer to the first **MAPIUID** structure to be tested.</span></span> 
    
 <span data-ttu-id="c6334-113">_lpuid2_</span><span class="sxs-lookup"><span data-stu-id="c6334-113">_lpuid2_</span></span>
  
> <span data-ttu-id="c6334-114">Pointeur vers la structure **MAPIUID** deuxième à tester.</span><span class="sxs-lookup"><span data-stu-id="c6334-114">Pointer to the second **MAPIUID** structure to be tested.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c6334-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="c6334-115">Remarks</span></span>

<span data-ttu-id="c6334-116">La macro **IsEqualMAPIUID** renvoie la valeur TRUE si les deux structures **MAPIUID** contiennent les mêmes identificateur et FALSE si elles n’est pas.</span><span class="sxs-lookup"><span data-stu-id="c6334-116">The **IsEqualMAPIUID** macro returns TRUE if the two **MAPIUID** structures contain the same identifier and FALSE if they do not.</span></span> 
  
<span data-ttu-id="c6334-117">La macro **IsEqualMAPIUID** exige que le fichier d’en-tête Memory.h être inclus.</span><span class="sxs-lookup"><span data-stu-id="c6334-117">The **IsEqualMAPIUID** macro requires that the header file Memory.h be included.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c6334-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c6334-118">See also</span></span>



[<span data-ttu-id="c6334-119">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="c6334-119">MAPIUID</span></span>](mapiuid.md)


[<span data-ttu-id="c6334-120">Macros liées aux structures</span><span class="sxs-lookup"><span data-stu-id="c6334-120">Macros Related to Structures</span></span>](macros-related-to-structures.md)

