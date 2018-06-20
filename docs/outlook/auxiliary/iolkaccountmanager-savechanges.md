---
title: IOlkAccountManagerSaveChanges
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 32a5d4b7-ead7-24e7-58f2-750232263a0d
description: Enregistre les modifications apportées au compte spécifié.
ms.openlocfilehash: 87b513659b632e88697fb63d1aeccccb77ed9fd1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782730"
---
# <a name="iolkaccountmanagersavechanges"></a><span data-ttu-id="f902d-103">IOlkAccountManager::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="f902d-103">IOlkAccountManager::SaveChanges</span></span>

<span data-ttu-id="f902d-104">Enregistre les modifications apportées au compte spécifié.</span><span class="sxs-lookup"><span data-stu-id="f902d-104">Saves changes to the specified account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="f902d-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="f902d-105">Quick info</span></span>

<span data-ttu-id="f902d-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="f902d-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::SaveChanges (  
    DWORD dwAcctID, 
    DWORD dwFlags 
); 
```

## <a name="parameters"></a><span data-ttu-id="f902d-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f902d-107">Parameters</span></span>

<span data-ttu-id="f902d-108">_dwAcctID_</span><span class="sxs-lookup"><span data-stu-id="f902d-108">_dwAcctID_</span></span>
  
> <span data-ttu-id="f902d-109">[in] L’ID de compte à enregistrer.</span><span class="sxs-lookup"><span data-stu-id="f902d-109">[in] The account ID to save.</span></span> 
    
<span data-ttu-id="f902d-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="f902d-110">_dwFlags_</span></span>
  
> <span data-ttu-id="f902d-111">[in] Indicateurs pour modifier le comportement.</span><span class="sxs-lookup"><span data-stu-id="f902d-111">[in] Flags to modify behavior.</span></span> <span data-ttu-id="f902d-112">OLK_ACCOUNT_NO_FLAGS est la seule valeur pris en charge.</span><span class="sxs-lookup"><span data-stu-id="f902d-112">OLK_ACCOUNT_NO_FLAGS is the only supported value.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="f902d-113">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="f902d-113">Return values</span></span>

|<span data-ttu-id="f902d-114">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="f902d-114">**HRESULT**</span></span>|<span data-ttu-id="f902d-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="f902d-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f902d-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="f902d-116">S_OK</span></span>  <br/> |<span data-ttu-id="f902d-117">L’appel a réussi</span><span class="sxs-lookup"><span data-stu-id="f902d-117">The call succeeded</span></span>  <br/> |
|<span data-ttu-id="f902d-118">E_ACCT_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="f902d-118">E_ACCT_NOT_FOUND</span></span>  <br/> |<span data-ttu-id="f902d-119">Le compte spécifié est introuvable.</span><span class="sxs-lookup"><span data-stu-id="f902d-119">The specified account cannot be found.</span></span>  <br/> |
|<span data-ttu-id="f902d-120">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="f902d-120">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="f902d-121">Le Gestionnaire de comptes n'a pas été initialisé pour une utilisation.</span><span class="sxs-lookup"><span data-stu-id="f902d-121">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f902d-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="f902d-122">Remarks</span></span>

<span data-ttu-id="f902d-123">Après avoir modifié la valeur des propriétés de compte à l’aide de [IOlkAccount::SetProp](iolkaccount-setprop.md), utilisez **IOlkAccountManager::SaveChanges** ou [IOlkAccount::SaveChanges](iolkaccount-savechanges.md) pour enregistrer ces modifications.</span><span class="sxs-lookup"><span data-stu-id="f902d-123">After changing the value of account properties by using [IOlkAccount::SetProp](iolkaccount-setprop.md), use **IOlkAccountManager::SaveChanges** or [IOlkAccount::SaveChanges](iolkaccount-savechanges.md) to save such changes.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f902d-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f902d-124">See also</span></span>

- [<span data-ttu-id="f902d-125">Constantes (API de gestion des comptes)</span><span class="sxs-lookup"><span data-stu-id="f902d-125">Constants (Account management API)</span></span>](constants-account-management-api.md) 
- [<span data-ttu-id="f902d-126">IOlkAccount::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="f902d-126">IOlkAccount::SaveChanges</span></span>](iolkaccount-savechanges.md)

