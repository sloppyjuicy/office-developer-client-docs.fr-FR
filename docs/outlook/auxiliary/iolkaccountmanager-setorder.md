---
title: IOlkAccountManagerSetOrder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e219adf6-e591-72e6-b9bd-2fc62eb5142d
description: Modifie l'ordre de la catégorie de comptes spécifiée.
ms.openlocfilehash: 29dfe4fd1bda9e323481297167361650c3b3a173
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322042"
---
# <a name="iolkaccountmanagersetorder"></a><span data-ttu-id="bf7dc-103">IOlkAccountManager::SetOrder</span><span class="sxs-lookup"><span data-stu-id="bf7dc-103">IOlkAccountManager::SetOrder</span></span>

<span data-ttu-id="bf7dc-104">Modifie l'ordre de la catégorie de comptes spécifiée.</span><span class="sxs-lookup"><span data-stu-id="bf7dc-104">Modifies the ordering of the specified category of accounts.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="bf7dc-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="bf7dc-105">Quick info</span></span>

<span data-ttu-id="bf7dc-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="bf7dc-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT SetOrder(
    const CLSID * pclsidCategory,
    DWORD cAccts,
    DWORD rgAccts[]
);

```

## <a name="parameters"></a><span data-ttu-id="bf7dc-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bf7dc-107">Parameters</span></span>

<span data-ttu-id="bf7dc-108">_pclsidCategory_</span><span class="sxs-lookup"><span data-stu-id="bf7dc-108">_pclsidCategory_</span></span>
  
> <span data-ttu-id="bf7dc-109">dans ID de classe de catégorie pour lequel définir l'ordre.</span><span class="sxs-lookup"><span data-stu-id="bf7dc-109">[in] The category class ID for which to set the order.</span></span> <span data-ttu-id="bf7dc-110">La valeur doit être l’une des suivantes :</span><span class="sxs-lookup"><span data-stu-id="bf7dc-110">The value must be one of the following:</span></span>
    
   - <span data-ttu-id="bf7dc-111">CLSID_OlkAddressBook</span><span class="sxs-lookup"><span data-stu-id="bf7dc-111">CLSID_OlkAddressBook</span></span>
    
   - <span data-ttu-id="bf7dc-112">CLSID_OlkStore</span><span class="sxs-lookup"><span data-stu-id="bf7dc-112">CLSID_OlkStore</span></span>
    
<span data-ttu-id="bf7dc-113">_cAccts_</span><span class="sxs-lookup"><span data-stu-id="bf7dc-113">_cAccts_</span></span>
  
> <span data-ttu-id="bf7dc-114">dans Nombre de comptes.</span><span class="sxs-lookup"><span data-stu-id="bf7dc-114">[in] The number of accounts.</span></span>
    
<span data-ttu-id="bf7dc-115">_rgAccts_</span><span class="sxs-lookup"><span data-stu-id="bf7dc-115">_rgAccts_</span></span>
  
> <span data-ttu-id="bf7dc-116">dans Tableau d'ID de compte.</span><span class="sxs-lookup"><span data-stu-id="bf7dc-116">[in] An array of account IDs.</span></span> <span data-ttu-id="bf7dc-117">La taille du tableau est _cAccts_.</span><span class="sxs-lookup"><span data-stu-id="bf7dc-117">The size of the array is  _cAccts_.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="bf7dc-118">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="bf7dc-118">Return values</span></span>

|<span data-ttu-id="bf7dc-119">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="bf7dc-119">**HRESULT**</span></span>|<span data-ttu-id="bf7dc-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="bf7dc-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bf7dc-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="bf7dc-121">S_OK</span></span>  <br/> |<span data-ttu-id="bf7dc-122">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="bf7dc-122">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="bf7dc-123">E_ACCT_WRONG_SORT_ORDER</span><span class="sxs-lookup"><span data-stu-id="bf7dc-123">E_ACCT_WRONG_SORT_ORDER</span></span>  <br/> |<span data-ttu-id="bf7dc-124">Le nouvel ordre de tri a un nombre de comptes différent de celui de l'ancien ordre de tri.</span><span class="sxs-lookup"><span data-stu-id="bf7dc-124">The new sort order has a different number of accounts than the old sort order.</span></span>  <br/> |
|<span data-ttu-id="bf7dc-125">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="bf7dc-125">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="bf7dc-126">Un ou plusieurs arguments ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="bf7dc-126">One or more arguments are invalid.</span></span>  <br/> |
|<span data-ttu-id="bf7dc-127">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="bf7dc-127">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="bf7dc-128">Le Gestionnaire de comptes n'a pas été initialisé pour une utilisation.</span><span class="sxs-lookup"><span data-stu-id="bf7dc-128">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bf7dc-129">Remarques</span><span class="sxs-lookup"><span data-stu-id="bf7dc-129">Remarks</span></span>

<span data-ttu-id="bf7dc-130">L'appelant alloue de la mémoire pour le pointeur de tableau _prgAccts_ ainsi que pour le tableau auquel _prgAccts_ pointe.</span><span class="sxs-lookup"><span data-stu-id="bf7dc-130">The caller allocates memory for the array pointer  _prgAccts_ as well as for the array at which  _prgAccts_ points.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bf7dc-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bf7dc-131">See also</span></span>

- [<span data-ttu-id="bf7dc-132">Constantes (API de gestion des comptes)</span><span class="sxs-lookup"><span data-stu-id="bf7dc-132">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="bf7dc-133">IOlkAccountManager::GetOrder</span><span class="sxs-lookup"><span data-stu-id="bf7dc-133">IOlkAccountManager::GetOrder</span></span>](iolkaccountmanager-getorder.md)

