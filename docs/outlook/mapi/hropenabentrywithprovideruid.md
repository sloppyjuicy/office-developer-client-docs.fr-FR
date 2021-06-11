---
title: HrOpenABEntryWithProviderUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 83821a86-abff-460c-bb8e-9fd9d232dc6b
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 20344185ffcbd90017fa3c3493218bd9b3ddfd74
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408893"
---
# <a name="hropenabentrywithprovideruid"></a><span data-ttu-id="4c3a4-103">HrOpenABEntryWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="4c3a4-103">HrOpenABEntryWithProviderUID</span></span>

  
  
<span data-ttu-id="4c3a4-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4c3a4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4c3a4-105">Ouvre **l’entryID à** l’aide Exchange carnet d’adresses identifié par _pEmsabpUID_.</span><span class="sxs-lookup"><span data-stu-id="4c3a4-105">Opens the **entryID** using the Exchange Address Book identified by  _pEmsabpUID_.</span></span> <span data-ttu-id="4c3a4-106">Cette fonction fonctionne de la même manière que [IAddrBook::OpenEntry,](iaddrbook-openentry.md) sauf que l’utilisation de cette fonction garantit que [IAddrBook::OpenEntry](iaddrbook-openentry.md) est ouvert à l’aide du fournisseur de carnet d’adresses Exchange attendu.</span><span class="sxs-lookup"><span data-stu-id="4c3a4-106">This function works similarly to [IAddrBook::OpenEntry](iaddrbook-openentry.md) except that using this function ensures that [IAddrBook::OpenEntry](iaddrbook-openentry.md) is opened by using the expected Exchange Address Book provider.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4c3a4-107">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="4c3a4-107">Header file:</span></span>  <br/> |<span data-ttu-id="4c3a4-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="4c3a4-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="4c3a4-109">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="4c3a4-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="4c3a4-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="4c3a4-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="4c3a4-111">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="4c3a4-111">Called by:</span></span>  <br/> |<span data-ttu-id="4c3a4-112">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="4c3a4-112">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="4c3a4-113">Parameters</span><span class="sxs-lookup"><span data-stu-id="4c3a4-113">Parameters</span></span>

 <span data-ttu-id="4c3a4-114">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="4c3a4-114">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="4c3a4-115">[in] Pointeur vers **un élément emsmdbUID** qui identifie le service Exchange qui contient le fournisseur de carnet d’adresses Exchange que cette fonction doit utiliser pour afficher des détails sur l’identificateur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="4c3a4-115">[in] A pointer to an **emsmdbUID** that identifies the Exchange Service that contains the Exchange Address Book Provider that this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="4c3a4-116">Si l’identificateur d’entrée entrante n’est pas un identificateur d’entrée du fournisseur de carnet d’adresses Exchange, ce paramètre est ignoré et l’appel de fonction se comporte comme [IAddrBook::D etails](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="4c3a4-116">If the incoming entry identifier is not an Exchange Address Book Provider entry identifier, this parameter is ignored and the function call behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="4c3a4-117">Si ce paramètre est NULL ou un MAPIUID zéro, cette fonction se comporte comme [IAddrBook::D etails](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="4c3a4-117">If this parameter is NULL or a zero MAPIUID, this function behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="4c3a4-118">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="4c3a4-118">_pAddrBook_</span></span>
  
> <span data-ttu-id="4c3a4-119">[in] Carnet d’adresses utilisé pour ouvrir l’identificateur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="4c3a4-119">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="4c3a4-120">Elle ne peut pas être NULL.</span><span class="sxs-lookup"><span data-stu-id="4c3a4-120">It cannot be NULL.</span></span>
    
 <span data-ttu-id="4c3a4-121">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="4c3a4-121">_cbEntryID_</span></span>
  
> <span data-ttu-id="4c3a4-122">[in] Nombre d’bytes de l’identificateur d’entrée spécifié par _le paramètre lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="4c3a4-122">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="4c3a4-123">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="4c3a4-123">_lpEntryID_</span></span>
  
>  <span data-ttu-id="4c3a4-124">[in] Pointeur vers l’identificateur d’entrée qui représente l’entrée de carnet d’adresses à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="4c3a4-124">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span> 
    
 <span data-ttu-id="4c3a4-125">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="4c3a4-125">_lpInterface_</span></span>
  
> <span data-ttu-id="4c3a4-126">[in] Pointeur vers l’identificateur d’interface (IID) de l’interface utilisée pour accéder à l’entrée ouverte.</span><span class="sxs-lookup"><span data-stu-id="4c3a4-126">[in] A pointer to the interface identifier (IID) of the interface that is used to access the open entry.</span></span> <span data-ttu-id="4c3a4-127">La transmission NULL renvoie l’interface standard de l’objet.</span><span class="sxs-lookup"><span data-stu-id="4c3a4-127">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="4c3a4-128">Pour les utilisateurs de messagerie, l’interface standard [est IMailUser : IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="4c3a4-128">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="4c3a4-129">Pour les listes de distribution, il s’agit de [IDistList : IMAPIContainer](idistlistimapicontainer.md)et pour les conteneurs, il s’agit de [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="4c3a4-129">For distribution lists, it is [IDistList : IMAPIContainer](idistlistimapicontainer.md)and for containers, it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="4c3a4-130">Les appelants peuvent définir  _lpInterface_ sur l’interface standard appropriée ou une interface dans la hiérarchie d’héritage.</span><span class="sxs-lookup"><span data-stu-id="4c3a4-130">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="4c3a4-131">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4c3a4-131">_ulFlags_</span></span>
  
> <span data-ttu-id="4c3a4-132">[in] Masque de bits d’indicateurs qui contrôle la façon dont l’entrée est ouverte, les indicateurs suivants peuvent être définies :</span><span class="sxs-lookup"><span data-stu-id="4c3a4-132">[in] A bitmask of flags that controls the how the entry is opened, The following flags can be set:</span></span>
    
<span data-ttu-id="4c3a4-133">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="4c3a4-133">MAPI_BEST_ACCESS</span></span>
  
> <span data-ttu-id="4c3a4-134">Demande l’ouverture de l’entrée avec le nombre maximal d’autorisations réseau et client autorisées.</span><span class="sxs-lookup"><span data-stu-id="4c3a4-134">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="4c3a4-135">Par exemple, si le client dispose d’autorisations de lecture et d’écriture, le fournisseur de carnet d’adresses tente d’ouvrir l’entrée avec des autorisations de lecture et d’écriture.</span><span class="sxs-lookup"><span data-stu-id="4c3a4-135">For example, if the client has read and write permission, the address book provider attempts to open the entry with read and write permission.</span></span> <span data-ttu-id="4c3a4-136">Le client peut récupérer le niveau d’accès accordé en appelant la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) de l’entrée ouverte et en récupérant la propriété PR_ACCESS_LEVEL (PidTagAccessLevel).</span><span class="sxs-lookup"><span data-stu-id="4c3a4-136">The client can retrieve the access level that was granted by calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method of the open entry and retrieving the PR_ACCESS_LEVEL (PidTagAccessLevel) property.</span></span> 
    
<span data-ttu-id="4c3a4-137">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="4c3a4-137">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="4c3a4-138">Utilisez uniquement le carnet d’adresses en mode hors connexion pour effectuer la résolution de noms.</span><span class="sxs-lookup"><span data-stu-id="4c3a4-138">Use only the offline address book to perform name resolution.</span></span> <span data-ttu-id="4c3a4-139">Par exemple, vous pouvez utiliser cet indicateur pour permettre à une application cliente d’ouvrir la liste d’adresses globale (LAL) en mode Exchange mis en cache et d’accéder à une entrée dans ce carnet d’adresses à partir du cache sans créer de trafic entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="4c3a4-139">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="4c3a4-140">Cet indicateur est pris en charge uniquement par le Exchange de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="4c3a4-140">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="4c3a4-141">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="4c3a4-141">MAPI_DEFERRED_ERRORS</span></span>
  
> <span data-ttu-id="4c3a4-142">Permet de réussir l’appel, éventuellement avant que l’entrée soit entièrement ouverte et disponible, ce qui signifie que les appels ultérieurs à l’entrée peuvent renvoyer une erreur.</span><span class="sxs-lookup"><span data-stu-id="4c3a4-142">Allows the call to succeed, potentially before the entry is fully open and available, implying that subsequent calls to the entry might return an error.</span></span>
    
<span data-ttu-id="4c3a4-143">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="4c3a4-143">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="4c3a4-144">Utilisez uniquement la LA GAL pour effectuer la résolution de noms.</span><span class="sxs-lookup"><span data-stu-id="4c3a4-144">Use only the GAL to perform name resolution.</span></span> <span data-ttu-id="4c3a4-145">Cet indicateur est pris en charge uniquement par le Exchange de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="4c3a4-145">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="4c3a4-146">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="4c3a4-146">MAPI_MODIFY</span></span>
  
> <span data-ttu-id="4c3a4-147">Demande l’ouverture de l’entrée avec une autorisation de lecture et d’écriture.</span><span class="sxs-lookup"><span data-stu-id="4c3a4-147">Requests that the entry be opened with read and write permission.</span></span> <span data-ttu-id="4c3a4-148">Étant donné que les entrées sont ouvertes avec un accès en lecture seule par défaut, les clients ne doivent pas supposer que l’autorisation de lecture et d’écriture a été accordée, qu’MAPI_MODIFY soit définie ou non.</span><span class="sxs-lookup"><span data-stu-id="4c3a4-148">Because entries are opened with read-only access by default, clients should not assume that read and write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="4c3a4-149">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="4c3a4-149">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="4c3a4-150">N’utilisez pas le carnet d’adresses en mode hors connexion pour effectuer la résolution de noms.</span><span class="sxs-lookup"><span data-stu-id="4c3a4-150">Do not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="4c3a4-151">Cet indicateur est pris en charge uniquement par le Exchange de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="4c3a4-151">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
 <span data-ttu-id="4c3a4-152">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="4c3a4-152">_lpulObjType_</span></span>
  
> <span data-ttu-id="4c3a4-153">[out] Pointeur vers le type de l’entrée ouverte.</span><span class="sxs-lookup"><span data-stu-id="4c3a4-153">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="4c3a4-154">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="4c3a4-154">_lppUnk_</span></span>
  
> <span data-ttu-id="4c3a4-155">[out] Pointeur vers un pointeur de l’entrée ouverte.</span><span class="sxs-lookup"><span data-stu-id="4c3a4-155">[out] A pointer to a pointer of the opened entry.</span></span>
    

