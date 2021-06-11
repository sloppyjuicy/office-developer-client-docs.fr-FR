---
title: HrOpenABEntryWithResolvedRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ce3a583c-16a9-4268-9476-926d2780eae5
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 2eb643e0002e2159e3197d66e021aba0bb8c126f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429907"
---
# <a name="hropenabentrywithresolvedrow"></a><span data-ttu-id="86450-103">HrOpenABEntryWithResolvedRow</span><span class="sxs-lookup"><span data-stu-id="86450-103">HrOpenABEntryWithResolvedRow</span></span>

  
  
<span data-ttu-id="86450-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="86450-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="86450-105">Effectue la même fonction que [HrOpenABEntryWithExchangeContext,](hropenabentrywithexchangecontext.md) sauf qu’il obtient automatiquement **emsabpUID** de la ligne résolue et ouvre l’entryID . </span><span class="sxs-lookup"><span data-stu-id="86450-105">Performs the same function as [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md) except that it automatically gets the **emsabpUID** from the resolved row and opens the **entryID**.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="86450-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="86450-106">Header file:</span></span>  <br/> |<span data-ttu-id="86450-107">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="86450-107">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="86450-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="86450-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="86450-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="86450-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="86450-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="86450-110">Called by:</span></span>  <br/> |<span data-ttu-id="86450-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="86450-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrOpenABEntryWithResolvedRow(
  LPSRow prwResolved,
  LPADRBOOK pAddrBook,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a><span data-ttu-id="86450-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="86450-112">Parameters</span></span>

 <span data-ttu-id="86450-113">_prwResolved_</span><span class="sxs-lookup"><span data-stu-id="86450-113">_prwResolved_</span></span>
  
> <span data-ttu-id="86450-114">[in] Pointeur vers la ligne résolue qui est utilisée pour obtenir **emsabpUID** et ouvrir **l’entryID**.</span><span class="sxs-lookup"><span data-stu-id="86450-114">[in] A pointer to the resolved row that is used to get the **emsabpUID** and open the **entryID**.</span></span>
    
 <span data-ttu-id="86450-115">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="86450-115">_pAddrBook_</span></span>
  
> <span data-ttu-id="86450-116">[in] Carnet d’adresses utilisé pour ouvrir l’identificateur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="86450-116">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="86450-117">Elle ne peut pas être NULL.</span><span class="sxs-lookup"><span data-stu-id="86450-117">It cannot be NULL.</span></span>
    
 <span data-ttu-id="86450-118">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="86450-118">_cbEntryID_</span></span>
  
> <span data-ttu-id="86450-119">[in] Nombre d’bytes de l’identificateur d’entrée spécifié par _le paramètre lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="86450-119">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="86450-120">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="86450-120">_lpEntryID_</span></span>
  
>  <span data-ttu-id="86450-121">[in] Pointeur vers l’identificateur d’entrée qui représente l’entrée de carnet d’adresses à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="86450-121">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span> 
    
 <span data-ttu-id="86450-122">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="86450-122">_lpInterface_</span></span>
  
> <span data-ttu-id="86450-123">[in] Pointeur vers l’identificateur d’interface (IID) de l’interface utilisée pour accéder à l’entrée ouverte.</span><span class="sxs-lookup"><span data-stu-id="86450-123">[in] A pointer to the interface identifier (IID) of the interface that is used to access the open entry.</span></span> <span data-ttu-id="86450-124">La transmission NULL renvoie l’interface standard de l’objet.</span><span class="sxs-lookup"><span data-stu-id="86450-124">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="86450-125">Pour les utilisateurs de messagerie, l’interface standard [est IMailUser : IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="86450-125">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="86450-126">Pour les listes de distribution, il s’agit de [IDistList : IMAPIContainer](idistlistimapicontainer.md)et pour les conteneurs, il s’agit de [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="86450-126">For distribution lists, it is [IDistList : IMAPIContainer](idistlistimapicontainer.md)and for containers, it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="86450-127">Les appelants peuvent définir  _lpInterface_ sur l’interface standard appropriée ou une interface dans la hiérarchie d’héritage.</span><span class="sxs-lookup"><span data-stu-id="86450-127">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="86450-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="86450-128">_ulFlags_</span></span>
  
> <span data-ttu-id="86450-129">[in] Masque de bits d’indicateurs qui contrôle la façon dont l’entrée est ouverte.</span><span class="sxs-lookup"><span data-stu-id="86450-129">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="86450-130">Les indicateurs suivants peuvent être définies :</span><span class="sxs-lookup"><span data-stu-id="86450-130">The following flags can be set:</span></span>
    
<span data-ttu-id="86450-131">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="86450-131">MAPI_BEST_ACCESS</span></span>
  
> <span data-ttu-id="86450-132">Demande l’ouverture de l’entrée avec le nombre maximal d’autorisations réseau et client autorisées.</span><span class="sxs-lookup"><span data-stu-id="86450-132">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="86450-133">Par exemple, si le client dispose d’autorisations de lecture et d’écriture, le fournisseur de carnet d’adresses tente d’ouvrir l’entrée avec des autorisations de lecture et d’écriture.</span><span class="sxs-lookup"><span data-stu-id="86450-133">For example, if the client has read and write permission, the address book provider attempts to open the entry with read and write permission.</span></span> <span data-ttu-id="86450-134">Le client peut récupérer le niveau d’accès accordé en appelant la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) de l’entrée ouverte et en récupérant la propriété PR_ACCESS_LEVEL (PidTagAccessLevel).</span><span class="sxs-lookup"><span data-stu-id="86450-134">The client can retrieve the access level that was granted by calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method of the open entry and retrieving the PR_ACCESS_LEVEL (PidTagAccessLevel) property.</span></span> 
    
<span data-ttu-id="86450-135">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="86450-135">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="86450-136">Utilise uniquement le carnet d’adresses en mode hors connexion pour effectuer la résolution de noms.</span><span class="sxs-lookup"><span data-stu-id="86450-136">Uses only the offline address book to perform name resolution.</span></span> <span data-ttu-id="86450-137">Par exemple, vous pouvez utiliser cet indicateur pour permettre à une application cliente d’ouvrir la liste d’adresses globale (LAL) en mode Exchange mis en cache et d’accéder à une entrée dans ce carnet d’adresses à partir du cache sans créer de trafic entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="86450-137">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="86450-138">Cet indicateur est pris en charge uniquement par le Exchange de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="86450-138">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="86450-139">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="86450-139">MAPI_DEFERRED_ERRORS</span></span>
  
> <span data-ttu-id="86450-140">Permet de réussir l’appel, éventuellement avant que l’entrée soit entièrement ouverte et disponible, ce qui signifie que les appels ultérieurs à l’entrée peuvent renvoyer une erreur.</span><span class="sxs-lookup"><span data-stu-id="86450-140">Allows the call to succeed, potentially before the entry is fully open and available, implying that subsequent calls to the entry might return an error.</span></span>
    
<span data-ttu-id="86450-141">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="86450-141">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="86450-142">Utilise uniquement la LA GAL pour effectuer la résolution de noms.</span><span class="sxs-lookup"><span data-stu-id="86450-142">Uses only the GAL to perform name resolution.</span></span> <span data-ttu-id="86450-143">Cet indicateur est pris en charge uniquement par le Exchange de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="86450-143">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="86450-144">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="86450-144">MAPI_MODIFY</span></span>
  
> <span data-ttu-id="86450-145">Demande l’ouverture de l’entrée avec une autorisation de lecture et d’écriture.</span><span class="sxs-lookup"><span data-stu-id="86450-145">Requests that the entry be opened with read and write permission.</span></span> <span data-ttu-id="86450-146">Étant donné que les entrées sont ouvertes avec un accès en lecture seule par défaut, les clients ne doivent pas supposer que l’autorisation de lecture et d’écriture a été accordée, qu’MAPI_MODIFY soit définie ou non.</span><span class="sxs-lookup"><span data-stu-id="86450-146">Because entries are opened with read-only access by default, clients should not assume that read and write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="86450-147">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="86450-147">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="86450-148">N’utilise pas le carnet d’adresses en mode hors connexion pour effectuer la résolution de noms.</span><span class="sxs-lookup"><span data-stu-id="86450-148">Does not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="86450-149">Cet indicateur est pris en charge uniquement par le Exchange de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="86450-149">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
 <span data-ttu-id="86450-150">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="86450-150">_lpulObjType_</span></span>
  
> <span data-ttu-id="86450-151">[out] Pointeur vers le type de l’entrée ouverte.</span><span class="sxs-lookup"><span data-stu-id="86450-151">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="86450-152">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="86450-152">_lppUnk_</span></span>
  
> <span data-ttu-id="86450-153">[out] Pointeur vers un pointeur de l’entrée ouverte.</span><span class="sxs-lookup"><span data-stu-id="86450-153">[out] A pointer to a pointer of the opened entry.</span></span>
    

