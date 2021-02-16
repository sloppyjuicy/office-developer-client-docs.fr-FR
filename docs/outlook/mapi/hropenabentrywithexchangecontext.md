---
title: HrOpenABEntryWithExchangeContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b640a5aa-4e36-4983-bf11-9428809e830b
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 415d108f7fd9e84ba2a9090658bc0923550390f2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434052"
---
# <a name="hropenabentrywithexchangecontext"></a><span data-ttu-id="f51fd-103">HrOpenABEntryWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="f51fd-103">HrOpenABEntryWithExchangeContext</span></span>

  
  
<span data-ttu-id="f51fd-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f51fd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f51fd-105">Ouvre **l’entryID à** l’aide du carnet d’adresses Exchange identifié **par pEmsmdbUID**.</span><span class="sxs-lookup"><span data-stu-id="f51fd-105">Opens the **entryID** using the Exchange Address Book identified by **pEmsmdbUID**.</span></span> <span data-ttu-id="f51fd-106">Cette fonction fonctionne de la même manière que [IAddrBook::D etails,](iaddrbook-details.md) sauf que l’utilisation de cette fonction garantit que [l’IAddrBook::OpenEntry](iaddrbook-openentry.md) est ouvert à l’aide du fournisseur de carnet d’adresses Exchange attendu.</span><span class="sxs-lookup"><span data-stu-id="f51fd-106">This function works similarly to [IAddrBook::Details](iaddrbook-details.md) except that using this function ensures that the [IAddrBook::OpenEntry](iaddrbook-openentry.md) is opened by using the expected Exchange Address Book Provider.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f51fd-107">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="f51fd-107">Header file:</span></span>  <br/> |<span data-ttu-id="f51fd-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="f51fd-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="f51fd-109">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="f51fd-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="f51fd-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="f51fd-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="f51fd-111">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="f51fd-111">Called by:</span></span>  <br/> |<span data-ttu-id="f51fd-112">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="f51fd-112">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrDoABDetailsWithExchangeContext(
  LPMAPISESSION pmsess,
  const MAPIUID *pEmsmdbUID,
  LPADRBOOK pAddrBook,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="f51fd-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f51fd-113">Parameters</span></span>

 <span data-ttu-id="f51fd-114">_pmsess_</span><span class="sxs-lookup"><span data-stu-id="f51fd-114">_pmsess_</span></span>
  
> <span data-ttu-id="f51fd-115">[in] **L’IMAPISession** connecté.</span><span class="sxs-lookup"><span data-stu-id="f51fd-115">[in] The logged on **IMAPISession**.</span></span> <span data-ttu-id="f51fd-116">Elle ne peut pas être NULL.</span><span class="sxs-lookup"><span data-stu-id="f51fd-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="f51fd-117">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="f51fd-117">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="f51fd-118">[in] Pointeur vers **un emsmdbUID** qui identifie le service Exchange qui contient le fournisseur de carnet d’adresses Exchange que cette fonction doit utiliser pour afficher des détails sur l’identificateur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="f51fd-118">[in] A pointer to an **emsmdbUID** that identifies the Exchange Service that contains the Exchange Address Book Provider that this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="f51fd-119">Si l’identificateur d’entrée entrante n’est pas un identificateur d’entrée du fournisseur de carnet d’adresses Exchange, ce paramètre est ignoré et l’appel de fonction se comporte comme [IAddrBook::D etails](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="f51fd-119">If the incoming entry identifier is not an Exchange Address Book Provider entry identifier, this parameter is ignored and the function call behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="f51fd-120">Si ce paramètre est NULL ou un MAPIUID zéro, cette fonction se comporte comme [IAddrBook::D etails](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="f51fd-120">If this parameter is NULL or a zero MAPIUID, this function behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="f51fd-121">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="f51fd-121">_pAddrBook_</span></span>
  
> <span data-ttu-id="f51fd-122">[in] Carnet d’adresses utilisé pour ouvrir l’identificateur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="f51fd-122">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="f51fd-123">Elle ne peut pas être NULL.</span><span class="sxs-lookup"><span data-stu-id="f51fd-123">It cannot be NULL.</span></span>
    
 <span data-ttu-id="f51fd-124">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="f51fd-124">_cbEntryID_</span></span>
  
> <span data-ttu-id="f51fd-125">[in] Nombre d’bytes de l’identificateur d’entrée spécifié par _le paramètre lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="f51fd-125">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="f51fd-126">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="f51fd-126">_lpEntryID_</span></span>
  
>  <span data-ttu-id="f51fd-127">[in] Pointeur vers l’identificateur d’entrée qui représente l’entrée de carnet d’adresses à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="f51fd-127">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span> 
    
 <span data-ttu-id="f51fd-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f51fd-128">_ulFlags_</span></span>
  
> <span data-ttu-id="f51fd-129">[in] Masque de bits d’indicateurs qui contrôle la façon dont l’entrée est ouverte.</span><span class="sxs-lookup"><span data-stu-id="f51fd-129">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="f51fd-130">Les indicateurs suivants peuvent être définies :</span><span class="sxs-lookup"><span data-stu-id="f51fd-130">The following flags can be set:</span></span>
    
<span data-ttu-id="f51fd-131">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="f51fd-131">MAPI_BEST_ACCESS</span></span>
  
> <span data-ttu-id="f51fd-132">Demande l’ouverture de l’entrée avec le nombre maximal d’autorisations réseau et client autorisées.</span><span class="sxs-lookup"><span data-stu-id="f51fd-132">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="f51fd-133">Par exemple, si le client dispose d’autorisations de lecture et d’écriture, le fournisseur de carnet d’adresses tente d’ouvrir l’entrée avec des autorisations de lecture et d’écriture.</span><span class="sxs-lookup"><span data-stu-id="f51fd-133">For example, if the client has read and write permission, the address book provider attempts to open the entry with read and write permission.</span></span> <span data-ttu-id="f51fd-134">Le client peut récupérer le niveau d’accès accordé en appelant la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) de l’entrée ouverte et en récupérant la propriété PR_ACCESS_LEVEL (PidTagAccessLevel).</span><span class="sxs-lookup"><span data-stu-id="f51fd-134">The client can retrieve the access level that was granted by calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method of the open entry and retrieving the PR_ACCESS_LEVEL (PidTagAccessLevel) property.</span></span> 
    
<span data-ttu-id="f51fd-135">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="f51fd-135">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="f51fd-136">Utilise uniquement le carnet d’adresses en mode hors connexion pour effectuer la résolution de noms.</span><span class="sxs-lookup"><span data-stu-id="f51fd-136">Uses only the offline address book to perform name resolution.</span></span> <span data-ttu-id="f51fd-137">Par exemple, vous pouvez utiliser cet indicateur pour permettre à une application cliente d’ouvrir la liste d’adresses globale (LAL) en mode Exchange mis en cache et d’accéder à une entrée dans ce carnet d’adresses à partir du cache sans créer de trafic entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="f51fd-137">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="f51fd-138">Cet indicateur est pris en charge uniquement par le fournisseur de carnet d’adresses Exchange.</span><span class="sxs-lookup"><span data-stu-id="f51fd-138">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="f51fd-139">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="f51fd-139">MAPI_DEFERRED_ERRORS</span></span>
  
> <span data-ttu-id="f51fd-140">Permet à l’appel de réussir, potentiellement avant que l’entrée soit entièrement ouverte et disponible, ce qui signifie que les appels ultérieurs à l’entrée peuvent renvoyer une erreur.</span><span class="sxs-lookup"><span data-stu-id="f51fd-140">Allows the call to succeed, potentially before the entry is fully open and available, implying that subsequent calls to the entry might return an error.</span></span>
    
<span data-ttu-id="f51fd-141">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="f51fd-141">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="f51fd-142">Utilise uniquement la LA GAL pour effectuer la résolution de noms.</span><span class="sxs-lookup"><span data-stu-id="f51fd-142">Uses only the GAL to perform name resolution.</span></span> <span data-ttu-id="f51fd-143">Cet indicateur est pris en charge uniquement par le fournisseur de carnet d’adresses Exchange.</span><span class="sxs-lookup"><span data-stu-id="f51fd-143">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="f51fd-144">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="f51fd-144">MAPI_MODIFY</span></span>
  
> <span data-ttu-id="f51fd-145">Demande l’ouverture de l’entrée avec une autorisation de lecture et d’écriture.</span><span class="sxs-lookup"><span data-stu-id="f51fd-145">Requests that the entry be opened with read and write permission.</span></span> <span data-ttu-id="f51fd-146">Étant donné que les entrées sont ouvertes avec un accès en lecture seule par défaut, les clients ne doivent pas supposer que les autorisations de lecture et d’écriture ont été accordées, qu’MAPI_MODIFY soit définie ou non.</span><span class="sxs-lookup"><span data-stu-id="f51fd-146">Because entries are opened with read-only access by default, clients should not assume that read and write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="f51fd-147">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="f51fd-147">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="f51fd-148">N’utilise pas le carnet d’adresses en mode hors connexion pour effectuer la résolution de noms.</span><span class="sxs-lookup"><span data-stu-id="f51fd-148">Does not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="f51fd-149">Cet indicateur est pris en charge uniquement par le fournisseur de carnet d’adresses Exchange.</span><span class="sxs-lookup"><span data-stu-id="f51fd-149">This flag is supported only by the Exchange Address Book Provider.</span></span>
    

