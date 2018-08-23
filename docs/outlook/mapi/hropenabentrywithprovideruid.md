---
title: HrOpenABEntryWithProviderUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 83821a86-abff-460c-bb8e-9fd9d232dc6b
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: ed68e1fdb7fb990a2c19aa0bd263439c0966231d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578205"
---
# <a name="hropenabentrywithprovideruid"></a><span data-ttu-id="e5be9-103">HrOpenABEntryWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="e5be9-103">HrOpenABEntryWithProviderUID</span></span>

  
  
<span data-ttu-id="e5be9-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e5be9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e5be9-105">Ouvre l' **ID d’entrée** à l’aide du carnet d’adresses Exchange identifié par _pEmsabpUID_.</span><span class="sxs-lookup"><span data-stu-id="e5be9-105">Opens the **entryID** using the Exchange Address Book identified by  _pEmsabpUID_.</span></span> <span data-ttu-id="e5be9-106">Cette fonction fonctionne comme [IAddrBook::OpenEntry](iaddrbook-openentry.md) , sauf que l’utilisation de cette fonction garantit que [IAddrBook::OpenEntry](iaddrbook-openentry.md) est ouvert à l’aide du fournisseur de carnet d’adresses Exchange attendu.</span><span class="sxs-lookup"><span data-stu-id="e5be9-106">This function works similarly to [IAddrBook::OpenEntry](iaddrbook-openentry.md) except that using this function ensures that [IAddrBook::OpenEntry](iaddrbook-openentry.md) is opened by using the expected Exchange Address Book provider.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e5be9-107">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="e5be9-107">Header file:</span></span>  <br/> |<span data-ttu-id="e5be9-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="e5be9-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="e5be9-109">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="e5be9-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="e5be9-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="e5be9-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="e5be9-111">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="e5be9-111">Called by:</span></span>  <br/> |<span data-ttu-id="e5be9-112">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="e5be9-112">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrOpenABEntryWithProviderUID(
  const MAPIUID *pEmsabpUID,
  LPADRBOOK pAddrBook,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a><span data-ttu-id="e5be9-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e5be9-113">Parameters</span></span>

 <span data-ttu-id="e5be9-114">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="e5be9-114">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="e5be9-115">[in] Pointeur vers un **emsmdbUID** qui identifie le Service Exchange qui contient le fournisseur de carnet d’adresses Exchange que cette fonction doit utiliser pour afficher plus d’informations sur l’identificateur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="e5be9-115">[in] A pointer to an **emsmdbUID** that identifies the Exchange Service that contains the Exchange Address Book Provider that this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="e5be9-116">Si l’identificateur d’entrée entrant n’est pas un identificateur d’entrée de carnet d’adresses Exchange, ce paramètre est ignoré et l’appel de fonction se comporte comme [IAddrBook::Details](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="e5be9-116">If the incoming entry identifier is not an Exchange Address Book Provider entry identifier, this parameter is ignored and the function call behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="e5be9-117">Si ce paramètre est NULL ou un zéro MAPIUID, cette fonction se comporte comme [IAddrBook::Details](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="e5be9-117">If this parameter is NULL or a zero MAPIUID, this function behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="e5be9-118">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="e5be9-118">_pAddrBook_</span></span>
  
> <span data-ttu-id="e5be9-119">[in] Le carnet d’adresses utilisée pour ouvrir l’identificateur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="e5be9-119">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="e5be9-120">Il ne peut pas être NULL.</span><span class="sxs-lookup"><span data-stu-id="e5be9-120">It cannot be NULL.</span></span>
    
 <span data-ttu-id="e5be9-121">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="e5be9-121">_cbEntryID_</span></span>
  
> <span data-ttu-id="e5be9-122">[in] Nombre d’octets de l’identificateur d’entrée spécifié par le paramètre _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="e5be9-122">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="e5be9-123">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="e5be9-123">_lpEntryID_</span></span>
  
>  <span data-ttu-id="e5be9-124">[in] Pointeur vers l’identificateur d’entrée qui représente l’entrée du carnet d’adresses à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="e5be9-124">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span> 
    
 <span data-ttu-id="e5be9-125">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="e5be9-125">_lpInterface_</span></span>
  
> <span data-ttu-id="e5be9-126">[in] Pointeur vers l’identificateur d’interface (IID) de l’interface qui est utilisée pour accéder à l’entrée open.</span><span class="sxs-lookup"><span data-stu-id="e5be9-126">[in] A pointer to the interface identifier (IID) of the interface that is used to access the open entry.</span></span> <span data-ttu-id="e5be9-127">Passage de NULL renvoie l’interface standard de l’objet.</span><span class="sxs-lookup"><span data-stu-id="e5be9-127">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="e5be9-128">Pour les utilisateurs de messagerie, l’interface standard est [IMailUser : IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="e5be9-128">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="e5be9-129">Pour les listes de distribution, il est [IDistList : IMAPIContainer](idistlistimapicontainer.md)et pour les conteneurs, il est [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="e5be9-129">For distribution lists, it is [IDistList : IMAPIContainer](idistlistimapicontainer.md)and for containers, it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="e5be9-130">Les appelants peuvent définir _lpInterface_ à l’interface standard ou d’une interface dans la hiérarchie d’héritage.</span><span class="sxs-lookup"><span data-stu-id="e5be9-130">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="e5be9-131">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e5be9-131">_ulFlags_</span></span>
  
> <span data-ttu-id="e5be9-132">[in] Un masque de bits d’indicateurs qui contrôle la façon dont l’entrée est ouvert, les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="e5be9-132">[in] A bitmask of flags that controls the how the entry is opened, The following flags can be set:</span></span>
    
<span data-ttu-id="e5be9-133">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="e5be9-133">MAPI_BEST_ACCESS</span></span>
  
> <span data-ttu-id="e5be9-134">Demandes que l’entrée s’ouvre avec les autorisations maximales autorisées réseau et le client.</span><span class="sxs-lookup"><span data-stu-id="e5be9-134">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="e5be9-135">Par exemple, si le client dispose de lecture et l’autorisation d’écriture, le fournisseur de carnet d’adresses essaie ouvrir l’entrée en lecture et l’autorisation d’écriture.</span><span class="sxs-lookup"><span data-stu-id="e5be9-135">For example, if the client has read and write permission, the address book provider attempts to open the entry with read and write permission.</span></span> <span data-ttu-id="e5be9-136">Le client peut extraire le niveau d’accès qui a été accordé en appelant la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) de l’écriture ouverte et de récupération de la propriété PR_ACCESS_LEVEL (PidTagAccessLevel).</span><span class="sxs-lookup"><span data-stu-id="e5be9-136">The client can retrieve the access level that was granted by calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method of the open entry and retrieving the PR_ACCESS_LEVEL (PidTagAccessLevel) property.</span></span> 
    
<span data-ttu-id="e5be9-137">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="e5be9-137">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="e5be9-138">Utilisez uniquement le carnet d’adresses en mode hors connexion pour effectuer la résolution de noms.</span><span class="sxs-lookup"><span data-stu-id="e5be9-138">Use only the offline address book to perform name resolution.</span></span> <span data-ttu-id="e5be9-139">Par exemple, vous pouvez utiliser cet indicateur pour autoriser une application cliente ouvrir la liste d’adresses globale (LAG) en mode exchange mis en cache et accéder à une entrée dans ce carnet d’adresses à partir du cache sans créer le trafic entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="e5be9-139">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="e5be9-140">Cet indicateur est pris en charge uniquement par le fournisseur de carnet d’adresses Exchange.</span><span class="sxs-lookup"><span data-stu-id="e5be9-140">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="e5be9-141">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="e5be9-141">MAPI_DEFERRED_ERRORS</span></span>
  
> <span data-ttu-id="e5be9-142">Permet l’appel aboutisse, potentiellement avant que l’entrée est entièrement ouverte et disponible, ce qui implique que les appels suivants à l’entrée renverra une erreur.</span><span class="sxs-lookup"><span data-stu-id="e5be9-142">Allows the call to succeed, potentially before the entry is fully open and available, implying that subsequent calls to the entry might return an error.</span></span>
    
<span data-ttu-id="e5be9-143">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="e5be9-143">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="e5be9-144">Utiliser uniquement la liste d’adresses globale pour effectuer la résolution de noms.</span><span class="sxs-lookup"><span data-stu-id="e5be9-144">Use only the GAL to perform name resolution.</span></span> <span data-ttu-id="e5be9-145">Cet indicateur est pris en charge uniquement par le fournisseur de carnet d’adresses Exchange.</span><span class="sxs-lookup"><span data-stu-id="e5be9-145">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="e5be9-146">N'</span><span class="sxs-lookup"><span data-stu-id="e5be9-146">MAPI_MODIFY</span></span>
  
> <span data-ttu-id="e5be9-147">Demandes ouvrir avec l’entrée de lire et écrire des autorisations.</span><span class="sxs-lookup"><span data-stu-id="e5be9-147">Requests that the entry be opened with read and write permission.</span></span> <span data-ttu-id="e5be9-148">Étant donné que les entrées sont ouvertes avec accès en lecture seule par défaut, les clients ne doivent pas supposer que lire et écrire l’autorisation a été accordée même si n’est définie.</span><span class="sxs-lookup"><span data-stu-id="e5be9-148">Because entries are opened with read-only access by default, clients should not assume that read and write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="e5be9-149">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="e5be9-149">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="e5be9-150">N’utilisez pas le carnet d’adresses en mode hors connexion pour effectuer la résolution de noms.</span><span class="sxs-lookup"><span data-stu-id="e5be9-150">Do not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="e5be9-151">Cet indicateur est pris en charge uniquement par le fournisseur de carnet d’adresses Exchange.</span><span class="sxs-lookup"><span data-stu-id="e5be9-151">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
 <span data-ttu-id="e5be9-152">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="e5be9-152">_lpulObjType_</span></span>
  
> <span data-ttu-id="e5be9-153">[out] Pointeur vers le type de l’entrée ouvert.</span><span class="sxs-lookup"><span data-stu-id="e5be9-153">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="e5be9-154">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="e5be9-154">_lppUnk_</span></span>
  
> <span data-ttu-id="e5be9-155">[out] Pointeur vers un pointeur de l’entrée ouvert.</span><span class="sxs-lookup"><span data-stu-id="e5be9-155">[out] A pointer to a pointer of the opened entry.</span></span>
    

