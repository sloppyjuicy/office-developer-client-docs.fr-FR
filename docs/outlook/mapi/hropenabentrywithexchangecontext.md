---
title: HrOpenABEntryWithExchangeContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b640a5aa-4e36-4983-bf11-9428809e830b
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: fcedaf689db8280b4649662ba61c8468d0f98305
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783552"
---
# <a name="hropenabentrywithexchangecontext"></a><span data-ttu-id="52f54-103">HrOpenABEntryWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="52f54-103">HrOpenABEntryWithExchangeContext</span></span>

  
  
<span data-ttu-id="52f54-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="52f54-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="52f54-105">Ouvre l' **ID d’entrée** à l’aide du carnet d’adresses Exchange identifié par **pEmsmdbUID**.</span><span class="sxs-lookup"><span data-stu-id="52f54-105">Opens the **entryID** using the Exchange Address Book identified by **pEmsmdbUID**.</span></span> <span data-ttu-id="52f54-106">Cette fonction fonctionne comme [IAddrBook::Details](iaddrbook-details.md) , sauf que l’utilisation de cette fonction garantit que [IAddrBook::OpenEntry](iaddrbook-openentry.md) est ouvert à l’aide du fournisseur de carnet d’adresses Exchange attendue.</span><span class="sxs-lookup"><span data-stu-id="52f54-106">This function works similarly to [IAddrBook::Details](iaddrbook-details.md) except that using this function ensures that the [IAddrBook::OpenEntry](iaddrbook-openentry.md) is opened by using the expected Exchange Address Book Provider.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="52f54-107">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="52f54-107">Header file:</span></span>  <br/> |<span data-ttu-id="52f54-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="52f54-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="52f54-109">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="52f54-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="52f54-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="52f54-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="52f54-111">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="52f54-111">Called by:</span></span>  <br/> |<span data-ttu-id="52f54-112">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="52f54-112">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="52f54-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="52f54-113">Parameters</span></span>

 <span data-ttu-id="52f54-114">_pmsess_</span><span class="sxs-lookup"><span data-stu-id="52f54-114">_pmsess_</span></span>
  
> <span data-ttu-id="52f54-115">[in] La session **IMAPISession**.</span><span class="sxs-lookup"><span data-stu-id="52f54-115">[in] The logged on **IMAPISession**.</span></span> <span data-ttu-id="52f54-116">Il ne peut pas être NULL.</span><span class="sxs-lookup"><span data-stu-id="52f54-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="52f54-117">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="52f54-117">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="52f54-118">[in] Pointeur vers un **emsmdbUID** qui identifie le Service Exchange qui contient le fournisseur de carnet d’adresses Exchange que cette fonction doit utiliser pour afficher plus d’informations sur l’identificateur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="52f54-118">[in] A pointer to an **emsmdbUID** that identifies the Exchange Service that contains the Exchange Address Book Provider that this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="52f54-119">Si l’identificateur d’entrée entrant n’est pas un identificateur d’entrée de carnet d’adresses Exchange, ce paramètre est ignoré et l’appel de fonction se comporte comme [IAddrBook::Details](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="52f54-119">If the incoming entry identifier is not an Exchange Address Book Provider entry identifier, this parameter is ignored and the function call behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="52f54-120">Si ce paramètre est NULL ou un zéro MAPIUID, cette fonction se comporte comme [IAddrBook::Details](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="52f54-120">If this parameter is NULL or a zero MAPIUID, this function behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="52f54-121">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="52f54-121">_pAddrBook_</span></span>
  
> <span data-ttu-id="52f54-122">[in] Le carnet d’adresses utilisée pour ouvrir l’identificateur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="52f54-122">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="52f54-123">Il ne peut pas être NULL.</span><span class="sxs-lookup"><span data-stu-id="52f54-123">It cannot be NULL.</span></span>
    
 <span data-ttu-id="52f54-124">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="52f54-124">_cbEntryID_</span></span>
  
> <span data-ttu-id="52f54-125">[in] Nombre d’octets de l’identificateur d’entrée spécifié par le paramètre _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="52f54-125">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="52f54-126">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="52f54-126">_lpEntryID_</span></span>
  
>  <span data-ttu-id="52f54-127">[in] Pointeur vers l’identificateur d’entrée qui représente l’entrée du carnet d’adresses à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="52f54-127">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span> 
    
 <span data-ttu-id="52f54-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="52f54-128">_ulFlags_</span></span>
  
> <span data-ttu-id="52f54-129">[in] Masque de bits d’indicateurs qui contrôle la façon dont l’entrée est ouvert.</span><span class="sxs-lookup"><span data-stu-id="52f54-129">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="52f54-130">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="52f54-130">The following flags can be set:</span></span>
    
<span data-ttu-id="52f54-131">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="52f54-131">MAPI_BEST_ACCESS</span></span>
  
> <span data-ttu-id="52f54-132">Demandes que l’entrée s’ouvre avec les autorisations maximales autorisées réseau et le client.</span><span class="sxs-lookup"><span data-stu-id="52f54-132">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="52f54-133">Par exemple, si le client dispose de lecture et l’autorisation d’écriture, le fournisseur de carnet d’adresses essaie ouvrir l’entrée en lecture et l’autorisation d’écriture.</span><span class="sxs-lookup"><span data-stu-id="52f54-133">For example, if the client has read and write permission, the address book provider attempts to open the entry with read and write permission.</span></span> <span data-ttu-id="52f54-134">Le client peut extraire le niveau d’accès qui a été accordé en appelant la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) de l’écriture ouverte et de récupération de la propriété PR_ACCESS_LEVEL (PidTagAccessLevel).</span><span class="sxs-lookup"><span data-stu-id="52f54-134">The client can retrieve the access level that was granted by calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method of the open entry and retrieving the PR_ACCESS_LEVEL (PidTagAccessLevel) property.</span></span> 
    
<span data-ttu-id="52f54-135">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="52f54-135">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="52f54-136">Utilise uniquement le carnet d’adresses en mode hors connexion pour effectuer la résolution de noms.</span><span class="sxs-lookup"><span data-stu-id="52f54-136">Uses only the offline address book to perform name resolution.</span></span> <span data-ttu-id="52f54-137">Par exemple, vous pouvez utiliser cet indicateur pour autoriser une application cliente ouvrir la liste d’adresses globale (LAG) en mode exchange mis en cache et accéder à une entrée dans ce carnet d’adresses à partir du cache sans créer le trafic entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="52f54-137">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="52f54-138">Cet indicateur est pris en charge uniquement par le fournisseur de carnet d’adresses Exchange.</span><span class="sxs-lookup"><span data-stu-id="52f54-138">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="52f54-139">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="52f54-139">MAPI_DEFERRED_ERRORS</span></span>
  
> <span data-ttu-id="52f54-140">Permet l’appel aboutisse, potentiellement avant que l’entrée est entièrement ouverte et disponible, ce qui implique que les appels suivants à l’entrée renverra une erreur.</span><span class="sxs-lookup"><span data-stu-id="52f54-140">Allows the call to succeed, potentially before the entry is fully open and available, implying that subsequent calls to the entry might return an error.</span></span>
    
<span data-ttu-id="52f54-141">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="52f54-141">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="52f54-142">Utilise uniquement la liste d’adresses globale pour effectuer la résolution de noms.</span><span class="sxs-lookup"><span data-stu-id="52f54-142">Uses only the GAL to perform name resolution.</span></span> <span data-ttu-id="52f54-143">Cet indicateur est pris en charge uniquement par le fournisseur de carnet d’adresses Exchange.</span><span class="sxs-lookup"><span data-stu-id="52f54-143">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="52f54-144">N'</span><span class="sxs-lookup"><span data-stu-id="52f54-144">MAPI_MODIFY</span></span>
  
> <span data-ttu-id="52f54-145">Demandes ouvrir avec l’entrée de lire et écrire des autorisations.</span><span class="sxs-lookup"><span data-stu-id="52f54-145">Requests that the entry be opened with read and write permission.</span></span> <span data-ttu-id="52f54-146">Étant donné que les entrées sont ouvertes avec accès en lecture seule par défaut, les clients ne doivent pas supposer que lire et écrire l’autorisation a été accordée même si n’est définie.</span><span class="sxs-lookup"><span data-stu-id="52f54-146">Because entries are opened with read-only access by default, clients should not assume that read and write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="52f54-147">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="52f54-147">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="52f54-148">N’utilise pas le carnet d’adresses en mode hors connexion pour effectuer la résolution de noms.</span><span class="sxs-lookup"><span data-stu-id="52f54-148">Does not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="52f54-149">Cet indicateur est pris en charge uniquement par le fournisseur de carnet d’adresses Exchange.</span><span class="sxs-lookup"><span data-stu-id="52f54-149">This flag is supported only by the Exchange Address Book Provider.</span></span>
    

