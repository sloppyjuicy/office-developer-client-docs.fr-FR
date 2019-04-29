---
title: IOlkAccountManagerDeleteAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: df210364-fe20-8e33-a455-9902f04ec739
description: Supprime le compte spécifié.
ms.openlocfilehash: 3e39b7b9af57f64dd124e1bf836db68664709b8c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431238"
---
# <a name="iolkaccountmanagerdeleteaccount"></a><span data-ttu-id="0c54e-103">IOlkAccountManager::DeleteAccount</span><span class="sxs-lookup"><span data-stu-id="0c54e-103">IOlkAccountManager::DeleteAccount</span></span>

<span data-ttu-id="0c54e-104">Supprime le compte spécifié.</span><span class="sxs-lookup"><span data-stu-id="0c54e-104">Deletes the specified account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="0c54e-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="0c54e-105">Quick info</span></span>

<span data-ttu-id="0c54e-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="0c54e-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::DeleteAccount (  
    DWORD dwAcctID, 
);
```

## <a name="parameters"></a><span data-ttu-id="0c54e-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0c54e-107">Parameters</span></span>

<span data-ttu-id="0c54e-108">_dwAcctID_</span><span class="sxs-lookup"><span data-stu-id="0c54e-108">_dwAcctID_</span></span>
  
> <span data-ttu-id="0c54e-109">dans ID du compte à supprimer.</span><span class="sxs-lookup"><span data-stu-id="0c54e-109">[in] The account ID of the account to be deleted.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="0c54e-110">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="0c54e-110">Return values</span></span>

|<span data-ttu-id="0c54e-111">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="0c54e-111">**HRESULT**</span></span>|<span data-ttu-id="0c54e-112">**Description**</span><span class="sxs-lookup"><span data-stu-id="0c54e-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0c54e-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="0c54e-113">S_OK</span></span>  <br/> |<span data-ttu-id="0c54e-114">L'appel a réussi</span><span class="sxs-lookup"><span data-stu-id="0c54e-114">The call succeeded</span></span>  <br/> |
|<span data-ttu-id="0c54e-115">E_ACCT_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="0c54e-115">E_ACCT_NOT_FOUND</span></span>  <br/> |<span data-ttu-id="0c54e-116">Le compte spécifié est introuvable.</span><span class="sxs-lookup"><span data-stu-id="0c54e-116">The specified account cannot be found.</span></span>  <br/> |
|<span data-ttu-id="0c54e-117">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="0c54e-117">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="0c54e-118">Le Gestionnaire de comptes n'a pas été initialisé pour une utilisation.</span><span class="sxs-lookup"><span data-stu-id="0c54e-118">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0c54e-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c54e-119">See also</span></span>

- [<span data-ttu-id="0c54e-120">Constantes (API de gestion des comptes)</span><span class="sxs-lookup"><span data-stu-id="0c54e-120">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="0c54e-121">IOlkAccountManager::FindAccount</span><span class="sxs-lookup"><span data-stu-id="0c54e-121">IOlkAccountManager::FindAccount</span></span>](iolkaccountmanager-findaccount.md)

