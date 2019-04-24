---
title: HrOpenABEntryWithProviderUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 83821a86-abff-460c-bb8e-9fd9d232dc6b
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 20344185ffcbd90017fa3c3493218bd9b3ddfd74
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347816"
---
# <a name="hropenabentrywithprovideruid"></a><span data-ttu-id="0644a-103">HrOpenABEntryWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="0644a-103">HrOpenABEntryWithProviderUID</span></span>

  
  
<span data-ttu-id="0644a-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0644a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0644a-105">Ouvre la propriété **entryID** à l'aide du carnet d'adresses Exchange identifié par _pEmsabpUID_.</span><span class="sxs-lookup"><span data-stu-id="0644a-105">Opens the **entryID** using the Exchange Address Book identified by  _pEmsabpUID_.</span></span> <span data-ttu-id="0644a-106">Cette fonction fonctionne de la même manière que [IAddrBook:: OpenEntry](iaddrbook-openentry.md) à l'exception du fait que l'utilisation de cette fonction garantit l'ouverture de [IAddrBook:: OpenEntry](iaddrbook-openentry.md) à l'aide du fournisseur de carnet d'adresses Exchange attendu.</span><span class="sxs-lookup"><span data-stu-id="0644a-106">This function works similarly to [IAddrBook::OpenEntry](iaddrbook-openentry.md) except that using this function ensures that [IAddrBook::OpenEntry](iaddrbook-openentry.md) is opened by using the expected Exchange Address Book provider.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0644a-107">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="0644a-107">Header file:</span></span>  <br/> |<span data-ttu-id="0644a-108">abhelp. h</span><span class="sxs-lookup"><span data-stu-id="0644a-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="0644a-109">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="0644a-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="0644a-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="0644a-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="0644a-111">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="0644a-111">Called by:</span></span>  <br/> |<span data-ttu-id="0644a-112">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="0644a-112">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="0644a-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0644a-113">Parameters</span></span>

 <span data-ttu-id="0644a-114">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="0644a-114">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="0644a-115">dans Pointeur vers un **emsmdbUID** qui identifie le service Exchange qui contient le fournisseur de carnets d'adresses Exchange que cette fonction doit utiliser pour afficher les détails sur l'identificateur d'entrée.</span><span class="sxs-lookup"><span data-stu-id="0644a-115">[in] A pointer to an **emsmdbUID** that identifies the Exchange Service that contains the Exchange Address Book Provider that this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="0644a-116">Si l'identificateur d'entrée entrante n'est pas un identificateur d'entrée de fournisseur de carnet d'adresses Exchange, ce paramètre est ignoré et l'appel de fonction se comporte comme [IAddrBook::D etails](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="0644a-116">If the incoming entry identifier is not an Exchange Address Book Provider entry identifier, this parameter is ignored and the function call behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="0644a-117">Si ce paramètre est NULL ou un zéro MAPIUID, cette fonction se comporte comme [IAddrBook::D etails](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="0644a-117">If this parameter is NULL or a zero MAPIUID, this function behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="0644a-118">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="0644a-118">_pAddrBook_</span></span>
  
> <span data-ttu-id="0644a-119">dans Carnet d'adresses utilisé pour ouvrir l'identificateur d'entrée.</span><span class="sxs-lookup"><span data-stu-id="0644a-119">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="0644a-120">Il ne peut pas être NULL.</span><span class="sxs-lookup"><span data-stu-id="0644a-120">It cannot be NULL.</span></span>
    
 <span data-ttu-id="0644a-121">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="0644a-121">_cbEntryID_</span></span>
  
> <span data-ttu-id="0644a-122">dans Nombre d'octets de l'identificateur d'entrée spécifié par le paramètre _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="0644a-122">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="0644a-123">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="0644a-123">_lpEntryID_</span></span>
  
>  <span data-ttu-id="0644a-124">dans Pointeur vers l'identificateur d'entrée qui représente l'entrée de carnet d'adresses à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="0644a-124">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span> 
    
 <span data-ttu-id="0644a-125">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="0644a-125">_lpInterface_</span></span>
  
> <span data-ttu-id="0644a-126">dans Pointeur vers l'identificateur d'interface (IID) de l'interface qui est utilisé pour accéder à l'entrée ouverte.</span><span class="sxs-lookup"><span data-stu-id="0644a-126">[in] A pointer to the interface identifier (IID) of the interface that is used to access the open entry.</span></span> <span data-ttu-id="0644a-127">Le passage de la valeur NULL renvoie l'interface standard de l'objet.</span><span class="sxs-lookup"><span data-stu-id="0644a-127">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="0644a-128">Pour les utilisateurs de messagerie, l'interface standard est [IMailUser: IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="0644a-128">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="0644a-129">Pour les listes de distribution, il s'agit de [IDistList: IMAPIContainer](idistlistimapicontainer.md)et pour les conteneurs, il s'agit de [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="0644a-129">For distribution lists, it is [IDistList : IMAPIContainer](idistlistimapicontainer.md)and for containers, it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="0644a-130">Les appelants peuvent définir _lpInterface_ sur l'interface standard appropriée ou une interface dans la hiérarchie d'héritage.</span><span class="sxs-lookup"><span data-stu-id="0644a-130">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="0644a-131">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0644a-131">_ulFlags_</span></span>
  
> <span data-ttu-id="0644a-132">dans Un masque de réindicateur des indicateurs qui contrôle le mode d'ouverture de l'entrée, les indicateurs suivants peuvent être définis:</span><span class="sxs-lookup"><span data-stu-id="0644a-132">[in] A bitmask of flags that controls the how the entry is opened, The following flags can be set:</span></span>
    
<span data-ttu-id="0644a-133">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="0644a-133">MAPI_BEST_ACCESS</span></span>
  
> <span data-ttu-id="0644a-134">Demande que l'entrée soit ouverte avec les autorisations réseau et client maximales autorisées.</span><span class="sxs-lookup"><span data-stu-id="0644a-134">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="0644a-135">Par exemple, si le client dispose d'une autorisation en lecture et en écriture, le fournisseur de carnet d'adresses tente d'ouvrir l'entrée avec une autorisation en lecture et en écriture.</span><span class="sxs-lookup"><span data-stu-id="0644a-135">For example, if the client has read and write permission, the address book provider attempts to open the entry with read and write permission.</span></span> <span data-ttu-id="0644a-136">Le client peut récupérer le niveau d'accès qui a été accordé en appelant la méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) de l'entrée ouverte et en récupérant la propriété PR_ACCESS_LEVEL (PidTagAccessLevel).</span><span class="sxs-lookup"><span data-stu-id="0644a-136">The client can retrieve the access level that was granted by calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method of the open entry and retrieving the PR_ACCESS_LEVEL (PidTagAccessLevel) property.</span></span> 
    
<span data-ttu-id="0644a-137">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="0644a-137">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="0644a-138">Utilisez uniquement le carnet d'adresses en mode hors connexion pour effectuer la résolution de noms.</span><span class="sxs-lookup"><span data-stu-id="0644a-138">Use only the offline address book to perform name resolution.</span></span> <span data-ttu-id="0644a-139">Par exemple, vous pouvez utiliser cet indicateur pour permettre à une application cliente d'ouvrir la liste d'adresses globale (LAG) en mode Exchange mis en cache et d'accéder à une entrée de ce carnet d'adresses à partir du cache sans créer de trafic entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="0644a-139">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="0644a-140">Cet indicateur est pris en charge uniquement par le fournisseur de carnet d'adresses Exchange.</span><span class="sxs-lookup"><span data-stu-id="0644a-140">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="0644a-141">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="0644a-141">MAPI_DEFERRED_ERRORS</span></span>
  
> <span data-ttu-id="0644a-142">Permet à l'appel de réussir, éventuellement avant que l'entrée soit entièrement ouverte et disponible, ce qui implique que des appels ultérieurs à l'entrée renvoient une erreur.</span><span class="sxs-lookup"><span data-stu-id="0644a-142">Allows the call to succeed, potentially before the entry is fully open and available, implying that subsequent calls to the entry might return an error.</span></span>
    
<span data-ttu-id="0644a-143">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="0644a-143">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="0644a-144">Utilisez uniquement la liste d'adresses globale pour effectuer la résolution de noms.</span><span class="sxs-lookup"><span data-stu-id="0644a-144">Use only the GAL to perform name resolution.</span></span> <span data-ttu-id="0644a-145">Cet indicateur est pris en charge uniquement par le fournisseur de carnet d'adresses Exchange.</span><span class="sxs-lookup"><span data-stu-id="0644a-145">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="0644a-146">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="0644a-146">MAPI_MODIFY</span></span>
  
> <span data-ttu-id="0644a-147">Demande que l'entrée soit ouverte avec une autorisation en lecture et en écriture.</span><span class="sxs-lookup"><span data-stu-id="0644a-147">Requests that the entry be opened with read and write permission.</span></span> <span data-ttu-id="0644a-148">Étant donné que les entrées sont ouvertes avec un accès en lecture seule par défaut, les clients ne doivent pas supposer que l'autorisation de lecture et d'écriture a été accordée, que MAPI_MODIFY soit défini ou non.</span><span class="sxs-lookup"><span data-stu-id="0644a-148">Because entries are opened with read-only access by default, clients should not assume that read and write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="0644a-149">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="0644a-149">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="0644a-150">N'utilisez pas le carnet d'adresses en mode hors connexion pour effectuer la résolution de noms.</span><span class="sxs-lookup"><span data-stu-id="0644a-150">Do not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="0644a-151">Cet indicateur est pris en charge uniquement par le fournisseur de carnet d'adresses Exchange.</span><span class="sxs-lookup"><span data-stu-id="0644a-151">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
 <span data-ttu-id="0644a-152">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="0644a-152">_lpulObjType_</span></span>
  
> <span data-ttu-id="0644a-153">remarquer Pointeur vers le type de l'entrée ouverte.</span><span class="sxs-lookup"><span data-stu-id="0644a-153">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="0644a-154">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="0644a-154">_lppUnk_</span></span>
  
> <span data-ttu-id="0644a-155">remarquer Pointeur vers un pointeur de l'entrée ouverte.</span><span class="sxs-lookup"><span data-stu-id="0644a-155">[out] A pointer to a pointer of the opened entry.</span></span>
    

