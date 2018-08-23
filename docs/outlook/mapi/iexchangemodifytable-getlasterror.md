---
title: IExchangeModifyTableGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IExchangeModifyTable.GetLastError
api_type:
- COM
ms.assetid: b850dc08-73c3-4b19-ae29-1892d6a2ff2f
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: f0d2ad118346dd06788af972b64b10d6f6f6d0fc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594291"
---
# <a name="iexchangemodifytablegetlasterror"></a><span data-ttu-id="56895-103">IExchangeModifyTable::GetLastError</span><span class="sxs-lookup"><span data-stu-id="56895-103">IExchangeModifyTable::GetLastError</span></span>

  
  
<span data-ttu-id="56895-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="56895-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="56895-105">Retourne des informations sur la dernière erreur qui s’est produite dans un objet table.</span><span class="sxs-lookup"><span data-stu-id="56895-105">Returns information about the last error that occurred in a table object.</span></span>
  
```cpp
HRESULT GetLastError( 
  HRESULT hResult, 
  ULONG ulFlags, 
  LPMAPIERROR FAR * lppMAPIError 
); 
```

## <a name="parameters"></a><span data-ttu-id="56895-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="56895-106">Parameters</span></span>

 <span data-ttu-id="56895-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="56895-107">_hResult_</span></span>
  
> <span data-ttu-id="56895-108">[in] La valeur renvoyée par la méthode qui a échoué.</span><span class="sxs-lookup"><span data-stu-id="56895-108">[in] The return value from the method that failed.</span></span>
    
 <span data-ttu-id="56895-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="56895-109">_ulFlags_</span></span>
  
> <span data-ttu-id="56895-110">[in] Ne pas utilisé, la valeur 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="56895-110">[in] Not used, set to 0 (zero).</span></span>
    
 <span data-ttu-id="56895-111">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="56895-111">_lppMAPIError_</span></span>
  
> <span data-ttu-id="56895-112">[out] Pointe vers une structure MAPI [MAPIERROR](mapierror.md) qui contient des informations sur la dernière erreur qui s’est produite pour un objet table.</span><span class="sxs-lookup"><span data-stu-id="56895-112">[out] Points to a MAPI [MAPIERROR](mapierror.md) structure that contains information about the last error that occurred for a table object.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="56895-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="56895-113">See also</span></span>



[<span data-ttu-id="56895-114">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="56895-114">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)
  
[<span data-ttu-id="56895-115">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="56895-115">MAPIERROR</span></span>](mapierror.md)


[<span data-ttu-id="56895-116">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="56895-116">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

