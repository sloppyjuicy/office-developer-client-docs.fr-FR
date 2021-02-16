---
title: IABLogonOpenEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.OpenEntry
api_type:
- COM
ms.assetid: 1cfb82f7-5215-4faa-af25-5b1da7e31209
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 70f61ef553350f08eed96c1ee4e9ab790359d1fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409229"
---
# <a name="iablogonopenentry"></a><span data-ttu-id="b2941-103">IABLogon::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="b2941-103">IABLogon::OpenEntry</span></span>

  
  
<span data-ttu-id="b2941-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b2941-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b2941-105">Ouvre un conteneur, un utilisateur de messagerie ou une liste de distribution et renvoie un pointeur vers une implémentation d’interface pour fournir un accès supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="b2941-105">Opens a container, messaging user, or distribution list, and returns a pointer to an interface implementation to provide further access.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="b2941-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b2941-106">Parameters</span></span>

 <span data-ttu-id="b2941-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="b2941-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="b2941-108">[in] Nombre d’bytes dans l’identificateur d’entrée pointé par _le paramètre lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="b2941-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="b2941-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="b2941-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="b2941-110">[in] Pointeur vers l’identificateur d’entrée du conteneur, de l’utilisateur de messagerie ou de la liste de distribution à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="b2941-110">[in] A pointer to the entry identifier of the container, messaging user, or distribution list to open.</span></span>
    
 <span data-ttu-id="b2941-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="b2941-111">_lpInterface_</span></span>
  
> <span data-ttu-id="b2941-112">[in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder à l’objet ouvert.</span><span class="sxs-lookup"><span data-stu-id="b2941-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the open object.</span></span> <span data-ttu-id="b2941-113">La transmission null renvoie l’identificateur de l’interface standard de l’objet.</span><span class="sxs-lookup"><span data-stu-id="b2941-113">Passing NULL returns the identifier for the object's standard interface.</span></span> <span data-ttu-id="b2941-114">Pour les conteneurs, l’interface standard [est IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="b2941-114">For containers, the standard interface is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="b2941-115">Les interfaces standard pour les objets de carnet d’adresses sont [IDistList : IMAPIContainer](idistlistimapicontainer.md) pour une liste de distribution et [IMailUser : IMAPIProp](imailuserimapiprop.md) pour un utilisateur de messagerie.</span><span class="sxs-lookup"><span data-stu-id="b2941-115">The standard interfaces for address book objects are [IDistList : IMAPIContainer](idistlistimapicontainer.md) for a distribution list and [IMailUser : IMAPIProp](imailuserimapiprop.md) for a messaging user.</span></span> 
    
 <span data-ttu-id="b2941-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b2941-116">_ulFlags_</span></span>
  
> <span data-ttu-id="b2941-117">[in] Masque de bits d’indicateurs qui contrôle la façon dont l’objet est ouvert.</span><span class="sxs-lookup"><span data-stu-id="b2941-117">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="b2941-118">Les indicateurs suivants peuvent être définies :</span><span class="sxs-lookup"><span data-stu-id="b2941-118">The following flags can be set:</span></span>
    
<span data-ttu-id="b2941-119">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="b2941-119">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="b2941-120">Demande l’ouverture de l’objet avec les autorisations réseau maximales autorisées pour l’utilisateur et l’accès maximal à l’application cliente.</span><span class="sxs-lookup"><span data-stu-id="b2941-120">Requests that the object be opened with the maximum network permissions allowed for the user and the maximum client application access.</span></span> <span data-ttu-id="b2941-121">Par exemple, si le client dispose d’une autorisation de lecture/écriture, l’objet doit être ouvert avec une autorisation de lecture/écriture . Si le client dispose d’une autorisation en lecture seule, l’objet doit être ouvert avec une autorisation en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="b2941-121">For example, if the client has read/write permission, the object should be opened with read/write permission; if the client has read-only permission, the object should be opened with read-only permission.</span></span>
    
<span data-ttu-id="b2941-122">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="b2941-122">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="b2941-123">Permet à la **méthode OpenEntry** de renvoyer correctement, éventuellement avant que le client appelant ait accédé entièrement à l’objet.</span><span class="sxs-lookup"><span data-stu-id="b2941-123">Allows the **OpenEntry** method to return successfully, possibly before the calling client has fully accessed the object.</span></span> <span data-ttu-id="b2941-124">Si l’objet n’est pas accessible, effectuer un appel d’objet ultérieur peut occasioner une erreur.</span><span class="sxs-lookup"><span data-stu-id="b2941-124">If the object is not accessed, making a subsequent object call can raise an error.</span></span> 
    
<span data-ttu-id="b2941-125">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="b2941-125">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="b2941-126">Demande une autorisation de lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="b2941-126">Requests read/write permission.</span></span> <span data-ttu-id="b2941-127">Par défaut, les objets sont ouverts avec un accès en lecture seule et les clients ne doivent pas supposer que l’autorisation lecture/écriture a été accordée.</span><span class="sxs-lookup"><span data-stu-id="b2941-127">By default, objects are opened with read-only access, and clients should not assume that read/write permission has been granted.</span></span>
    
 <span data-ttu-id="b2941-128">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="b2941-128">_lpulObjType_</span></span>
  
> <span data-ttu-id="b2941-129">[out] Pointeur vers le type de l’objet ouvert.</span><span class="sxs-lookup"><span data-stu-id="b2941-129">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="b2941-130">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="b2941-130">_lppUnk_</span></span>
  
> <span data-ttu-id="b2941-131">[out] Pointeur vers un pointeur vers l’objet ouvert.</span><span class="sxs-lookup"><span data-stu-id="b2941-131">[out] A pointer to a pointer to the opened object.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b2941-132">Remarques</span><span class="sxs-lookup"><span data-stu-id="b2941-132">Remarks</span></span>

<span data-ttu-id="b2941-133">S_OK</span><span class="sxs-lookup"><span data-stu-id="b2941-133">S_OK</span></span> 
  
> <span data-ttu-id="b2941-134">L’objet a été ouvert avec succès.</span><span class="sxs-lookup"><span data-stu-id="b2941-134">The object was successfully opened.</span></span>
    
<span data-ttu-id="b2941-135">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="b2941-135">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="b2941-136">Soit l’utilisateur ne dispose pas des autorisations suffisantes pour ouvrir l’objet, soit une tentative d’ouverture d’un objet en lecture seule avec une autorisation de lecture/écriture a été tentée.</span><span class="sxs-lookup"><span data-stu-id="b2941-136">Either the user has insufficient permissions to open the object, or an attempt was made to open a read-only object with read/write permission.</span></span>
    
<span data-ttu-id="b2941-137">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="b2941-137">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="b2941-138">L’identificateur d’entrée spécifié  _par lpEntryID_ ne représente pas un objet.</span><span class="sxs-lookup"><span data-stu-id="b2941-138">The entry identifier specified by  _lpEntryID_ does not represent an object.</span></span> 
    
<span data-ttu-id="b2941-139">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="b2941-139">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="b2941-140">L’identificateur d’entrée dans  _le paramètre lpEntryID_ n’est pas d’un format reconnu par le fournisseur de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="b2941-140">The entry identifier in the  _lpEntryID_ parameter is not of a format recognized by the address book provider.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b2941-141">Remarques</span><span class="sxs-lookup"><span data-stu-id="b2941-141">Remarks</span></span>

<span data-ttu-id="b2941-142">MAPI appelle la **méthode OpenEntry** pour ouvrir un conteneur, un utilisateur de messagerie ou une liste de distribution.</span><span class="sxs-lookup"><span data-stu-id="b2941-142">MAPI calls the **OpenEntry** method to open a container, messaging user, or distribution list.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="b2941-143">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="b2941-143">Notes to implementers</span></span>

<span data-ttu-id="b2941-144">Avant que MAPI appelle **votre méthode OpenEntry,** il détermine que l’identificateur d’entrée dans le paramètre  _lpEntryID_ vous appartient et non à un autre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="b2941-144">Before MAPI calls your **OpenEntry** method, it determines that the entry identifier in the  _lpEntryID_ parameter belongs to you and not to another provider.</span></span> <span data-ttu-id="b2941-145">POUR ce faire, MAPI fait correspondre la structure [MAPIUID](mapiuid.md) dans l’identificateur d’entrée avec le **MAPIUID** que vous avez enregistré en appelant la méthode [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) au démarrage.</span><span class="sxs-lookup"><span data-stu-id="b2941-145">MAPI does this by matching the [MAPIUID](mapiuid.md) structure in the entry identifier with the **MAPIUID** that you registered by calling the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method at startup.</span></span> 
  
<span data-ttu-id="b2941-146">Ouvrez l’objet en lecture seule, sauf si l’MAPI_MODIFY ou MAPI_BEST_ACCESS est définie dans le _paramètre ulFlags._</span><span class="sxs-lookup"><span data-stu-id="b2941-146">Open the object as read-only, unless the MAPI_MODIFY or MAPI_BEST_ACCESS flag is set in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="b2941-147">Si vous n’autorisez pas la modification de l’objet demandé, n’ouvrez pas l’objet et ne renvoyez aucune MAPI_E_NO_ACCESS.</span><span class="sxs-lookup"><span data-stu-id="b2941-147">If you do not allow modification for the requested object, do not open the object at all and return MAPI_E_NO_ACCESS.</span></span> 
  
<span data-ttu-id="b2941-148">Si MAPI transmet la valeur NULL pour  _lpEntryID,_ ouvrez le conteneur racine dans votre hiérarchie de conteneur.</span><span class="sxs-lookup"><span data-stu-id="b2941-148">If MAPI passes NULL for  _lpEntryID_, open the root container in your container hierarchy.</span></span>
  
<span data-ttu-id="b2941-149">L’objet que vous êtes invité à ouvrir peut être un objet copié à partir d’un autre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="b2941-149">The object that you are being asked to open might be an object copied from another provider.</span></span> <span data-ttu-id="b2941-150">Dans ce cas, il prendra en charge la **propriété PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b2941-150">In this case, it will support the **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property.</span></span> <span data-ttu-id="b2941-151">Si l’objet prend en charge cette propriété, appelez la méthode [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) pour établir une liaison avec le code de cette entrée dans le fournisseur étranger, en passant **PR_TEMPLATEID** dans le paramètre _lpTemplateID_ et 0 dans le paramètre _ulTemplateFlags._</span><span class="sxs-lookup"><span data-stu-id="b2941-151">If the object does support this property, call the [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) method to bind to code for this entry in the foreign provider, passing **PR_TEMPLATEID** in the  _lpTemplateID_ parameter and 0 in the  _ulTemplateFlags_ parameter.</span></span> <span data-ttu-id="b2941-152">**IMAPISupport::OpenTemplateID** transmet ces informations au fournisseur étranger dans un appel à la méthode [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) du fournisseur étranger.</span><span class="sxs-lookup"><span data-stu-id="b2941-152">**IMAPISupport::OpenTemplateID** passes this information to the foreign provider in a call to the foreign provider's [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) method.</span></span> <span data-ttu-id="b2941-153">Si **IMAPISupport::OpenTemplateID** lève une erreur, généralement parce que le fournisseur étranger n’est pas disponible ou n’est pas inclus dans le profil, essayez de continuer en traitant l’entrée indépendant comme étant en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="b2941-153">If **IMAPISupport::OpenTemplateID** raises an error, usually because the foreign provider is unavailable or not included in the profile, try to continue by treating the unbound entry as read-only.</span></span> <span data-ttu-id="b2941-154">Pour plus d’informations sur l’ouverture d’entrées de carnet d’adresses étrangères, voir Agir en tant que fournisseur de [carnet d’adresses hôte.](acting-as-a-host-address-book-provider.md)</span><span class="sxs-lookup"><span data-stu-id="b2941-154">For more information about opening foreign address book entries, see [Acting as a Host Address Book Provider](acting-as-a-host-address-book-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b2941-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b2941-155">See also</span></span>



[<span data-ttu-id="b2941-156">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b2941-156">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

