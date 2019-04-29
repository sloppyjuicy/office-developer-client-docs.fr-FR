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
# <a name="hropenabentrywithresolvedrow"></a><span data-ttu-id="cd5da-103">HrOpenABEntryWithResolvedRow</span><span class="sxs-lookup"><span data-stu-id="cd5da-103">HrOpenABEntryWithResolvedRow</span></span>

  
  
<span data-ttu-id="cd5da-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cd5da-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cd5da-105">Effectue la même fonction que [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md) , sauf qu'il obtient automatiquement **emsabpUID** à partir de la ligne résolue et ouvre la propriété **entryID**.</span><span class="sxs-lookup"><span data-stu-id="cd5da-105">Performs the same function as [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md) except that it automatically gets the **emsabpUID** from the resolved row and opens the **entryID**.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cd5da-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="cd5da-106">Header file:</span></span>  <br/> |<span data-ttu-id="cd5da-107">abhelp. h</span><span class="sxs-lookup"><span data-stu-id="cd5da-107">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="cd5da-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="cd5da-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="cd5da-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="cd5da-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="cd5da-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="cd5da-110">Called by:</span></span>  <br/> |<span data-ttu-id="cd5da-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="cd5da-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="cd5da-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cd5da-112">Parameters</span></span>

 <span data-ttu-id="cd5da-113">_prwResolved_</span><span class="sxs-lookup"><span data-stu-id="cd5da-113">_prwResolved_</span></span>
  
> <span data-ttu-id="cd5da-114">dans Pointeur vers la ligne résolue utilisée pour obtenir le **emsabpUID** et ouvrir la propriété **entryID**.</span><span class="sxs-lookup"><span data-stu-id="cd5da-114">[in] A pointer to the resolved row that is used to get the **emsabpUID** and open the **entryID**.</span></span>
    
 <span data-ttu-id="cd5da-115">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="cd5da-115">_pAddrBook_</span></span>
  
> <span data-ttu-id="cd5da-116">dans Carnet d'adresses utilisé pour ouvrir l'identificateur d'entrée.</span><span class="sxs-lookup"><span data-stu-id="cd5da-116">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="cd5da-117">Il ne peut pas être NULL.</span><span class="sxs-lookup"><span data-stu-id="cd5da-117">It cannot be NULL.</span></span>
    
 <span data-ttu-id="cd5da-118">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="cd5da-118">_cbEntryID_</span></span>
  
> <span data-ttu-id="cd5da-119">dans Nombre d'octets de l'identificateur d'entrée spécifié par le paramètre _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="cd5da-119">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="cd5da-120">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="cd5da-120">_lpEntryID_</span></span>
  
>  <span data-ttu-id="cd5da-121">dans Pointeur vers l'identificateur d'entrée qui représente l'entrée de carnet d'adresses à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="cd5da-121">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span> 
    
 <span data-ttu-id="cd5da-122">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="cd5da-122">_lpInterface_</span></span>
  
> <span data-ttu-id="cd5da-123">dans Pointeur vers l'identificateur d'interface (IID) de l'interface qui est utilisé pour accéder à l'entrée ouverte.</span><span class="sxs-lookup"><span data-stu-id="cd5da-123">[in] A pointer to the interface identifier (IID) of the interface that is used to access the open entry.</span></span> <span data-ttu-id="cd5da-124">Le passage de la valeur NULL renvoie l'interface standard de l'objet.</span><span class="sxs-lookup"><span data-stu-id="cd5da-124">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="cd5da-125">Pour les utilisateurs de messagerie, l'interface standard est [IMailUser: IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="cd5da-125">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="cd5da-126">Pour les listes de distribution, il s'agit de [IDistList: IMAPIContainer](idistlistimapicontainer.md)et pour les conteneurs, il s'agit de [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="cd5da-126">For distribution lists, it is [IDistList : IMAPIContainer](idistlistimapicontainer.md)and for containers, it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="cd5da-127">Les appelants peuvent définir _lpInterface_ sur l'interface standard appropriée ou une interface dans la hiérarchie d'héritage.</span><span class="sxs-lookup"><span data-stu-id="cd5da-127">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="cd5da-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="cd5da-128">_ulFlags_</span></span>
  
> <span data-ttu-id="cd5da-129">dans Masque de des indicateurs qui contrôle le mode d'ouverture de l'entrée.</span><span class="sxs-lookup"><span data-stu-id="cd5da-129">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="cd5da-130">Les indicateurs suivants peuvent être définis:</span><span class="sxs-lookup"><span data-stu-id="cd5da-130">The following flags can be set:</span></span>
    
<span data-ttu-id="cd5da-131">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="cd5da-131">MAPI_BEST_ACCESS</span></span>
  
> <span data-ttu-id="cd5da-132">Demande que l'entrée soit ouverte avec les autorisations réseau et client maximales autorisées.</span><span class="sxs-lookup"><span data-stu-id="cd5da-132">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="cd5da-133">Par exemple, si le client dispose d'une autorisation en lecture et en écriture, le fournisseur de carnet d'adresses tente d'ouvrir l'entrée avec une autorisation en lecture et en écriture.</span><span class="sxs-lookup"><span data-stu-id="cd5da-133">For example, if the client has read and write permission, the address book provider attempts to open the entry with read and write permission.</span></span> <span data-ttu-id="cd5da-134">Le client peut récupérer le niveau d'accès qui a été accordé en appelant la méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) de l'entrée ouverte et en récupérant la propriété PR_ACCESS_LEVEL (PidTagAccessLevel).</span><span class="sxs-lookup"><span data-stu-id="cd5da-134">The client can retrieve the access level that was granted by calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method of the open entry and retrieving the PR_ACCESS_LEVEL (PidTagAccessLevel) property.</span></span> 
    
<span data-ttu-id="cd5da-135">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="cd5da-135">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="cd5da-136">Utilise uniquement le carnet d'adresses en mode hors connexion pour effectuer la résolution de noms.</span><span class="sxs-lookup"><span data-stu-id="cd5da-136">Uses only the offline address book to perform name resolution.</span></span> <span data-ttu-id="cd5da-137">Par exemple, vous pouvez utiliser cet indicateur pour permettre à une application cliente d'ouvrir la liste d'adresses globale (LAG) en mode Exchange mis en cache et d'accéder à une entrée de ce carnet d'adresses à partir du cache sans créer de trafic entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="cd5da-137">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="cd5da-138">Cet indicateur est pris en charge uniquement par le fournisseur de carnet d'adresses Exchange.</span><span class="sxs-lookup"><span data-stu-id="cd5da-138">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="cd5da-139">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="cd5da-139">MAPI_DEFERRED_ERRORS</span></span>
  
> <span data-ttu-id="cd5da-140">Permet à l'appel de réussir, éventuellement avant que l'entrée soit entièrement ouverte et disponible, ce qui implique que des appels ultérieurs à l'entrée renvoient une erreur.</span><span class="sxs-lookup"><span data-stu-id="cd5da-140">Allows the call to succeed, potentially before the entry is fully open and available, implying that subsequent calls to the entry might return an error.</span></span>
    
<span data-ttu-id="cd5da-141">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="cd5da-141">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="cd5da-142">Utilise uniquement la liste d'adresses globale pour effectuer la résolution de noms.</span><span class="sxs-lookup"><span data-stu-id="cd5da-142">Uses only the GAL to perform name resolution.</span></span> <span data-ttu-id="cd5da-143">Cet indicateur est pris en charge uniquement par le fournisseur de carnet d'adresses Exchange.</span><span class="sxs-lookup"><span data-stu-id="cd5da-143">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="cd5da-144">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="cd5da-144">MAPI_MODIFY</span></span>
  
> <span data-ttu-id="cd5da-145">Demande que l'entrée soit ouverte avec une autorisation en lecture et en écriture.</span><span class="sxs-lookup"><span data-stu-id="cd5da-145">Requests that the entry be opened with read and write permission.</span></span> <span data-ttu-id="cd5da-146">Étant donné que les entrées sont ouvertes avec un accès en lecture seule par défaut, les clients ne doivent pas supposer que l'autorisation de lecture et d'écriture a été accordée, que MAPI_MODIFY soit défini ou non.</span><span class="sxs-lookup"><span data-stu-id="cd5da-146">Because entries are opened with read-only access by default, clients should not assume that read and write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="cd5da-147">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="cd5da-147">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="cd5da-148">N'utilise pas le carnet d'adresses en mode hors connexion pour effectuer la résolution de noms.</span><span class="sxs-lookup"><span data-stu-id="cd5da-148">Does not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="cd5da-149">Cet indicateur est pris en charge uniquement par le fournisseur de carnet d'adresses Exchange.</span><span class="sxs-lookup"><span data-stu-id="cd5da-149">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
 <span data-ttu-id="cd5da-150">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="cd5da-150">_lpulObjType_</span></span>
  
> <span data-ttu-id="cd5da-151">remarquer Pointeur vers le type de l'entrée ouverte.</span><span class="sxs-lookup"><span data-stu-id="cd5da-151">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="cd5da-152">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="cd5da-152">_lppUnk_</span></span>
  
> <span data-ttu-id="cd5da-153">remarquer Pointeur vers un pointeur de l'entrée ouverte.</span><span class="sxs-lookup"><span data-stu-id="cd5da-153">[out] A pointer to a pointer of the opened entry.</span></span>
    

