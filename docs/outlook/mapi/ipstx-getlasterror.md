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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: e061808c57f25f881cc17fa5251e46ed5d524acd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784445"
---
# <a name="ipstxgetlasterror"></a><span data-ttu-id="80e50-103">IPSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="80e50-103">IPSTX::GetLastError</span></span>

  
  
<span data-ttu-id="80e50-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="80e50-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="80e50-105">Obtient des informations sur la dernière erreur étendues.</span><span class="sxs-lookup"><span data-stu-id="80e50-105">Gets extended information about the last error.</span></span>
  
```cpp
HRESULT GetLastError( 
    HRESULT hResult, 
    ULONG ulFlags, 
    LPMAPIERROR *lppMAPIError 
);
```

## <a name="parameters"></a><span data-ttu-id="80e50-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="80e50-106">Parameters</span></span>

 <span data-ttu-id="80e50-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="80e50-107">_hResult_</span></span>
  
>  <span data-ttu-id="80e50-108">[in] Code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="80e50-108">[in] Error code.</span></span> 
    
 <span data-ttu-id="80e50-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="80e50-109">_ulFlags_</span></span>
  
>  <span data-ttu-id="80e50-110">[in] Indicateurs pour modifier le comportement.</span><span class="sxs-lookup"><span data-stu-id="80e50-110">[in] Flags to modify behavior.</span></span> <span data-ttu-id="80e50-111">Ce doit être 0.</span><span class="sxs-lookup"><span data-stu-id="80e50-111">This must be 0.</span></span> 
    
 <span data-ttu-id="80e50-112">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="80e50-112">_lppMAPIError_</span></span>
  
>  <span data-ttu-id="80e50-113">[out] Pointeur vers la structure **MAPIERROR** qui contient les informations d’étendue de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="80e50-113">[out] Pointer to the **MAPIERROR** structure that contains the extended information for the error.</span></span> <span data-ttu-id="80e50-114">Voir mapidefs.h pour la définition du type de **LPMAPIERROR**.</span><span class="sxs-lookup"><span data-stu-id="80e50-114">See mapidefs.h for the type definition of **LPMAPIERROR**.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="80e50-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="80e50-115">See also</span></span>



[<span data-ttu-id="80e50-116">IPSTX::EmulateSpooler</span><span class="sxs-lookup"><span data-stu-id="80e50-116">IPSTX::EmulateSpooler</span></span>](ipstx-emulatespooler.md)
  
[<span data-ttu-id="80e50-117">IPSTX::GetSyncObject</span><span class="sxs-lookup"><span data-stu-id="80e50-117">IPSTX::GetSyncObject</span></span>](ipstx-getsyncobject.md)

