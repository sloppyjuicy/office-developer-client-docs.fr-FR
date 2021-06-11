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
# <a name="iolkaccountmanagerdeleteaccount"></a><span data-ttu-id="3845c-103">IOlkAccountManager::DeleteAccount</span><span class="sxs-lookup"><span data-stu-id="3845c-103">IOlkAccountManager::DeleteAccount</span></span>

<span data-ttu-id="3845c-104">Supprime le compte spécifié.</span><span class="sxs-lookup"><span data-stu-id="3845c-104">Deletes the specified account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="3845c-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="3845c-105">Quick info</span></span>

<span data-ttu-id="3845c-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="3845c-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::DeleteAccount (  
    DWORD dwAcctID, 
);
```

## <a name="parameters"></a><span data-ttu-id="3845c-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="3845c-107">Parameters</span></span>

<span data-ttu-id="3845c-108">_dwAcctID_</span><span class="sxs-lookup"><span data-stu-id="3845c-108">_dwAcctID_</span></span>
  
> <span data-ttu-id="3845c-109">[in] ID de compte du compte à supprimer.</span><span class="sxs-lookup"><span data-stu-id="3845c-109">[in] The account ID of the account to be deleted.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="3845c-110">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="3845c-110">Return values</span></span>

|<span data-ttu-id="3845c-111">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="3845c-111">**HRESULT**</span></span>|<span data-ttu-id="3845c-112">**Description**</span><span class="sxs-lookup"><span data-stu-id="3845c-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3845c-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="3845c-113">S_OK</span></span>  <br/> |<span data-ttu-id="3845c-114">L’appel a réussi</span><span class="sxs-lookup"><span data-stu-id="3845c-114">The call succeeded</span></span>  <br/> |
|<span data-ttu-id="3845c-115">E_ACCT_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="3845c-115">E_ACCT_NOT_FOUND</span></span>  <br/> |<span data-ttu-id="3845c-116">Le compte spécifié est in trouver.</span><span class="sxs-lookup"><span data-stu-id="3845c-116">The specified account cannot be found.</span></span>  <br/> |
|<span data-ttu-id="3845c-117">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="3845c-117">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="3845c-118">Le Gestionnaire de comptes n'a pas été initialisé pour une utilisation.</span><span class="sxs-lookup"><span data-stu-id="3845c-118">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3845c-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3845c-119">See also</span></span>

- [<span data-ttu-id="3845c-120">Constantes (API de gestion des comptes)</span><span class="sxs-lookup"><span data-stu-id="3845c-120">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="3845c-121">IOlkAccountManager::FindAccount</span><span class="sxs-lookup"><span data-stu-id="3845c-121">IOlkAccountManager::FindAccount</span></span>](iolkaccountmanager-findaccount.md)

