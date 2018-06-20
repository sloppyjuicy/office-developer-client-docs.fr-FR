---
title: HrOpenABEntryWithResolvedRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ce3a583c-16a9-4268-9476-926d2780eae5
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 0e39f4edc871b49675f1ffcc1bc541345c8829d5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783579"
---
# <a name="hropenabentrywithresolvedrow"></a><span data-ttu-id="b3f78-103">HrOpenABEntryWithResolvedRow</span><span class="sxs-lookup"><span data-stu-id="b3f78-103">HrOpenABEntryWithResolvedRow</span></span>

  
  
<span data-ttu-id="b3f78-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b3f78-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b3f78-105">Effectue la même fonction que [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md) sauf qu’elle obtient **emsabpUID** à partir de la ligne résolue et ouvre **propriété entryID**automatiquement.</span><span class="sxs-lookup"><span data-stu-id="b3f78-105">Performs the same function as [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md) except that it automatically gets the **emsabpUID** from the resolved row and opens the **entryID**.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b3f78-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="b3f78-106">Header file:</span></span>  <br/> |<span data-ttu-id="b3f78-107">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="b3f78-107">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="b3f78-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="b3f78-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="b3f78-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="b3f78-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="b3f78-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="b3f78-110">Called by:</span></span>  <br/> |<span data-ttu-id="b3f78-111">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="b3f78-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="b3f78-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b3f78-112">Parameters</span></span>

 <span data-ttu-id="b3f78-113">_prwResolved_</span><span class="sxs-lookup"><span data-stu-id="b3f78-113">_prwResolved_</span></span>
  
> <span data-ttu-id="b3f78-114">[in] Pointeur vers la ligne résolu qui est utilisée pour obtenir **emsabpUID** et ouvrez **entryID**.</span><span class="sxs-lookup"><span data-stu-id="b3f78-114">[in] A pointer to the resolved row that is used to get the **emsabpUID** and open the **entryID**.</span></span>
    
 <span data-ttu-id="b3f78-115">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="b3f78-115">_pAddrBook_</span></span>
  
> <span data-ttu-id="b3f78-116">[in] Le carnet d’adresses utilisée pour ouvrir l’identificateur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="b3f78-116">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="b3f78-117">Il ne peut pas être NULL.</span><span class="sxs-lookup"><span data-stu-id="b3f78-117">It cannot be NULL.</span></span>
    
 <span data-ttu-id="b3f78-118">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="b3f78-118">_cbEntryID_</span></span>
  
> <span data-ttu-id="b3f78-119">[in] Nombre d’octets de l’identificateur d’entrée spécifié par le paramètre _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="b3f78-119">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="b3f78-120">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="b3f78-120">_lpEntryID_</span></span>
  
>  <span data-ttu-id="b3f78-121">[in] Pointeur vers l’identificateur d’entrée qui représente l’entrée du carnet d’adresses à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="b3f78-121">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span> 
    
 <span data-ttu-id="b3f78-122">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="b3f78-122">_lpInterface_</span></span>
  
> <span data-ttu-id="b3f78-123">[in] Pointeur vers l’identificateur d’interface (IID) de l’interface qui est utilisée pour accéder à l’entrée open.</span><span class="sxs-lookup"><span data-stu-id="b3f78-123">[in] A pointer to the interface identifier (IID) of the interface that is used to access the open entry.</span></span> <span data-ttu-id="b3f78-124">Passage de NULL renvoie l’interface standard de l’objet.</span><span class="sxs-lookup"><span data-stu-id="b3f78-124">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="b3f78-125">Pour les utilisateurs de messagerie, l’interface standard est [IMailUser : IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="b3f78-125">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="b3f78-126">Pour les listes de distribution, il est [IDistList : IMAPIContainer](idistlistimapicontainer.md)et pour les conteneurs, il est [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="b3f78-126">For distribution lists, it is [IDistList : IMAPIContainer](idistlistimapicontainer.md)and for containers, it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="b3f78-127">Les appelants peuvent définir _lpInterface_ à l’interface standard ou d’une interface dans la hiérarchie d’héritage.</span><span class="sxs-lookup"><span data-stu-id="b3f78-127">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="b3f78-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b3f78-128">_ulFlags_</span></span>
  
> <span data-ttu-id="b3f78-129">[in] Masque de bits d’indicateurs qui contrôle la façon dont l’entrée est ouvert.</span><span class="sxs-lookup"><span data-stu-id="b3f78-129">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="b3f78-130">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="b3f78-130">The following flags can be set:</span></span>
    
<span data-ttu-id="b3f78-131">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="b3f78-131">MAPI_BEST_ACCESS</span></span>
  
> <span data-ttu-id="b3f78-132">Demandes que l’entrée s’ouvre avec les autorisations maximales autorisées réseau et le client.</span><span class="sxs-lookup"><span data-stu-id="b3f78-132">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="b3f78-133">Par exemple, si le client dispose de lecture et l’autorisation d’écriture, le fournisseur de carnet d’adresses essaie ouvrir l’entrée en lecture et l’autorisation d’écriture.</span><span class="sxs-lookup"><span data-stu-id="b3f78-133">For example, if the client has read and write permission, the address book provider attempts to open the entry with read and write permission.</span></span> <span data-ttu-id="b3f78-134">Le client peut extraire le niveau d’accès qui a été accordé en appelant la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) de l’écriture ouverte et de récupération de la propriété PR_ACCESS_LEVEL (PidTagAccessLevel).</span><span class="sxs-lookup"><span data-stu-id="b3f78-134">The client can retrieve the access level that was granted by calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method of the open entry and retrieving the PR_ACCESS_LEVEL (PidTagAccessLevel) property.</span></span> 
    
<span data-ttu-id="b3f78-135">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="b3f78-135">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="b3f78-136">Utilise uniquement le carnet d’adresses en mode hors connexion pour effectuer la résolution de noms.</span><span class="sxs-lookup"><span data-stu-id="b3f78-136">Uses only the offline address book to perform name resolution.</span></span> <span data-ttu-id="b3f78-137">Par exemple, vous pouvez utiliser cet indicateur pour autoriser une application cliente ouvrir la liste d’adresses globale (LAG) en mode exchange mis en cache et accéder à une entrée dans ce carnet d’adresses à partir du cache sans créer le trafic entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="b3f78-137">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="b3f78-138">Cet indicateur est pris en charge uniquement par le fournisseur de carnet d’adresses Exchange.</span><span class="sxs-lookup"><span data-stu-id="b3f78-138">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="b3f78-139">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="b3f78-139">MAPI_DEFERRED_ERRORS</span></span>
  
> <span data-ttu-id="b3f78-140">Permet l’appel aboutisse, potentiellement avant que l’entrée est entièrement ouverte et disponible, ce qui implique que les appels suivants à l’entrée renverra une erreur.</span><span class="sxs-lookup"><span data-stu-id="b3f78-140">Allows the call to succeed, potentially before the entry is fully open and available, implying that subsequent calls to the entry might return an error.</span></span>
    
<span data-ttu-id="b3f78-141">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="b3f78-141">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="b3f78-142">Utilise uniquement la liste d’adresses globale pour effectuer la résolution de noms.</span><span class="sxs-lookup"><span data-stu-id="b3f78-142">Uses only the GAL to perform name resolution.</span></span> <span data-ttu-id="b3f78-143">Cet indicateur est pris en charge uniquement par le fournisseur de carnet d’adresses Exchange.</span><span class="sxs-lookup"><span data-stu-id="b3f78-143">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="b3f78-144">N'</span><span class="sxs-lookup"><span data-stu-id="b3f78-144">MAPI_MODIFY</span></span>
  
> <span data-ttu-id="b3f78-145">Demandes ouvrir avec l’entrée de lire et écrire des autorisations.</span><span class="sxs-lookup"><span data-stu-id="b3f78-145">Requests that the entry be opened with read and write permission.</span></span> <span data-ttu-id="b3f78-146">Étant donné que les entrées sont ouvertes avec accès en lecture seule par défaut, les clients ne doivent pas supposer que lire et écrire l’autorisation a été accordée même si n’est définie.</span><span class="sxs-lookup"><span data-stu-id="b3f78-146">Because entries are opened with read-only access by default, clients should not assume that read and write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="b3f78-147">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="b3f78-147">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="b3f78-148">N’utilise pas le carnet d’adresses en mode hors connexion pour effectuer la résolution de noms.</span><span class="sxs-lookup"><span data-stu-id="b3f78-148">Does not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="b3f78-149">Cet indicateur est pris en charge uniquement par le fournisseur de carnet d’adresses Exchange.</span><span class="sxs-lookup"><span data-stu-id="b3f78-149">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
 <span data-ttu-id="b3f78-150">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="b3f78-150">_lpulObjType_</span></span>
  
> <span data-ttu-id="b3f78-151">[out] Pointeur vers le type de l’entrée ouvert.</span><span class="sxs-lookup"><span data-stu-id="b3f78-151">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="b3f78-152">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="b3f78-152">_lppUnk_</span></span>
  
> <span data-ttu-id="b3f78-153">[out] Pointeur vers un pointeur de l’entrée ouvert.</span><span class="sxs-lookup"><span data-stu-id="b3f78-153">[out] A pointer to a pointer of the opened entry.</span></span>
    

