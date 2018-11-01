---
title: IAddrBookOpenEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.OpenEntry
api_type:
- COM
ms.assetid: bd7746f4-8070-4cc5-8b8e-c527c5847545
description: 'Derni�re modification�: vendredi 1 f�vrier 2013'
ms.openlocfilehash: 4d380f784094064232cdb7369080612ba9ccac0e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576868"
---
# <a name="iaddrbookopenentry"></a><span data-ttu-id="c38e2-103">IAddrBook::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="c38e2-103">IAddrBook::OpenEntry</span></span>

<span data-ttu-id="c38e2-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c38e2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c38e2-105">Ouvre une entrée de carnet d’adresses et retourne un pointeur vers une interface qui peut servir à accéder à l’entrée.</span><span class="sxs-lookup"><span data-stu-id="c38e2-105">Opens an address book entry and returns a pointer to an interface that can be used to access the entry.</span></span>
  
```cpp
HRESULT OpenEntry(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a><span data-ttu-id="c38e2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c38e2-106">Parameters</span></span>

<span data-ttu-id="c38e2-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="c38e2-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="c38e2-108">[in] Le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="c38e2-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
<span data-ttu-id="c38e2-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="c38e2-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="c38e2-110">[in] Pointeur vers l’identificateur d’entrée qui représente l’entrée du carnet d’adresses à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="c38e2-110">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
<span data-ttu-id="c38e2-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="c38e2-111">_lpInterface_</span></span>
  
> <span data-ttu-id="c38e2-112">[in] Pointeur vers l’identificateur d’interface (IID) de l’interface à utiliser pour accéder à l’entrée open.</span><span class="sxs-lookup"><span data-stu-id="c38e2-112">[in] A pointer to the interface identifier (IID) of the interface to be used to access the open entry.</span></span> <span data-ttu-id="c38e2-113">Passage de NULL renvoie interface standard de l’objet.</span><span class="sxs-lookup"><span data-stu-id="c38e2-113">Passing NULL returns the object's standard interface.</span></span> <span data-ttu-id="c38e2-114">Pour les utilisateurs de messagerie, l’interface standard est [IMailUser : IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="c38e2-114">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="c38e2-115">Pour les listes de distribution, il est [IDistList : IMAPIContainer](idistlistimapicontainer.md) et pour les conteneurs, il est [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="c38e2-115">For distribution lists, it is [IDistList : IMAPIContainer](idistlistimapicontainer.md) and for containers, it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="c38e2-116">Les appelants peuvent définir _lpInterface_ à l’interface standard ou d’une interface dans la hiérarchie d’héritage.</span><span class="sxs-lookup"><span data-stu-id="c38e2-116">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
<span data-ttu-id="c38e2-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c38e2-117">_ulFlags_</span></span>
  
> <span data-ttu-id="c38e2-118">[in] Masque de bits d’indicateurs qui contrôle la façon dont l’entrée est ouvert.</span><span class="sxs-lookup"><span data-stu-id="c38e2-118">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="c38e2-119">Les indicateurs suivants peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="c38e2-119">The following flags can be set.</span></span>
    
<span data-ttu-id="c38e2-120">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="c38e2-120">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="c38e2-121">Demandes que l’entrée s’ouvre avec les autorisations maximales autorisées réseau et le client.</span><span class="sxs-lookup"><span data-stu-id="c38e2-121">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="c38e2-122">Par exemple, si le client a l’autorisation de lecture/écriture, le fournisseur de carnet d’adresses doit essayer ouvrir l’entrée avec une autorisation en lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="c38e2-122">For example, if the client has read/write permission, the address book provider should attempt to open the entry with read/write permission.</span></span> <span data-ttu-id="c38e2-123">Le client peut extraire le niveau d’accès qui a été accordé par l’appel de méthode de [IMAPIProp::GetProps](imapiprop-getprops.md) open de l’entrée et la récupération de la propriété **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="c38e2-123">The client can retrieve the access level that was granted by calling the open entry's [IMAPIProp::GetProps](imapiprop-getprops.md) method and retrieving the **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property.</span></span>
    
<span data-ttu-id="c38e2-124">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="c38e2-124">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="c38e2-125">Ouvre une entrée de carnet d’adresses et y accède uniquement à partir du cache.</span><span class="sxs-lookup"><span data-stu-id="c38e2-125">Opens an address book entry and accesses it only from the cache.</span></span> <span data-ttu-id="c38e2-126">Par exemple, vous pouvez utiliser cet indicateur pour autoriser une application cliente ouvrir la liste d’adresses globale (LAG) en mode exchange mis en cache et accéder à une entrée dans ce carnet d’adresses à partir du cache sans créer le trafic entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="c38e2-126">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="c38e2-127">Cet indicateur est pris en charge uniquement par le fournisseur de carnet d’adresses Exchange.</span><span class="sxs-lookup"><span data-stu-id="c38e2-127">This flag is supported only by the Exchange address book provider.</span></span>
    
<span data-ttu-id="c38e2-128">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="c38e2-128">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="c38e2-129">Permet l’appel aboutisse, potentiellement avant que l’entrée est entièrement ouverte et disponible, ce qui implique que les appels ultérieurs à l’entrée de renvoyer une erreur.</span><span class="sxs-lookup"><span data-stu-id="c38e2-129">Allows the call to succeed, potentially before the entry is fully open and available, implying that later calls to the entry might return an error.</span></span>
    
<span data-ttu-id="c38e2-130">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="c38e2-130">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="c38e2-131">Utiliser uniquement la liste d’adresses globale pour effectuer la résolution de noms.</span><span class="sxs-lookup"><span data-stu-id="c38e2-131">Use only the GAL to perform name resolution.</span></span> <span data-ttu-id="c38e2-132">Cet indicateur est pris en charge uniquement par le fournisseur de carnet d’adresses Exchange.</span><span class="sxs-lookup"><span data-stu-id="c38e2-132">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
  > [!NOTE]
  > <span data-ttu-id="c38e2-133">_ulFlags_ MAPI_GAL_ONLY pas peuvent être définis dans le fichier d’en-tête téléchargeables que vous avez actuellement, auquel cas vous pouvez l’ajouter à votre code à l’aide de la valeur suivante : >`#define MAPI_GAL_ONLY (0x00000080)`</span><span class="sxs-lookup"><span data-stu-id="c38e2-133">The  _ulFlags_ MAPI_GAL_ONLY might not be defined in the downloadable header file you currently have, in which case you can add it to your code using the following value: >  `#define MAPI_GAL_ONLY (0x00000080)`</span></span>
  
<span data-ttu-id="c38e2-134">N'</span><span class="sxs-lookup"><span data-stu-id="c38e2-134">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="c38e2-135">Demandes que l’entrée est ouvert en lecture/écriture autorisation.</span><span class="sxs-lookup"><span data-stu-id="c38e2-135">Requests that the entry be opened with read/write permission.</span></span> <span data-ttu-id="c38e2-136">Étant donné que les entrées sont ouvertes avec accès en lecture seule par défaut, les clients ne doivent pas supposer que l’autorisation de lecture/écriture bénéficie même si n’est définie.</span><span class="sxs-lookup"><span data-stu-id="c38e2-136">Because entries are opened with read-only access by default, clients should not assume that read/write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="c38e2-137">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="c38e2-137">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="c38e2-138">N’utilisez pas le carnet d’adresses en mode hors connexion pour effectuer la résolution de noms.</span><span class="sxs-lookup"><span data-stu-id="c38e2-138">Do not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="c38e2-139">Cet indicateur est pris en charge uniquement par le fournisseur de carnet d’adresses Exchange.</span><span class="sxs-lookup"><span data-stu-id="c38e2-139">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="c38e2-140">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="c38e2-140">_lpulObjType_</span></span>
  
> <span data-ttu-id="c38e2-141">[out] Pointeur vers le type de l’entrée ouvert.</span><span class="sxs-lookup"><span data-stu-id="c38e2-141">[out] A pointer to the type of the opened entry.</span></span>
    
<span data-ttu-id="c38e2-142">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="c38e2-142">_lppUnk_</span></span>
  
> <span data-ttu-id="c38e2-143">[out] Pointeur vers un pointeur vers l’entrée ouvert.</span><span class="sxs-lookup"><span data-stu-id="c38e2-143">[out] A pointer to a pointer to the opened entry.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c38e2-144">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c38e2-144">Return value</span></span>

<span data-ttu-id="c38e2-145">S_OK</span><span class="sxs-lookup"><span data-stu-id="c38e2-145">S_OK</span></span> 
  
> <span data-ttu-id="c38e2-146">L’entrée a été ouvert avec succès.</span><span class="sxs-lookup"><span data-stu-id="c38e2-146">The entry was successfully opened.</span></span>
    
<span data-ttu-id="c38e2-147">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="c38e2-147">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="c38e2-148">Une tentative a été effectuée pour ouvrir une entrée pour lequel l’utilisateur dispose d’autorisations insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="c38e2-148">An attempt was made to open an entry for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="c38e2-149">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="c38e2-149">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="c38e2-150">L’entrée représentée par _lpEntryID_ n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="c38e2-150">The entry represented by  _lpEntryID_ does not exist.</span></span> 
    
<span data-ttu-id="c38e2-151">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="c38e2-151">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="c38e2-152">L’identificateur d’entrée spécifié dans _lpEntryID_ n’est pas reconnue.</span><span class="sxs-lookup"><span data-stu-id="c38e2-152">The entry identifier specified in  _lpEntryID_ is not recognized.</span></span> <span data-ttu-id="c38e2-153">Cette valeur est généralement renvoyée si le fournisseur de carnet d’adresses responsable de l’entrée correspondante n’est pas ouvert.</span><span class="sxs-lookup"><span data-stu-id="c38e2-153">This value is typically returned if the address book provider responsible for the corresponding entry is not open.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c38e2-154">Remarques</span><span class="sxs-lookup"><span data-stu-id="c38e2-154">Remarks</span></span>

<span data-ttu-id="c38e2-155">Clients et fournisseurs de services appellent la méthode **IAddrBook::OpenEntry** pour ouvrir une entrée de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="c38e2-155">Clients and service providers call the **IAddrBook::OpenEntry** method to open an address book entry.</span></span> <span data-ttu-id="c38e2-156">MAPI transfère l’appel vers le fournisseur de carnet d’adresse appropriée, en fonction de la structure [MAPIUID](mapiuid.md) incluse dans l’identificateur d’entrée passé dans le paramètre _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="c38e2-156">MAPI forwards the call to the appropriate address book provider, based on the [MAPIUID](mapiuid.md) structure included in the entry identifier passed in the  _lpEntryID_ parameter.</span></span> <span data-ttu-id="c38e2-157">Le fournisseur de carnet d’adresses ouvre l’entrée en lecture seule, sauf si l’indicateur n’ou MAPI_BEST_ACCESS dans le paramètre _ulFlags_ est défini.</span><span class="sxs-lookup"><span data-stu-id="c38e2-157">The address book provider opens the entry as read-only unless the MAPI_MODIFY or MAPI_BEST_ACCESS flag in the  _ulFlags_ parameter is set.</span></span> <span data-ttu-id="c38e2-158">Toutefois, ces indicateurs sont des suggestions.</span><span class="sxs-lookup"><span data-stu-id="c38e2-158">However, these flags are suggestions.</span></span> <span data-ttu-id="c38e2-159">Si le fournisseur de carnet d’adresses n’autorise pas la modification de l’entrée demandée, il renvoie MAPI_E_NO_ACCESS.</span><span class="sxs-lookup"><span data-stu-id="c38e2-159">If the address book provider does not allow modification for the entry requested, it returns MAPI_E_NO_ACCESS.</span></span> 
  
<span data-ttu-id="c38e2-160">Le paramètre _lpInterface_ indique l’interface qui doit être utilisé pour accéder à l’entrée ouverte.</span><span class="sxs-lookup"><span data-stu-id="c38e2-160">The  _lpInterface_ parameter indicates which interface should be used to access the opened entry.</span></span> <span data-ttu-id="c38e2-161">Passage de NULL dans _lpInterface_ indique l’interface MAPI standard pour ce type d’entrée doit être utilisé.</span><span class="sxs-lookup"><span data-stu-id="c38e2-161">Passing NULL in  _lpInterface_ indicates the standard MAPI interface for that type of entry should be used.</span></span> <span data-ttu-id="c38e2-162">Étant donné que le fournisseur de carnet d’adresses peut retourner une interface différente de celle suggérée par le paramètre _lpInterface_ , l’appelant doit vérifier la valeur renvoyée dans le paramètre _lpulObjType_ pour déterminer si le type d’objet retourné est ce qui était attendu.</span><span class="sxs-lookup"><span data-stu-id="c38e2-162">Because the address book provider might return a different interface than the one suggested by the  _lpInterface_ parameter, the caller should check the value returned in the  _lpulObjType_ parameter to determine whether the object type returned is what was expected.</span></span> <span data-ttu-id="c38e2-163">Si le type d’objet n’est pas du type attendu, l’appelant peut effectuer un cast le paramètre _lppUnk_ à un type qui est plus approprié.</span><span class="sxs-lookup"><span data-stu-id="c38e2-163">If the object type is not of the type expected, the caller can cast the  _lppUnk_ parameter to a type that is more appropriate.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c38e2-164">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c38e2-164">See also</span></span>

- [<span data-ttu-id="c38e2-165">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="c38e2-165">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

