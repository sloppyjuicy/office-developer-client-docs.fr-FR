---
title: IOlkAccountSaveChanges
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8f1ab61e-7d1c-50d5-ae21-8cb4b08d729c
description: Valider les modifications apportées à l’objet de compte en écrivant dans le magasin du Registre.
ms.openlocfilehash: c23cefbbda62de9b7e159e500d95b8db5ff34ef4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425833"
---
# <a name="iolkaccountsavechanges"></a><span data-ttu-id="d4b02-103">IOlkAccount::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="d4b02-103">IOlkAccount::SaveChanges</span></span>

<span data-ttu-id="d4b02-104">Valider les modifications apportées à l’objet de compte en écrivant dans le magasin du Registre.</span><span class="sxs-lookup"><span data-stu-id="d4b02-104">Commits changes to the account object by writing to the registry store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="d4b02-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="d4b02-105">Quick info</span></span>

<span data-ttu-id="d4b02-106">Voir [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="d4b02-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
```cpp
HRESULT IOlkAccount::SaveChanges (  
    DWORD dwFlags 
); 
```

## <a name="parameters"></a><span data-ttu-id="d4b02-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d4b02-107">Parameters</span></span>

<span data-ttu-id="d4b02-108">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="d4b02-108">_dwFlags_</span></span>
  
> <span data-ttu-id="d4b02-109">[in] Indicateurs pour modifier le comportement.</span><span class="sxs-lookup"><span data-stu-id="d4b02-109">[in] Flags to modify behavior.</span></span> <span data-ttu-id="d4b02-110">OLK_ACCOUNT_NO_FLAGS est la seule valeur prise en charge.</span><span class="sxs-lookup"><span data-stu-id="d4b02-110">OLK_ACCOUNT_NO_FLAGS is the only supported value.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="d4b02-111">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="d4b02-111">Return values</span></span>

|<span data-ttu-id="d4b02-112">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="d4b02-112">**HRESULT**</span></span>|<span data-ttu-id="d4b02-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="d4b02-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d4b02-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="d4b02-114">S_OK</span></span>  <br/> |<span data-ttu-id="d4b02-115">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="d4b02-115">The method was successful.</span></span>  <br/> |
|<span data-ttu-id="d4b02-116">E_ACCT_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="d4b02-116">E_ACCT_NOT_FOUND</span></span>  <br/> |<span data-ttu-id="d4b02-117">Impossible de trouver le compte spécifié.</span><span class="sxs-lookup"><span data-stu-id="d4b02-117">Cannot find the specified account.</span></span>  <br/> |
|<span data-ttu-id="d4b02-118">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="d4b02-118">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="d4b02-119">Le Gestionnaire de comptes n'a pas été initialisé pour une utilisation.</span><span class="sxs-lookup"><span data-stu-id="d4b02-119">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d4b02-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="d4b02-120">Remarks</span></span>

<span data-ttu-id="d4b02-121">Après avoir changé la valeur des propriétés du compte à l’aide [d’IOlkAccount::SetProp](iolkaccount-setprop.md), utilisez **IOlkAccount::SaveChanges** pour enregistrer ces modifications.</span><span class="sxs-lookup"><span data-stu-id="d4b02-121">After changing the value of account properties by using [IOlkAccount::SetProp](iolkaccount-setprop.md), use **IOlkAccount::SaveChanges** to save such changes.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d4b02-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d4b02-122">See also</span></span>

- [<span data-ttu-id="d4b02-123">Constantes (API de gestion des comptes)</span><span class="sxs-lookup"><span data-stu-id="d4b02-123">Constants (Account management API)</span></span>](constants-account-management-api.md) 
- [<span data-ttu-id="d4b02-124">IOlkAccountManager::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="d4b02-124">IOlkAccountManager::SaveChanges</span></span>](iolkaccountmanager-savechanges.md)

