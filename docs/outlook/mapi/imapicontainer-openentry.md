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
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 9598e0c90c16db14cdc3a46d2b2ae74e0d9a9300
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286931"
---
# <a name="imapicontaineropenentry"></a><span data-ttu-id="8bd01-103">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="8bd01-103">IMAPIContainer::OpenEntry</span></span>

  
  
<span data-ttu-id="8bd01-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8bd01-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8bd01-105">Ouvre un objet dans le conteneur, en renvoyant un pointeur d'interface pour un accès supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="8bd01-105">Opens an object in the container, returning an interface pointer for further access.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="8bd01-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8bd01-106">Parameters</span></span>

 <span data-ttu-id="8bd01-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="8bd01-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="8bd01-108">dans Nombre d'octets dans l'identificateur d'entrée pointé par le paramètre _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="8bd01-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="8bd01-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="8bd01-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="8bd01-110">dans Pointeur vers l'identificateur d'entrée de l'objet à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="8bd01-110">[in] A pointer to the entry identifier of the object to open.</span></span> <span data-ttu-id="8bd01-111">Si _lpEntryID_ est défini sur null, le conteneur de niveau supérieur dans la hiérarchie du conteneur est ouvert.</span><span class="sxs-lookup"><span data-stu-id="8bd01-111">If  _lpEntryID_ is set to NULL, the top-level container in the container's hierarchy is opened.</span></span> 
    
 <span data-ttu-id="8bd01-112">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="8bd01-112">_lpInterface_</span></span>
  
> <span data-ttu-id="8bd01-113">dans Pointeur vers l'identificateur d'interface (IID) qui représente l'interface à utiliser pour accéder à l'objet.</span><span class="sxs-lookup"><span data-stu-id="8bd01-113">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the object.</span></span> <span data-ttu-id="8bd01-114">La transmission de la valeur NULL entraîne le renvoi de l'interface standard de l'objet.</span><span class="sxs-lookup"><span data-stu-id="8bd01-114">Passing NULL results in the identifier for the object's standard interface being returned.</span></span> <span data-ttu-id="8bd01-115">Pour les messages, l'interface standard est [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md); pour les dossiers, il s'agit de [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="8bd01-115">For messages, the standard interface is [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md); for folders, it is [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="8bd01-116">Les interfaces standard pour les objets de carnet d'adresses sont [IDistList: IMAPIContainer](idistlistimapicontainer.md) pour une liste de distribution et [IMailUser: IMAPIProp](imailuserimapiprop.md) pour un utilisateur de messagerie.</span><span class="sxs-lookup"><span data-stu-id="8bd01-116">The standard interfaces for address book objects are [IDistList : IMAPIContainer](idistlistimapicontainer.md) for a distribution list and [IMailUser : IMAPIProp](imailuserimapiprop.md) for a messaging user.</span></span> 
    
 <span data-ttu-id="8bd01-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8bd01-117">_ulFlags_</span></span>
  
> <span data-ttu-id="8bd01-118">dans Masque de des indicateurs qui contrôle le mode d'ouverture de l'objet.</span><span class="sxs-lookup"><span data-stu-id="8bd01-118">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="8bd01-119">Les indicateurs suivants peuvent être définis:</span><span class="sxs-lookup"><span data-stu-id="8bd01-119">The following flags can be set:</span></span>
    
<span data-ttu-id="8bd01-120">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="8bd01-120">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="8bd01-121">Demande que l'objet soit ouvert avec les autorisations réseau maximales accordées à l'utilisateur et l'accès maximal de l'application cliente.</span><span class="sxs-lookup"><span data-stu-id="8bd01-121">Requests that the object will be opened with the maximum network permissions allowed for the user and the maximum client application access.</span></span> <span data-ttu-id="8bd01-122">Par exemple, si le client dispose d'une autorisation en lecture/écriture, l'objet doit être ouvert avec une autorisation en lecture/écriture; Si le client dispose d'un accès en lecture seule, l'objet doit être ouvert avec un accès en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="8bd01-122">For example, if the client has read/write permission, the object should be opened with read/write permission; if the client has read-only access, the object should be opened with read-only access.</span></span> 
    
<span data-ttu-id="8bd01-123">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="8bd01-123">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="8bd01-124">Permet à **OpenEntry** de retourner correctement, éventuellement avant que l'objet soit entièrement disponible pour le client appelant.</span><span class="sxs-lookup"><span data-stu-id="8bd01-124">Allows **OpenEntry** to return successfully, possibly before the object is fully available to the calling client.</span></span> <span data-ttu-id="8bd01-125">Si l'objet n'est pas disponible, un appel d'objet ultérieur peut déclencher une erreur.</span><span class="sxs-lookup"><span data-stu-id="8bd01-125">If the object is not available, making a subsequent object call can raise an error.</span></span> 
    
<span data-ttu-id="8bd01-126">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="8bd01-126">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="8bd01-127">Demande une autorisation en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="8bd01-127">Requests read/write permission.</span></span> <span data-ttu-id="8bd01-128">Par défaut, les objets sont ouverts avec un accès en lecture seule et les clients ne doivent pas travailler en supposant que l'autorisation de lecture/écriture a été octroyée.</span><span class="sxs-lookup"><span data-stu-id="8bd01-128">By default, objects are opened with read-only access, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
<span data-ttu-id="8bd01-129">SHOW_SOFT_DELETES</span><span class="sxs-lookup"><span data-stu-id="8bd01-129">SHOW_SOFT_DELETES</span></span>
  
> <span data-ttu-id="8bd01-130">Affiche les éléments qui sont actuellement marqués comme étant supprimés de manière récupérable, c'est-à-dire qu'ils se trouvent dans la phase de durée de rétention des éléments supprimés.</span><span class="sxs-lookup"><span data-stu-id="8bd01-130">Shows items that are currently marked as soft deleted—that is, they are in the deleted item retention time phase.</span></span>
    
 <span data-ttu-id="8bd01-131">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="8bd01-131">_lpulObjType_</span></span>
  
> <span data-ttu-id="8bd01-132">remarquer Pointeur vers le type de l'objet ouvert.</span><span class="sxs-lookup"><span data-stu-id="8bd01-132">[out] A pointer to the opened object's type.</span></span>
    
 <span data-ttu-id="8bd01-133">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="8bd01-133">_lppUnk_</span></span>
  
> <span data-ttu-id="8bd01-134">remarquer Pointeur vers un pointeur vers l'implémentation de l'interface à utiliser pour accéder à l'objet ouvert.</span><span class="sxs-lookup"><span data-stu-id="8bd01-134">[out] A pointer to a pointer to the interface implementation to use to access the open object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8bd01-135">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8bd01-135">Return value</span></span>

<span data-ttu-id="8bd01-136">S_OK</span><span class="sxs-lookup"><span data-stu-id="8bd01-136">S_OK</span></span> 
  
> <span data-ttu-id="8bd01-137">L'objet a été ouvert avec succès.</span><span class="sxs-lookup"><span data-stu-id="8bd01-137">The object was successfully opened.</span></span>
    
<span data-ttu-id="8bd01-138">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="8bd01-138">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="8bd01-139">Soit l'utilisateur ne dispose pas des autorisations suffisantes pour ouvrir l'objet, soit une tentative d'ouverture d'un objet en lecture seule avec une autorisation en lecture/écriture a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="8bd01-139">Either the user has insufficient permissions to open the object or an attempt was made to open a read-only object with read/write permission.</span></span>
    
<span data-ttu-id="8bd01-140">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="8bd01-140">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="8bd01-141">L'identificateur d'entrée spécifié par _lpEntryID_ ne représente pas un objet.</span><span class="sxs-lookup"><span data-stu-id="8bd01-141">The entry identifier specified by  _lpEntryID_ does not represent an object.</span></span> 
    
<span data-ttu-id="8bd01-142">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="8bd01-142">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="8bd01-143">L'identificateur d'entrée dans le paramètre _lpEntryID_ n'est pas un format reconnu par le conteneur.</span><span class="sxs-lookup"><span data-stu-id="8bd01-143">The entry identifier in the  _lpEntryID_ parameter is not of a format recognized by the container.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="8bd01-144">Remarques</span><span class="sxs-lookup"><span data-stu-id="8bd01-144">Remarks</span></span>

<span data-ttu-id="8bd01-145">La méthode **IMAPIContainer:: OpenEntry** ouvre un objet dans tout un conteneur et renvoie un pointeur vers une implémentation d'interface à utiliser pour un accès supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="8bd01-145">The **IMAPIContainer::OpenEntry** method opens an object throughout a container and returns a pointer to an interface implementation to use for further access.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="8bd01-146">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="8bd01-146">Notes to callers</span></span>

<span data-ttu-id="8bd01-147">Étant donné que les fournisseurs de services ne sont pas tenus de retourner une implémentation d'interface du type spécifié par l'identificateur d'interface dans le paramètre _lpInterface_ , vérifiez la valeur pointée par le paramètre _lpulObjType_ .</span><span class="sxs-lookup"><span data-stu-id="8bd01-147">Because service providers are not required to return an interface implementation of the type specified by the interface identifier in the  _lpInterface_ parameter, check the value pointed to by the  _lpulObjType_ parameter.</span></span> <span data-ttu-id="8bd01-148">Si nécessaire, effectuez un cast du pointeur renvoyé dans _lppUnk_ vers un pointeur du type approprié.</span><span class="sxs-lookup"><span data-stu-id="8bd01-148">If necessary, cast the pointer returned in  _lppUnk_ to a pointer of the appropriate type.</span></span> 
  
<span data-ttu-id="8bd01-149">Par défaut, les fournisseurs de services ouvrent des objets avec un accès en lecture seule, sauf si vous définissez l'indicateur MAPI_MODIFY ou MAPI_BEST_ACCESS.</span><span class="sxs-lookup"><span data-stu-id="8bd01-149">By default, service providers open objects with read-only access unless you set either the MAPI_MODIFY or MAPI_BEST_ACCESS flag.</span></span> <span data-ttu-id="8bd01-150">Lorsque l'un de ces indicateurs est défini, les fournisseurs de services tentent de renvoyer un objet modifiable.</span><span class="sxs-lookup"><span data-stu-id="8bd01-150">When one of these flags is set, service providers attempt to return a modifiable object.</span></span> <span data-ttu-id="8bd01-151">Toutefois, ne partez pas du principe que vous avez demandé un objet modifiable que l'objet ouvert dispose d'une autorisation en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="8bd01-151">However, do not assume that because you requested a modifiable object that the opened object has read/write permission.</span></span> <span data-ttu-id="8bd01-152">Planifiez la possibilité d'une modification ultérieure de l'échec ou récupérez la propriété **PR_ACCESS_LEVEL** de l'objet pour déterminer le niveau d'accès accordé par **OpenEntry**.</span><span class="sxs-lookup"><span data-stu-id="8bd01-152">Either plan for the chance of a subsequent modification to fail or retrieve the object's **PR_ACCESS_LEVEL** property to determine the access level granted by **OpenEntry**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8bd01-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8bd01-153">See also</span></span>



[<span data-ttu-id="8bd01-154">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="8bd01-154">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)

