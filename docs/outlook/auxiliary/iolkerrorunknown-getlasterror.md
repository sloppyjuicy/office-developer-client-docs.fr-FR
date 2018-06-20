---
title: IOlkErrorUnknownGetLastError
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f332de3-470d-9bc2-0c65-684bb58bcd7a
description: Obtient une chaîne de message de l’erreur spécifiée.
ms.openlocfilehash: 7b00392cdf65d1d4990f2231769e5126c9ae26dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782743"
---
# <a name="iolkerrorunknowngetlasterror"></a><span data-ttu-id="9478f-103">IOlkErrorUnknown::GetLastError</span><span class="sxs-lookup"><span data-stu-id="9478f-103">IOlkErrorUnknown::GetLastError</span></span>

<span data-ttu-id="9478f-104">Obtient une chaîne de message de l’erreur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="9478f-104">Gets a message string for the specified error.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="9478f-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="9478f-105">Quick info</span></span>

<span data-ttu-id="9478f-106">Voir [IOlkErrorUnknown](iolkerrorunknown.md).</span><span class="sxs-lookup"><span data-stu-id="9478f-106">See [IOlkErrorUnknown](iolkerrorunknown.md).</span></span>
  
```cpp
HRESULT IOlkErrorUnknown::GetLastError(  
    HRESULT hr, 
    LPWSTR *ppwszError 
); 

```

## <a name="parameters"></a><span data-ttu-id="9478f-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9478f-107">Parameters</span></span>

<span data-ttu-id="9478f-108">_ressources humaines_</span><span class="sxs-lookup"><span data-stu-id="9478f-108">_hr_</span></span>
  
> <span data-ttu-id="9478f-109">[in] Le code d’erreur à rechercher.</span><span class="sxs-lookup"><span data-stu-id="9478f-109">[in] The error code to look up.</span></span>
    
<span data-ttu-id="9478f-110">_ppwszError_</span><span class="sxs-lookup"><span data-stu-id="9478f-110">_ppwszError_</span></span>
  
> <span data-ttu-id="9478f-111">[out] Le message d’erreur qui correspond à des *ressources humaines* .</span><span class="sxs-lookup"><span data-stu-id="9478f-111">[out] The error message that corresponds to  *hr*  .</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="9478f-112">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="9478f-112">Return values</span></span>

|<span data-ttu-id="9478f-113">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="9478f-113">**HRESULT**</span></span>|<span data-ttu-id="9478f-114">**Description**</span><span class="sxs-lookup"><span data-stu-id="9478f-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9478f-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="9478f-115">S_OK</span></span>  <br/> |<span data-ttu-id="9478f-116">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="9478f-116">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="9478f-117">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="9478f-117">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="9478f-118">Un ou plusieurs arguments ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="9478f-118">One or more arguments are invalid.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9478f-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9478f-119">See also</span></span>

- [<span data-ttu-id="9478f-120">Constantes (API de gestion des comptes)</span><span class="sxs-lookup"><span data-stu-id="9478f-120">Constants (Account management API)</span></span>](constants-account-management-api.md)

