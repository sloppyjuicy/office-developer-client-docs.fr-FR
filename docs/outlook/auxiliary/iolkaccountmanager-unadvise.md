---
title: IOlkAccountManagerUnadvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea5cbf9f-25cc-9cca-9be0-d2deed576153
description: Désinsère un client auprès du gestionnaire de comptes pour les notifications pour tous les comptes.
ms.openlocfilehash: 0b954413b06cb1aa1b6fc4e0e9666f108bf81fbe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430986"
---
# <a name="iolkaccountmanagerunadvise"></a><span data-ttu-id="ee8da-103">IOlkAccountManager::Unadvise</span><span class="sxs-lookup"><span data-stu-id="ee8da-103">IOlkAccountManager::Unadvise</span></span>

<span data-ttu-id="ee8da-104">Désinsère un client auprès du gestionnaire de comptes pour les notifications pour tous les comptes.</span><span class="sxs-lookup"><span data-stu-id="ee8da-104">Unregisters a client with the account manager for notifications for all accounts.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="ee8da-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="ee8da-105">Quick info</span></span>

<span data-ttu-id="ee8da-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="ee8da-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT Unadvise(
    DWORD dwCookie
);

```

## <a name="parameters"></a><span data-ttu-id="ee8da-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ee8da-107">Parameters</span></span>

<span data-ttu-id="ee8da-108">_dwCookie_</span><span class="sxs-lookup"><span data-stu-id="ee8da-108">_dwCookie_</span></span>
  
> <span data-ttu-id="ee8da-109">[in] Cookie renvoyé par [IOlkAccountManager::Advise](iolkaccountmanager-advise.md).</span><span class="sxs-lookup"><span data-stu-id="ee8da-109">[in] The cookie returned by [IOlkAccountManager::Advise](iolkaccountmanager-advise.md).</span></span>
    
## <a name="return-values"></a><span data-ttu-id="ee8da-110">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="ee8da-110">Return values</span></span>

|<span data-ttu-id="ee8da-111">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="ee8da-111">**HRESULT**</span></span>|<span data-ttu-id="ee8da-112">**Description**</span><span class="sxs-lookup"><span data-stu-id="ee8da-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ee8da-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="ee8da-113">S_OK</span></span>  <br/> |<span data-ttu-id="ee8da-114">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="ee8da-114">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="ee8da-115">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="ee8da-115">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="ee8da-116">Un ou plusieurs arguments ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="ee8da-116">One or more arguments are invalid.</span></span>  <br/> |
|<span data-ttu-id="ee8da-117">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="ee8da-117">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="ee8da-118">Le Gestionnaire de comptes n'a pas été initialisé pour une utilisation.</span><span class="sxs-lookup"><span data-stu-id="ee8da-118">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ee8da-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ee8da-119">See also</span></span>

- [<span data-ttu-id="ee8da-120">Constantes (API de gestion des comptes)</span><span class="sxs-lookup"><span data-stu-id="ee8da-120">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="ee8da-121">IOlkAccountManager::Advise</span><span class="sxs-lookup"><span data-stu-id="ee8da-121">IOlkAccountManager::Advise</span></span>](iolkaccountmanager-advise.md)

