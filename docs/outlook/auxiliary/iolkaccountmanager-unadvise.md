---
title: IOlkAccountManagerUnadvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea5cbf9f-25cc-9cca-9be0-d2deed576153
description: Annule l’inscription d’un client avec le Gestionnaire de comptes pour les notifications pour tous les comptes.
ms.openlocfilehash: 0632bc6bd98e218cf323262ea480b020185438f3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782724"
---
# <a name="iolkaccountmanagerunadvise"></a><span data-ttu-id="da391-103">IOlkAccountManager::Unadvise</span><span class="sxs-lookup"><span data-stu-id="da391-103">IOlkAccountManager::Unadvise</span></span>

<span data-ttu-id="da391-104">Annule l’inscription d’un client avec le Gestionnaire de comptes pour les notifications pour tous les comptes.</span><span class="sxs-lookup"><span data-stu-id="da391-104">Unregisters a client with the account manager for notifications for all accounts.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="da391-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="da391-105">Quick info</span></span>

<span data-ttu-id="da391-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="da391-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT Unadvise(
    DWORD dwCookie
);

```

## <a name="parameters"></a><span data-ttu-id="da391-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="da391-107">Parameters</span></span>

<span data-ttu-id="da391-108">_dwCookie_</span><span class="sxs-lookup"><span data-stu-id="da391-108">_dwCookie_</span></span>
  
> <span data-ttu-id="da391-109">[in] Le cookie retourné par [IOlkAccountManager::Advise](iolkaccountmanager-advise.md).</span><span class="sxs-lookup"><span data-stu-id="da391-109">[in] The cookie returned by [IOlkAccountManager::Advise](iolkaccountmanager-advise.md).</span></span>
    
## <a name="return-values"></a><span data-ttu-id="da391-110">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="da391-110">Return values</span></span>

|<span data-ttu-id="da391-111">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="da391-111">**HRESULT**</span></span>|<span data-ttu-id="da391-112">**Description**</span><span class="sxs-lookup"><span data-stu-id="da391-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="da391-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="da391-113">S_OK</span></span>  <br/> |<span data-ttu-id="da391-114">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="da391-114">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="da391-115">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="da391-115">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="da391-116">Un ou plusieurs arguments ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="da391-116">One or more arguments are invalid.</span></span>  <br/> |
|<span data-ttu-id="da391-117">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="da391-117">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="da391-118">Le Gestionnaire de comptes n'a pas été initialisé pour une utilisation.</span><span class="sxs-lookup"><span data-stu-id="da391-118">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="da391-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="da391-119">See also</span></span>

- [<span data-ttu-id="da391-120">Constantes (API de gestion des comptes)</span><span class="sxs-lookup"><span data-stu-id="da391-120">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="da391-121">IOlkAccountManager::Advise</span><span class="sxs-lookup"><span data-stu-id="da391-121">IOlkAccountManager::Advise</span></span>](iolkaccountmanager-advise.md)

