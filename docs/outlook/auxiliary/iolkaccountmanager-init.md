---
title: IOlkAccountManagerInit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0e5ffb61-1469-bc91-f237-27d1156179cd
description: Initialise le Gestionnaire de comptes à utiliser.
ms.openlocfilehash: 621c6a73ab2bcbdff17b87ce15af8b4e0c2e1e24
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782712"
---
# <a name="iolkaccountmanagerinit"></a><span data-ttu-id="64523-103">IOlkAccountManager::Init</span><span class="sxs-lookup"><span data-stu-id="64523-103">IOlkAccountManager::Init</span></span>

<span data-ttu-id="64523-104">Initialise le Gestionnaire de comptes à utiliser.</span><span class="sxs-lookup"><span data-stu-id="64523-104">Initializes the account manager for use.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="64523-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="64523-105">Quick info</span></span>

<span data-ttu-id="64523-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="64523-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::Init (  
    IOlkAccountHelper *pAcctHelper, 
    DWORD dwFlags 
);

```

## <a name="parameters"></a><span data-ttu-id="64523-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="64523-107">Parameters</span></span>

<span data-ttu-id="64523-108">_pAcctHelper_</span><span class="sxs-lookup"><span data-stu-id="64523-108">_pAcctHelper_</span></span>
  
> <span data-ttu-id="64523-109">[in] Interface [IOlkAccountHelper](iolkaccounthelper.md) qui fournit des fonctionnalités d’assistance de compte.</span><span class="sxs-lookup"><span data-stu-id="64523-109">[in] An [IOlkAccountHelper](iolkaccounthelper.md) interface that provides account helper functionality.</span></span> 
    
<span data-ttu-id="64523-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="64523-110">_dwFlags_</span></span>
  
> <span data-ttu-id="64523-111">[in] Indicateurs pour modifier le comportement.</span><span class="sxs-lookup"><span data-stu-id="64523-111">[in] Flags to modify behavior.</span></span>
    
   - <span data-ttu-id="64523-112">**ACCT_INIT_NO_STORES_CHECK** — empêche une synchronisation avec un magasin associé à un compte (par exemple, un compte IMAP).</span><span class="sxs-lookup"><span data-stu-id="64523-112">**ACCT_INIT_NO_STORES_CHECK** —Prevents an account (such as an IMAP account) from synchronizing with an associated store.</span></span> 
    
   - <span data-ttu-id="64523-113">**ACCT_INIT_NOSYNCH_MAPI_ACCTS** — services MAPI empêche de la synchronisation avec des comptes.</span><span class="sxs-lookup"><span data-stu-id="64523-113">**ACCT_INIT_NOSYNCH_MAPI_ACCTS** —Prevents MAPI services from synchronizing with accounts.</span></span> 
    
   - <span data-ttu-id="64523-114">**OLK_ACCOUNT_NO_FLAGS** — services MAPI se synchronise avec les comptes.</span><span class="sxs-lookup"><span data-stu-id="64523-114">**OLK_ACCOUNT_NO_FLAGS** —Synchronizes MAPI services with accounts.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="64523-115">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="64523-115">Return values</span></span>

|<span data-ttu-id="64523-116">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="64523-116">**HRESULT**</span></span>|<span data-ttu-id="64523-117">**Description**</span><span class="sxs-lookup"><span data-stu-id="64523-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="64523-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="64523-118">S_OK</span></span>  <br/> |<span data-ttu-id="64523-119">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="64523-119">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="64523-120">E_OLK_ALREADY_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="64523-120">E_OLK_ALREADY_INITIALIZED</span></span>  <br/> |<span data-ttu-id="64523-121">**Init** a déjà été appelée.</span><span class="sxs-lookup"><span data-stu-id="64523-121">**Init** has already been called.</span></span>  <br/> |
|<span data-ttu-id="64523-122">E_OLK_REGISTRY</span><span class="sxs-lookup"><span data-stu-id="64523-122">E_OLK_REGISTRY</span></span>  <br/> |<span data-ttu-id="64523-123">Le Gestionnaire de comptes n’a pas pu accéder les paramètres de Registre nécessaires.</span><span class="sxs-lookup"><span data-stu-id="64523-123">The account manager could not access the required registry settings.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="64523-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="64523-124">Remarks</span></span>

<span data-ttu-id="64523-125">Le client doit appeler **IOlkAccountManager::Init** pour initialiser le compte responsable avant d’utiliser le Gestionnaire de comptes pour accéder aux comptes ou configurer des notifications.</span><span class="sxs-lookup"><span data-stu-id="64523-125">The client must call **IOlkAccountManager::Init** to initialize the account manager before using the account manager to access accounts or set up notifications.</span></span> <span data-ttu-id="64523-126">Étant donné que Outlook synchronise automatiquement les services MAPI avec des comptes au démarrage, utilisez **ACCT_INIT_NOSYNCH_MAPI_ACCTS** sauf s’il existe une cause spécifique à synchroniser.</span><span class="sxs-lookup"><span data-stu-id="64523-126">Because Outlook automatically synchronizes MAPI services with accounts on startup, use **ACCT_INIT_NOSYNCH_MAPI_ACCTS** unless there is a specific cause to synchronize.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="64523-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="64523-127">See also</span></span>

- [<span data-ttu-id="64523-128">Constantes (API de gestion des comptes)</span><span class="sxs-lookup"><span data-stu-id="64523-128">Constants (Account management API)</span></span>](constants-account-management-api.md)

