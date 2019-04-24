---
title: IOlkAccountManagerUnadvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea5cbf9f-25cc-9cca-9be0-d2deed576153
description: Annule l'inscription d'un client avec le gestionnaire de comptes pour les notifications pour tous les comptes.
ms.openlocfilehash: 0b954413b06cb1aa1b6fc4e0e9666f108bf81fbe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322007"
---
# <a name="iolkaccountmanagerunadvise"></a><span data-ttu-id="7fd0d-103">IOlkAccountManager::Unadvise</span><span class="sxs-lookup"><span data-stu-id="7fd0d-103">IOlkAccountManager::Unadvise</span></span>

<span data-ttu-id="7fd0d-104">Annule l'inscription d'un client avec le gestionnaire de comptes pour les notifications pour tous les comptes.</span><span class="sxs-lookup"><span data-stu-id="7fd0d-104">Unregisters a client with the account manager for notifications for all accounts.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="7fd0d-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="7fd0d-105">Quick info</span></span>

<span data-ttu-id="7fd0d-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="7fd0d-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT Unadvise(
    DWORD dwCookie
);

```

## <a name="parameters"></a><span data-ttu-id="7fd0d-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7fd0d-107">Parameters</span></span>

<span data-ttu-id="7fd0d-108">_dwCookie_</span><span class="sxs-lookup"><span data-stu-id="7fd0d-108">_dwCookie_</span></span>
  
> <span data-ttu-id="7fd0d-109">dans Cookie renvoyé par [IOlkAccountManager:: Advise](iolkaccountmanager-advise.md).</span><span class="sxs-lookup"><span data-stu-id="7fd0d-109">[in] The cookie returned by [IOlkAccountManager::Advise](iolkaccountmanager-advise.md).</span></span>
    
## <a name="return-values"></a><span data-ttu-id="7fd0d-110">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="7fd0d-110">Return values</span></span>

|<span data-ttu-id="7fd0d-111">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="7fd0d-111">**HRESULT**</span></span>|<span data-ttu-id="7fd0d-112">**Description**</span><span class="sxs-lookup"><span data-stu-id="7fd0d-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7fd0d-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="7fd0d-113">S_OK</span></span>  <br/> |<span data-ttu-id="7fd0d-114">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="7fd0d-114">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="7fd0d-115">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="7fd0d-115">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="7fd0d-116">Un ou plusieurs arguments ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="7fd0d-116">One or more arguments are invalid.</span></span>  <br/> |
|<span data-ttu-id="7fd0d-117">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="7fd0d-117">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="7fd0d-118">Le Gestionnaire de comptes n'a pas été initialisé pour une utilisation.</span><span class="sxs-lookup"><span data-stu-id="7fd0d-118">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7fd0d-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7fd0d-119">See also</span></span>

- [<span data-ttu-id="7fd0d-120">Constantes (API de gestion des comptes)</span><span class="sxs-lookup"><span data-stu-id="7fd0d-120">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="7fd0d-121">IOlkAccountManager::Advise</span><span class="sxs-lookup"><span data-stu-id="7fd0d-121">IOlkAccountManager::Advise</span></span>](iolkaccountmanager-advise.md)

