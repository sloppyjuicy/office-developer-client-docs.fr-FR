---
title: IOlkAccountManagerGetOrder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bd22026c-e4f7-2f25-0ef2-5d9539fd7eee
description: Obtient le classement de la catégorie spécifiée de comptes.
ms.openlocfilehash: d05e354e25d49a51b3d3f8f053c2b39dc37b333f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782722"
---
# <a name="iolkaccountmanagergetorder"></a><span data-ttu-id="d3e8f-103">IOlkAccountManager::GetOrder</span><span class="sxs-lookup"><span data-stu-id="d3e8f-103">IOlkAccountManager::GetOrder</span></span>

<span data-ttu-id="d3e8f-104">Obtient le classement de la catégorie spécifiée de comptes.</span><span class="sxs-lookup"><span data-stu-id="d3e8f-104">Gets the ordering of the specified category of accounts.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="d3e8f-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="d3e8f-105">Quick info</span></span>

<span data-ttu-id="d3e8f-106">Voir [IOlkAccountManager](iolkaccountmanager.md)</span><span class="sxs-lookup"><span data-stu-id="d3e8f-106">See [IOlkAccountManager](iolkaccountmanager.md)</span></span>
  
```cpp
HRESULT IOlkAccountManager::GetOrder (  
    const CLSID *pclsidCategory, 
    DWORD *pcAccts, 
    DWORD *prgAccts[] 
); 
```

## <a name="parameters"></a><span data-ttu-id="d3e8f-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d3e8f-107">Parameters</span></span>

<span data-ttu-id="d3e8f-108">_pclsidCategory_</span><span class="sxs-lookup"><span data-stu-id="d3e8f-108">_pclsidCategory_</span></span>
  
> <span data-ttu-id="d3e8f-109">[in] L’identificateur de classe de catégorie pour laquelle obtenir l’ordre.</span><span class="sxs-lookup"><span data-stu-id="d3e8f-109">[in] The category class ID for which to get the order.</span></span> <span data-ttu-id="d3e8f-110">La valeur doit être une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="d3e8f-110">The value must be one of the following:</span></span>
    
   - <span data-ttu-id="d3e8f-111">CLSID_OlkMail</span><span class="sxs-lookup"><span data-stu-id="d3e8f-111">CLSID_OlkMail</span></span>
    
   - <span data-ttu-id="d3e8f-112">CLSID_OlkAddressBook</span><span class="sxs-lookup"><span data-stu-id="d3e8f-112">CLSID_OlkAddressBook</span></span>
    
   - <span data-ttu-id="d3e8f-113">CLSID_OlkStore</span><span class="sxs-lookup"><span data-stu-id="d3e8f-113">CLSID_OlkStore</span></span>
    
<span data-ttu-id="d3e8f-114">_pcAccts_</span><span class="sxs-lookup"><span data-stu-id="d3e8f-114">_pcAccts_</span></span>
  
>  <span data-ttu-id="d3e8f-115">[out] Le nombre de comptes.</span><span class="sxs-lookup"><span data-stu-id="d3e8f-115">[out] The number of accounts.</span></span> 
    
<span data-ttu-id="d3e8f-116">_prgAccts_</span><span class="sxs-lookup"><span data-stu-id="d3e8f-116">_prgAccts_</span></span>
  
> <span data-ttu-id="d3e8f-117">[out] Pointeur vers un tableau de comptes.</span><span class="sxs-lookup"><span data-stu-id="d3e8f-117">[out] A pointer to an array of accounts.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="d3e8f-118">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="d3e8f-118">Return values</span></span>

|<span data-ttu-id="d3e8f-119">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="d3e8f-119">**HRESULT**</span></span>|<span data-ttu-id="d3e8f-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="d3e8f-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d3e8f-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="d3e8f-121">S_OK</span></span>  <br/> |<span data-ttu-id="d3e8f-122">L’appel a réussi</span><span class="sxs-lookup"><span data-stu-id="d3e8f-122">The call succeeded</span></span>  <br/> |
|<span data-ttu-id="d3e8f-123">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="d3e8f-123">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="d3e8f-124">Un ou plusieurs arguments ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="d3e8f-124">One or more arguments are invalid.</span></span>  <br/> |
|<span data-ttu-id="d3e8f-125">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="d3e8f-125">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="d3e8f-126">Le Gestionnaire de comptes n'a pas été initialisé pour une utilisation.</span><span class="sxs-lookup"><span data-stu-id="d3e8f-126">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d3e8f-127">Remarques</span><span class="sxs-lookup"><span data-stu-id="d3e8f-127">Remarks</span></span>

<span data-ttu-id="d3e8f-128">Avant d’appeler cette méthode, l’appelant alloue uniquement un pointeur tableau *prgAccts* , mais pas de mémoire pour le tableau qui pointe *prgAccts* .</span><span class="sxs-lookup"><span data-stu-id="d3e8f-128">Before calling this method, the caller allocates only an array pointer  *prgAccts*  but no memory for the array at which  *prgAccts*  points.</span></span> <span data-ttu-id="d3e8f-129">Une fois que cette méthode retourne, l’appelant doit utiliser [IOlkAccountManager::FreeMemory](iolkaccountmanager-freememory.md) pour libérer la mémoire allouée à *prgAccts* .</span><span class="sxs-lookup"><span data-stu-id="d3e8f-129">After this method returns, the caller must use [IOlkAccountManager::FreeMemory](iolkaccountmanager-freememory.md) to release the memory allocated for  *prgAccts*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d3e8f-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d3e8f-130">See also</span></span>

- [<span data-ttu-id="d3e8f-131">Constantes (API de gestion des comptes)</span><span class="sxs-lookup"><span data-stu-id="d3e8f-131">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="d3e8f-132">IOlkAccountManager::SetOrder</span><span class="sxs-lookup"><span data-stu-id="d3e8f-132">IOlkAccountManager::SetOrder</span></span>](iolkaccountmanager-setorder.md)

