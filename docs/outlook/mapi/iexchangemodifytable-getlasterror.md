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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 1c817f7ec02e79b956cdd0090ea54ea4528022ad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783683"
---
# <a name="iexchangemodifytablegetlasterror"></a><span data-ttu-id="6305a-103">IExchangeModifyTable::GetLastError</span><span class="sxs-lookup"><span data-stu-id="6305a-103">IExchangeModifyTable::GetLastError</span></span>

  
  
<span data-ttu-id="6305a-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6305a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6305a-105">Retourne des informations sur la dernière erreur qui s’est produite dans un objet table.</span><span class="sxs-lookup"><span data-stu-id="6305a-105">Returns information about the last error that occurred in a table object.</span></span>
  
```cpp
HRESULT GetLastError( 
  HRESULT hResult, 
  ULONG ulFlags, 
  LPMAPIERROR FAR * lppMAPIError 
); 
```

## <a name="parameters"></a><span data-ttu-id="6305a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6305a-106">Parameters</span></span>

 <span data-ttu-id="6305a-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="6305a-107">_hResult_</span></span>
  
> <span data-ttu-id="6305a-108">[in] La valeur renvoyée par la méthode qui a échoué.</span><span class="sxs-lookup"><span data-stu-id="6305a-108">[in] The return value from the method that failed.</span></span>
    
 <span data-ttu-id="6305a-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6305a-109">_ulFlags_</span></span>
  
> <span data-ttu-id="6305a-110">[in] Ne pas utilisé, la valeur 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="6305a-110">[in] Not used, set to 0 (zero).</span></span>
    
 <span data-ttu-id="6305a-111">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="6305a-111">_lppMAPIError_</span></span>
  
> <span data-ttu-id="6305a-112">[out] Pointe vers une structure MAPI [MAPIERROR](mapierror.md) qui contient des informations sur la dernière erreur qui s’est produite pour un objet table.</span><span class="sxs-lookup"><span data-stu-id="6305a-112">[out] Points to a MAPI [MAPIERROR](mapierror.md) structure that contains information about the last error that occurred for a table object.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="6305a-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6305a-113">See also</span></span>



[<span data-ttu-id="6305a-114">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6305a-114">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)
  
[<span data-ttu-id="6305a-115">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="6305a-115">MAPIERROR</span></span>](mapierror.md)


[<span data-ttu-id="6305a-116">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="6305a-116">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

