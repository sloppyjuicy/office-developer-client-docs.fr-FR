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
ms.openlocfilehash: 415d108f7fd9e84ba2a9090658bc0923550390f2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347788"
---
# <a name="hropenabentrywithexchangecontext"></a><span data-ttu-id="aa639-103">HrOpenABEntryWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="aa639-103">HrOpenABEntryWithExchangeContext</span></span>

  
  
<span data-ttu-id="aa639-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aa639-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aa639-105">Ouvre la propriété **entryID** à l'aide du carnet d'adresses Exchange identifié par **pEmsmdbUID**.</span><span class="sxs-lookup"><span data-stu-id="aa639-105">Opens the **entryID** using the Exchange Address Book identified by **pEmsmdbUID**.</span></span> <span data-ttu-id="aa639-106">Cette fonction fonctionne de la même manière que [IAddrBook::D etails](iaddrbook-details.md) , sauf que l'utilisation de cette fonction garantit l'ouverture de l' [IAddrBook:: OpenEntry](iaddrbook-openentry.md) à l'aide du fournisseur de carnet d'adresses Exchange attendu.</span><span class="sxs-lookup"><span data-stu-id="aa639-106">This function works similarly to [IAddrBook::Details](iaddrbook-details.md) except that using this function ensures that the [IAddrBook::OpenEntry](iaddrbook-openentry.md) is opened by using the expected Exchange Address Book Provider.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="aa639-107">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="aa639-107">Header file:</span></span>  <br/> |<span data-ttu-id="aa639-108">abhelp. h</span><span class="sxs-lookup"><span data-stu-id="aa639-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="aa639-109">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="aa639-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="aa639-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="aa639-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="aa639-111">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="aa639-111">Called by:</span></span>  <br/> |<span data-ttu-id="aa639-112">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="aa639-112">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="aa639-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="aa639-113">Parameters</span></span>

 <span data-ttu-id="aa639-114">_pmsess_</span><span class="sxs-lookup"><span data-stu-id="aa639-114">_pmsess_</span></span>
  
> <span data-ttu-id="aa639-115">dans Le **IMAPISession**connecté.</span><span class="sxs-lookup"><span data-stu-id="aa639-115">[in] The logged on **IMAPISession**.</span></span> <span data-ttu-id="aa639-116">Il ne peut pas être NULL.</span><span class="sxs-lookup"><span data-stu-id="aa639-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="aa639-117">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="aa639-117">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="aa639-118">dans Pointeur vers un **emsmdbUID** qui identifie le service Exchange qui contient le fournisseur de carnets d'adresses Exchange que cette fonction doit utiliser pour afficher les détails sur l'identificateur d'entrée.</span><span class="sxs-lookup"><span data-stu-id="aa639-118">[in] A pointer to an **emsmdbUID** that identifies the Exchange Service that contains the Exchange Address Book Provider that this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="aa639-119">Si l'identificateur d'entrée entrante n'est pas un identificateur d'entrée de fournisseur de carnet d'adresses Exchange, ce paramètre est ignoré et l'appel de fonction se comporte comme [IAddrBook::D etails](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="aa639-119">If the incoming entry identifier is not an Exchange Address Book Provider entry identifier, this parameter is ignored and the function call behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="aa639-120">Si ce paramètre est NULL ou un zéro MAPIUID, cette fonction se comporte comme [IAddrBook::D etails](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="aa639-120">If this parameter is NULL or a zero MAPIUID, this function behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="aa639-121">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="aa639-121">_pAddrBook_</span></span>
  
> <span data-ttu-id="aa639-122">dans Carnet d'adresses utilisé pour ouvrir l'identificateur d'entrée.</span><span class="sxs-lookup"><span data-stu-id="aa639-122">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="aa639-123">Il ne peut pas être NULL.</span><span class="sxs-lookup"><span data-stu-id="aa639-123">It cannot be NULL.</span></span>
    
 <span data-ttu-id="aa639-124">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="aa639-124">_cbEntryID_</span></span>
  
> <span data-ttu-id="aa639-125">dans Nombre d'octets de l'identificateur d'entrée spécifié par le paramètre _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="aa639-125">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="aa639-126">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="aa639-126">_lpEntryID_</span></span>
  
>  <span data-ttu-id="aa639-127">dans Pointeur vers l'identificateur d'entrée qui représente l'entrée de carnet d'adresses à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="aa639-127">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span> 
    
 <span data-ttu-id="aa639-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="aa639-128">_ulFlags_</span></span>
  
> <span data-ttu-id="aa639-129">dans Masque de des indicateurs qui contrôle le mode d'ouverture de l'entrée.</span><span class="sxs-lookup"><span data-stu-id="aa639-129">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="aa639-130">Les indicateurs suivants peuvent être définis:</span><span class="sxs-lookup"><span data-stu-id="aa639-130">The following flags can be set:</span></span>
    
<span data-ttu-id="aa639-131">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="aa639-131">MAPI_BEST_ACCESS</span></span>
  
> <span data-ttu-id="aa639-132">Demande que l'entrée soit ouverte avec les autorisations réseau et client maximales autorisées.</span><span class="sxs-lookup"><span data-stu-id="aa639-132">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="aa639-133">Par exemple, si le client dispose d'une autorisation en lecture et en écriture, le fournisseur de carnet d'adresses tente d'ouvrir l'entrée avec une autorisation en lecture et en écriture.</span><span class="sxs-lookup"><span data-stu-id="aa639-133">For example, if the client has read and write permission, the address book provider attempts to open the entry with read and write permission.</span></span> <span data-ttu-id="aa639-134">Le client peut récupérer le niveau d'accès qui a été accordé en appelant la méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) de l'entrée ouverte et en récupérant la propriété PR_ACCESS_LEVEL (PidTagAccessLevel).</span><span class="sxs-lookup"><span data-stu-id="aa639-134">The client can retrieve the access level that was granted by calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method of the open entry and retrieving the PR_ACCESS_LEVEL (PidTagAccessLevel) property.</span></span> 
    
<span data-ttu-id="aa639-135">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="aa639-135">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="aa639-136">Utilise uniquement le carnet d'adresses en mode hors connexion pour effectuer la résolution de noms.</span><span class="sxs-lookup"><span data-stu-id="aa639-136">Uses only the offline address book to perform name resolution.</span></span> <span data-ttu-id="aa639-137">Par exemple, vous pouvez utiliser cet indicateur pour permettre à une application cliente d'ouvrir la liste d'adresses globale (LAG) en mode Exchange mis en cache et d'accéder à une entrée de ce carnet d'adresses à partir du cache sans créer de trafic entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="aa639-137">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="aa639-138">Cet indicateur est pris en charge uniquement par le fournisseur de carnet d'adresses Exchange.</span><span class="sxs-lookup"><span data-stu-id="aa639-138">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="aa639-139">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="aa639-139">MAPI_DEFERRED_ERRORS</span></span>
  
> <span data-ttu-id="aa639-140">Permet à l'appel de réussir, éventuellement avant que l'entrée soit entièrement ouverte et disponible, ce qui implique que des appels ultérieurs à l'entrée renvoient une erreur.</span><span class="sxs-lookup"><span data-stu-id="aa639-140">Allows the call to succeed, potentially before the entry is fully open and available, implying that subsequent calls to the entry might return an error.</span></span>
    
<span data-ttu-id="aa639-141">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="aa639-141">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="aa639-142">Utilise uniquement la liste d'adresses globale pour effectuer la résolution de noms.</span><span class="sxs-lookup"><span data-stu-id="aa639-142">Uses only the GAL to perform name resolution.</span></span> <span data-ttu-id="aa639-143">Cet indicateur est pris en charge uniquement par le fournisseur de carnet d'adresses Exchange.</span><span class="sxs-lookup"><span data-stu-id="aa639-143">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="aa639-144">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="aa639-144">MAPI_MODIFY</span></span>
  
> <span data-ttu-id="aa639-145">Demande que l'entrée soit ouverte avec une autorisation en lecture et en écriture.</span><span class="sxs-lookup"><span data-stu-id="aa639-145">Requests that the entry be opened with read and write permission.</span></span> <span data-ttu-id="aa639-146">Étant donné que les entrées sont ouvertes avec un accès en lecture seule par défaut, les clients ne doivent pas supposer que l'autorisation de lecture et d'écriture a été accordée, que MAPI_MODIFY soit défini ou non.</span><span class="sxs-lookup"><span data-stu-id="aa639-146">Because entries are opened with read-only access by default, clients should not assume that read and write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="aa639-147">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="aa639-147">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="aa639-148">N'utilise pas le carnet d'adresses en mode hors connexion pour effectuer la résolution de noms.</span><span class="sxs-lookup"><span data-stu-id="aa639-148">Does not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="aa639-149">Cet indicateur est pris en charge uniquement par le fournisseur de carnet d'adresses Exchange.</span><span class="sxs-lookup"><span data-stu-id="aa639-149">This flag is supported only by the Exchange Address Book Provider.</span></span>
    

