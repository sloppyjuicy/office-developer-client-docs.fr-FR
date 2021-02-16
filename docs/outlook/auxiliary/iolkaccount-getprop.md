---
title: IOlkAccountGetProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5725eb52-3a78-897d-f9e3-c5a494fb78c0
description: Obtient la valeur de la propriété de compte spécifiée.
ms.openlocfilehash: d24df8cfa9d54bee4614c1f31e12268748b8c986
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433737"
---
# <a name="iolkaccountgetprop"></a><span data-ttu-id="dbb6b-103">IOlkAccount::GetProp</span><span class="sxs-lookup"><span data-stu-id="dbb6b-103">IOlkAccount::GetProp</span></span>

<span data-ttu-id="dbb6b-104">Obtient la valeur de la propriété de compte spécifiée.</span><span class="sxs-lookup"><span data-stu-id="dbb6b-104">Gets the value of the specified account property.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="dbb6b-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="dbb6b-105">Quick info</span></span>

<span data-ttu-id="dbb6b-106">Voir [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="dbb6b-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
```cpp
HRESULT IOlkAccount::GetProp(  
DWORD dwProp, 
ACCT_VARIANT *pVar 
);
```

## <a name="parameters"></a><span data-ttu-id="dbb6b-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dbb6b-107">Parameters</span></span>

<span data-ttu-id="dbb6b-108">_dwProp_</span><span class="sxs-lookup"><span data-stu-id="dbb6b-108">_dwProp_</span></span>
  
> <span data-ttu-id="dbb6b-109">[in] Balise de propriété de la propriété de compte à obtenir.</span><span class="sxs-lookup"><span data-stu-id="dbb6b-109">[in] The property tag of the account property to get.</span></span>
    
<span data-ttu-id="dbb6b-110">_pVar_</span><span class="sxs-lookup"><span data-stu-id="dbb6b-110">_pVar_</span></span>
  
> <span data-ttu-id="dbb6b-111">[out] Valeur de la propriété spécifiée.</span><span class="sxs-lookup"><span data-stu-id="dbb6b-111">[out] The value of the specified property.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="dbb6b-112">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="dbb6b-112">Return values</span></span>

|<span data-ttu-id="dbb6b-113">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="dbb6b-113">**HRESULT**</span></span>|<span data-ttu-id="dbb6b-114">**Description**</span><span class="sxs-lookup"><span data-stu-id="dbb6b-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="dbb6b-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="dbb6b-115">S_OK</span></span>  <br/> |<span data-ttu-id="dbb6b-116">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="dbb6b-116">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="dbb6b-117">E_ACCT_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="dbb6b-117">E_ACCT_NOT_FOUND</span></span>  <br/> |<span data-ttu-id="dbb6b-118">La propriété n’est pas trouvée pour le compte donné.</span><span class="sxs-lookup"><span data-stu-id="dbb6b-118">The property is not found for the given account.</span></span>  <br/> |
|<span data-ttu-id="dbb6b-119">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="dbb6b-119">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="dbb6b-120">Une balise de propriété non valide a été spécifiée.</span><span class="sxs-lookup"><span data-stu-id="dbb6b-120">An invalid property tag has been specified.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dbb6b-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="dbb6b-121">Remarks</span></span>

<span data-ttu-id="dbb6b-122">Après le retour de cette méthode, si la valeur de la propriété de compte est binaire ou de type chaîne, vous devez libérer  *pVar*  à l’aide de [IOlkAccount::FreeMemory](iolkaccount-freememory.md).</span><span class="sxs-lookup"><span data-stu-id="dbb6b-122">After this method returns, if the value of the account property is a binary or string type, you must free  *pVar*  by using [IOlkAccount::FreeMemory](iolkaccount-freememory.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="dbb6b-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dbb6b-123">See also</span></span>

- [<span data-ttu-id="dbb6b-124">Constantes (API de gestion des comptes)</span><span class="sxs-lookup"><span data-stu-id="dbb6b-124">Constants (Account management API)</span></span>](constants-account-management-api.md) 
- [<span data-ttu-id="dbb6b-125">IOlkAccount::FreeMemory</span><span class="sxs-lookup"><span data-stu-id="dbb6b-125">IOlkAccount::FreeMemory</span></span>](iolkaccount-freememory.md)  
- [<span data-ttu-id="dbb6b-126">IOlkAccount::SetProp</span><span class="sxs-lookup"><span data-stu-id="dbb6b-126">IOlkAccount::SetProp</span></span>](iolkaccount-setprop.md)

