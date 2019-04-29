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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431700"
---
# <a name="iolkerrorunknowngetlasterror"></a><span data-ttu-id="8ea5e-103">IOlkErrorUnknown::GetLastError</span><span class="sxs-lookup"><span data-stu-id="8ea5e-103">IOlkErrorUnknown::GetLastError</span></span>

<span data-ttu-id="8ea5e-104">Obtient une chaîne de message pour l'erreur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="8ea5e-104">Gets a message string for the specified error.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="8ea5e-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="8ea5e-105">Quick info</span></span>

<span data-ttu-id="8ea5e-106">Voir [IOlkErrorUnknown](iolkerrorunknown.md).</span><span class="sxs-lookup"><span data-stu-id="8ea5e-106">See [IOlkErrorUnknown](iolkerrorunknown.md).</span></span>
  
```cpp
HRESULT IOlkErrorUnknown::GetLastError(  
    HRESULT hr, 
    LPWSTR *ppwszError 
); 

```

## <a name="parameters"></a><span data-ttu-id="8ea5e-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8ea5e-107">Parameters</span></span>

<span data-ttu-id="8ea5e-108">_confidentiel_</span><span class="sxs-lookup"><span data-stu-id="8ea5e-108">_hr_</span></span>
  
> <span data-ttu-id="8ea5e-109">dans Code d'erreur à rechercher.</span><span class="sxs-lookup"><span data-stu-id="8ea5e-109">[in] The error code to look up.</span></span>
    
<span data-ttu-id="8ea5e-110">_ppwszError_</span><span class="sxs-lookup"><span data-stu-id="8ea5e-110">_ppwszError_</span></span>
  
> <span data-ttu-id="8ea5e-111">remarquer Message d'erreur correspondant à *RH* .</span><span class="sxs-lookup"><span data-stu-id="8ea5e-111">[out] The error message that corresponds to  *hr*  .</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="8ea5e-112">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="8ea5e-112">Return values</span></span>

|<span data-ttu-id="8ea5e-113">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="8ea5e-113">**HRESULT**</span></span>|<span data-ttu-id="8ea5e-114">**Description**</span><span class="sxs-lookup"><span data-stu-id="8ea5e-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8ea5e-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="8ea5e-115">S_OK</span></span>  <br/> |<span data-ttu-id="8ea5e-116">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="8ea5e-116">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="8ea5e-117">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="8ea5e-117">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="8ea5e-118">Un ou plusieurs arguments ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="8ea5e-118">One or more arguments are invalid.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8ea5e-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8ea5e-119">See also</span></span>

- [<span data-ttu-id="8ea5e-120">Constantes (API de gestion des comptes)</span><span class="sxs-lookup"><span data-stu-id="8ea5e-120">Constants (Account management API)</span></span>](constants-account-management-api.md)

