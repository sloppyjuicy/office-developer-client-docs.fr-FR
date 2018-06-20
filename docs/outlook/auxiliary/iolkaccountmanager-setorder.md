---
title: IOlkAccountManagerSetOrder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e219adf6-e591-72e6-b9bd-2fc62eb5142d
description: Modifie l’ordre de la catégorie spécifiée de comptes.
ms.openlocfilehash: fcb27404471c9b551320027b0ed6979926ad3d58
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782718"
---
# <a name="iolkaccountmanagersetorder"></a><span data-ttu-id="13051-103">IOlkAccountManager::SetOrder</span><span class="sxs-lookup"><span data-stu-id="13051-103">IOlkAccountManager::SetOrder</span></span>

<span data-ttu-id="13051-104">Modifie l’ordre de la catégorie spécifiée de comptes.</span><span class="sxs-lookup"><span data-stu-id="13051-104">Modifies the ordering of the specified category of accounts.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="13051-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="13051-105">Quick info</span></span>

<span data-ttu-id="13051-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="13051-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT SetOrder(
    const CLSID * pclsidCategory,
    DWORD cAccts,
    DWORD rgAccts[]
);

```

## <a name="parameters"></a><span data-ttu-id="13051-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="13051-107">Parameters</span></span>

<span data-ttu-id="13051-108">_pclsidCategory_</span><span class="sxs-lookup"><span data-stu-id="13051-108">_pclsidCategory_</span></span>
  
> <span data-ttu-id="13051-109">[in] L’identificateur de classe de catégorie pour laquelle définir l’ordre.</span><span class="sxs-lookup"><span data-stu-id="13051-109">[in] The category class ID for which to set the order.</span></span> <span data-ttu-id="13051-110">La valeur doit être une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="13051-110">The value must be one of the following:</span></span>
    
   - <span data-ttu-id="13051-111">CLSID_OlkAddressBook</span><span class="sxs-lookup"><span data-stu-id="13051-111">CLSID_OlkAddressBook</span></span>
    
   - <span data-ttu-id="13051-112">CLSID_OlkStore</span><span class="sxs-lookup"><span data-stu-id="13051-112">CLSID_OlkStore</span></span>
    
<span data-ttu-id="13051-113">_cAccts_</span><span class="sxs-lookup"><span data-stu-id="13051-113">_cAccts_</span></span>
  
> <span data-ttu-id="13051-114">[in] Le nombre de comptes.</span><span class="sxs-lookup"><span data-stu-id="13051-114">[in] The number of accounts.</span></span>
    
<span data-ttu-id="13051-115">_rgAccts_</span><span class="sxs-lookup"><span data-stu-id="13051-115">_rgAccts_</span></span>
  
> <span data-ttu-id="13051-116">[in] Tableau des ID de compte.</span><span class="sxs-lookup"><span data-stu-id="13051-116">[in] An array of account IDs.</span></span> <span data-ttu-id="13051-117">La taille du tableau est _cAccts_.</span><span class="sxs-lookup"><span data-stu-id="13051-117">The size of the array is  _cAccts_.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="13051-118">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="13051-118">Return values</span></span>

|<span data-ttu-id="13051-119">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="13051-119">**HRESULT**</span></span>|<span data-ttu-id="13051-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="13051-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="13051-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="13051-121">S_OK</span></span>  <br/> |<span data-ttu-id="13051-122">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="13051-122">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="13051-123">E_ACCT_WRONG_SORT_ORDER</span><span class="sxs-lookup"><span data-stu-id="13051-123">E_ACCT_WRONG_SORT_ORDER</span></span>  <br/> |<span data-ttu-id="13051-124">Le nouvel ordre de tri a un nombre différent de comptes à l’ancien ordre de tri.</span><span class="sxs-lookup"><span data-stu-id="13051-124">The new sort order has a different number of accounts than the old sort order.</span></span>  <br/> |
|<span data-ttu-id="13051-125">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="13051-125">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="13051-126">Un ou plusieurs arguments ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="13051-126">One or more arguments are invalid.</span></span>  <br/> |
|<span data-ttu-id="13051-127">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="13051-127">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="13051-128">Le Gestionnaire de comptes n'a pas été initialisé pour une utilisation.</span><span class="sxs-lookup"><span data-stu-id="13051-128">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="13051-129">Remarques</span><span class="sxs-lookup"><span data-stu-id="13051-129">Remarks</span></span>

<span data-ttu-id="13051-130">L’appelant alloue de la mémoire pour le pointeur de tableau _prgAccts_ , ainsi que pour le tableau qui pointe _prgAccts_ .</span><span class="sxs-lookup"><span data-stu-id="13051-130">The caller allocates memory for the array pointer  _prgAccts_ as well as for the array at which  _prgAccts_ points.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="13051-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="13051-131">See also</span></span>

- [<span data-ttu-id="13051-132">Constantes (API de gestion des comptes)</span><span class="sxs-lookup"><span data-stu-id="13051-132">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="13051-133">IOlkAccountManager::GetOrder</span><span class="sxs-lookup"><span data-stu-id="13051-133">IOlkAccountManager::GetOrder</span></span>](iolkaccountmanager-getorder.md)

