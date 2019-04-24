---
title: IOlkAccountSaveChanges
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8f1ab61e-7d1c-50d5-ae21-8cb4b08d729c
description: Valide les modifications apportées à l'objet Account en écrivant dans le magasin de registre.
ms.openlocfilehash: c23cefbbda62de9b7e159e500d95b8db5ff34ef4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322259"
---
# <a name="iolkaccountsavechanges"></a><span data-ttu-id="4e74e-103">IOlkAccount::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="4e74e-103">IOlkAccount::SaveChanges</span></span>

<span data-ttu-id="4e74e-104">Valide les modifications apportées à l'objet Account en écrivant dans le magasin de registre.</span><span class="sxs-lookup"><span data-stu-id="4e74e-104">Commits changes to the account object by writing to the registry store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="4e74e-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="4e74e-105">Quick info</span></span>

<span data-ttu-id="4e74e-106">Voir [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="4e74e-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
```cpp
HRESULT IOlkAccount::SaveChanges (  
    DWORD dwFlags 
); 
```

## <a name="parameters"></a><span data-ttu-id="4e74e-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4e74e-107">Parameters</span></span>

<span data-ttu-id="4e74e-108">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="4e74e-108">_dwFlags_</span></span>
  
> <span data-ttu-id="4e74e-109">[in] Indicateurs pour modifier le comportement.</span><span class="sxs-lookup"><span data-stu-id="4e74e-109">[in] Flags to modify behavior.</span></span> <span data-ttu-id="4e74e-110">OLK_ACCOUNT_NO_FLAGS est la seule valeur prise en charge.</span><span class="sxs-lookup"><span data-stu-id="4e74e-110">OLK_ACCOUNT_NO_FLAGS is the only supported value.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="4e74e-111">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="4e74e-111">Return values</span></span>

|<span data-ttu-id="4e74e-112">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="4e74e-112">**HRESULT**</span></span>|<span data-ttu-id="4e74e-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="4e74e-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4e74e-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="4e74e-114">S_OK</span></span>  <br/> |<span data-ttu-id="4e74e-115">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="4e74e-115">The method was successful.</span></span>  <br/> |
|<span data-ttu-id="4e74e-116">E_ACCT_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="4e74e-116">E_ACCT_NOT_FOUND</span></span>  <br/> |<span data-ttu-id="4e74e-117">Le compte spécifié est introuvable.</span><span class="sxs-lookup"><span data-stu-id="4e74e-117">Cannot find the specified account.</span></span>  <br/> |
|<span data-ttu-id="4e74e-118">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="4e74e-118">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="4e74e-119">Le Gestionnaire de comptes n'a pas été initialisé pour une utilisation.</span><span class="sxs-lookup"><span data-stu-id="4e74e-119">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4e74e-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="4e74e-120">Remarks</span></span>

<span data-ttu-id="4e74e-121">Après avoir modifié la valeur des propriétés de compte à l'aide de [IOlkAccount:: SetProp](iolkaccount-setprop.md), utilisez **IOlkAccount:: SaveChanges** pour enregistrer ces modifications.</span><span class="sxs-lookup"><span data-stu-id="4e74e-121">After changing the value of account properties by using [IOlkAccount::SetProp](iolkaccount-setprop.md), use **IOlkAccount::SaveChanges** to save such changes.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4e74e-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4e74e-122">See also</span></span>

- [<span data-ttu-id="4e74e-123">Constantes (API de gestion des comptes)</span><span class="sxs-lookup"><span data-stu-id="4e74e-123">Constants (Account management API)</span></span>](constants-account-management-api.md) 
- [<span data-ttu-id="4e74e-124">IOlkAccountManager::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="4e74e-124">IOlkAccountManager::SaveChanges</span></span>](iolkaccountmanager-savechanges.md)

