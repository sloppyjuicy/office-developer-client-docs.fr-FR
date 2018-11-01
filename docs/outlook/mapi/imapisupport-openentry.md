---
title: IMAPISupportOpenEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.OpenEntry
api_type:
- COM
ms.assetid: 84662230-6a25-4403-b87e-871427a40c6e
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 8b122c98715bd2f6916fe6302fc0b7a01d2cc936
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584610"
---
# <a name="imapisupportopenentry"></a><span data-ttu-id="fa06f-103">IMAPISupport::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="fa06f-103">IMAPISupport::OpenEntry</span></span>

  
  
<span data-ttu-id="fa06f-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fa06f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fa06f-105">Ouvre un objet et retourne un pointeur d’interface pour l’accès des autres.</span><span class="sxs-lookup"><span data-stu-id="fa06f-105">Opens an object and returns an interface pointer for further access.</span></span> 
  
```cpp
HRESULT OpenEntry(
ULONG cbEntryID,
LPENTRYID lpEntryID,
LPCIID lpInterface,
ULONG ulOpenFlags,
ULONG FAR * lpulObjType,
LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a><span data-ttu-id="fa06f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fa06f-106">Parameters</span></span>

 <span data-ttu-id="fa06f-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="fa06f-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="fa06f-108">[in] Le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="fa06f-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="fa06f-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="fa06f-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="fa06f-110">[in] Pointeur vers l’identificateur d’entrée de l’objet à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="fa06f-110">[in] A pointer to the entry identifier of the object to open.</span></span>
    
 <span data-ttu-id="fa06f-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="fa06f-111">_lpInterface_</span></span>
  
> <span data-ttu-id="fa06f-112">[in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder à l’objet.</span><span class="sxs-lookup"><span data-stu-id="fa06f-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the object.</span></span> <span data-ttu-id="fa06f-113">Transmission NULL des résultats de l’interface standard de l’objet retourné.</span><span class="sxs-lookup"><span data-stu-id="fa06f-113">Passing NULL results in the object's standard interface being returned.</span></span> <span data-ttu-id="fa06f-114">Par exemple, si l’objet à ouvrir est un message, l’interface standard est [IMessage](imessageimapiprop.md); pour les dossiers, il est [IMAPIFolder](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="fa06f-114">For example, if the object to be opened is a message, the standard interface is [IMessage](imessageimapiprop.md); for folders, it is [IMAPIFolder](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="fa06f-115">Les interfaces standards pour les objets de carnet d’adresses sont [IDistList](idistlistimapicontainer.md) pour une liste de distribution et les [IMailUser](imailuserimapiprop.md) pour un utilisateur de messagerie.</span><span class="sxs-lookup"><span data-stu-id="fa06f-115">The standard interfaces for address book objects are [IDistList](idistlistimapicontainer.md) for a distribution list and [IMailUser](imailuserimapiprop.md) for a messaging user.</span></span> 
    
 <span data-ttu-id="fa06f-116">_ulOpenFlags_</span><span class="sxs-lookup"><span data-stu-id="fa06f-116">_ulOpenFlags_</span></span>
  
> <span data-ttu-id="fa06f-117">[in] Masque de bits d’indicateurs qui contrôle la façon dont l’objet est ouvert.</span><span class="sxs-lookup"><span data-stu-id="fa06f-117">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="fa06f-118">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="fa06f-118">The following flags can be set:</span></span>
    
<span data-ttu-id="fa06f-119">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="fa06f-119">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="fa06f-120">Demande que l’objet s’ouvre avec les autorisations de réseau maximale autorisées pour l’appelant.</span><span class="sxs-lookup"><span data-stu-id="fa06f-120">Requests that the object be opened with the maximum network permissions allowed for the caller.</span></span> <span data-ttu-id="fa06f-121">Par exemple, si l’appelant a l’autorisation de lecture/écriture, l’objet doit être ouvert en lecture/écriture ; Si l’appelant a l’autorisation en lecture seule, l’objet doit être ouvert en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="fa06f-121">For example, if the caller has read/write permission, the object should be opened as read/write; if the caller has read-only permission, the object should be opened as read-only.</span></span> 
    
<span data-ttu-id="fa06f-122">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="fa06f-122">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="fa06f-123">Permet **OpenEntry** retournée correctement, éventuellement, avant de l’objet est accessible à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="fa06f-123">Allows **OpenEntry** to return successfully, possibly before the object is fully accessible to the caller.</span></span> <span data-ttu-id="fa06f-124">Si l’objet n’est pas accessible, passer un appel d’objet suivantes permettre provoquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="fa06f-124">If the object is not accessible, making a subsequent object call can result in an error.</span></span> 
    
<span data-ttu-id="fa06f-125">N'</span><span class="sxs-lookup"><span data-stu-id="fa06f-125">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="fa06f-126">Demandes d’autorisation de lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="fa06f-126">Requests read/write permission.</span></span> <span data-ttu-id="fa06f-127">Par défaut, les objets sont ouverts en lecture seule, et les appelants ne doivent pas travailler sur l’hypothèse que bénéficie des autorisations en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="fa06f-127">By default, objects are opened as read-only, and callers should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="fa06f-128">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="fa06f-128">_lpulObjType_</span></span>
  
> <span data-ttu-id="fa06f-129">[out] Pointeur vers le type de l’objet ouvert.</span><span class="sxs-lookup"><span data-stu-id="fa06f-129">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="fa06f-130">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="fa06f-130">_lppUnk_</span></span>
  
> <span data-ttu-id="fa06f-131">[out] Pointeur vers un pointeur vers l’objet ouvert.</span><span class="sxs-lookup"><span data-stu-id="fa06f-131">[out] A pointer to a pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="fa06f-132">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="fa06f-132">Return value</span></span>

<span data-ttu-id="fa06f-133">S_OK</span><span class="sxs-lookup"><span data-stu-id="fa06f-133">S_OK</span></span> 
  
> <span data-ttu-id="fa06f-134">L’objet a été ouvert avec succès.</span><span class="sxs-lookup"><span data-stu-id="fa06f-134">The object was successfully opened.</span></span>
    
<span data-ttu-id="fa06f-135">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="fa06f-135">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="fa06f-136">Une tentative a été effectuée pour modifier un objet en lecture seule, ou tentative d’accès à un objet pour lequel l’utilisateur dispose d’autorisations insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="fa06f-136">An attempt was made to modify a read-only object, or an attempt was made to access an object for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="fa06f-137">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="fa06f-137">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="fa06f-138">Il n’est pas un objet associé à l’identificateur d’entrée passé dans le paramètre _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="fa06f-138">There is not an object associated with the entry identifier passed in the  _lpEntryID_ parameter.</span></span> 
    
<span data-ttu-id="fa06f-139">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="fa06f-139">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="fa06f-140">L’identificateur d’entrée passé dans le paramètre _lpEntryID_ est dans un format non reconnaissable.</span><span class="sxs-lookup"><span data-stu-id="fa06f-140">The entry identifier passed in the  _lpEntryID_ parameter is in an unrecognizable format.</span></span> <span data-ttu-id="fa06f-141">Cette valeur est généralement renvoyée si le fournisseur de carnet d’adresses qui contient l’objet n’est pas ouvert.</span><span class="sxs-lookup"><span data-stu-id="fa06f-141">This value is typically returned if the address book provider that contains the object is not open.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="fa06f-142">Remarques</span><span class="sxs-lookup"><span data-stu-id="fa06f-142">Remarks</span></span>

<span data-ttu-id="fa06f-143">La méthode **IMAPISupport::OpenEntry** est implémentée pour tous les objets de prise en charge de fournisseur de service.</span><span class="sxs-lookup"><span data-stu-id="fa06f-143">The **IMAPISupport::OpenEntry** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="fa06f-144">Fournisseurs de services d’appel **IMAPISupport::OpenEntry** pour récupérer un pointeur vers une interface qui peut être utilisé pour accéder à un objet particulier.</span><span class="sxs-lookup"><span data-stu-id="fa06f-144">Service providers call **IMAPISupport::OpenEntry** to retrieve a pointer to an interface that can be used to access a particular object.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="fa06f-145">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="fa06f-145">Notes to callers</span></span>

<span data-ttu-id="fa06f-146">Appelez **IMAPISupport::OpenEntry** uniquement lorsque vous ne savez pas quel type d’objet que vous ouvrez.</span><span class="sxs-lookup"><span data-stu-id="fa06f-146">Call **IMAPISupport::OpenEntry** only when you do not know what kind of object you are opening.</span></span> <span data-ttu-id="fa06f-147">Si vous connaissez que l’ouverture d’un dossier ou un message, appelez [IMsgStore::OpenEntry](imsgstore-openentry.md) à la place.</span><span class="sxs-lookup"><span data-stu-id="fa06f-147">If you know you are opening a folder or a message, call [IMsgStore::OpenEntry](imsgstore-openentry.md) instead.</span></span> <span data-ttu-id="fa06f-148">Si vous connaissez que l’ouverture d’un conteneur de carnet d’adresses, un utilisateur de messagerie ou une liste de distribution, appelez [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="fa06f-148">If you know you are opening an address book container, a messaging user, or a distribution list, call [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span></span> <span data-ttu-id="fa06f-149">Ces méthodes plus spécifiques sont plus rapides que **IMAPISupport::OpenEntry**.</span><span class="sxs-lookup"><span data-stu-id="fa06f-149">These more specific methods are faster than **IMAPISupport::OpenEntry**.</span></span> 
  
 <span data-ttu-id="fa06f-150">**IMAPISupport::OpenEntry** ouvre tous les objets en lecture seule, sauf si vous définissez l’indicateur n’ou MAPI_BEST_ACCESS dans le paramètre _ulFlags_ et vos autorisations sont suffisantes.</span><span class="sxs-lookup"><span data-stu-id="fa06f-150">**IMAPISupport::OpenEntry** opens all objects as read-only, unless you set the MAPI_MODIFY or MAPI_BEST_ACCESS flag in the  _ulFlags_ parameter and your permissions are sufficient.</span></span> <span data-ttu-id="fa06f-151">Définition de l’une de ces indicateurs ne garantit pas un type particulier d’accès ; les autorisations qui vous sont accordées dépendent de votre niveau d’accès, l’objet et le fournisseur de services qui détient l’objet.</span><span class="sxs-lookup"><span data-stu-id="fa06f-151">Setting one of these flags does not guarantee a particular type of access; the permissions that you are granted depend on your access level, the object, and the service provider that owns the object.</span></span> <span data-ttu-id="fa06f-152">Pour déterminer le niveau d’accès de l’objet ouvert, récupérez sa propriété **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="fa06f-152">To determine the access level of the opened object, retrieve its **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="fa06f-153">Vérifiez la valeur renvoyée dans le paramètre _lpulObjType_ pour déterminer que le type d’objet retourné est attendue.</span><span class="sxs-lookup"><span data-stu-id="fa06f-153">Check the value returned in the  _lpulObjType_ parameter to determine that the object type returned is what you expected.</span></span> <span data-ttu-id="fa06f-154">Si le type d’objet est comme prévu, convertir le pointeur à partir du paramètre _lppUnk_ vers un pointeur du type approprié.</span><span class="sxs-lookup"><span data-stu-id="fa06f-154">If the object type is as expected, cast the pointer from the  _lppUnk_ parameter to a pointer of the appropriate type.</span></span> <span data-ttu-id="fa06f-155">Par exemple, si vous ouvrez un dossier, un cast _lppUnk_ à un pointeur du type LPMAPIFOLDER.</span><span class="sxs-lookup"><span data-stu-id="fa06f-155">For example, if you are opening a folder, cast  _lppUnk_ to a pointer of type LPMAPIFOLDER.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fa06f-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa06f-156">See also</span></span>



[<span data-ttu-id="fa06f-157">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fa06f-157">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

