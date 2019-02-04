---
title: IOlkAccountManagerInit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0e5ffb61-1469-bc91-f237-27d1156179cd
description: Initialise le Gestionnaire de comptes à utiliser.
ms.openlocfilehash: 5a643a4636251afc98750be8acf47cd3bdab3847
ms.sourcegitcommit: b361919ae2d3ac000d9fcaa3030713df7062ecd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/02/2019
ms.locfileid: "29715339"
---
# <a name="iolkaccountmanagerinit"></a><span data-ttu-id="657f6-103">IOlkAccountManager::Init</span><span class="sxs-lookup"><span data-stu-id="657f6-103">IOlkAccountManager::Init</span></span>

<span data-ttu-id="657f6-104">Initialise le Gestionnaire de comptes à utiliser.</span><span class="sxs-lookup"><span data-stu-id="657f6-104">Initializes the account manager for use.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="657f6-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="657f6-105">Quick info</span></span>

<span data-ttu-id="657f6-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="657f6-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::Init (  
    IOlkAccountHelper *pAcctHelper, 
    DWORD dwFlags 
);

```

## <a name="parameters"></a><span data-ttu-id="657f6-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="657f6-107">Parameters</span></span>

<span data-ttu-id="657f6-108">_pAcctHelper_</span><span class="sxs-lookup"><span data-stu-id="657f6-108">_pAcctHelper_</span></span>
  
> <span data-ttu-id="657f6-109">[in] Interface [IOlkAccountHelper](iolkaccounthelper.md) qui fournit des fonctionnalités d’assistance de compte.</span><span class="sxs-lookup"><span data-stu-id="657f6-109">[in] An [IOlkAccountHelper](iolkaccounthelper.md) interface that provides account helper functionality.</span></span> 
    
<span data-ttu-id="657f6-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="657f6-110">_dwFlags_</span></span>
  
> <span data-ttu-id="657f6-111">[in] Indicateurs pour modifier le comportement.</span><span class="sxs-lookup"><span data-stu-id="657f6-111">[in] Flags to modify behavior.</span></span>
    
   - <span data-ttu-id="657f6-112">**ACCT_INIT_NO_STORES_CHECK** — empêche une synchronisation avec un magasin associé à un compte (par exemple, un compte IMAP).</span><span class="sxs-lookup"><span data-stu-id="657f6-112">**ACCT_INIT_NO_STORES_CHECK** —Prevents an account (such as an IMAP account) from synchronizing with an associated store.</span></span> 
    
   - <span data-ttu-id="657f6-113">**ACCT_INIT_NOSYNCH_MAPI_ACCTS** — services MAPI empêche de la synchronisation avec des comptes.</span><span class="sxs-lookup"><span data-stu-id="657f6-113">**ACCT_INIT_NOSYNCH_MAPI_ACCTS** —Prevents MAPI services from synchronizing with accounts.</span></span> 
   
   - <span data-ttu-id="657f6-114">**ACCT_INIT_NO_NOTIFICATIONS** — empêche le Gestionnaire de comptes d’intercepter les messages de diffusion destinées aux autres applications.</span><span class="sxs-lookup"><span data-stu-id="657f6-114">**ACCT_INIT_NO_NOTIFICATIONS** —Prevents the Account Manager from intercepting broadcast messages intended for other applications.</span></span> 
   
   - <span data-ttu-id="657f6-115">**OLK_ACCOUNT_NO_FLAGS** — services MAPI se synchronise avec les comptes.</span><span class="sxs-lookup"><span data-stu-id="657f6-115">**OLK_ACCOUNT_NO_FLAGS** —Synchronizes MAPI services with accounts.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="657f6-116">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="657f6-116">Return values</span></span>

|<span data-ttu-id="657f6-117">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="657f6-117">**HRESULT**</span></span>|<span data-ttu-id="657f6-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="657f6-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="657f6-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="657f6-119">S_OK</span></span>  <br/> |<span data-ttu-id="657f6-120">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="657f6-120">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="657f6-121">E_OLK_ALREADY_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="657f6-121">E_OLK_ALREADY_INITIALIZED</span></span>  <br/> |<span data-ttu-id="657f6-122">**Init** a déjà été appelée.</span><span class="sxs-lookup"><span data-stu-id="657f6-122">**Init** has already been called.</span></span>  <br/> |
|<span data-ttu-id="657f6-123">E_OLK_REGISTRY</span><span class="sxs-lookup"><span data-stu-id="657f6-123">E_OLK_REGISTRY</span></span>  <br/> |<span data-ttu-id="657f6-124">Le Gestionnaire de comptes n’a pas pu accéder les paramètres de Registre nécessaires.</span><span class="sxs-lookup"><span data-stu-id="657f6-124">The account manager could not access the required registry settings.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="657f6-125">Remarques</span><span class="sxs-lookup"><span data-stu-id="657f6-125">Remarks</span></span>

<span data-ttu-id="657f6-126">Le client doit appeler **IOlkAccountManager::Init** pour initialiser le compte responsable avant d’utiliser le Gestionnaire de comptes pour accéder aux comptes ou configurer des notifications.</span><span class="sxs-lookup"><span data-stu-id="657f6-126">The client must call **IOlkAccountManager::Init** to initialize the account manager before using the account manager to access accounts or set up notifications.</span></span> <span data-ttu-id="657f6-127">Étant donné que Outlook synchronise automatiquement les services MAPI avec des comptes au démarrage, utilisez **ACCT_INIT_NOSYNCH_MAPI_ACCTS** sauf s’il existe une cause spécifique à synchroniser.</span><span class="sxs-lookup"><span data-stu-id="657f6-127">Because Outlook automatically synchronizes MAPI services with accounts on startup, use **ACCT_INIT_NOSYNCH_MAPI_ACCTS** unless there is a specific cause to synchronize.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="657f6-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="657f6-128">See also</span></span>

- [<span data-ttu-id="657f6-129">Constantes (API de gestion des comptes)</span><span class="sxs-lookup"><span data-stu-id="657f6-129">Constants (Account management API)</span></span>](constants-account-management-api.md)

