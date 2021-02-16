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
ms.openlocfilehash: 1d0fb16ba63548a44dba3920670c0e65f8c700a1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414976"
---
# <a name="ipstxgetlasterror"></a><span data-ttu-id="ed1e1-103">IPSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="ed1e1-103">IPSTX::GetLastError</span></span>

  
  
<span data-ttu-id="ed1e1-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ed1e1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ed1e1-105">Obtient des informations étendues sur la dernière erreur.</span><span class="sxs-lookup"><span data-stu-id="ed1e1-105">Gets extended information about the last error.</span></span>
  
```cpp
HRESULT GetLastError( 
    HRESULT hResult, 
    ULONG ulFlags, 
    LPMAPIERROR *lppMAPIError 
);
```

## <a name="parameters"></a><span data-ttu-id="ed1e1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ed1e1-106">Parameters</span></span>

 <span data-ttu-id="ed1e1-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="ed1e1-107">_hResult_</span></span>
  
>  <span data-ttu-id="ed1e1-108">[in] Code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="ed1e1-108">[in] Error code.</span></span> 
    
 <span data-ttu-id="ed1e1-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ed1e1-109">_ulFlags_</span></span>
  
>  <span data-ttu-id="ed1e1-110">[in] Indicateurs pour modifier le comportement.</span><span class="sxs-lookup"><span data-stu-id="ed1e1-110">[in] Flags to modify behavior.</span></span> <span data-ttu-id="ed1e1-111">Ce doit être 0.</span><span class="sxs-lookup"><span data-stu-id="ed1e1-111">This must be 0.</span></span> 
    
 <span data-ttu-id="ed1e1-112">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="ed1e1-112">_lppMAPIError_</span></span>
  
>  <span data-ttu-id="ed1e1-113">[out] Pointeur vers la structure **MAPIERROR** qui contient les informations étendues de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="ed1e1-113">[out] Pointer to the **MAPIERROR** structure that contains the extended information for the error.</span></span> <span data-ttu-id="ed1e1-114">Voir mapidefs.h pour la définition de type **de LPMAPIERROR**.</span><span class="sxs-lookup"><span data-stu-id="ed1e1-114">See mapidefs.h for the type definition of **LPMAPIERROR**.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="ed1e1-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ed1e1-115">See also</span></span>



[<span data-ttu-id="ed1e1-116">IPSTX::EmulateSpooler</span><span class="sxs-lookup"><span data-stu-id="ed1e1-116">IPSTX::EmulateSpooler</span></span>](ipstx-emulatespooler.md)
  
[<span data-ttu-id="ed1e1-117">IPSTX::GetSyncObject</span><span class="sxs-lookup"><span data-stu-id="ed1e1-117">IPSTX::GetSyncObject</span></span>](ipstx-getsyncobject.md)

