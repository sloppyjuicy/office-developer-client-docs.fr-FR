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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: c13ab9ce9c2564c39bfe9b2689f05439bc7b74ff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783691"
---
# <a name="imapicontaineropenentry"></a><span data-ttu-id="2140d-103">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="2140d-103">IMAPIContainer::OpenEntry</span></span>

  
  
<span data-ttu-id="2140d-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2140d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2140d-105">Ouvre un objet dans le conteneur, en retournant un pointeur d’interface pour l’accès des autres.</span><span class="sxs-lookup"><span data-stu-id="2140d-105">Opens an object in the container, returning an interface pointer for further access.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="2140d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2140d-106">Parameters</span></span>

 <span data-ttu-id="2140d-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="2140d-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="2140d-108">[in] Le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="2140d-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="2140d-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="2140d-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="2140d-110">[in] Pointeur vers l’identificateur d’entrée de l’objet à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="2140d-110">[in] A pointer to the entry identifier of the object to open.</span></span> <span data-ttu-id="2140d-111">Si _lpEntryID_ est défini sur NULL, le conteneur de niveau supérieur dans la hiérarchie du conteneur est ouvert.</span><span class="sxs-lookup"><span data-stu-id="2140d-111">If  _lpEntryID_ is set to NULL, the top-level container in the container's hierarchy is opened.</span></span> 
    
 <span data-ttu-id="2140d-112">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="2140d-112">_lpInterface_</span></span>
  
> <span data-ttu-id="2140d-113">[in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder à l’objet.</span><span class="sxs-lookup"><span data-stu-id="2140d-113">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the object.</span></span> <span data-ttu-id="2140d-114">Transmission NULL génère l’identificateur de l’interface standard de l’objet retourné.</span><span class="sxs-lookup"><span data-stu-id="2140d-114">Passing NULL results in the identifier for the object's standard interface being returned.</span></span> <span data-ttu-id="2140d-115">Pour les messages, l’interface standard est [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md); pour les dossiers, il est [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="2140d-115">For messages, the standard interface is [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md); for folders, it is [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="2140d-116">Pour les objets de carnet d’adresses sont des interfaces de la norme [IDistList : IMAPIContainer](idistlistimapicontainer.md) pour une liste de distribution et [IMailUser : IMAPIProp](imailuserimapiprop.md) pour un utilisateur de messagerie.</span><span class="sxs-lookup"><span data-stu-id="2140d-116">The standard interfaces for address book objects are [IDistList : IMAPIContainer](idistlistimapicontainer.md) for a distribution list and [IMailUser : IMAPIProp](imailuserimapiprop.md) for a messaging user.</span></span> 
    
 <span data-ttu-id="2140d-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2140d-117">_ulFlags_</span></span>
  
> <span data-ttu-id="2140d-118">[in] Masque de bits d’indicateurs qui contrôle la façon dont l’objet est ouvert.</span><span class="sxs-lookup"><span data-stu-id="2140d-118">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="2140d-119">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="2140d-119">The following flags can be set:</span></span>
    
<span data-ttu-id="2140d-120">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="2140d-120">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="2140d-121">Demande que l’objet est ouvert avec les autorisations de réseau maximale autorisées pour l’accès des utilisateurs et le nombre maximal de clients application.</span><span class="sxs-lookup"><span data-stu-id="2140d-121">Requests that the object will be opened with the maximum network permissions allowed for the user and the maximum client application access.</span></span> <span data-ttu-id="2140d-122">Par exemple, si le client a l’autorisation de lecture/écriture, l’objet doit être ouvert avec l’autorisation de lecture/écriture ; Si le client dispose d’un accès en lecture seule, l’objet doit être ouvert avec accès en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="2140d-122">For example, if the client has read/write permission, the object should be opened with read/write permission; if the client has read-only access, the object should be opened with read-only access.</span></span> 
    
<span data-ttu-id="2140d-123">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="2140d-123">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="2140d-124">Permet **OpenEntry** renvoyer avec succès, éventuellement, avant de l’objet est entièrement disponible au client appelant.</span><span class="sxs-lookup"><span data-stu-id="2140d-124">Allows **OpenEntry** to return successfully, possibly before the object is fully available to the calling client.</span></span> <span data-ttu-id="2140d-125">Si l’objet n’est pas disponible, l’émission d’un appel d’objet suivantes peut déclencher une erreur.</span><span class="sxs-lookup"><span data-stu-id="2140d-125">If the object is not available, making a subsequent object call can raise an error.</span></span> 
    
<span data-ttu-id="2140d-126">N'</span><span class="sxs-lookup"><span data-stu-id="2140d-126">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="2140d-127">Demandes d’autorisation de lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="2140d-127">Requests read/write permission.</span></span> <span data-ttu-id="2140d-128">Par défaut, les objets sont ouverts avec un accès en lecture seule et clients ne doivent pas fonctionner en supposant que bénéficie des autorisations en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="2140d-128">By default, objects are opened with read-only access, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
<span data-ttu-id="2140d-129">SHOW_SOFT_DELETES</span><span class="sxs-lookup"><span data-stu-id="2140d-129">SHOW_SOFT_DELETES</span></span>
  
> <span data-ttu-id="2140d-130">Affiche les éléments qui sont actuellement marqués comme logicielles supprimés — autrement dit, ils sont dans la rétention des éléments supprimés phase de temps.</span><span class="sxs-lookup"><span data-stu-id="2140d-130">Shows items that are currently marked as soft deleted—that is, they are in the deleted item retention time phase.</span></span>
    
 <span data-ttu-id="2140d-131">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="2140d-131">_lpulObjType_</span></span>
  
> <span data-ttu-id="2140d-132">[out] Pointeur vers le type de l’objet ouvert.</span><span class="sxs-lookup"><span data-stu-id="2140d-132">[out] A pointer to the opened object's type.</span></span>
    
 <span data-ttu-id="2140d-133">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="2140d-133">_lppUnk_</span></span>
  
> <span data-ttu-id="2140d-134">[out] Pointeur vers un pointeur vers l’implémentation d’interface à utiliser pour accéder à l’objet ouvert.</span><span class="sxs-lookup"><span data-stu-id="2140d-134">[out] A pointer to a pointer to the interface implementation to use to access the open object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2140d-135">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="2140d-135">Return value</span></span>

<span data-ttu-id="2140d-136">S_OK</span><span class="sxs-lookup"><span data-stu-id="2140d-136">S_OK</span></span> 
  
> <span data-ttu-id="2140d-137">L’objet a été ouvert avec succès.</span><span class="sxs-lookup"><span data-stu-id="2140d-137">The object was successfully opened.</span></span>
    
<span data-ttu-id="2140d-138">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="2140d-138">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="2140d-139">L’utilisateur dispose des autorisations suffisantes pour ouvrir l’objet ou un utilisateur a tenté d’ouvrir un objet en lecture seule avec une autorisation en lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="2140d-139">Either the user has insufficient permissions to open the object or an attempt was made to open a read-only object with read/write permission.</span></span>
    
<span data-ttu-id="2140d-140">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="2140d-140">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="2140d-141">L’identificateur d’entrée spécifié par _lpEntryID_ ne représente pas un objet.</span><span class="sxs-lookup"><span data-stu-id="2140d-141">The entry identifier specified by  _lpEntryID_ does not represent an object.</span></span> 
    
<span data-ttu-id="2140d-142">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="2140d-142">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="2140d-143">L’identificateur d’entrée dans le paramètre _lpEntryID_ n’est pas un format reconnu par le conteneur.</span><span class="sxs-lookup"><span data-stu-id="2140d-143">The entry identifier in the  _lpEntryID_ parameter is not of a format recognized by the container.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="2140d-144">Remarques</span><span class="sxs-lookup"><span data-stu-id="2140d-144">Remarks</span></span>

<span data-ttu-id="2140d-145">La méthode **IMAPIContainer::OpenEntry** ouvre un objet dans un conteneur et retourne un pointeur vers une implémentation de l’interface à utiliser pour l’accès des autres.</span><span class="sxs-lookup"><span data-stu-id="2140d-145">The **IMAPIContainer::OpenEntry** method opens an object throughout a container and returns a pointer to an interface implementation to use for further access.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="2140d-146">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="2140d-146">Notes to callers</span></span>

<span data-ttu-id="2140d-147">Étant donné que les fournisseurs de services ne sont pas tenus de retourner une implémentation de l’interface du type spécifié par l’identificateur d’interface dans le paramètre _lpInterface_ , vérifiez la valeur indiquée par le paramètre _lpulObjType_ .</span><span class="sxs-lookup"><span data-stu-id="2140d-147">Because service providers are not required to return an interface implementation of the type specified by the interface identifier in the  _lpInterface_ parameter, check the value pointed to by the  _lpulObjType_ parameter.</span></span> <span data-ttu-id="2140d-148">Si nécessaire, effectuer un cast du pointeur renvoyé dans _lppUnk_ à un pointeur du type approprié.</span><span class="sxs-lookup"><span data-stu-id="2140d-148">If necessary, cast the pointer returned in  _lppUnk_ to a pointer of the appropriate type.</span></span> 
  
<span data-ttu-id="2140d-149">Par défaut, les fournisseurs de services ouvrent des objets avec accès en lecture seule, sauf si vous définissez l’indicateur MAPI_BEST_ACCESS ou ne.</span><span class="sxs-lookup"><span data-stu-id="2140d-149">By default, service providers open objects with read-only access unless you set either the MAPI_MODIFY or MAPI_BEST_ACCESS flag.</span></span> <span data-ttu-id="2140d-150">Lorsqu’une de ces indicateurs est définie, essaient de fournisseurs de services renvoyer un objet modifiable.</span><span class="sxs-lookup"><span data-stu-id="2140d-150">When one of these flags is set, service providers attempt to return a modifiable object.</span></span> <span data-ttu-id="2140d-151">Toutefois, ne supposent que vous avez demandé un objet modifiable que l’objet ouvert a l’autorisation de lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="2140d-151">However, do not assume that because you requested a modifiable object that the opened object has read/write permission.</span></span> <span data-ttu-id="2140d-152">Soit prévoir le risque d’une modification ultérieure échec ou récupérer la propriété l’objet **PR_ACCESS_LEVEL** déterminer le niveau d’accès accordé par **OpenEntry**.</span><span class="sxs-lookup"><span data-stu-id="2140d-152">Either plan for the chance of a subsequent modification to fail or retrieve the object's **PR_ACCESS_LEVEL** property to determine the access level granted by **OpenEntry**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2140d-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2140d-153">See also</span></span>



[<span data-ttu-id="2140d-154">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="2140d-154">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)

