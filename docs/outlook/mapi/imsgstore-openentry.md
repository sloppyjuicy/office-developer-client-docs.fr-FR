---
title: IMsgStoreOpenEntry
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.OpenEntry
api_type:
- COM
ms.assetid: a63c42cf-36af-466b-b41e-d6b53ce1c9fb
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 07667558a21a9110d684164d2e6c143d6a519368
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409334"
---
# <a name="imsgstoreopenentry"></a><span data-ttu-id="323c7-103">IMsgStore::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="323c7-103">IMsgStore::OpenEntry</span></span>

  
  
<span data-ttu-id="323c7-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="323c7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="323c7-105">Ouvre un dossier ou un message et renvoie un pointeur d'interface pour un accès supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="323c7-105">Opens a folder or message and returns an interface pointer for further access.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="323c7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="323c7-106">Parameters</span></span>

 <span data-ttu-id="323c7-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="323c7-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="323c7-108">dans Nombre d'octets dans l'identificateur d'entrée pointé par le paramètre _lpEntryID_ _._</span><span class="sxs-lookup"><span data-stu-id="323c7-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter  _._</span></span>
    
 <span data-ttu-id="323c7-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="323c7-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="323c7-110">dans Pointeur vers l'identificateur d'entrée de l'objet à ouvrir ou valeur NULL.</span><span class="sxs-lookup"><span data-stu-id="323c7-110">[in] A pointer to the entry identifier of the object to open, or NULL.</span></span> <span data-ttu-id="323c7-111">Si _lpEntryID_ est défini sur null, **OpenEntry** ouvre le dossier racine de la Banque de messages.</span><span class="sxs-lookup"><span data-stu-id="323c7-111">If  _lpEntryID_ is set to NULL, **OpenEntry** opens the root folder for the message store.</span></span> 
    
 <span data-ttu-id="323c7-112">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="323c7-112">_lpInterface_</span></span>
  
> <span data-ttu-id="323c7-113">dans Pointeur vers l'identificateur d'interface (IID) qui représente l'interface à utiliser pour accéder à l'objet ouvert.</span><span class="sxs-lookup"><span data-stu-id="323c7-113">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the opened object.</span></span> <span data-ttu-id="323c7-114">Le passage des résultats de la valeur NULL dans l'interface standard de l'objet ([IMAPIFolder](imapifolderimapicontainer.md) pour les dossiers et [IMessage](imessageimapiprop.md) pour les messages) est renvoyé.</span><span class="sxs-lookup"><span data-stu-id="323c7-114">Passing NULL results in the object's standard interface ([IMAPIFolder](imapifolderimapicontainer.md) for folders and [IMessage](imessageimapiprop.md) for messages) being returned.</span></span> 
    
 <span data-ttu-id="323c7-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="323c7-115">_ulFlags_</span></span>
  
> <span data-ttu-id="323c7-116">dans Masque de des indicateurs qui contrôle le mode d'ouverture de l'objet.</span><span class="sxs-lookup"><span data-stu-id="323c7-116">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="323c7-117">Les indicateurs suivants peuvent être utilisés:</span><span class="sxs-lookup"><span data-stu-id="323c7-117">The following flags can be used:</span></span>
    
<span data-ttu-id="323c7-118">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="323c7-118">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="323c7-119">Demande l'ouverture de l'objet à l'aide des autorisations réseau maximales autorisées pour l'utilisateur et de l'accès à l'application cliente maximale.</span><span class="sxs-lookup"><span data-stu-id="323c7-119">Requests that the object be opened by using the maximum network permissions allowed for the user and the maximum client application access.</span></span> <span data-ttu-id="323c7-120">Par exemple, si le client dispose d'une autorisation en lecture/écriture, l'objet doit être ouvert à l'aide de l'autorisation de lecture/écriture; Si le client dispose d'une autorisation en lecture seule, l'objet doit être ouvert à l'aide de l'autorisation en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="323c7-120">For example, if the client has read/write permission, the object should be opened by using read/write permission; if the client has read-only permission, the object should be opened by using read-only permission.</span></span> 
    
<span data-ttu-id="323c7-121">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="323c7-121">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="323c7-122">Permet à **OpenEntry** de retourner correctement, éventuellement avant que l'objet soit entièrement disponible pour le client appelant.</span><span class="sxs-lookup"><span data-stu-id="323c7-122">Allows **OpenEntry** to return successfully, possibly before the object is fully available to the calling client.</span></span> <span data-ttu-id="323c7-123">Si l'objet n'est pas disponible, un appel d'objet ultérieur peut déclencher une erreur.</span><span class="sxs-lookup"><span data-stu-id="323c7-123">If the object is not available, making a subsequent object call can raise an error.</span></span> 
    
<span data-ttu-id="323c7-124">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="323c7-124">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="323c7-125">Demande une autorisation en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="323c7-125">Requests read/write permission.</span></span> <span data-ttu-id="323c7-126">Par défaut, les objets sont ouverts avec une autorisation en lecture seule, et les clients ne doivent pas travailler en supposant que l'autorisation de lecture/écriture est accordée.</span><span class="sxs-lookup"><span data-stu-id="323c7-126">By default, objects are opened with read-only permission, and clients should not work on the assumption that read/write permission is granted.</span></span> 
    
 <span data-ttu-id="323c7-127">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="323c7-127">_lpulObjType_</span></span>
  
> <span data-ttu-id="323c7-128">remarquer Pointeur vers le type de l'objet ouvert.</span><span class="sxs-lookup"><span data-stu-id="323c7-128">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="323c7-129">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="323c7-129">_lppUnk_</span></span>
  
> <span data-ttu-id="323c7-130">remarquer Pointeur vers un pointeur vers l'objet ouvert.</span><span class="sxs-lookup"><span data-stu-id="323c7-130">[out] A pointer to a pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="323c7-131">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="323c7-131">Return value</span></span>

<span data-ttu-id="323c7-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="323c7-132">S_OK</span></span> 
  
> <span data-ttu-id="323c7-133">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="323c7-133">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="323c7-134">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="323c7-134">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="323c7-135">Une tentative de modification d'un objet en lecture seule ou d'accès à un objet pour lequel l'utilisateur ne dispose pas des autorisations suffisantes a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="323c7-135">An attempt was made to modify a read-only object or to access an object for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="323c7-136">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="323c7-136">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="323c7-137">Lorsqu'un magasin est ouvert en mode mis en cache, un client ou un fournisseur de services peut appeler **IMsgStore:: OpenEntry**, en définissant l'indicateur MAPI_NO_CACHE pour ouvrir un élément ou un dossier sur le magasin distant.</span><span class="sxs-lookup"><span data-stu-id="323c7-137">When a store is opened in cached mode, a client or service provider can call **IMsgStore::OpenEntry**, setting the MAPI_NO_CACHE flag to open an item or a folder on the remote store.</span></span> <span data-ttu-id="323c7-138">Si vous ouvrez la Banque de messages avec l'indicateur MDB_ONLINE sur le serveur distant, il n'est pas nécessaire d'utiliser l'indicateur MAPI_NO_CACHE.</span><span class="sxs-lookup"><span data-stu-id="323c7-138">If you open the message store with the MDB_ONLINE flag on the remote server, you do not have to use the MAPI_NO_CACHE flag.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="323c7-139">Remarques</span><span class="sxs-lookup"><span data-stu-id="323c7-139">Remarks</span></span>

<span data-ttu-id="323c7-140">La méthode **IMsgStore:: OpenEntry** ouvre un dossier ou un message et renvoie un pointeur vers une interface qui peut être utilisée pour un accès supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="323c7-140">The **IMsgStore::OpenEntry** method opens a folder or message and returns a pointer to an interface that can be used for further access.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="323c7-141">Lors de l'ouverture d'entrées de dossier dans une banque publique, telles que des dossiers et des messages, utilisez **IMsgStore:: OpenEntry** au lieu de [IMAPISession:: OpenEntry](imapisession-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="323c7-141">When opening folder entries on a public store, such as folders and messages, use **IMsgStore::OpenEntry** instead of [IMAPISession::OpenEntry](imapisession-openentry.md).</span></span> <span data-ttu-id="323c7-142">Cela permet de s'assurer que les dossiers publics fonctionnent correctement lorsque plusieurs comptes Exchange sont définis dans un profil.</span><span class="sxs-lookup"><span data-stu-id="323c7-142">This ensures that public folders function correctly when multiple Exchange accounts are defined in a profile.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="323c7-143">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="323c7-143">Notes to callers</span></span>

<span data-ttu-id="323c7-144">Les dossiers et les messages sont automatiquement ouverts en lecture seule, sauf si vous définissez l'indicateur MAPI_MODIFY ou MAPI_BEST_ACCESS dans le paramètre _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="323c7-144">Folders and messages are automatically opened with read-only permission, unless you set the MAPI_MODIFY or MAPI_BEST_ACCESS flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="323c7-145">Le fait de définir l'un de ces indicateurs ne garantit pas un type d'autorisation particulier; les autorisations que vous êtes accordé dépendent du fournisseur de banque de messages, de votre niveau d'accès et de l'objet.</span><span class="sxs-lookup"><span data-stu-id="323c7-145">Setting one of these flags does not guarantee a particular type of permission; the permissions that you are granted depend on the message store provider, your access level, and the object.</span></span> <span data-ttu-id="323c7-146">Pour déterminer le niveau d'accès de l'objet ouvert, récupérez sa propriété **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="323c7-146">To determine the access level of the opened object, retrieve its **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="323c7-147">Bien que **IMsgStore:: OpenEntry** puisse être utilisé pour ouvrir un dossier ou un message, il est généralement plus rapide d'utiliser la méthode [IMAPIContainer:: OpenEntry](imapicontainer-openentry.md) si vous avez accès au dossier parent du dossier ou du message à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="323c7-147">Although **IMsgStore::OpenEntry** can be used to open any folder or message, it is usually faster to use the [IMAPIContainer::OpenEntry](imapicontainer-openentry.md) method if you have access to the parent folder of the folder or message to be opened.</span></span> 
  
<span data-ttu-id="323c7-148">Vérifiez la valeur renvoyée dans le paramètre _lpulObjType_ pour déterminer si le type d'objet renvoyé est celui que vous attendiez.</span><span class="sxs-lookup"><span data-stu-id="323c7-148">Check the value returned in the  _lpulObjType_ parameter to determine whether the returned object type is what you expected.</span></span> <span data-ttu-id="323c7-149">Si le type d'objet n'est pas le type attendu, castez le pointeur du paramètre _lppUnk_ en pointeur du type approprié.</span><span class="sxs-lookup"><span data-stu-id="323c7-149">If the object type is not the expected type, cast the pointer from the  _lppUnk_ parameter to a pointer of the appropriate type.</span></span> <span data-ttu-id="323c7-150">Par exemple, si vous ouvrez un dossier, castez _lppUnk_ en pointeur de type **LPMAPIFOLDER**.</span><span class="sxs-lookup"><span data-stu-id="323c7-150">For example, if you are opening a folder, cast  _lppUnk_ to a pointer of type **LPMAPIFOLDER**.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="323c7-151">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="323c7-151">MFCMAPI reference</span></span>

<span data-ttu-id="323c7-152">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="323c7-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="323c7-153">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="323c7-153">**File**</span></span>|<span data-ttu-id="323c7-154">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="323c7-154">**Function**</span></span>|<span data-ttu-id="323c7-155">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="323c7-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="323c7-156">MAPIFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="323c7-156">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="323c7-157">CallOpenEntry</span><span class="sxs-lookup"><span data-stu-id="323c7-157">CallOpenEntry</span></span>  <br/> |<span data-ttu-id="323c7-158">MFCMAPI utilise la méthode **IMsgStore:: OpenEntry** pour ouvrir l'objet associé à un ID d'entrée.</span><span class="sxs-lookup"><span data-stu-id="323c7-158">MFCMAPI uses the **IMsgStore::OpenEntry** method to open the object associated with an entry ID.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="323c7-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="323c7-159">See also</span></span>



[<span data-ttu-id="323c7-160">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="323c7-160">IMAPIContainer::OpenEntry</span></span>](imapicontainer-openentry.md)
  
[<span data-ttu-id="323c7-161">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="323c7-161">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="323c7-162">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="323c7-162">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

