---
title: IOlkAccountManagerGetOrder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bd22026c-e4f7-2f25-0ef2-5d9539fd7eee
description: Obtient le classement de la catégorie de comptes spécifiée.
ms.openlocfilehash: 3eb6dd96caa43f81eba86a389c938ef90c9533b2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424622"
---
# <a name="iolkaccountmanagergetorder"></a><span data-ttu-id="08b4c-103">IOlkAccountManager::GetOrder</span><span class="sxs-lookup"><span data-stu-id="08b4c-103">IOlkAccountManager::GetOrder</span></span>

<span data-ttu-id="08b4c-104">Obtient le classement de la catégorie de comptes spécifiée.</span><span class="sxs-lookup"><span data-stu-id="08b4c-104">Gets the ordering of the specified category of accounts.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="08b4c-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="08b4c-105">Quick info</span></span>

<span data-ttu-id="08b4c-106">Voir [IOlkAccountManager](iolkaccountmanager.md)</span><span class="sxs-lookup"><span data-stu-id="08b4c-106">See [IOlkAccountManager](iolkaccountmanager.md)</span></span>
  
```cpp
HRESULT IOlkAccountManager::GetOrder (  
    const CLSID *pclsidCategory, 
    DWORD *pcAccts, 
    DWORD *prgAccts[] 
); 
```

## <a name="parameters"></a><span data-ttu-id="08b4c-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="08b4c-107">Parameters</span></span>

<span data-ttu-id="08b4c-108">_pclsidCategory_</span><span class="sxs-lookup"><span data-stu-id="08b4c-108">_pclsidCategory_</span></span>
  
> <span data-ttu-id="08b4c-109">[in] ID de classe de catégorie pour lequel obtenir la commande.</span><span class="sxs-lookup"><span data-stu-id="08b4c-109">[in] The category class ID for which to get the order.</span></span> <span data-ttu-id="08b4c-110">La valeur doit être une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="08b4c-110">The value must be one of the following:</span></span>
    
   - <span data-ttu-id="08b4c-111">CLSID_OlkMail</span><span class="sxs-lookup"><span data-stu-id="08b4c-111">CLSID_OlkMail</span></span>
    
   - <span data-ttu-id="08b4c-112">CLSID_OlkAddressBook</span><span class="sxs-lookup"><span data-stu-id="08b4c-112">CLSID_OlkAddressBook</span></span>
    
   - <span data-ttu-id="08b4c-113">CLSID_OlkStore</span><span class="sxs-lookup"><span data-stu-id="08b4c-113">CLSID_OlkStore</span></span>
    
<span data-ttu-id="08b4c-114">_pcAccts_</span><span class="sxs-lookup"><span data-stu-id="08b4c-114">_pcAccts_</span></span>
  
>  <span data-ttu-id="08b4c-115">[out] Nombre de comptes.</span><span class="sxs-lookup"><span data-stu-id="08b4c-115">[out] The number of accounts.</span></span> 
    
<span data-ttu-id="08b4c-116">_prgAccts_</span><span class="sxs-lookup"><span data-stu-id="08b4c-116">_prgAccts_</span></span>
  
> <span data-ttu-id="08b4c-117">[out] Pointeur vers un tableau de comptes.</span><span class="sxs-lookup"><span data-stu-id="08b4c-117">[out] A pointer to an array of accounts.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="08b4c-118">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="08b4c-118">Return values</span></span>

|<span data-ttu-id="08b4c-119">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="08b4c-119">**HRESULT**</span></span>|<span data-ttu-id="08b4c-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="08b4c-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="08b4c-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="08b4c-121">S_OK</span></span>  <br/> |<span data-ttu-id="08b4c-122">L’appel a réussi</span><span class="sxs-lookup"><span data-stu-id="08b4c-122">The call succeeded</span></span>  <br/> |
|<span data-ttu-id="08b4c-123">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="08b4c-123">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="08b4c-124">Un ou plusieurs arguments ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="08b4c-124">One or more arguments are invalid.</span></span>  <br/> |
|<span data-ttu-id="08b4c-125">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="08b4c-125">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="08b4c-126">Le Gestionnaire de comptes n'a pas été initialisé pour une utilisation.</span><span class="sxs-lookup"><span data-stu-id="08b4c-126">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="08b4c-127">Remarques</span><span class="sxs-lookup"><span data-stu-id="08b4c-127">Remarks</span></span>

<span data-ttu-id="08b4c-128">Avant d’appeler cette méthode, l’appelant alloue uniquement un pointeur de tableau  *prgAccts,*  mais pas de mémoire pour le tableau auquel  *prgAccts*  pointe.</span><span class="sxs-lookup"><span data-stu-id="08b4c-128">Before calling this method, the caller allocates only an array pointer  *prgAccts*  but no memory for the array at which  *prgAccts*  points.</span></span> <span data-ttu-id="08b4c-129">Après le retour de cette méthode, l’appelant doit utiliser [IOlkAccountManager::FreeMemory](iolkaccountmanager-freememory.md) pour libérer la mémoire allouée pour  *prgAccts*  .</span><span class="sxs-lookup"><span data-stu-id="08b4c-129">After this method returns, the caller must use [IOlkAccountManager::FreeMemory](iolkaccountmanager-freememory.md) to release the memory allocated for  *prgAccts*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="08b4c-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="08b4c-130">See also</span></span>

- [<span data-ttu-id="08b4c-131">Constantes (API de gestion des comptes)</span><span class="sxs-lookup"><span data-stu-id="08b4c-131">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="08b4c-132">IOlkAccountManager::SetOrder</span><span class="sxs-lookup"><span data-stu-id="08b4c-132">IOlkAccountManager::SetOrder</span></span>](iolkaccountmanager-setorder.md)

