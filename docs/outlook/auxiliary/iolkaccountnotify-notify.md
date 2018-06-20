---
title: IOlkAccountNotifyNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: dbce1c47-1252-ddeb-64ae-d52118e6821f
description: Notifie le client des modifications apportées au compte spécifié.
ms.openlocfilehash: ea4cab8cb8571cf5f34637c08935c78c657e5503
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782735"
---
# <a name="iolkaccountnotifynotify"></a><span data-ttu-id="1a4f4-103">IOlkAccountNotify::Notify</span><span class="sxs-lookup"><span data-stu-id="1a4f4-103">IOlkAccountNotify::Notify</span></span>

<span data-ttu-id="1a4f4-104">Notifie le client des modifications apportées au compte spécifié.</span><span class="sxs-lookup"><span data-stu-id="1a4f4-104">Notifies the client of changes to the specified account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="1a4f4-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="1a4f4-105">Quick info</span></span>

<span data-ttu-id="1a4f4-106">Voir [IOlkAccountNotify](iolkaccountnotify.md).</span><span class="sxs-lookup"><span data-stu-id="1a4f4-106">See [IOlkAccountNotify](iolkaccountnotify.md).</span></span>
  
```cpp
HRESULT IOlkAccount::Notify(  
    DWORD dwNotify, 
    DWORD dwAcctID, 
    DWORD dwFlags 
);

```

## <a name="parameters"></a><span data-ttu-id="1a4f4-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1a4f4-107">Parameters</span></span>

<span data-ttu-id="1a4f4-108">_dwNotify_</span><span class="sxs-lookup"><span data-stu-id="1a4f4-108">_dwNotify_</span></span>
  
> <span data-ttu-id="1a4f4-109">[in] Le type de notification.</span><span class="sxs-lookup"><span data-stu-id="1a4f4-109">[in] The type of notification.</span></span> <span data-ttu-id="1a4f4-110">La valeur doit être une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="1a4f4-110">The value must be one of the following:</span></span>
    
   - <span data-ttu-id="1a4f4-111">NOTIFY_ACCT_CHANGED</span><span class="sxs-lookup"><span data-stu-id="1a4f4-111">NOTIFY_ACCT_CHANGED</span></span> 
    
   - <span data-ttu-id="1a4f4-112">NOTIFY_ACCT_CREATED</span><span class="sxs-lookup"><span data-stu-id="1a4f4-112">NOTIFY_ACCT_CREATED</span></span> 
    
   - <span data-ttu-id="1a4f4-113">NOTIFY_ACCT_DELETED</span><span class="sxs-lookup"><span data-stu-id="1a4f4-113">NOTIFY_ACCT_DELETED</span></span>
    
   - <span data-ttu-id="1a4f4-114">NOTIFY_ACCT_ORDER_CHANGED</span><span class="sxs-lookup"><span data-stu-id="1a4f4-114">NOTIFY_ACCT_ORDER_CHANGED</span></span> 
    
   - <span data-ttu-id="1a4f4-115">NOTIFY_ACCT_PREDELETED</span><span class="sxs-lookup"><span data-stu-id="1a4f4-115">NOTIFY_ACCT_PREDELETED</span></span> 
    
 <span data-ttu-id="1a4f4-116">_dwAcctID_</span><span class="sxs-lookup"><span data-stu-id="1a4f4-116">_dwAcctID_</span></span>
  
> <span data-ttu-id="1a4f4-117">[in] L’ID de compte du compte qui a été créé, modifié, supprimé ou préalable supprimé.</span><span class="sxs-lookup"><span data-stu-id="1a4f4-117">[in] The account ID of the account that has been created, changed, deleted, or pre-deleted.</span></span>
    
 <span data-ttu-id="1a4f4-118">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="1a4f4-118">_dwFlags_</span></span>
  
>  <span data-ttu-id="1a4f4-119">[in] Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="1a4f4-119">[in] Not used.</span></span> <span data-ttu-id="1a4f4-120">OLK_ACCOUNT_NO_FLAGS est la seule valeur pris en charge.</span><span class="sxs-lookup"><span data-stu-id="1a4f4-120">OLK_ACCOUNT_NO_FLAGS is the only supported value.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="1a4f4-121">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="1a4f4-121">Return values</span></span>

<span data-ttu-id="1a4f4-122">S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.</span><span class="sxs-lookup"><span data-stu-id="1a4f4-122">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1a4f4-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1a4f4-123">See also</span></span>

- [<span data-ttu-id="1a4f4-124">Constantes (API de gestion des comptes)</span><span class="sxs-lookup"><span data-stu-id="1a4f4-124">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="1a4f4-125">IOlkAccountManager</span><span class="sxs-lookup"><span data-stu-id="1a4f4-125">IOlkAccountManager</span></span>](iolkaccountmanager.md)

