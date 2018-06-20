---
title: IOlkAccountSaveChanges
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8f1ab61e-7d1c-50d5-ae21-8cb4b08d729c
description: Valide les modifications de l’objet account en écrivant dans le magasin de Registre.
ms.openlocfilehash: ebff8af8af8a7512b577b36a2c31f76f3297a19d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782660"
---
# <a name="iolkaccountsavechanges"></a><span data-ttu-id="39aeb-103">IOlkAccount::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="39aeb-103">IOlkAccount::SaveChanges</span></span>

<span data-ttu-id="39aeb-104">Valide les modifications de l’objet account en écrivant dans le magasin de Registre.</span><span class="sxs-lookup"><span data-stu-id="39aeb-104">Commits changes to the account object by writing to the registry store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="39aeb-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="39aeb-105">Quick info</span></span>

<span data-ttu-id="39aeb-106">Voir [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="39aeb-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
```cpp
HRESULT IOlkAccount::SaveChanges (  
    DWORD dwFlags 
); 
```

## <a name="parameters"></a><span data-ttu-id="39aeb-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="39aeb-107">Parameters</span></span>

<span data-ttu-id="39aeb-108">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="39aeb-108">_dwFlags_</span></span>
  
> <span data-ttu-id="39aeb-109">[in] Indicateurs pour modifier le comportement.</span><span class="sxs-lookup"><span data-stu-id="39aeb-109">[in] Flags to modify behavior.</span></span> <span data-ttu-id="39aeb-110">OLK_ACCOUNT_NO_FLAGS est la seule valeur pris en charge.</span><span class="sxs-lookup"><span data-stu-id="39aeb-110">OLK_ACCOUNT_NO_FLAGS is the only supported value.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="39aeb-111">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="39aeb-111">Return values</span></span>

|<span data-ttu-id="39aeb-112">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="39aeb-112">**HRESULT**</span></span>|<span data-ttu-id="39aeb-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="39aeb-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="39aeb-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="39aeb-114">S_OK</span></span>  <br/> |<span data-ttu-id="39aeb-115">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="39aeb-115">The method was successful.</span></span>  <br/> |
|<span data-ttu-id="39aeb-116">E_ACCT_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="39aeb-116">E_ACCT_NOT_FOUND</span></span>  <br/> |<span data-ttu-id="39aeb-117">Impossible de trouver le compte spécifié.</span><span class="sxs-lookup"><span data-stu-id="39aeb-117">Cannot find the specified account.</span></span>  <br/> |
|<span data-ttu-id="39aeb-118">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="39aeb-118">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="39aeb-119">Le Gestionnaire de comptes n'a pas été initialisé pour une utilisation.</span><span class="sxs-lookup"><span data-stu-id="39aeb-119">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="39aeb-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="39aeb-120">Remarks</span></span>

<span data-ttu-id="39aeb-121">Après avoir modifié la valeur des propriétés de compte à l’aide de [IOlkAccount::SetProp](iolkaccount-setprop.md), utilisez **IOlkAccount::SaveChanges** pour enregistrer ces modifications.</span><span class="sxs-lookup"><span data-stu-id="39aeb-121">After changing the value of account properties by using [IOlkAccount::SetProp](iolkaccount-setprop.md), use **IOlkAccount::SaveChanges** to save such changes.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="39aeb-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="39aeb-122">See also</span></span>

- [<span data-ttu-id="39aeb-123">Constantes (API de gestion des comptes)</span><span class="sxs-lookup"><span data-stu-id="39aeb-123">Constants (Account management API)</span></span>](constants-account-management-api.md) 
- [<span data-ttu-id="39aeb-124">IOlkAccountManager::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="39aeb-124">IOlkAccountManager::SaveChanges</span></span>](iolkaccountmanager-savechanges.md)

