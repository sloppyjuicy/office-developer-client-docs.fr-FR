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
ms.openlocfilehash: 611680db87c02b9370d6c1b3ac7a8d68b47f3050
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574026"
---
# <a name="imsgstoreopenentry"></a><span data-ttu-id="632df-103">IMsgStore::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="632df-103">IMsgStore::OpenEntry</span></span>

  
  
<span data-ttu-id="632df-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="632df-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="632df-105">Ouvre un dossier ou un message et retourne un pointeur d’interface pour l’accès des autres.</span><span class="sxs-lookup"><span data-stu-id="632df-105">Opens a folder or message and returns an interface pointer for further access.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="632df-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="632df-106">Parameters</span></span>

 <span data-ttu-id="632df-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="632df-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="632df-108">[in] Le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lpEntryID_ _._</span><span class="sxs-lookup"><span data-stu-id="632df-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter  _._</span></span>
    
 <span data-ttu-id="632df-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="632df-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="632df-110">[in] Pointeur vers l’identificateur d’entrée de l’objet à ouvrir ou valeur NULL.</span><span class="sxs-lookup"><span data-stu-id="632df-110">[in] A pointer to the entry identifier of the object to open, or NULL.</span></span> <span data-ttu-id="632df-111">Si _lpEntryID_ est défini sur NULL, **OpenEntry** ouvre le dossier racine de la banque de messages.</span><span class="sxs-lookup"><span data-stu-id="632df-111">If  _lpEntryID_ is set to NULL, **OpenEntry** opens the root folder for the message store.</span></span> 
    
 <span data-ttu-id="632df-112">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="632df-112">_lpInterface_</span></span>
  
> <span data-ttu-id="632df-113">[in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder à l’objet ouvert.</span><span class="sxs-lookup"><span data-stu-id="632df-113">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the opened object.</span></span> <span data-ttu-id="632df-114">NULL de transmission des résultats de l’objet de l’interface standard ([IMAPIFolder](imapifolderimapicontainer.md) pour des dossiers) et [IMessage](imessageimapiprop.md) pour les messages renvoyé.</span><span class="sxs-lookup"><span data-stu-id="632df-114">Passing NULL results in the object's standard interface ([IMAPIFolder](imapifolderimapicontainer.md) for folders and [IMessage](imessageimapiprop.md) for messages) being returned.</span></span> 
    
 <span data-ttu-id="632df-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="632df-115">_ulFlags_</span></span>
  
> <span data-ttu-id="632df-116">[in] Masque de bits d’indicateurs qui contrôle la façon dont l’objet est ouvert.</span><span class="sxs-lookup"><span data-stu-id="632df-116">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="632df-117">Les indicateurs suivants peuvent être utilisés :</span><span class="sxs-lookup"><span data-stu-id="632df-117">The following flags can be used:</span></span>
    
<span data-ttu-id="632df-118">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="632df-118">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="632df-119">Demande que l’objet s’ouvre avec les autorisations de réseau maximale autorisées pour l’accès des utilisateurs et le nombre maximal de clients application.</span><span class="sxs-lookup"><span data-stu-id="632df-119">Requests that the object be opened by using the maximum network permissions allowed for the user and the maximum client application access.</span></span> <span data-ttu-id="632df-120">Par exemple, si le client a l’autorisation de lecture/écriture, l’objet doit être ouvert à l’aide de l’autorisation de lecture/écriture ; Si le client dispose des autorisations en lecture seule, l’objet doit être ouvert à l’aide des autorisations en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="632df-120">For example, if the client has read/write permission, the object should be opened by using read/write permission; if the client has read-only permission, the object should be opened by using read-only permission.</span></span> 
    
<span data-ttu-id="632df-121">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="632df-121">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="632df-122">Permet **OpenEntry** renvoyer avec succès, éventuellement, avant de l’objet est entièrement disponible au client appelant.</span><span class="sxs-lookup"><span data-stu-id="632df-122">Allows **OpenEntry** to return successfully, possibly before the object is fully available to the calling client.</span></span> <span data-ttu-id="632df-123">Si l’objet n’est pas disponible, l’émission d’un appel d’objet suivantes peut déclencher une erreur.</span><span class="sxs-lookup"><span data-stu-id="632df-123">If the object is not available, making a subsequent object call can raise an error.</span></span> 
    
<span data-ttu-id="632df-124">N'</span><span class="sxs-lookup"><span data-stu-id="632df-124">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="632df-125">Demandes d’autorisation de lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="632df-125">Requests read/write permission.</span></span> <span data-ttu-id="632df-126">Par défaut, les objets sont ouverts avec l’autorisation en lecture seule et clients ne doivent pas fonctionner en supposant que l’autorisation est accordée en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="632df-126">By default, objects are opened with read-only permission, and clients should not work on the assumption that read/write permission is granted.</span></span> 
    
 <span data-ttu-id="632df-127">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="632df-127">_lpulObjType_</span></span>
  
> <span data-ttu-id="632df-128">[out] Pointeur vers le type de l’objet ouvert.</span><span class="sxs-lookup"><span data-stu-id="632df-128">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="632df-129">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="632df-129">_lppUnk_</span></span>
  
> <span data-ttu-id="632df-130">[out] Pointeur vers un pointeur vers l’objet ouvert.</span><span class="sxs-lookup"><span data-stu-id="632df-130">[out] A pointer to a pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="632df-131">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="632df-131">Return value</span></span>

<span data-ttu-id="632df-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="632df-132">S_OK</span></span> 
  
> <span data-ttu-id="632df-133">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="632df-133">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="632df-134">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="632df-134">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="632df-135">Une tentative a été effectuée pour modifier un objet en lecture seule ou pour accéder à un objet pour lequel l’utilisateur dispose d’autorisations insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="632df-135">An attempt was made to modify a read-only object or to access an object for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="632df-136">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="632df-136">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="632df-137">Lorsqu’une banque est ouvert en mode mis en cache, un client ou fournisseur de services peut appeler **IMsgStore::OpenEntry**, l’indicateur MAPI_NO_CACHE pour ouvrir un élément ou un dossier sur le magasin distant.</span><span class="sxs-lookup"><span data-stu-id="632df-137">When a store is opened in cached mode, a client or service provider can call **IMsgStore::OpenEntry**, setting the MAPI_NO_CACHE flag to open an item or a folder on the remote store.</span></span> <span data-ttu-id="632df-138">Si vous ouvrez la banque de messages avec l’indicateur MDB_ONLINE sur le serveur distant, vous n’avez pas d’utiliser l’indicateur MAPI_NO_CACHE.</span><span class="sxs-lookup"><span data-stu-id="632df-138">If you open the message store with the MDB_ONLINE flag on the remote server, you do not have to use the MAPI_NO_CACHE flag.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="632df-139">Remarques</span><span class="sxs-lookup"><span data-stu-id="632df-139">Remarks</span></span>

<span data-ttu-id="632df-140">La méthode **IMsgStore::OpenEntry** ouvre un dossier ou un message et retourne un pointeur vers une interface qui peut être utilisée pour l’accès des autres.</span><span class="sxs-lookup"><span data-stu-id="632df-140">The **IMsgStore::OpenEntry** method opens a folder or message and returns a pointer to an interface that can be used for further access.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="632df-141">Lors de l’ouverture des entrées de dossier sur un magasin public, telles que les dossiers et messages, utilisez **IMsgStore::OpenEntry** au lieu de [IMAPISession::OpenEntry](imapisession-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="632df-141">When opening folder entries on a public store, such as folders and messages, use **IMsgStore::OpenEntry** instead of [IMAPISession::OpenEntry](imapisession-openentry.md).</span></span> <span data-ttu-id="632df-142">Ainsi, cette fonction de dossiers publics correctement lorsque plusieurs comptes Exchange sont définis dans un profil.</span><span class="sxs-lookup"><span data-stu-id="632df-142">This ensures that public folders function correctly when multiple Exchange accounts are defined in a profile.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="632df-143">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="632df-143">Notes to callers</span></span>

<span data-ttu-id="632df-144">Dossiers et messages sont automatiquement ouverts avec des autorisations en lecture seule, sauf si vous définissez l’indicateur n’ou MAPI_BEST_ACCESS dans le paramètre _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="632df-144">Folders and messages are automatically opened with read-only permission, unless you set the MAPI_MODIFY or MAPI_BEST_ACCESS flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="632df-145">Définition de l’une de ces indicateurs ne garantit pas un type particulier d’autorisation ; les autorisations qui vous sont accordées dépendent de l’objet, votre niveau d’accès et le fournisseur de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="632df-145">Setting one of these flags does not guarantee a particular type of permission; the permissions that you are granted depend on the message store provider, your access level, and the object.</span></span> <span data-ttu-id="632df-146">Pour déterminer le niveau d’accès de l’objet ouvert, récupérez sa propriété **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="632df-146">To determine the access level of the opened object, retrieve its **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="632df-147">Bien que **IMsgStore::OpenEntry** peut être utilisé pour ouvrir un dossier ou un message, il est généralement plus rapide d’utiliser la méthode [IMAPIContainer::OpenEntry](imapicontainer-openentry.md) si vous avez accès au dossier parent du dossier ou du message à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="632df-147">Although **IMsgStore::OpenEntry** can be used to open any folder or message, it is usually faster to use the [IMAPIContainer::OpenEntry](imapicontainer-openentry.md) method if you have access to the parent folder of the folder or message to be opened.</span></span> 
  
<span data-ttu-id="632df-148">Vérifiez la valeur renvoyée dans le paramètre _lpulObjType_ pour déterminer si le type d’objet retourné est attendue.</span><span class="sxs-lookup"><span data-stu-id="632df-148">Check the value returned in the  _lpulObjType_ parameter to determine whether the returned object type is what you expected.</span></span> <span data-ttu-id="632df-149">Si le type d’objet n’est pas le type attendu, convertir le pointeur à partir du paramètre _lppUnk_ vers un pointeur du type approprié.</span><span class="sxs-lookup"><span data-stu-id="632df-149">If the object type is not the expected type, cast the pointer from the  _lppUnk_ parameter to a pointer of the appropriate type.</span></span> <span data-ttu-id="632df-150">Par exemple, si vous ouvrez un dossier, un cast _lppUnk_ à un pointeur du type **LPMAPIFOLDER**.</span><span class="sxs-lookup"><span data-stu-id="632df-150">For example, if you are opening a folder, cast  _lppUnk_ to a pointer of type **LPMAPIFOLDER**.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="632df-151">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="632df-151">MFCMAPI reference</span></span>

<span data-ttu-id="632df-152">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="632df-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="632df-153">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="632df-153">**File**</span></span>|<span data-ttu-id="632df-154">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="632df-154">**Function**</span></span>|<span data-ttu-id="632df-155">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="632df-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="632df-156">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="632df-156">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="632df-157">CallOpenEntry</span><span class="sxs-lookup"><span data-stu-id="632df-157">CallOpenEntry</span></span>  <br/> |<span data-ttu-id="632df-158">MFCMAPI utilise la méthode **IMsgStore::OpenEntry** pour ouvrir l’objet associé à un ID d’entrée.</span><span class="sxs-lookup"><span data-stu-id="632df-158">MFCMAPI uses the **IMsgStore::OpenEntry** method to open the object associated with an entry ID.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="632df-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="632df-159">See also</span></span>



[<span data-ttu-id="632df-160">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="632df-160">IMAPIContainer::OpenEntry</span></span>](imapicontainer-openentry.md)
  
[<span data-ttu-id="632df-161">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="632df-161">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="632df-162">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="632df-162">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

