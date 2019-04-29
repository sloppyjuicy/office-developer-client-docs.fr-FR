---
title: IMAPISessionOpenEntry
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.OpenEntry
api_type:
- COM
ms.assetid: a4df4860-cf4f-4e97-97c4-fcd89b7f1f91
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 10992fdf53c416c473b90b5748b9c5fa4f65cffc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426386"
---
# <a name="imapisessionopenentry"></a><span data-ttu-id="40e9f-103">IMAPISession::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="40e9f-103">IMAPISession::OpenEntry</span></span>

  
  
<span data-ttu-id="40e9f-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="40e9f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="40e9f-105">Ouvre un objet et renvoie un pointeur d'interface pour un accès supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="40e9f-105">Opens an object and returns an interface pointer for additional access.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="40e9f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="40e9f-106">Parameters</span></span>

 <span data-ttu-id="40e9f-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="40e9f-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="40e9f-108">dans Nombre d'octets dans l'identificateur d'entrée pointé par le paramètre _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="40e9f-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="40e9f-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="40e9f-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="40e9f-110">dans Pointeur vers l'identificateur d'entrée de l'objet à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="40e9f-110">[in] A pointer to the entry identifier of the object to open.</span></span>
    
 <span data-ttu-id="40e9f-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="40e9f-111">_lpInterface_</span></span>
  
> <span data-ttu-id="40e9f-112">dans Pointeur vers l'identificateur d'interface (IID) qui représente l'interface à utiliser pour accéder à l'objet ouvert.</span><span class="sxs-lookup"><span data-stu-id="40e9f-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the opened object.</span></span> <span data-ttu-id="40e9f-113">La transmission de la valeur NULL renvoie l'interface standard de l'objet.</span><span class="sxs-lookup"><span data-stu-id="40e9f-113">Passing NULL returns the object's standard interface.</span></span> <span data-ttu-id="40e9f-114">Par exemple, si l'objet à ouvrir est un message, l'interface standard est [IMessage](imessageimapiprop.md); pour les dossiers, il s'agit de [IMAPIFolder](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="40e9f-114">For example, if the object to be opened is a message, the standard interface is [IMessage](imessageimapiprop.md); for folders, it is [IMAPIFolder](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="40e9f-115">Les interfaces standard pour les objets de carnet d'adresses sont [IDistList](idistlistimapicontainer.md) pour une liste de distribution et [IMailUser](imailuserimapiprop.md) pour un utilisateur de messagerie.</span><span class="sxs-lookup"><span data-stu-id="40e9f-115">The standard interfaces for address book objects are [IDistList](idistlistimapicontainer.md) for a distribution list and [IMailUser](imailuserimapiprop.md) for a messaging user.</span></span> 
    
 <span data-ttu-id="40e9f-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="40e9f-116">_ulFlags_</span></span>
  
> <span data-ttu-id="40e9f-117">dans Masque de des indicateurs qui contrôle le mode d'ouverture de l'objet.</span><span class="sxs-lookup"><span data-stu-id="40e9f-117">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="40e9f-118">Les indicateurs suivants peuvent être utilisés:</span><span class="sxs-lookup"><span data-stu-id="40e9f-118">The following flags can be used:</span></span>
    
<span data-ttu-id="40e9f-119">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="40e9f-119">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="40e9f-120">Demande l'ouverture de l'objet à l'aide des autorisations réseau maximales autorisées pour l'utilisateur et de l'accès à l'application cliente maximale.</span><span class="sxs-lookup"><span data-stu-id="40e9f-120">Requests that the object be opened by using the maximum network permissions allowed for the user and the maximum client application access.</span></span> <span data-ttu-id="40e9f-121">Par exemple, si le client dispose d'une autorisation en lecture/écriture, l'objet doit être ouvert avec une autorisation en lecture/écriture; Si le client dispose d'une autorisation en lecture seule, l'objet doit être ouvert en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="40e9f-121">For example, if the client has read/write permission, the object should be opened with read/write permission; if the client has read-only permission, the object should be opened with read-only permission.</span></span> 
    
<span data-ttu-id="40e9f-122">MAPI_CACHE_OK</span><span class="sxs-lookup"><span data-stu-id="40e9f-122">MAPI_CACHE_OK</span></span>
  
> <span data-ttu-id="40e9f-123">Utilisez tous les moyens, y compris les carnets d'adresses en mode hors connexion, pour effectuer la résolution de noms.</span><span class="sxs-lookup"><span data-stu-id="40e9f-123">Use all means, including offline address books, to perform name resolution.</span></span>
    
<span data-ttu-id="40e9f-124">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="40e9f-124">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="40e9f-125">Utilisez uniquement le carnet d'adresses en mode hors connexion pour effectuer la résolution de noms.</span><span class="sxs-lookup"><span data-stu-id="40e9f-125">Use only the offline address book to perform name resolution.</span></span> <span data-ttu-id="40e9f-126">Par exemple, vous pouvez utiliser cet indicateur pour permettre à une application cliente d'ouvrir la liste d'adresses globale (LAG) en mode Exchange mis en cache et d'accéder à une entrée de ce carnet d'adresses à partir du cache sans créer de trafic entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="40e9f-126">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="40e9f-127">Cet indicateur est pris en charge uniquement par le fournisseur de carnet d'adresses Exchange.</span><span class="sxs-lookup"><span data-stu-id="40e9f-127">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="40e9f-128">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="40e9f-128">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="40e9f-129">Permet à **OpenEntry** de retourner correctement, éventuellement avant que l'objet soit entièrement disponible pour le client appelant.</span><span class="sxs-lookup"><span data-stu-id="40e9f-129">Allows **OpenEntry** to return successfully, possibly before the object is fully available to the calling client.</span></span> <span data-ttu-id="40e9f-130">Si l'objet n'est pas disponible, un appel d'objet ultérieur peut entraîner une erreur.</span><span class="sxs-lookup"><span data-stu-id="40e9f-130">If the object is not available, making a subsequent object call can cause an error.</span></span> 
    
<span data-ttu-id="40e9f-131">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="40e9f-131">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="40e9f-132">Demande une autorisation en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="40e9f-132">Requests read/write permission.</span></span> <span data-ttu-id="40e9f-133">Par défaut, les objets sont ouverts avec une autorisation en lecture seule, et les clients ne doivent pas travailler en supposant que l'autorisation de lecture/écriture est accordée.</span><span class="sxs-lookup"><span data-stu-id="40e9f-133">By default, objects are opened with read-only permission, and clients should not work on the assumption that read/write permission is granted.</span></span> 
    
<span data-ttu-id="40e9f-134">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="40e9f-134">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="40e9f-135">N'utilisez pas le carnet d'adresses en mode hors connexion pour effectuer la résolution de noms.</span><span class="sxs-lookup"><span data-stu-id="40e9f-135">Do not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="40e9f-136">Cet indicateur est pris en charge uniquement par le fournisseur de carnet d'adresses Exchange.</span><span class="sxs-lookup"><span data-stu-id="40e9f-136">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="40e9f-137">SHOW_SOFT_DELETES</span><span class="sxs-lookup"><span data-stu-id="40e9f-137">SHOW_SOFT_DELETES</span></span>
  
> <span data-ttu-id="40e9f-138">Affiche les éléments qui sont actuellement marqués comme étant supprimés de manière récupérable (c'est-à-dire qu'ils se trouvent dans la phase de rétention des éléments supprimés).</span><span class="sxs-lookup"><span data-stu-id="40e9f-138">Show items that are currently marked as soft deleted (that is, they are in the deleted item retention time phase).</span></span>
    
 <span data-ttu-id="40e9f-139">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="40e9f-139">_lpulObjType_</span></span>
  
> <span data-ttu-id="40e9f-140">remarquer Pointeur vers le type de l'objet ouvert.</span><span class="sxs-lookup"><span data-stu-id="40e9f-140">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="40e9f-141">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="40e9f-141">_lppUnk_</span></span>
  
> <span data-ttu-id="40e9f-142">remarquer Pointeur vers un pointeur vers l'objet ouvert.</span><span class="sxs-lookup"><span data-stu-id="40e9f-142">[out] A pointer to a pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="40e9f-143">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="40e9f-143">Return value</span></span>

<span data-ttu-id="40e9f-144">S_OK</span><span class="sxs-lookup"><span data-stu-id="40e9f-144">S_OK</span></span> 
  
> <span data-ttu-id="40e9f-145">L'objet a été ouvert avec succès.</span><span class="sxs-lookup"><span data-stu-id="40e9f-145">The object was opened successfully.</span></span>
    
<span data-ttu-id="40e9f-146">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="40e9f-146">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="40e9f-147">Une tentative de modification d'un objet en lecture seule ou d'une tentative d'accès à un objet pour lequel l'utilisateur ne dispose pas des autorisations suffisantes a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="40e9f-147">An attempt was made to modify a read-only object or an attempt was made to access an object for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="40e9f-148">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="40e9f-148">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="40e9f-149">Il n'y a pas d'objet associé à l'identificateur d'entrée passé dans le paramètre _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="40e9f-149">There is not an object associated with the entry identifier passed in the  _lpEntryID_ parameter.</span></span> 
    
<span data-ttu-id="40e9f-150">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="40e9f-150">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="40e9f-151">Le format de l'identificateur d'entrée transmis dans le paramètre _lpEntryID_ n'est pas reconnu.</span><span class="sxs-lookup"><span data-stu-id="40e9f-151">The entry identifier passed in the  _lpEntryID_ parameter is in an unrecognizable format.</span></span> <span data-ttu-id="40e9f-152">Cette valeur est généralement renvoyée si le fournisseur de services qui contient l'objet n'est pas ouvert.</span><span class="sxs-lookup"><span data-stu-id="40e9f-152">This value is typically returned if the service provider that contains the object is not open.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="40e9f-153">Remarques</span><span class="sxs-lookup"><span data-stu-id="40e9f-153">Remarks</span></span>

<span data-ttu-id="40e9f-154">La méthode **IMAPISession:: OpenEntry** ouvre une banque de messages ou un objet de carnet d'adresses, renvoyant un pointeur vers une interface qui peut être utilisée pour accéder à l'objet.</span><span class="sxs-lookup"><span data-stu-id="40e9f-154">The **IMAPISession::OpenEntry** method opens a message store or address book object, returning a pointer to an interface that can be used to access the object.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="40e9f-155">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="40e9f-155">Notes to callers</span></span>

> [!IMPORTANT]
> <span data-ttu-id="40e9f-156">Lors de l'ouverture d'entrées de dossier dans une banque publique, telles que des dossiers et des messages, utilisez [IMsgStore:: OpenEntry](imsgstore-openentry.md) au lieu de **IMAPISession:: OpenEntry**.</span><span class="sxs-lookup"><span data-stu-id="40e9f-156">When opening folder entries on a public store, such as folders and messages, use [IMsgStore::OpenEntry](imsgstore-openentry.md) instead of **IMAPISession::OpenEntry**.</span></span> <span data-ttu-id="40e9f-157">Cela permet de s'assurer que les dossiers publics fonctionnent correctement lorsque plusieurs comptes Exchange sont définis dans un profil.</span><span class="sxs-lookup"><span data-stu-id="40e9f-157">This ensures that public folders function correctly when multiple Exchange accounts are defined in a profile.</span></span> 
  
<span data-ttu-id="40e9f-158">Appelez **IMAPISession:: OpenEntry** uniquement lorsque vous ne connaissez pas le type d'objet que vous ouvrez.</span><span class="sxs-lookup"><span data-stu-id="40e9f-158">Call **IMAPISession::OpenEntry** only when you do not know what kind of object that you are opening.</span></span> <span data-ttu-id="40e9f-159">Si vous êtes certain que vous ouvrez un dossier ou un message, appelez [IMsgStore:: OpenEntry](imsgstore-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="40e9f-159">If you know that you are opening a folder or a message, call [IMsgStore::OpenEntry](imsgstore-openentry.md).</span></span> <span data-ttu-id="40e9f-160">Si vous êtes certain que vous ouvrez un conteneur de carnet d'adresses, un utilisateur de messagerie ou une liste de distribution, appelez [IAddrBook:: OpenEntry](iaddrbook-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="40e9f-160">If you know that you are opening an address book container, a messaging user, or a distribution list, call [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span></span> <span data-ttu-id="40e9f-161">Ces méthodes plus spécifiques sont plus rapides que **IMAPISession:: OpenEntry**.</span><span class="sxs-lookup"><span data-stu-id="40e9f-161">These more specific methods are faster than **IMAPISession::OpenEntry**.</span></span> 
  
<span data-ttu-id="40e9f-162">MAPI ouvre tous les objets avec une autorisation en lecture seule, sauf si vous définissez l'indicateur MAPI_MODIFY ou MAPI_BEST_ACCESS dans le paramètre _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="40e9f-162">MAPI opens all objects with read-only permission, unless you set the MAPI_MODIFY or MAPI_BEST_ACCESS flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="40e9f-163">Le fait de définir l'un de ces indicateurs ne garantit pas un type d'accès particulier; les autorisations qui sont accordées dépendent du fournisseur de services, du niveau d'accès et de l'objet.</span><span class="sxs-lookup"><span data-stu-id="40e9f-163">Setting one of these flags does not guarantee a particular type of access; the permissions that are granted depend on the service provider, the access level, and the object.</span></span> <span data-ttu-id="40e9f-164">Pour déterminer le niveau d'accès de l'objet ouvert, récupérez sa propriété **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="40e9f-164">To determine the access level of the opened object, retrieve its **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="40e9f-165">L'appel de **IMAPISession:: OpenEntry** et la définition de _lpEntryID_ pour pointer vers l'identificateur d'entrée d'une banque de messages est identique à l'appel de la méthode [IMAPISession:: OpenMsgStore](imapisession-openmsgstore.md) avec l'indicateur MDB_NO_DIALOG défini.</span><span class="sxs-lookup"><span data-stu-id="40e9f-165">Calling **IMAPISession::OpenEntry** and setting  _lpEntryID_ to point to the entry identifier of a message store is the same as calling the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method with the MDB_NO_DIALOG flag set.</span></span> <span data-ttu-id="40e9f-166">Les paramètres d'indicateur sont également équivalents, sauf que pour demander une autorisation en lecture/écriture avec **OpenMsgStore**, vous devez définir l'indicateur MDB_WRITE au lieu de MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="40e9f-166">The flag settings are also equivalent, except that to request read/write permission with **OpenMsgStore**, you must set the MDB_WRITE flag instead of MAPI_MODIFY.</span></span> 
  
<span data-ttu-id="40e9f-167">Vérifiez la valeur renvoyée dans le paramètre _lpulObjType_ pour déterminer si le type d'objet renvoyé est celui que vous attendiez.</span><span class="sxs-lookup"><span data-stu-id="40e9f-167">Check the value returned in the  _lpulObjType_ parameter to determine whether the object type returned is what you expected.</span></span> <span data-ttu-id="40e9f-168">Si le type d'objet n'est pas le type attendu, castez le pointeur du paramètre _lppUnk_ en pointeur du type approprié.</span><span class="sxs-lookup"><span data-stu-id="40e9f-168">If the object type is not the type that you expected, cast the pointer from the  _lppUnk_ parameter to a pointer of the appropriate type.</span></span> <span data-ttu-id="40e9f-169">Par exemple, si vous ouvrez un dossier, castez _lppUnk_ en pointeur de type LPMAPIFOLDER.</span><span class="sxs-lookup"><span data-stu-id="40e9f-169">For example, if you are opening a folder, cast  _lppUnk_ to a pointer of type LPMAPIFOLDER.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="40e9f-170">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="40e9f-170">MFCMAPI reference</span></span>

<span data-ttu-id="40e9f-171">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="40e9f-171">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="40e9f-172">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="40e9f-172">**File**</span></span>|<span data-ttu-id="40e9f-173">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="40e9f-173">**Function**</span></span>|<span data-ttu-id="40e9f-174">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="40e9f-174">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="40e9f-175">MAPIFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="40e9f-175">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="40e9f-176">CallOpenEntry</span><span class="sxs-lookup"><span data-stu-id="40e9f-176">CallOpenEntry</span></span>  <br/> |<span data-ttu-id="40e9f-177">MFCMAPI utilise la méthode **IMAPISession:: OpenEntry** pour ouvrir un objet.</span><span class="sxs-lookup"><span data-stu-id="40e9f-177">MFCMAPI uses the **IMAPISession::OpenEntry** method to open an object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="40e9f-178">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="40e9f-178">See also</span></span>



[<span data-ttu-id="40e9f-179">IAddrBook::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="40e9f-179">IAddrBook::OpenEntry</span></span>](iaddrbook-openentry.md)
  
[<span data-ttu-id="40e9f-180">IDistList : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="40e9f-180">IDistList : IMAPIContainer</span></span>](idistlistimapicontainer.md)
  
[<span data-ttu-id="40e9f-181">IMailUser : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="40e9f-181">IMailUser : IMAPIProp</span></span>](imailuserimapiprop.md)
  
[<span data-ttu-id="40e9f-182">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="40e9f-182">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
  
[<span data-ttu-id="40e9f-183">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="40e9f-183">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)
  
[<span data-ttu-id="40e9f-184">IMessage : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="40e9f-184">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)
  
[<span data-ttu-id="40e9f-185">IMsgStore::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="40e9f-185">IMsgStore::OpenEntry</span></span>](imsgstore-openentry.md)
  
[<span data-ttu-id="40e9f-186">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="40e9f-186">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="40e9f-187">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="40e9f-187">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

