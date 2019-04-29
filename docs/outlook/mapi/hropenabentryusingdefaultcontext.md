---
title: HrOpenABEntryUsingDefaultContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17cba69b-2b25-4b99-99d9-ec68fb8a35b5
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: f60c4d3761694439d10b073fda5bc36443c13e43
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434339"
---
# <a name="hropenabentryusingdefaultcontext"></a><span data-ttu-id="dff58-103">HrOpenABEntryUsingDefaultContext</span><span class="sxs-lookup"><span data-stu-id="dff58-103">HrOpenABEntryUsingDefaultContext</span></span>

  
  
<span data-ttu-id="dff58-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dff58-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dff58-105">Effectue la même fonction que [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md) , sauf qu'il utilise le **emsmdbUID** hérité comme paramètre _pEmsmdbUID_ .</span><span class="sxs-lookup"><span data-stu-id="dff58-105">Performs the same function as [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md) except that it uses the legacy **emsmdbUID** as the  _pEmsmdbUID_ parameter.</span></span> <span data-ttu-id="dff58-106">N'utilisez pas cette fonction, sauf si vous ne pouvez pas obtenir le **emsmdbUID** approprié pour l'appel vers [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md).</span><span class="sxs-lookup"><span data-stu-id="dff58-106">Do not use this function unless you cannot obtain the correct **emsmdbUID** for the call to [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="dff58-107">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="dff58-107">Header file:</span></span>  <br/> |<span data-ttu-id="dff58-108">abhelp. h</span><span class="sxs-lookup"><span data-stu-id="dff58-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="dff58-109">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="dff58-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="dff58-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="dff58-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="dff58-111">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="dff58-111">Called by:</span></span>  <br/> |<span data-ttu-id="dff58-112">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="dff58-112">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrOpenABEntryUsingDefaultContext(
  LPMAPISESSION pmsess,
  LPADRBOOK pAddrBook,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a><span data-ttu-id="dff58-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dff58-113">Parameters</span></span>

 <span data-ttu-id="dff58-114">_pmsess_</span><span class="sxs-lookup"><span data-stu-id="dff58-114">_pmsess_</span></span>
  
> <span data-ttu-id="dff58-115">dans Le **IMAPISession**connecté.</span><span class="sxs-lookup"><span data-stu-id="dff58-115">[in] The logged on **IMAPISession**.</span></span> <span data-ttu-id="dff58-116">Il ne peut pas être NULL.</span><span class="sxs-lookup"><span data-stu-id="dff58-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="dff58-117">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="dff58-117">_pAddrBook_</span></span>
  
> <span data-ttu-id="dff58-118">dans Carnet d'adresses utilisé pour ouvrir l'identificateur d'entrée.</span><span class="sxs-lookup"><span data-stu-id="dff58-118">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="dff58-119">Il ne peut pas être NULL.</span><span class="sxs-lookup"><span data-stu-id="dff58-119">It cannot be NULL.</span></span>
    
 <span data-ttu-id="dff58-120">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="dff58-120">_cbEntryID_</span></span>
  
> <span data-ttu-id="dff58-121">dans Nombre d'octets de l'identificateur d'entrée spécifié par le paramètre _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="dff58-121">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="dff58-122">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="dff58-122">_lpEntryID_</span></span>
  
>  <span data-ttu-id="dff58-123">dans Pointeur vers l'identificateur d'entrée qui représente l'entrée de carnet d'adresses à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="dff58-123">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span> 
    
 <span data-ttu-id="dff58-124">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="dff58-124">_lpInterface_</span></span>
  
> <span data-ttu-id="dff58-125">dans Pointeur vers l'identificateur d'interface (IID) de l'interface qui est utilisé pour accéder à l'entrée ouverte.</span><span class="sxs-lookup"><span data-stu-id="dff58-125">[in] A pointer to the interface identifier (IID) of the interface that is used to access the open entry.</span></span> <span data-ttu-id="dff58-126">Le passage de la valeur NULL renvoie l'interface standard de l'objet.</span><span class="sxs-lookup"><span data-stu-id="dff58-126">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="dff58-127">Pour les utilisateurs de messagerie, l'interface standard est [IMailUser: IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="dff58-127">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="dff58-128">Pour les listes de distribution, il s'agit de [IDistList: IMAPIContainer](idistlistimapicontainer.md)et pour les conteneurs dont il est [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="dff58-128">For distribution lists it is [IDistList : IMAPIContainer](idistlistimapicontainer.md), and for containers it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="dff58-129">Les appelants peuvent définir _lpInterface_ sur l'interface standard appropriée ou une interface dans la hiérarchie d'héritage.</span><span class="sxs-lookup"><span data-stu-id="dff58-129">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="dff58-130">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="dff58-130">_ulFlags_</span></span>
  
> <span data-ttu-id="dff58-131">dans Masque de des indicateurs qui contrôle le mode d'ouverture de l'entrée.</span><span class="sxs-lookup"><span data-stu-id="dff58-131">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="dff58-132">Les indicateurs suivants peuvent être définis:</span><span class="sxs-lookup"><span data-stu-id="dff58-132">The following flags can be set:</span></span>
    
<span data-ttu-id="dff58-133">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="dff58-133">MAPI_BEST_ACCESS</span></span>
  
> <span data-ttu-id="dff58-134">Demande que l'entrée soit ouverte avec les autorisations réseau et client maximales autorisées.</span><span class="sxs-lookup"><span data-stu-id="dff58-134">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="dff58-135">Par exemple, si le client dispose d'une autorisation en lecture et en écriture, le fournisseur de carnet d'adresses tente d'ouvrir l'entrée avec une autorisation en lecture et en écriture.</span><span class="sxs-lookup"><span data-stu-id="dff58-135">For example, if the client has read and write permission, the address book provider attempts to open the entry with read and write permission.</span></span> <span data-ttu-id="dff58-136">Le client peut récupérer le niveau d'accès qui a été accordé en appelant la méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) de l'entrée ouverte et en récupérant la propriété PR_ACCESS_LEVEL (PidTagAccessLevel).</span><span class="sxs-lookup"><span data-stu-id="dff58-136">The client can retrieve the access level that was granted by calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method of the open entry and retrieving the PR_ACCESS_LEVEL (PidTagAccessLevel) property.</span></span> 
    
<span data-ttu-id="dff58-137">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="dff58-137">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="dff58-138">Utilise uniquement le carnet d'adresses en mode hors connexion pour effectuer la résolution de noms.</span><span class="sxs-lookup"><span data-stu-id="dff58-138">Uses only the offline address book to perform name resolution.</span></span> <span data-ttu-id="dff58-139">Par exemple, vous pouvez utiliser cet indicateur pour permettre à une application cliente d'ouvrir la liste d'adresses globale (LAG) en mode Exchange mis en cache et d'accéder à une entrée de ce carnet d'adresses à partir du cache sans créer de trafic entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="dff58-139">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="dff58-140">Cet indicateur est pris en charge uniquement par le fournisseur de carnet d'adresses Exchange.</span><span class="sxs-lookup"><span data-stu-id="dff58-140">This flag is supported only by the Exchange address book provider.</span></span>
    
<span data-ttu-id="dff58-141">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="dff58-141">MAPI_DEFERRED_ERRORS</span></span>
  
> <span data-ttu-id="dff58-142">Permet à l'appel de réussir, éventuellement avant que l'entrée soit entièrement ouverte et disponible, ce qui implique que des appels ultérieurs à l'entrée renvoient une erreur.</span><span class="sxs-lookup"><span data-stu-id="dff58-142">Allows the call to succeed, potentially before the entry is fully open and available, implying that subsequent calls to the entry might return an error.</span></span>
    
<span data-ttu-id="dff58-143">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="dff58-143">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="dff58-144">Utilise uniquement la liste d'adresses globale pour effectuer la résolution de noms.</span><span class="sxs-lookup"><span data-stu-id="dff58-144">Uses only the GAL to perform name resolution.</span></span> <span data-ttu-id="dff58-145">Cet indicateur est pris en charge uniquement par le fournisseur de carnet d'adresses Exchange.</span><span class="sxs-lookup"><span data-stu-id="dff58-145">This flag is supported only by the Exchange address book provider.</span></span>
    
<span data-ttu-id="dff58-146">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="dff58-146">MAPI_MODIFY</span></span>
  
> <span data-ttu-id="dff58-147">Demande que l'entrée soit ouverte avec une autorisation en lecture et en écriture.</span><span class="sxs-lookup"><span data-stu-id="dff58-147">Requests that the entry be opened with read and write permission.</span></span> <span data-ttu-id="dff58-148">Étant donné que les entrées sont ouvertes avec un accès en lecture seule par défaut, les clients ne doivent pas supposer que l'autorisation de lecture et d'écriture a été accordée, que MAPI_MODIFY soit défini ou non.</span><span class="sxs-lookup"><span data-stu-id="dff58-148">Because entries are opened with read-only access by default, clients should not assume that read and write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="dff58-149">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="dff58-149">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="dff58-150">N'utilise pas le carnet d'adresses en mode hors connexion pour effectuer la résolution de noms.</span><span class="sxs-lookup"><span data-stu-id="dff58-150">Does not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="dff58-151">Cet indicateur est pris en charge uniquement par le fournisseur de carnet d'adresses Exchange.</span><span class="sxs-lookup"><span data-stu-id="dff58-151">This flag is supported only by the Exchange address book provider.</span></span>
    
 <span data-ttu-id="dff58-152">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="dff58-152">_lpulObjType_</span></span>
  
> <span data-ttu-id="dff58-153">remarquer Pointeur vers le type de l'entrée ouverte.</span><span class="sxs-lookup"><span data-stu-id="dff58-153">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="dff58-154">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="dff58-154">_lppUnk_</span></span>
  
> <span data-ttu-id="dff58-155">remarquer Pointeur vers un pointeur de l'entrée ouverte.</span><span class="sxs-lookup"><span data-stu-id="dff58-155">[out] A pointer to a pointer of the opened entry.</span></span>
    

