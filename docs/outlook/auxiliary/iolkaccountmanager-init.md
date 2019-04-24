---
title: IOlkAccountManagerInit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0e5ffb61-1469-bc91-f237-27d1156179cd
description: Initialise le gestionnaire de comptes en vue de son utilisation.
ms.openlocfilehash: 5a643a4636251afc98750be8acf47cd3bdab3847
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322035"
---
# <a name="iolkaccountmanagerinit"></a><span data-ttu-id="b1960-103">IOlkAccountManager::Init</span><span class="sxs-lookup"><span data-stu-id="b1960-103">IOlkAccountManager::Init</span></span>

<span data-ttu-id="b1960-104">Initialise le gestionnaire de comptes en vue de son utilisation.</span><span class="sxs-lookup"><span data-stu-id="b1960-104">Initializes the account manager for use.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="b1960-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="b1960-105">Quick info</span></span>

<span data-ttu-id="b1960-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="b1960-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::Init (  
    IOlkAccountHelper *pAcctHelper, 
    DWORD dwFlags 
);

```

## <a name="parameters"></a><span data-ttu-id="b1960-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b1960-107">Parameters</span></span>

<span data-ttu-id="b1960-108">_pAcctHelper_</span><span class="sxs-lookup"><span data-stu-id="b1960-108">_pAcctHelper_</span></span>
  
> <span data-ttu-id="b1960-109">dans Interface [IOlkAccountHelper](iolkaccounthelper.md) qui fournit la fonctionnalité d'assistance de compte.</span><span class="sxs-lookup"><span data-stu-id="b1960-109">[in] An [IOlkAccountHelper](iolkaccounthelper.md) interface that provides account helper functionality.</span></span> 
    
<span data-ttu-id="b1960-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="b1960-110">_dwFlags_</span></span>
  
> <span data-ttu-id="b1960-111">[in] Indicateurs pour modifier le comportement.</span><span class="sxs-lookup"><span data-stu-id="b1960-111">[in] Flags to modify behavior.</span></span>
    
   - <span data-ttu-id="b1960-112">**ACCT_INIT_NO_STORES_CHECK** — empêche un compte (tel qu'un compte IMAP) d'être synchronisé avec un magasin associé.</span><span class="sxs-lookup"><span data-stu-id="b1960-112">**ACCT_INIT_NO_STORES_CHECK** —Prevents an account (such as an IMAP account) from synchronizing with an associated store.</span></span> 
    
   - <span data-ttu-id="b1960-113">**ACCT_INIT_NOSYNCH_MAPI_ACCTS** — empêche les services MAPI de procéder à une synchronisation avec les comptes.</span><span class="sxs-lookup"><span data-stu-id="b1960-113">**ACCT_INIT_NOSYNCH_MAPI_ACCTS** —Prevents MAPI services from synchronizing with accounts.</span></span> 
   
   - <span data-ttu-id="b1960-114">**ACCT_INIT_NO_NOTIFICATIONS** — empêche le gestionnaire de comptes d'intercepter les messages de diffusion destinés à d'autres applications.</span><span class="sxs-lookup"><span data-stu-id="b1960-114">**ACCT_INIT_NO_NOTIFICATIONS** —Prevents the Account Manager from intercepting broadcast messages intended for other applications.</span></span> 
   
   - <span data-ttu-id="b1960-115">**OLK_ACCOUNT_NO_FLAGS** : synchronise les services MAPI avec des comptes.</span><span class="sxs-lookup"><span data-stu-id="b1960-115">**OLK_ACCOUNT_NO_FLAGS** —Synchronizes MAPI services with accounts.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="b1960-116">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="b1960-116">Return values</span></span>

|<span data-ttu-id="b1960-117">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="b1960-117">**HRESULT**</span></span>|<span data-ttu-id="b1960-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="b1960-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b1960-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="b1960-119">S_OK</span></span>  <br/> |<span data-ttu-id="b1960-120">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="b1960-120">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="b1960-121">E_OLK_ALREADY_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="b1960-121">E_OLK_ALREADY_INITIALIZED</span></span>  <br/> |<span data-ttu-id="b1960-122">**Init** a déjà été appelé.</span><span class="sxs-lookup"><span data-stu-id="b1960-122">**Init** has already been called.</span></span>  <br/> |
|<span data-ttu-id="b1960-123">E_OLK_REGISTRY</span><span class="sxs-lookup"><span data-stu-id="b1960-123">E_OLK_REGISTRY</span></span>  <br/> |<span data-ttu-id="b1960-124">Le gestionnaire de comptes n'a pas pu accéder aux paramètres de registre requis.</span><span class="sxs-lookup"><span data-stu-id="b1960-124">The account manager could not access the required registry settings.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b1960-125">Remarques</span><span class="sxs-lookup"><span data-stu-id="b1960-125">Remarks</span></span>

<span data-ttu-id="b1960-126">Le client doit appeler **IOlkAccountManager:: init** pour initialiser le gestionnaire de comptes avant d'utiliser le gestionnaire de comptes pour accéder aux comptes ou configurer des notifications.</span><span class="sxs-lookup"><span data-stu-id="b1960-126">The client must call **IOlkAccountManager::Init** to initialize the account manager before using the account manager to access accounts or set up notifications.</span></span> <span data-ttu-id="b1960-127">Étant donné qu'Outlook synchronise automatiquement les services MAPI avec les comptes au démarrage, utilisez **ACCT_INIT_NOSYNCH_MAPI_ACCTS** à moins qu'il n'y ait une cause spécifique de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="b1960-127">Because Outlook automatically synchronizes MAPI services with accounts on startup, use **ACCT_INIT_NOSYNCH_MAPI_ACCTS** unless there is a specific cause to synchronize.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b1960-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b1960-128">See also</span></span>

- [<span data-ttu-id="b1960-129">Constantes (API de gestion des comptes)</span><span class="sxs-lookup"><span data-stu-id="b1960-129">Constants (Account management API)</span></span>](constants-account-management-api.md)

