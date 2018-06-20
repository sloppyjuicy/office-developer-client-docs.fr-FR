---
title: IMAPISessionOpenMsgStore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.OpenMsgStore
api_type:
- COM
ms.assetid: 7f73b5cf-7093-42e9-8acc-63d73df77cf5
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 983c22772acfea7837e85d409b7928a35aed91ce
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783945"
---
# <a name="imapisessionopenmsgstore"></a><span data-ttu-id="f5295-103">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="f5295-103">IMAPISession::OpenMsgStore</span></span>

<span data-ttu-id="f5295-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f5295-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f5295-105">Ouvre une banque de messages et retourne un pointeur [IMsgStore](imsgstoreimapiprop.md) pour davantage d’accès.</span><span class="sxs-lookup"><span data-stu-id="f5295-105">Opens a message store and returns an [IMsgStore](imsgstoreimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenMsgStore(
  ULONG_PTR ulUIParam,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPMDB FAR * lppMDB
);
```

## <a name="parameters"></a><span data-ttu-id="f5295-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f5295-106">Parameters</span></span>

<span data-ttu-id="f5295-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="f5295-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="f5295-108">[in] Un handle vers la fenêtre parent de la boîte de dialogue commune adresse et d’autres liées affiche.</span><span class="sxs-lookup"><span data-stu-id="f5295-108">[in] A handle to the parent window of the common address dialog box and other related displays.</span></span>
    
<span data-ttu-id="f5295-109">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="f5295-109">_cbEntryID_</span></span>
  
> <span data-ttu-id="f5295-110">[in] Le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="f5295-110">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
<span data-ttu-id="f5295-111">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="f5295-111">_lpEntryID_</span></span>
  
> <span data-ttu-id="f5295-112">[in] Pointeur vers l’identificateur d’entrée de la banque de messages à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="f5295-112">[in] A pointer to the entry identifier of the message store to be opened.</span></span> <span data-ttu-id="f5295-113">Le paramètre _lpEntryID_ ne doit pas être NULL.</span><span class="sxs-lookup"><span data-stu-id="f5295-113">The  _lpEntryID_ parameter must not be NULL.</span></span> 
    
<span data-ttu-id="f5295-114">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="f5295-114">_lpInterface_</span></span>
  
> <span data-ttu-id="f5295-115">[in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder au magasin de message.</span><span class="sxs-lookup"><span data-stu-id="f5295-115">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the message store.</span></span> <span data-ttu-id="f5295-116">Passage de NULL entraîne le paramètre _lppMDB_ renvoyer un pointeur vers l’interface standard pour une banque de messages (**IMsgStore**).</span><span class="sxs-lookup"><span data-stu-id="f5295-116">Passing NULL causes the  _lppMDB_ parameter to return a pointer to the standard interface for a message store (**IMsgStore**).</span></span>
    
<span data-ttu-id="f5295-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f5295-117">_ulFlags_</span></span>
  
> <span data-ttu-id="f5295-118">[in] Masque de bits d’indicateurs qui contrôle la façon dont l’objet est ouvert.</span><span class="sxs-lookup"><span data-stu-id="f5295-118">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="f5295-119">Les indicateurs suivants peuvent être utilisés :</span><span class="sxs-lookup"><span data-stu-id="f5295-119">The following flags can be used:</span></span>
    
  - <span data-ttu-id="f5295-120">MAPI_BEST_ACCESS : Demandes que la banque de messages s’ouvre avec les autorisations de réseau maximum autorisé pour l’utilisateur et le nombre maximal de clients application.</span><span class="sxs-lookup"><span data-stu-id="f5295-120">MAPI_BEST_ACCESS: Requests that the message store be opened with the maximum network permissions allowed for the user and the maximum client application permissions.</span></span> <span data-ttu-id="f5295-121">Par exemple, si le client a l’autorisation de lecture/écriture, la banque de messages doit être ouvert avec l’autorisation de lecture/écriture ; Si le client dispose des autorisations en lecture seule, la banque de messages doit être ouvert avec l’autorisation en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="f5295-121">For example, if the client has read/write permission, the message store should be opened with read/write permission; if the client has read-only permission, the message store should be opened with read-only permission.</span></span> 
      
  - <span data-ttu-id="f5295-122">MAPI_DEFERRED_ERRORS : Permet **OpenMsgStore** retournée correctement, éventuellement avant le message magasin est totalement disponible au client appelant.</span><span class="sxs-lookup"><span data-stu-id="f5295-122">MAPI_DEFERRED_ERRORS: Allows **OpenMsgStore** to return successfully, possibly before the message store is fully available to the calling client.</span></span> <span data-ttu-id="f5295-123">Si la banque de messages n’est pas disponible, l’émission d’un appel d’objet suivantes peut déclencher une erreur.</span><span class="sxs-lookup"><span data-stu-id="f5295-123">If the message store is not available, making a subsequent object call can raise an error.</span></span> 
      
  - <span data-ttu-id="f5295-124">MDB\_NO_DIALOG : empêche l’affichage des boîtes de dialogue d’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="f5295-124">MDB\_NO_DIALOG: Prevents the display of logon dialog boxes.</span></span> <span data-ttu-id="f5295-125">Si cet indicateur est défini et **OpenMsgStore** contient des informations de configuration insuffisante pour ouvrir la banque de messages sans l’aide de l’utilisateur, elle renvoie MAPI_E_LOGON_FAILED.</span><span class="sxs-lookup"><span data-stu-id="f5295-125">If this flag is set, and **OpenMsgStore** has insufficient configuration information to open the message store without the user's help, it returns MAPI_E_LOGON_FAILED.</span></span> <span data-ttu-id="f5295-126">Si cet indicateur n’est pas défini, le fournisseur de banque de message peut inviter l’utilisateur pour corriger un nom ou le mot de passe ou pour effectuer d’autres actions qui sont nécessaires pour établir une connexion avec la banque de messages.</span><span class="sxs-lookup"><span data-stu-id="f5295-126">If this flag is not set, the message store provider can prompt the user to correct a name or password or to perform other actions that are needed to establish a connection to the message store.</span></span> 
      
  - <span data-ttu-id="f5295-127">MDB\_NO_MAIL : la banque de messages ne doit pas être utilisée pour envoyer ou recevoir de courrier.</span><span class="sxs-lookup"><span data-stu-id="f5295-127">MDB\_NO_MAIL: The message store should not be used for sending or receiving mail.</span></span> <span data-ttu-id="f5295-128">Lorsque cet indicateur est défini, MAPI ne notifie pas les le spouleur MAPI que cette banque de messages est en cours d’ouverture.</span><span class="sxs-lookup"><span data-stu-id="f5295-128">When this flag is set, MAPI does not notify the MAPI spooler that this message store is being opened.</span></span>
      
  - <span data-ttu-id="f5295-129">MDB\_en ligne : en Mode Exchange mis en cache, un client ou fournisseur de services peut appeler cette méthode avec MDB_ONLINE pour remplacer la connexion à la base de messages locale et ouvrez le magasin sur le serveur distant.</span><span class="sxs-lookup"><span data-stu-id="f5295-129">MDB\_ONLINE: In Cached Exchange Mode, a client or service provider can call this method with MDB_ONLINE to override the connection to the local message store and open the store on the remote server.</span></span> <span data-ttu-id="f5295-130">Impossible d’ouvrir une banque Exchange en mode mis en cache et en mode non mis en cache en même temps dans la même session MAPI.</span><span class="sxs-lookup"><span data-stu-id="f5295-130">You cannot open an Exchange store in cached mode and in non-cached mode at the same time in the same MAPI session.</span></span> <span data-ttu-id="f5295-131">Si vous avez déjà ouvert la banque de messages mis en cache, vous devez soit fermer le magasin avant d’ouvrir avec cet indicateur ou ouvrir une nouvelle session MAPI où vous pouvez ouvrir la banque d’informations Exchange sur le serveur distant à l’aide de cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="f5295-131">If you have already opened the cached message store, you must either close the store before you open it with this flag, or open a new MAPI session where you can open the Exchange store on the remote server by using this flag.</span></span>
      
  - <span data-ttu-id="f5295-132">MDB_TEMPORARY : Demande à MAPI que la banque de messages n’est pas définitive et ne doit pas être ajoutée à la table.</span><span class="sxs-lookup"><span data-stu-id="f5295-132">MDB_TEMPORARY: Instructs MAPI that the message store is not permanent and should not be added to the message store table.</span></span> <span data-ttu-id="f5295-133">Cet indicateur est utilisé pour vous connecter à la banque de messages afin que les informations peuvent être récupérées par programme dans la section de profil.</span><span class="sxs-lookup"><span data-stu-id="f5295-133">This flag is used to log on to the message store so information can be retrieved programmatically from the profile section.</span></span> 
      
  - <span data-ttu-id="f5295-134">MDB_WRITE : Demandes de lecture/écriture autorisation de la banque de messages.</span><span class="sxs-lookup"><span data-stu-id="f5295-134">MDB_WRITE: Requests read/write permission to the message store.</span></span>
    
<span data-ttu-id="f5295-135">_lppMDB_</span><span class="sxs-lookup"><span data-stu-id="f5295-135">_lppMDB_</span></span>
  
> <span data-ttu-id="f5295-136">[out] Pointeur vers un pointeur de la banque de messages.</span><span class="sxs-lookup"><span data-stu-id="f5295-136">[out] Pointer to a pointer of the message store.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f5295-137">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="f5295-137">Return value</span></span>

<span data-ttu-id="f5295-138">S_OK</span><span class="sxs-lookup"><span data-stu-id="f5295-138">S_OK</span></span> 
  
> <span data-ttu-id="f5295-139">La banque de messages a été ouvert avec succès.</span><span class="sxs-lookup"><span data-stu-id="f5295-139">The message store was successfully opened.</span></span>
    
<span data-ttu-id="f5295-140">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="f5295-140">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="f5295-141">Une tentative a été effectuée pour accéder à une banque de messages pour lesquels l’utilisateur dispose d’autorisations insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="f5295-141">An attempt was made to access a message store for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="f5295-142">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="f5295-142">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="f5295-143">La banque de messages indiquée par _lpEntryID_ n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="f5295-143">The message store indicated by  _lpEntryID_ does not exist.</span></span> 
    
<span data-ttu-id="f5295-144">MAPI_E_UNKNOWN_CPID</span><span class="sxs-lookup"><span data-stu-id="f5295-144">MAPI_E_UNKNOWN_CPID</span></span> 
  
> <span data-ttu-id="f5295-145">Le serveur n’est pas configuré pour prendre en charge de la page de codes du client.</span><span class="sxs-lookup"><span data-stu-id="f5295-145">The server is not configured to support the client's code page.</span></span>
    
<span data-ttu-id="f5295-146">MAPI_E_UNKNOWN_LCID</span><span class="sxs-lookup"><span data-stu-id="f5295-146">MAPI_E_UNKNOWN_LCID</span></span> 
  
> <span data-ttu-id="f5295-147">Le serveur n’est pas configuré pour prendre en charge les informations de paramètres régionaux du client.</span><span class="sxs-lookup"><span data-stu-id="f5295-147">The server is not configured to support the client's locale information.</span></span>
    
<span data-ttu-id="f5295-148">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="f5295-148">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="f5295-149">L’appel a réussi, mais le fournisseur de banque de messages a des informations d’erreur disponibles.</span><span class="sxs-lookup"><span data-stu-id="f5295-149">The call succeeded, but the message store provider has error information available.</span></span> <span data-ttu-id="f5295-150">Lorsque cet avertissement est renvoyé, l’appel doit être traité comme étant réussi.</span><span class="sxs-lookup"><span data-stu-id="f5295-150">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="f5295-151">Pour obtenir les informations d’erreur à partir du fournisseur, appelez la méthode [IMAPISession::GetLastError](imapisession-getlasterror.md) .</span><span class="sxs-lookup"><span data-stu-id="f5295-151">To get the error information from the provider, call the [IMAPISession::GetLastError](imapisession-getlasterror.md) method.</span></span> <span data-ttu-id="f5295-152">Pour tester cet avertissement, utilisez la macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="f5295-152">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="f5295-153">Pour plus d’informations, consultez [Utilisation de Macros pour gérer les erreurs](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="f5295-153">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f5295-154">Remarques</span><span class="sxs-lookup"><span data-stu-id="f5295-154">Remarks</span></span>

<span data-ttu-id="f5295-155">La méthode **IMAPISession::OpenMsgStore** ouvre une banque de messages donnée.</span><span class="sxs-lookup"><span data-stu-id="f5295-155">The **IMAPISession::OpenMsgStore** method opens a particular message store.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="f5295-156">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="f5295-156">Notes to callers</span></span>

<span data-ttu-id="f5295-157">Le niveau d’autorisation par défaut pour les banques de messages est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="f5295-157">The default permission level for message stores is read-only.</span></span> <span data-ttu-id="f5295-158">Si vous définissez l’indicateur MDB_WRITE, vous toujours ne pourrez pas être autorisation en lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="f5295-158">If you set the MDB_WRITE flag, you still might not be granted read/write permission.</span></span> <span data-ttu-id="f5295-159">Le dernier niveau d’accès MAPI attribue à la banque de messages dépend de votre niveau d’autorisation, la banque de messages lui-même et le fournisseur de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="f5295-159">The final level of access that MAPI assigns to the message store depends on your permission level, the message store itself, and the message store provider.</span></span> 
  
<span data-ttu-id="f5295-160">Si vous appelez **OpenMsgStore** pour ouvrir une banque de messages avec une autorisation en lecture seule, les éléments suivants se produisent :</span><span class="sxs-lookup"><span data-stu-id="f5295-160">If you call **OpenMsgStore** to open a message store with read-only permission, the following will occur:</span></span> 
  
- <span data-ttu-id="f5295-161">La banque de **PR\_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) propriété n’aura pas son magasin\_MODIFY_OK et le magasin de\_CREATE_OK bits set.</span><span class="sxs-lookup"><span data-stu-id="f5295-161">The store's **PR\_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property will not have its STORE\_MODIFY_OK and STORE\_CREATE_OK bits set.</span></span> 
    
- <span data-ttu-id="f5295-162">Les appels pour ouvrir un des dossiers ou des messages de la banque de messages à l’aide de [IMAPISession::OpenEntry](imapisession-openentry.md) avec l’indicateur n’échoue.</span><span class="sxs-lookup"><span data-stu-id="f5295-162">Calls to open one of the message store's messages or folders by using [IMAPISession::OpenEntry](imapisession-openentry.md) with the MAPI_MODIFY flag set will fail.</span></span> 
    
- <span data-ttu-id="f5295-163">Les appels pour ouvrir une des propriétés des dossiers ou des messages de la banque de messages à l’aide de [IMAPIProp::OpenProperty](imapiprop-openproperty.md) avec l’indicateur n’échoue.</span><span class="sxs-lookup"><span data-stu-id="f5295-163">Calls to open one of the properties of the message store's messages or folders by using [IMAPIProp::OpenProperty](imapiprop-openproperty.md) with the MAPI_MODIFY flag will fail.</span></span> 
    
- <span data-ttu-id="f5295-164">Les appels à une des méthodes suivantes échoueront :</span><span class="sxs-lookup"><span data-stu-id="f5295-164">Calls to any of the following methods will fail:</span></span> 
    
  - [<span data-ttu-id="f5295-165">IMAPIFolder::CreateMessage</span><span class="sxs-lookup"><span data-stu-id="f5295-165">IMAPIFolder::CreateMessage</span></span>](imapifolder-createmessage.md)
    
  - [<span data-ttu-id="f5295-166">IMAPIFolder::DeleteMessages</span><span class="sxs-lookup"><span data-stu-id="f5295-166">IMAPIFolder::DeleteMessages</span></span>](imapifolder-deletemessages.md)
    
  - [<span data-ttu-id="f5295-167">IMAPIFolder::CreateFolder</span><span class="sxs-lookup"><span data-stu-id="f5295-167">IMAPIFolder::CreateFolder</span></span>](imapifolder-createfolder.md)
    
  - [<span data-ttu-id="f5295-168">IMAPIFolder::DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="f5295-168">IMAPIFolder::DeleteFolder</span></span>](imapifolder-deletefolder.md)
    
  - [<span data-ttu-id="f5295-169">IMAPIFolder::SetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="f5295-169">IMAPIFolder::SetMessageStatus</span></span>](imapifolder-setmessagestatus.md)
    
  - [<span data-ttu-id="f5295-170">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="f5295-170">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
    
  - [<span data-ttu-id="f5295-171">IMAPIProp::DeleteProps</span><span class="sxs-lookup"><span data-stu-id="f5295-171">IMAPIProp::DeleteProps</span></span>](imapiprop-deleteprops.md)
  
- <span data-ttu-id="f5295-172">Appels aux méthodes suivantes échoueront si la destination pour le message copié est en lecture seule, si la destination est la même que la banque de messages source ou un autre magasin en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="f5295-172">Calls to the following methods will fail if the destination for the copied message is read-only, whether the destination is the same as the source message store or is another read-only store.</span></span>
    
  - [<span data-ttu-id="f5295-173">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="f5295-173">IMAPIFolder::CopyMessages</span></span>](imapifolder-copymessages.md)
    
  - [<span data-ttu-id="f5295-174">IMAPIFolder::CopyFolder</span><span class="sxs-lookup"><span data-stu-id="f5295-174">IMAPIFolder::CopyFolder</span></span>](imapifolder-copyfolder.md)
    
  - [<span data-ttu-id="f5295-175">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="f5295-175">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f5295-176">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="f5295-176">MFCMAPI reference</span></span>

<span data-ttu-id="f5295-177">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="f5295-177">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f5295-178">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="f5295-178">**File**</span></span>|<span data-ttu-id="f5295-179">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="f5295-179">**Function**</span></span>|<span data-ttu-id="f5295-180">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="f5295-180">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f5295-181">MAPIStoreFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="f5295-181">MAPIStoreFunctions.cpp</span></span>  <br/> |<span data-ttu-id="f5295-182">CallOpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="f5295-182">CallOpenMsgStore</span></span>  <br/> |<span data-ttu-id="f5295-183">MFCMAPI utilise la méthode **IMAPISession::OpenMsgStore** pour ouvrir une banque de messages.</span><span class="sxs-lookup"><span data-stu-id="f5295-183">MFCMAPI uses the **IMAPISession::OpenMsgStore** method to open a message store.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f5295-184">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f5295-184">See also</span></span>

- [<span data-ttu-id="f5295-185">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="f5295-185">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)
- [<span data-ttu-id="f5295-186">IMAPISession::GetLastError</span><span class="sxs-lookup"><span data-stu-id="f5295-186">IMAPISession::GetLastError</span></span>](imapisession-getlasterror.md)
- [<span data-ttu-id="f5295-187">IMAPISession::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="f5295-187">IMAPISession::OpenEntry</span></span>](imapisession-openentry.md)
- [<span data-ttu-id="f5295-188">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="f5295-188">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
- [<span data-ttu-id="f5295-189">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f5295-189">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)
- [<span data-ttu-id="f5295-190">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="f5295-190">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
- [<span data-ttu-id="f5295-191">Utilisation de Macros pour la gestion des erreurs</span><span class="sxs-lookup"><span data-stu-id="f5295-191">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

