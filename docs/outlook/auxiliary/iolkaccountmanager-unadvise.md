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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430986"
---
# <a name="iolkaccountmanagerunadvise"></a><span data-ttu-id="d71e2-103">IOlkAccountManager::Unadvise</span><span class="sxs-lookup"><span data-stu-id="d71e2-103">IOlkAccountManager::Unadvise</span></span>

<span data-ttu-id="d71e2-104">Annule l'inscription d'un client avec le gestionnaire de comptes pour les notifications pour tous les comptes.</span><span class="sxs-lookup"><span data-stu-id="d71e2-104">Unregisters a client with the account manager for notifications for all accounts.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="d71e2-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="d71e2-105">Quick info</span></span>

<span data-ttu-id="d71e2-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="d71e2-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT Unadvise(
    DWORD dwCookie
);

```

## <a name="parameters"></a><span data-ttu-id="d71e2-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d71e2-107">Parameters</span></span>

<span data-ttu-id="d71e2-108">_dwCookie_</span><span class="sxs-lookup"><span data-stu-id="d71e2-108">_dwCookie_</span></span>
  
> <span data-ttu-id="d71e2-109">dans Cookie renvoyé par [IOlkAccountManager:: Advise](iolkaccountmanager-advise.md).</span><span class="sxs-lookup"><span data-stu-id="d71e2-109">[in] The cookie returned by [IOlkAccountManager::Advise](iolkaccountmanager-advise.md).</span></span>
    
## <a name="return-values"></a><span data-ttu-id="d71e2-110">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="d71e2-110">Return values</span></span>

|<span data-ttu-id="d71e2-111">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="d71e2-111">**HRESULT**</span></span>|<span data-ttu-id="d71e2-112">**Description**</span><span class="sxs-lookup"><span data-stu-id="d71e2-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d71e2-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="d71e2-113">S_OK</span></span>  <br/> |<span data-ttu-id="d71e2-114">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="d71e2-114">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="d71e2-115">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="d71e2-115">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="d71e2-116">Un ou plusieurs arguments ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="d71e2-116">One or more arguments are invalid.</span></span>  <br/> |
|<span data-ttu-id="d71e2-117">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="d71e2-117">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="d71e2-118">Le Gestionnaire de comptes n'a pas été initialisé pour une utilisation.</span><span class="sxs-lookup"><span data-stu-id="d71e2-118">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d71e2-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d71e2-119">See also</span></span>

- [<span data-ttu-id="d71e2-120">Constantes (API de gestion des comptes)</span><span class="sxs-lookup"><span data-stu-id="d71e2-120">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="d71e2-121">IOlkAccountManager::Advise</span><span class="sxs-lookup"><span data-stu-id="d71e2-121">IOlkAccountManager::Advise</span></span>](iolkaccountmanager-advise.md)

