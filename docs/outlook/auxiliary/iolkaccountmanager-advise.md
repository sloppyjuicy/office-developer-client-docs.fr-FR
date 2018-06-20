---
title: IOlkAccountManagerAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c88f087e-4ff4-0837-186d-b6e761468a4d
description: Enregistre un client avec le Gestionnaire de comptes pour les notifications relatives à tous les comptes.
ms.openlocfilehash: 1fb697fef44b9ed32888527c3c9e467be69ba4c7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782708"
---
# <a name="iolkaccountmanageradvise"></a><span data-ttu-id="eca55-103">IOlkAccountManager::Advise</span><span class="sxs-lookup"><span data-stu-id="eca55-103">IOlkAccountManager::Advise</span></span>

<span data-ttu-id="eca55-104">Enregistre un client avec le Gestionnaire de comptes pour les notifications relatives à tous les comptes.</span><span class="sxs-lookup"><span data-stu-id="eca55-104">Registers a client with the account manager for notifications regarding all accounts.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="eca55-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="eca55-105">Quick info</span></span>

<span data-ttu-id="eca55-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="eca55-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::Advise (  
    IOlkAccountNotify *pNotify, 
    DWORD *pdwCookie 
);
```

## <a name="parameters"></a><span data-ttu-id="eca55-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eca55-107">Parameters</span></span>

<span data-ttu-id="eca55-108">_pNotify_</span><span class="sxs-lookup"><span data-stu-id="eca55-108">_pNotify_</span></span>
  
> <span data-ttu-id="eca55-109">[in] Interface [IOlkAccountNotify](iolkaccountnotify.md) que le Gestionnaire de comptes utilisera pour envoyer des notifications au client.</span><span class="sxs-lookup"><span data-stu-id="eca55-109">[in] An [IOlkAccountNotify](iolkaccountnotify.md) interface that the account manager will use to send notifications to the client.</span></span> 
    
<span data-ttu-id="eca55-110">_pdwCookie_</span><span class="sxs-lookup"><span data-stu-id="eca55-110">_pdwCookie_</span></span>
  
> <span data-ttu-id="eca55-111">[out] Un cookie [IOlkAccountManager::Unadvise](iolkaccountmanager-unadvise.md) utilisera lors de la suppression de l’inscription pour le compte.</span><span class="sxs-lookup"><span data-stu-id="eca55-111">[out] A cookie that [IOlkAccountManager::Unadvise](iolkaccountmanager-unadvise.md) will use when removing the registration for the account.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="eca55-112">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="eca55-112">Return values</span></span>

|<span data-ttu-id="eca55-113">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="eca55-113">**HRESULT**</span></span>|<span data-ttu-id="eca55-114">**Description**</span><span class="sxs-lookup"><span data-stu-id="eca55-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="eca55-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="eca55-115">S_OK</span></span>  <br/> |<span data-ttu-id="eca55-116">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="eca55-116">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="eca55-117">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="eca55-117">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="eca55-118">Un argument non valide a été fourni.</span><span class="sxs-lookup"><span data-stu-id="eca55-118">An invalid argument has been provided.</span></span>  <br/> |
|<span data-ttu-id="eca55-119">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="eca55-119">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="eca55-120">Le Gestionnaire de comptes n'a pas été initialisé pour une utilisation.</span><span class="sxs-lookup"><span data-stu-id="eca55-120">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="eca55-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eca55-121">See also</span></span>

- [<span data-ttu-id="eca55-122">Constantes (API de gestion des comptes)</span><span class="sxs-lookup"><span data-stu-id="eca55-122">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="eca55-123">IOlkAccountManager::Unadvise</span><span class="sxs-lookup"><span data-stu-id="eca55-123">IOlkAccountManager::Unadvise</span></span>](iolkaccountmanager-unadvise.md)

