---
title: IOlkErrorUnknownGetLastError
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f332de3-470d-9bc2-0c65-684bb58bcd7a
description: Obtient une chaîne de message pour l'erreur spécifiée.
ms.openlocfilehash: 4d2aa3a7513687484988921734eb4c0e6f91226b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321881"
---
# <a name="iolkerrorunknowngetlasterror"></a><span data-ttu-id="1461b-103">IOlkErrorUnknown::GetLastError</span><span class="sxs-lookup"><span data-stu-id="1461b-103">IOlkErrorUnknown::GetLastError</span></span>

<span data-ttu-id="1461b-104">Obtient une chaîne de message pour l'erreur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="1461b-104">Gets a message string for the specified error.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="1461b-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="1461b-105">Quick info</span></span>

<span data-ttu-id="1461b-106">Voir [IOlkErrorUnknown](iolkerrorunknown.md).</span><span class="sxs-lookup"><span data-stu-id="1461b-106">See [IOlkErrorUnknown](iolkerrorunknown.md).</span></span>
  
```cpp
HRESULT IOlkErrorUnknown::GetLastError(  
    HRESULT hr, 
    LPWSTR *ppwszError 
); 

```

## <a name="parameters"></a><span data-ttu-id="1461b-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1461b-107">Parameters</span></span>

<span data-ttu-id="1461b-108">_hr_</span><span class="sxs-lookup"><span data-stu-id="1461b-108">_hr_</span></span>
  
> <span data-ttu-id="1461b-109">dans Code d'erreur à rechercher.</span><span class="sxs-lookup"><span data-stu-id="1461b-109">[in] The error code to look up.</span></span>
    
<span data-ttu-id="1461b-110">_ppwszError_</span><span class="sxs-lookup"><span data-stu-id="1461b-110">_ppwszError_</span></span>
  
> <span data-ttu-id="1461b-111">remarquer Message d'erreur correspondant à *RH* .</span><span class="sxs-lookup"><span data-stu-id="1461b-111">[out] The error message that corresponds to  *hr*  .</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="1461b-112">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="1461b-112">Return values</span></span>

|<span data-ttu-id="1461b-113">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="1461b-113">**HRESULT**</span></span>|<span data-ttu-id="1461b-114">**Description**</span><span class="sxs-lookup"><span data-stu-id="1461b-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1461b-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="1461b-115">S_OK</span></span>  <br/> |<span data-ttu-id="1461b-116">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="1461b-116">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="1461b-117">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="1461b-117">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="1461b-118">Un ou plusieurs arguments ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="1461b-118">One or more arguments are invalid.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1461b-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1461b-119">See also</span></span>

- [<span data-ttu-id="1461b-120">Constantes (API de gestion des comptes)</span><span class="sxs-lookup"><span data-stu-id="1461b-120">Constants (Account management API)</span></span>](constants-account-management-api.md)

