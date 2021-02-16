---
title: IOlkAccountManagerAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c88f087e-4ff4-0837-186d-b6e761468a4d
description: Enregistre un client auprès du gestionnaire de comptes pour les notifications concernant tous les comptes.
ms.openlocfilehash: 5460d55d906d382ce40ecd3fd9277cf370295680
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427709"
---
# <a name="iolkaccountmanageradvise"></a><span data-ttu-id="23f25-103">IOlkAccountManager::Advise</span><span class="sxs-lookup"><span data-stu-id="23f25-103">IOlkAccountManager::Advise</span></span>

<span data-ttu-id="23f25-104">Enregistre un client auprès du gestionnaire de comptes pour les notifications concernant tous les comptes.</span><span class="sxs-lookup"><span data-stu-id="23f25-104">Registers a client with the account manager for notifications regarding all accounts.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="23f25-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="23f25-105">Quick info</span></span>

<span data-ttu-id="23f25-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="23f25-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::Advise (  
    IOlkAccountNotify *pNotify, 
    DWORD *pdwCookie 
);
```

## <a name="parameters"></a><span data-ttu-id="23f25-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="23f25-107">Parameters</span></span>

<span data-ttu-id="23f25-108">_pNotify_</span><span class="sxs-lookup"><span data-stu-id="23f25-108">_pNotify_</span></span>
  
> <span data-ttu-id="23f25-109">[in] Interface [IOlkAccountNotify](iolkaccountnotify.md) que le gestionnaire de comptes utilisera pour envoyer des notifications au client.</span><span class="sxs-lookup"><span data-stu-id="23f25-109">[in] An [IOlkAccountNotify](iolkaccountnotify.md) interface that the account manager will use to send notifications to the client.</span></span> 
    
<span data-ttu-id="23f25-110">_pdwCookie_</span><span class="sxs-lookup"><span data-stu-id="23f25-110">_pdwCookie_</span></span>
  
> <span data-ttu-id="23f25-111">[out] Un cookie que [IOlkAccountManager::Unadvise](iolkaccountmanager-unadvise.md) utilisera lors de la suppression de l’inscription pour le compte.</span><span class="sxs-lookup"><span data-stu-id="23f25-111">[out] A cookie that [IOlkAccountManager::Unadvise](iolkaccountmanager-unadvise.md) will use when removing the registration for the account.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="23f25-112">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="23f25-112">Return values</span></span>

|<span data-ttu-id="23f25-113">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="23f25-113">**HRESULT**</span></span>|<span data-ttu-id="23f25-114">**Description**</span><span class="sxs-lookup"><span data-stu-id="23f25-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="23f25-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="23f25-115">S_OK</span></span>  <br/> |<span data-ttu-id="23f25-116">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="23f25-116">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="23f25-117">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="23f25-117">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="23f25-118">Un argument non valide a été fourni.</span><span class="sxs-lookup"><span data-stu-id="23f25-118">An invalid argument has been provided.</span></span>  <br/> |
|<span data-ttu-id="23f25-119">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="23f25-119">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="23f25-120">Le Gestionnaire de comptes n'a pas été initialisé pour une utilisation.</span><span class="sxs-lookup"><span data-stu-id="23f25-120">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="23f25-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="23f25-121">See also</span></span>

- [<span data-ttu-id="23f25-122">Constantes (API de gestion des comptes)</span><span class="sxs-lookup"><span data-stu-id="23f25-122">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="23f25-123">IOlkAccountManager::Unadvise</span><span class="sxs-lookup"><span data-stu-id="23f25-123">IOlkAccountManager::Unadvise</span></span>](iolkaccountmanager-unadvise.md)

