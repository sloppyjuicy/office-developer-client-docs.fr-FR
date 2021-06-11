---
title: IOlkAccountNotifyNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: dbce1c47-1252-ddeb-64ae-d52118e6821f
description: Avertit le client des modifications apportées au compte spécifié.
ms.openlocfilehash: 269d8a8bd605c9d8a0a4057e87895522d8587ee9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424566"
---
# <a name="iolkaccountnotifynotify"></a><span data-ttu-id="12be8-103">IOlkAccountNotify::Notify</span><span class="sxs-lookup"><span data-stu-id="12be8-103">IOlkAccountNotify::Notify</span></span>

<span data-ttu-id="12be8-104">Avertit le client des modifications apportées au compte spécifié.</span><span class="sxs-lookup"><span data-stu-id="12be8-104">Notifies the client of changes to the specified account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="12be8-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="12be8-105">Quick info</span></span>

<span data-ttu-id="12be8-106">Voir [IOlkAccountNotify](iolkaccountnotify.md).</span><span class="sxs-lookup"><span data-stu-id="12be8-106">See [IOlkAccountNotify](iolkaccountnotify.md).</span></span>
  
```cpp
HRESULT IOlkAccount::Notify(  
    DWORD dwNotify, 
    DWORD dwAcctID, 
    DWORD dwFlags 
);

```

## <a name="parameters"></a><span data-ttu-id="12be8-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="12be8-107">Parameters</span></span>

<span data-ttu-id="12be8-108">_dwNotify_</span><span class="sxs-lookup"><span data-stu-id="12be8-108">_dwNotify_</span></span>
  
> <span data-ttu-id="12be8-109">[in] Type de notification.</span><span class="sxs-lookup"><span data-stu-id="12be8-109">[in] The type of notification.</span></span> <span data-ttu-id="12be8-110">La valeur doit être l’une des suivantes :</span><span class="sxs-lookup"><span data-stu-id="12be8-110">The value must be one of the following:</span></span>
    
   - <span data-ttu-id="12be8-111">NOTIFY_ACCT_CHANGED</span><span class="sxs-lookup"><span data-stu-id="12be8-111">NOTIFY_ACCT_CHANGED</span></span> 
    
   - <span data-ttu-id="12be8-112">NOTIFY_ACCT_CREATED</span><span class="sxs-lookup"><span data-stu-id="12be8-112">NOTIFY_ACCT_CREATED</span></span> 
    
   - <span data-ttu-id="12be8-113">NOTIFY_ACCT_DELETED</span><span class="sxs-lookup"><span data-stu-id="12be8-113">NOTIFY_ACCT_DELETED</span></span>
    
   - <span data-ttu-id="12be8-114">NOTIFY_ACCT_ORDER_CHANGED</span><span class="sxs-lookup"><span data-stu-id="12be8-114">NOTIFY_ACCT_ORDER_CHANGED</span></span> 
    
   - <span data-ttu-id="12be8-115">NOTIFY_ACCT_PREDELETED</span><span class="sxs-lookup"><span data-stu-id="12be8-115">NOTIFY_ACCT_PREDELETED</span></span> 
    
 <span data-ttu-id="12be8-116">_dwAcctID_</span><span class="sxs-lookup"><span data-stu-id="12be8-116">_dwAcctID_</span></span>
  
> <span data-ttu-id="12be8-117">[in] ID de compte du compte qui a été créé, modifié, supprimé ou pré-supprimé.</span><span class="sxs-lookup"><span data-stu-id="12be8-117">[in] The account ID of the account that has been created, changed, deleted, or pre-deleted.</span></span>
    
 <span data-ttu-id="12be8-118">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="12be8-118">_dwFlags_</span></span>
  
>  <span data-ttu-id="12be8-119">[in] Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="12be8-119">[in] Not used.</span></span> <span data-ttu-id="12be8-120">OLK_ACCOUNT_NO_FLAGS est la seule valeur prise en charge.</span><span class="sxs-lookup"><span data-stu-id="12be8-120">OLK_ACCOUNT_NO_FLAGS is the only supported value.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="12be8-121">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="12be8-121">Return values</span></span>

<span data-ttu-id="12be8-122">S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.</span><span class="sxs-lookup"><span data-stu-id="12be8-122">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="12be8-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="12be8-123">See also</span></span>

- [<span data-ttu-id="12be8-124">Constantes (API de gestion des comptes)</span><span class="sxs-lookup"><span data-stu-id="12be8-124">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="12be8-125">IOlkAccountManager</span><span class="sxs-lookup"><span data-stu-id="12be8-125">IOlkAccountManager</span></span>](iolkaccountmanager.md)

