---
title: IPSTXGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTX.GetLastError
api_type:
- COM
ms.assetid: 68dc0ecc-881e-de69-faaa-90acb9857031
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: f45b070464fe1b3c177088ff6aa3295f961d45f6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592590"
---
# <a name="ipstxgetlasterror"></a><span data-ttu-id="33fa9-103">IPSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="33fa9-103">IPSTX::GetLastError</span></span>

  
  
<span data-ttu-id="33fa9-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="33fa9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="33fa9-105">Obtient des informations sur la dernière erreur étendues.</span><span class="sxs-lookup"><span data-stu-id="33fa9-105">Gets extended information about the last error.</span></span>
  
```cpp
HRESULT GetLastError( 
    HRESULT hResult, 
    ULONG ulFlags, 
    LPMAPIERROR *lppMAPIError 
);
```

## <a name="parameters"></a><span data-ttu-id="33fa9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="33fa9-106">Parameters</span></span>

 <span data-ttu-id="33fa9-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="33fa9-107">_hResult_</span></span>
  
>  <span data-ttu-id="33fa9-108">[in] Code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="33fa9-108">[in] Error code.</span></span> 
    
 <span data-ttu-id="33fa9-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="33fa9-109">_ulFlags_</span></span>
  
>  <span data-ttu-id="33fa9-110">[in] Indicateurs pour modifier le comportement.</span><span class="sxs-lookup"><span data-stu-id="33fa9-110">[in] Flags to modify behavior.</span></span> <span data-ttu-id="33fa9-111">Ce doit être 0.</span><span class="sxs-lookup"><span data-stu-id="33fa9-111">This must be 0.</span></span> 
    
 <span data-ttu-id="33fa9-112">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="33fa9-112">_lppMAPIError_</span></span>
  
>  <span data-ttu-id="33fa9-113">[out] Pointeur vers la structure **MAPIERROR** qui contient les informations d’étendue de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="33fa9-113">[out] Pointer to the **MAPIERROR** structure that contains the extended information for the error.</span></span> <span data-ttu-id="33fa9-114">Voir mapidefs.h pour la définition du type de **LPMAPIERROR**.</span><span class="sxs-lookup"><span data-stu-id="33fa9-114">See mapidefs.h for the type definition of **LPMAPIERROR**.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="33fa9-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="33fa9-115">See also</span></span>



[<span data-ttu-id="33fa9-116">IPSTX::EmulateSpooler</span><span class="sxs-lookup"><span data-stu-id="33fa9-116">IPSTX::EmulateSpooler</span></span>](ipstx-emulatespooler.md)
  
[<span data-ttu-id="33fa9-117">IPSTX::GetSyncObject</span><span class="sxs-lookup"><span data-stu-id="33fa9-117">IPSTX::GetSyncObject</span></span>](ipstx-getsyncobject.md)

