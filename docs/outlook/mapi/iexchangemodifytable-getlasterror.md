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
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 8d5d4895e4440945896ee4f2212c5fca6da8610d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350861"
---
# <a name="iexchangemodifytablegetlasterror"></a><span data-ttu-id="a53b6-103">IExchangeModifyTable::GetLastError</span><span class="sxs-lookup"><span data-stu-id="a53b6-103">IExchangeModifyTable::GetLastError</span></span>

  
  
<span data-ttu-id="a53b6-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a53b6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a53b6-105">Renvoie des informations sur la dernière erreur qui s'est produite dans un objet table.</span><span class="sxs-lookup"><span data-stu-id="a53b6-105">Returns information about the last error that occurred in a table object.</span></span>
  
```cpp
HRESULT GetLastError( 
  HRESULT hResult, 
  ULONG ulFlags, 
  LPMAPIERROR FAR * lppMAPIError 
); 
```

## <a name="parameters"></a><span data-ttu-id="a53b6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a53b6-106">Parameters</span></span>

 <span data-ttu-id="a53b6-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="a53b6-107">_hResult_</span></span>
  
> <span data-ttu-id="a53b6-108">dans Valeur renvoyée par la méthode qui a échoué.</span><span class="sxs-lookup"><span data-stu-id="a53b6-108">[in] The return value from the method that failed.</span></span>
    
 <span data-ttu-id="a53b6-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a53b6-109">_ulFlags_</span></span>
  
> <span data-ttu-id="a53b6-110">dans Non utilisé, défini sur 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="a53b6-110">[in] Not used, set to 0 (zero).</span></span>
    
 <span data-ttu-id="a53b6-111">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="a53b6-111">_lppMAPIError_</span></span>
  
> <span data-ttu-id="a53b6-112">remarquer Pointe vers une structure [MAPIERROR](mapierror.md) MAPI qui contient des informations sur la dernière erreur survenue pour un objet table.</span><span class="sxs-lookup"><span data-stu-id="a53b6-112">[out] Points to a MAPI [MAPIERROR](mapierror.md) structure that contains information about the last error that occurred for a table object.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="a53b6-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a53b6-113">See also</span></span>



[<span data-ttu-id="a53b6-114">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a53b6-114">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)
  
[<span data-ttu-id="a53b6-115">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="a53b6-115">MAPIERROR</span></span>](mapierror.md)


[<span data-ttu-id="a53b6-116">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="a53b6-116">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

