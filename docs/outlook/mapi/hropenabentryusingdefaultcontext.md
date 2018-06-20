---
title: HrOpenABEntryUsingDefaultContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17cba69b-2b25-4b99-99d9-ec68fb8a35b5
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 74660de551d43c589cb903b5c3852136f2f18269
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783553"
---
# <a name="hropenabentryusingdefaultcontext"></a><span data-ttu-id="878ac-103">HrOpenABEntryUsingDefaultContext</span><span class="sxs-lookup"><span data-stu-id="878ac-103">HrOpenABEntryUsingDefaultContext</span></span>

  
  
<span data-ttu-id="878ac-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="878ac-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="878ac-105">Effectue la même fonction que [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md) sauf qu’il utilise hérité **emsmdbUID** en tant que paramètre _pEmsmdbUID_ .</span><span class="sxs-lookup"><span data-stu-id="878ac-105">Performs the same function as [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md) except that it uses the legacy **emsmdbUID** as the  _pEmsmdbUID_ parameter.</span></span> <span data-ttu-id="878ac-106">N’utilisez pas cette fonction, sauf si vous ne peut pas obtenir correct **emsmdbUID** pour l’appel à [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md).</span><span class="sxs-lookup"><span data-stu-id="878ac-106">Do not use this function unless you cannot obtain the correct **emsmdbUID** for the call to [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="878ac-107">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="878ac-107">Header file:</span></span>  <br/> |<span data-ttu-id="878ac-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="878ac-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="878ac-109">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="878ac-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="878ac-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="878ac-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="878ac-111">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="878ac-111">Called by:</span></span>  <br/> |<span data-ttu-id="878ac-112">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="878ac-112">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="878ac-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="878ac-113">Parameters</span></span>

 <span data-ttu-id="878ac-114">_pmsess_</span><span class="sxs-lookup"><span data-stu-id="878ac-114">_pmsess_</span></span>
  
> <span data-ttu-id="878ac-115">[in] La session **IMAPISession**.</span><span class="sxs-lookup"><span data-stu-id="878ac-115">[in] The logged on **IMAPISession**.</span></span> <span data-ttu-id="878ac-116">Il ne peut pas être NULL.</span><span class="sxs-lookup"><span data-stu-id="878ac-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="878ac-117">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="878ac-117">_pAddrBook_</span></span>
  
> <span data-ttu-id="878ac-118">[in] Le carnet d’adresses utilisée pour ouvrir l’identificateur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="878ac-118">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="878ac-119">Il ne peut pas être NULL.</span><span class="sxs-lookup"><span data-stu-id="878ac-119">It cannot be NULL.</span></span>
    
 <span data-ttu-id="878ac-120">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="878ac-120">_cbEntryID_</span></span>
  
> <span data-ttu-id="878ac-121">[in] Nombre d’octets de l’identificateur d’entrée spécifié par le paramètre _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="878ac-121">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="878ac-122">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="878ac-122">_lpEntryID_</span></span>
  
>  <span data-ttu-id="878ac-123">[in] Pointeur vers l’identificateur d’entrée qui représente l’entrée du carnet d’adresses à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="878ac-123">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span> 
    
 <span data-ttu-id="878ac-124">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="878ac-124">_lpInterface_</span></span>
  
> <span data-ttu-id="878ac-125">[in] Pointeur vers l’identificateur d’interface (IID) de l’interface qui est utilisée pour accéder à l’entrée open.</span><span class="sxs-lookup"><span data-stu-id="878ac-125">[in] A pointer to the interface identifier (IID) of the interface that is used to access the open entry.</span></span> <span data-ttu-id="878ac-126">Passage de NULL renvoie l’interface standard de l’objet.</span><span class="sxs-lookup"><span data-stu-id="878ac-126">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="878ac-127">Pour les utilisateurs de messagerie, l’interface standard est [IMailUser : IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="878ac-127">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="878ac-128">Pour les listes de distribution, il est [IDistList : IMAPIContainer](idistlistimapicontainer.md)et il s’agit de conteneurs [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="878ac-128">For distribution lists it is [IDistList : IMAPIContainer](idistlistimapicontainer.md), and for containers it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="878ac-129">Les appelants peuvent définir _lpInterface_ à l’interface standard ou d’une interface dans la hiérarchie d’héritage.</span><span class="sxs-lookup"><span data-stu-id="878ac-129">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="878ac-130">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="878ac-130">_ulFlags_</span></span>
  
> <span data-ttu-id="878ac-131">[in] Masque de bits d’indicateurs qui contrôle la façon dont l’entrée est ouvert.</span><span class="sxs-lookup"><span data-stu-id="878ac-131">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="878ac-132">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="878ac-132">The following flags can be set:</span></span>
    
<span data-ttu-id="878ac-133">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="878ac-133">MAPI_BEST_ACCESS</span></span>
  
> <span data-ttu-id="878ac-134">Demandes que l’entrée s’ouvre avec les autorisations maximales autorisées réseau et le client.</span><span class="sxs-lookup"><span data-stu-id="878ac-134">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="878ac-135">Par exemple, si le client dispose de lecture et l’autorisation d’écriture, le fournisseur de carnet d’adresses essaie ouvrir l’entrée en lecture et l’autorisation d’écriture.</span><span class="sxs-lookup"><span data-stu-id="878ac-135">For example, if the client has read and write permission, the address book provider attempts to open the entry with read and write permission.</span></span> <span data-ttu-id="878ac-136">Le client peut extraire le niveau d’accès qui a été accordé en appelant la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) de l’écriture ouverte et de récupération de la propriété PR_ACCESS_LEVEL (PidTagAccessLevel).</span><span class="sxs-lookup"><span data-stu-id="878ac-136">The client can retrieve the access level that was granted by calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method of the open entry and retrieving the PR_ACCESS_LEVEL (PidTagAccessLevel) property.</span></span> 
    
<span data-ttu-id="878ac-137">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="878ac-137">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="878ac-138">Utilise uniquement le carnet d’adresses en mode hors connexion pour effectuer la résolution de noms.</span><span class="sxs-lookup"><span data-stu-id="878ac-138">Uses only the offline address book to perform name resolution.</span></span> <span data-ttu-id="878ac-139">Par exemple, vous pouvez utiliser cet indicateur pour autoriser une application cliente ouvrir la liste d’adresses globale (LAG) en mode exchange mis en cache et accéder à une entrée dans ce carnet d’adresses à partir du cache sans créer le trafic entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="878ac-139">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="878ac-140">Cet indicateur est pris en charge uniquement par le fournisseur de carnet d’adresses Exchange.</span><span class="sxs-lookup"><span data-stu-id="878ac-140">This flag is supported only by the Exchange address book provider.</span></span>
    
<span data-ttu-id="878ac-141">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="878ac-141">MAPI_DEFERRED_ERRORS</span></span>
  
> <span data-ttu-id="878ac-142">Permet l’appel aboutisse, potentiellement avant que l’entrée est entièrement ouverte et disponible, ce qui implique que les appels suivants à l’entrée renverra une erreur.</span><span class="sxs-lookup"><span data-stu-id="878ac-142">Allows the call to succeed, potentially before the entry is fully open and available, implying that subsequent calls to the entry might return an error.</span></span>
    
<span data-ttu-id="878ac-143">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="878ac-143">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="878ac-144">Utilise uniquement la liste d’adresses globale pour effectuer la résolution de noms.</span><span class="sxs-lookup"><span data-stu-id="878ac-144">Uses only the GAL to perform name resolution.</span></span> <span data-ttu-id="878ac-145">Cet indicateur est pris en charge uniquement par le fournisseur de carnet d’adresses Exchange.</span><span class="sxs-lookup"><span data-stu-id="878ac-145">This flag is supported only by the Exchange address book provider.</span></span>
    
<span data-ttu-id="878ac-146">N'</span><span class="sxs-lookup"><span data-stu-id="878ac-146">MAPI_MODIFY</span></span>
  
> <span data-ttu-id="878ac-147">Demandes ouvrir avec l’entrée de lire et écrire des autorisations.</span><span class="sxs-lookup"><span data-stu-id="878ac-147">Requests that the entry be opened with read and write permission.</span></span> <span data-ttu-id="878ac-148">Étant donné que les entrées sont ouvertes avec accès en lecture seule par défaut, les clients ne doivent pas supposer que lire et écrire l’autorisation a été accordée même si n’est définie.</span><span class="sxs-lookup"><span data-stu-id="878ac-148">Because entries are opened with read-only access by default, clients should not assume that read and write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="878ac-149">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="878ac-149">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="878ac-150">N’utilise pas le carnet d’adresses en mode hors connexion pour effectuer la résolution de noms.</span><span class="sxs-lookup"><span data-stu-id="878ac-150">Does not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="878ac-151">Cet indicateur est pris en charge uniquement par le fournisseur de carnet d’adresses Exchange.</span><span class="sxs-lookup"><span data-stu-id="878ac-151">This flag is supported only by the Exchange address book provider.</span></span>
    
 <span data-ttu-id="878ac-152">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="878ac-152">_lpulObjType_</span></span>
  
> <span data-ttu-id="878ac-153">[out] Pointeur vers le type de l’entrée ouvert.</span><span class="sxs-lookup"><span data-stu-id="878ac-153">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="878ac-154">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="878ac-154">_lppUnk_</span></span>
  
> <span data-ttu-id="878ac-155">[out] Pointeur vers un pointeur de l’entrée ouvert.</span><span class="sxs-lookup"><span data-stu-id="878ac-155">[out] A pointer to a pointer of the opened entry.</span></span>
    

