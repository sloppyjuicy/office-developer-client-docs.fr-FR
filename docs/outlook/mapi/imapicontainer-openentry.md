---
title: IMAPIContainerOpenEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer.OpenEntry
api_type:
- COM
ms.assetid: 0c46c1fb-dd63-4ac5-960e-80f68e75d8f4
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 9598e0c90c16db14cdc3a46d2b2ae74e0d9a9300
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423635"
---
# <a name="imapicontaineropenentry"></a><span data-ttu-id="a9c0a-103">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="a9c0a-103">IMAPIContainer::OpenEntry</span></span>

  
  
<span data-ttu-id="a9c0a-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a9c0a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a9c0a-105">Ouvre un objet dans le conteneur, renvoyant un pointeur d’interface pour un accès supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="a9c0a-105">Opens an object in the container, returning an interface pointer for further access.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="a9c0a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a9c0a-106">Parameters</span></span>

 <span data-ttu-id="a9c0a-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="a9c0a-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="a9c0a-108">[in] Nombre d’bytes dans l’identificateur d’entrée pointé par _le paramètre lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="a9c0a-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="a9c0a-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="a9c0a-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="a9c0a-110">[in] Pointeur vers l’identificateur d’entrée de l’objet à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="a9c0a-110">[in] A pointer to the entry identifier of the object to open.</span></span> <span data-ttu-id="a9c0a-111">Si  _lpEntryID_ est définie sur NULL, le conteneur de niveau supérieur dans la hiérarchie du conteneur est ouvert.</span><span class="sxs-lookup"><span data-stu-id="a9c0a-111">If  _lpEntryID_ is set to NULL, the top-level container in the container's hierarchy is opened.</span></span> 
    
 <span data-ttu-id="a9c0a-112">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="a9c0a-112">_lpInterface_</span></span>
  
> <span data-ttu-id="a9c0a-113">[in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder à l’objet.</span><span class="sxs-lookup"><span data-stu-id="a9c0a-113">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the object.</span></span> <span data-ttu-id="a9c0a-114">La transmission DE NULL entraîne le retour de l’identificateur de l’interface standard de l’objet.</span><span class="sxs-lookup"><span data-stu-id="a9c0a-114">Passing NULL results in the identifier for the object's standard interface being returned.</span></span> <span data-ttu-id="a9c0a-115">Pour les messages, l’interface standard [est IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md); pour les dossiers, il s’agit [de IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="a9c0a-115">For messages, the standard interface is [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md); for folders, it is [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="a9c0a-116">Les interfaces standard pour les objets de carnet d’adresses sont [IDistList : IMAPIContainer](idistlistimapicontainer.md) pour une liste de distribution et [IMailUser : IMAPIProp](imailuserimapiprop.md) pour un utilisateur de messagerie.</span><span class="sxs-lookup"><span data-stu-id="a9c0a-116">The standard interfaces for address book objects are [IDistList : IMAPIContainer](idistlistimapicontainer.md) for a distribution list and [IMailUser : IMAPIProp](imailuserimapiprop.md) for a messaging user.</span></span> 
    
 <span data-ttu-id="a9c0a-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a9c0a-117">_ulFlags_</span></span>
  
> <span data-ttu-id="a9c0a-118">[in] Masque de bits d’indicateurs qui contrôle la façon dont l’objet est ouvert.</span><span class="sxs-lookup"><span data-stu-id="a9c0a-118">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="a9c0a-119">Les indicateurs suivants peuvent être définies :</span><span class="sxs-lookup"><span data-stu-id="a9c0a-119">The following flags can be set:</span></span>
    
<span data-ttu-id="a9c0a-120">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="a9c0a-120">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="a9c0a-121">Demande que l’objet soit ouvert avec les autorisations réseau maximales autorisées pour l’utilisateur et l’accès maximal à l’application cliente.</span><span class="sxs-lookup"><span data-stu-id="a9c0a-121">Requests that the object will be opened with the maximum network permissions allowed for the user and the maximum client application access.</span></span> <span data-ttu-id="a9c0a-122">Par exemple, si le client dispose d’une autorisation de lecture/écriture, l’objet doit être ouvert avec une autorisation de lecture/écriture . Si le client dispose d’un accès en lecture seule, l’objet doit être ouvert avec un accès en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="a9c0a-122">For example, if the client has read/write permission, the object should be opened with read/write permission; if the client has read-only access, the object should be opened with read-only access.</span></span> 
    
<span data-ttu-id="a9c0a-123">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="a9c0a-123">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="a9c0a-124">Permet à **OpenEntry** de renvoyer correctement, éventuellement avant que l’objet soit entièrement disponible pour le client appelant.</span><span class="sxs-lookup"><span data-stu-id="a9c0a-124">Allows **OpenEntry** to return successfully, possibly before the object is fully available to the calling client.</span></span> <span data-ttu-id="a9c0a-125">Si l’objet n’est pas disponible, effectuer un appel d’objet ultérieur peut occasioner une erreur.</span><span class="sxs-lookup"><span data-stu-id="a9c0a-125">If the object is not available, making a subsequent object call can raise an error.</span></span> 
    
<span data-ttu-id="a9c0a-126">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="a9c0a-126">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="a9c0a-127">Demande une autorisation de lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="a9c0a-127">Requests read/write permission.</span></span> <span data-ttu-id="a9c0a-128">Par défaut, les objets sont ouverts avec un accès en lecture seule et les clients ne doivent pas fonctionner sur l’hypothèse que l’autorisation lecture/écriture a été accordée.</span><span class="sxs-lookup"><span data-stu-id="a9c0a-128">By default, objects are opened with read-only access, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
<span data-ttu-id="a9c0a-129">SHOW_SOFT_DELETES</span><span class="sxs-lookup"><span data-stu-id="a9c0a-129">SHOW_SOFT_DELETES</span></span>
  
> <span data-ttu-id="a9c0a-130">Affiche les éléments qui sont actuellement marqués comme supprimés (supprimés (supprimés( en d’autres cas), ils sont dans la phase de rétention des éléments supprimés.</span><span class="sxs-lookup"><span data-stu-id="a9c0a-130">Shows items that are currently marked as soft deleted—that is, they are in the deleted item retention time phase.</span></span>
    
 <span data-ttu-id="a9c0a-131">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="a9c0a-131">_lpulObjType_</span></span>
  
> <span data-ttu-id="a9c0a-132">[out] Pointeur vers le type de l’objet ouvert.</span><span class="sxs-lookup"><span data-stu-id="a9c0a-132">[out] A pointer to the opened object's type.</span></span>
    
 <span data-ttu-id="a9c0a-133">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="a9c0a-133">_lppUnk_</span></span>
  
> <span data-ttu-id="a9c0a-134">[out] Pointeur vers un pointeur vers l’implémentation de l’interface à utiliser pour accéder à l’objet ouvert.</span><span class="sxs-lookup"><span data-stu-id="a9c0a-134">[out] A pointer to a pointer to the interface implementation to use to access the open object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a9c0a-135">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a9c0a-135">Return value</span></span>

<span data-ttu-id="a9c0a-136">S_OK</span><span class="sxs-lookup"><span data-stu-id="a9c0a-136">S_OK</span></span> 
  
> <span data-ttu-id="a9c0a-137">L’objet a été ouvert avec succès.</span><span class="sxs-lookup"><span data-stu-id="a9c0a-137">The object was successfully opened.</span></span>
    
<span data-ttu-id="a9c0a-138">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="a9c0a-138">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="a9c0a-139">Soit l’utilisateur ne dispose pas des autorisations suffisantes pour ouvrir l’objet, soit une tentative d’ouverture d’un objet en lecture seule avec une autorisation de lecture/écriture a été tentée.</span><span class="sxs-lookup"><span data-stu-id="a9c0a-139">Either the user has insufficient permissions to open the object or an attempt was made to open a read-only object with read/write permission.</span></span>
    
<span data-ttu-id="a9c0a-140">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="a9c0a-140">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="a9c0a-141">L’identificateur d’entrée spécifié  _par lpEntryID_ ne représente pas un objet.</span><span class="sxs-lookup"><span data-stu-id="a9c0a-141">The entry identifier specified by  _lpEntryID_ does not represent an object.</span></span> 
    
<span data-ttu-id="a9c0a-142">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="a9c0a-142">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="a9c0a-143">L’identificateur d’entrée dans  _le paramètre lpEntryID_ n’est pas d’un format reconnu par le conteneur.</span><span class="sxs-lookup"><span data-stu-id="a9c0a-143">The entry identifier in the  _lpEntryID_ parameter is not of a format recognized by the container.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a9c0a-144">Remarques</span><span class="sxs-lookup"><span data-stu-id="a9c0a-144">Remarks</span></span>

<span data-ttu-id="a9c0a-145">La **méthode IMAPIContainer::OpenEntry** ouvre un objet dans un conteneur et renvoie un pointeur vers une implémentation d’interface à utiliser pour un accès supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="a9c0a-145">The **IMAPIContainer::OpenEntry** method opens an object throughout a container and returns a pointer to an interface implementation to use for further access.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a9c0a-146">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="a9c0a-146">Notes to callers</span></span>

<span data-ttu-id="a9c0a-147">Étant donné que les fournisseurs de services ne sont pas tenus de retourner une implémentation d’interface du type spécifié par l’identificateur d’interface dans le paramètre _lpInterface,_ vérifiez la valeur pointée par le paramètre _lpulObjType._</span><span class="sxs-lookup"><span data-stu-id="a9c0a-147">Because service providers are not required to return an interface implementation of the type specified by the interface identifier in the  _lpInterface_ parameter, check the value pointed to by the  _lpulObjType_ parameter.</span></span> <span data-ttu-id="a9c0a-148">Si nécessaire, cast le pointeur renvoyé dans  _lppUnk_ vers un pointeur du type approprié.</span><span class="sxs-lookup"><span data-stu-id="a9c0a-148">If necessary, cast the pointer returned in  _lppUnk_ to a pointer of the appropriate type.</span></span> 
  
<span data-ttu-id="a9c0a-149">Par défaut, les fournisseurs de services ouvrent des objets avec un accès en lecture seule, sauf si vous définissez l’MAPI_MODIFY ou MAPI_BEST_ACCESS’indicateur.</span><span class="sxs-lookup"><span data-stu-id="a9c0a-149">By default, service providers open objects with read-only access unless you set either the MAPI_MODIFY or MAPI_BEST_ACCESS flag.</span></span> <span data-ttu-id="a9c0a-150">Lorsque l’un de ces indicateurs est définie, les fournisseurs de services tentent de renvoyer un objet modifiable.</span><span class="sxs-lookup"><span data-stu-id="a9c0a-150">When one of these flags is set, service providers attempt to return a modifiable object.</span></span> <span data-ttu-id="a9c0a-151">Toutefois, ne supposez pas que, étant donné que vous avez demandé un objet modifiable, l’objet ouvert dispose d’une autorisation de lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="a9c0a-151">However, do not assume that because you requested a modifiable object that the opened object has read/write permission.</span></span> <span data-ttu-id="a9c0a-152">Planifiez l’échec d’une modification ultérieure ou récupérez la propriété **PR_ACCESS_LEVEL** de l’objet pour déterminer le niveau d’accès accordé par **OpenEntry**.</span><span class="sxs-lookup"><span data-stu-id="a9c0a-152">Either plan for the chance of a subsequent modification to fail or retrieve the object's **PR_ACCESS_LEVEL** property to determine the access level granted by **OpenEntry**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a9c0a-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a9c0a-153">See also</span></span>



[<span data-ttu-id="a9c0a-154">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="a9c0a-154">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)

