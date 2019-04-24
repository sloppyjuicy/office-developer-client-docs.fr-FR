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
ms.openlocfilehash: 19d3df004676a71e2bf6243d9288efd824d99c33
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325766"
---
# <a name="imapisessionopenmsgstore"></a><span data-ttu-id="1dad7-103">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="1dad7-103">IMAPISession::OpenMsgStore</span></span>

<span data-ttu-id="1dad7-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1dad7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1dad7-105">Ouvre une banque de messages et renvoie un pointeur [IMsgStore](imsgstoreimapiprop.md) pour un accès supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="1dad7-105">Opens a message store and returns an [IMsgStore](imsgstoreimapiprop.md) pointer for further access.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="1dad7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1dad7-106">Parameters</span></span>

<span data-ttu-id="1dad7-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="1dad7-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="1dad7-108">dans Un handle vers la fenêtre parent de la boîte de dialogue adresse commune et d'autres affichages connexes.</span><span class="sxs-lookup"><span data-stu-id="1dad7-108">[in] A handle to the parent window of the common address dialog box and other related displays.</span></span>
    
<span data-ttu-id="1dad7-109">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="1dad7-109">_cbEntryID_</span></span>
  
> <span data-ttu-id="1dad7-110">dans Nombre d'octets dans l'identificateur d'entrée pointé par le paramètre _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="1dad7-110">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
<span data-ttu-id="1dad7-111">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="1dad7-111">_lpEntryID_</span></span>
  
> <span data-ttu-id="1dad7-112">dans Pointeur vers l'identificateur d'entrée de la Banque de messages à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="1dad7-112">[in] A pointer to the entry identifier of the message store to be opened.</span></span> <span data-ttu-id="1dad7-113">Le paramètre _lpEntryID_ ne doit pas être null.</span><span class="sxs-lookup"><span data-stu-id="1dad7-113">The  _lpEntryID_ parameter must not be NULL.</span></span> 
    
<span data-ttu-id="1dad7-114">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="1dad7-114">_lpInterface_</span></span>
  
> <span data-ttu-id="1dad7-115">dans Pointeur vers l'identificateur d'interface (IID) qui représente l'interface à utiliser pour accéder à la Banque de messages.</span><span class="sxs-lookup"><span data-stu-id="1dad7-115">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the message store.</span></span> <span data-ttu-id="1dad7-116">En passant la valeur NULL, le paramètre _lppMDB_ renvoie un pointeur vers l'interface standard pour une banque de messages (**IMsgStore**).</span><span class="sxs-lookup"><span data-stu-id="1dad7-116">Passing NULL causes the  _lppMDB_ parameter to return a pointer to the standard interface for a message store (**IMsgStore**).</span></span>
    
<span data-ttu-id="1dad7-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1dad7-117">_ulFlags_</span></span>
  
> <span data-ttu-id="1dad7-118">dans Masque de des indicateurs qui contrôle le mode d'ouverture de l'objet.</span><span class="sxs-lookup"><span data-stu-id="1dad7-118">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="1dad7-119">Les indicateurs suivants peuvent être utilisés:</span><span class="sxs-lookup"><span data-stu-id="1dad7-119">The following flags can be used:</span></span>
    
  - <span data-ttu-id="1dad7-120">MAPI_BEST_ACCESS: demande l'ouverture de la Banque de messages avec les autorisations réseau maximales accordées à l'utilisateur et les autorisations d'application client maximales.</span><span class="sxs-lookup"><span data-stu-id="1dad7-120">MAPI_BEST_ACCESS: Requests that the message store be opened with the maximum network permissions allowed for the user and the maximum client application permissions.</span></span> <span data-ttu-id="1dad7-121">Par exemple, si le client dispose d'une autorisation en lecture/écriture, la Banque de messages doit être ouverte avec une autorisation en lecture/écriture; Si le client dispose d'une autorisation en lecture seule, la Banque de messages doit être ouverte en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="1dad7-121">For example, if the client has read/write permission, the message store should be opened with read/write permission; if the client has read-only permission, the message store should be opened with read-only permission.</span></span> 
      
  - <span data-ttu-id="1dad7-122">MAPI_DEFERRED_ERRORS: permet à **OpenMsgStore** de renvoyer correctement, éventuellement avant que la Banque de messages soit entièrement disponible pour le client appelant.</span><span class="sxs-lookup"><span data-stu-id="1dad7-122">MAPI_DEFERRED_ERRORS: Allows **OpenMsgStore** to return successfully, possibly before the message store is fully available to the calling client.</span></span> <span data-ttu-id="1dad7-123">Si la Banque de messages n'est pas disponible, un appel d'objet ultérieur peut déclencher une erreur.</span><span class="sxs-lookup"><span data-stu-id="1dad7-123">If the message store is not available, making a subsequent object call can raise an error.</span></span> 
      
  - <span data-ttu-id="1dad7-124">MDB\_NO_DIALOG: empêche l'affichage des boîtes de dialogue d'ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="1dad7-124">MDB\_NO_DIALOG: Prevents the display of logon dialog boxes.</span></span> <span data-ttu-id="1dad7-125">Si cet indicateur est défini et que **OpenMsgStore** ne dispose pas des informations de configuration suffisantes pour ouvrir la Banque de messages sans l'aide de l'utilisateur, elle renvoie MAPI_E_LOGON_FAILED.</span><span class="sxs-lookup"><span data-stu-id="1dad7-125">If this flag is set, and **OpenMsgStore** has insufficient configuration information to open the message store without the user's help, it returns MAPI_E_LOGON_FAILED.</span></span> <span data-ttu-id="1dad7-126">Si cet indicateur n'est pas défini, le fournisseur de banque de messages peut demander à l'utilisateur de corriger un nom ou un mot de passe ou d'effectuer d'autres actions nécessaires pour établir une connexion à la Banque de messages.</span><span class="sxs-lookup"><span data-stu-id="1dad7-126">If this flag is not set, the message store provider can prompt the user to correct a name or password or to perform other actions that are needed to establish a connection to the message store.</span></span> 
      
  - <span data-ttu-id="1dad7-127">MDB\_NO_MAIL: la Banque de messages ne doit pas être utilisée pour l'envoi ou la réception de messages.</span><span class="sxs-lookup"><span data-stu-id="1dad7-127">MDB\_NO_MAIL: The message store should not be used for sending or receiving mail.</span></span> <span data-ttu-id="1dad7-128">Lorsque cet indicateur est défini, MAPI n'avertit pas le spouleur MAPI que cette banque de messages est ouverte.</span><span class="sxs-lookup"><span data-stu-id="1dad7-128">When this flag is set, MAPI does not notify the MAPI spooler that this message store is being opened.</span></span>
      
  - <span data-ttu-id="1dad7-129">MDB\_en ligne: en mode Exchange mis en cache, un client ou un fournisseur de services peut appeler cette méthode avec MDB_ONLINE pour remplacer la connexion à la Banque de messages locale et ouvrir la Banque sur le serveur distant.</span><span class="sxs-lookup"><span data-stu-id="1dad7-129">MDB\_ONLINE: In Cached Exchange Mode, a client or service provider can call this method with MDB_ONLINE to override the connection to the local message store and open the store on the remote server.</span></span> <span data-ttu-id="1dad7-130">Vous ne pouvez pas ouvrir une banque Exchange en mode mis en cache et en mode non mis en cache en même temps dans la même session MAPI.</span><span class="sxs-lookup"><span data-stu-id="1dad7-130">You cannot open an Exchange store in cached mode and in non-cached mode at the same time in the same MAPI session.</span></span> <span data-ttu-id="1dad7-131">Si vous avez déjà ouvert la banque de messages mise en cache, vous devez fermer la banque avant de l’ouvrir avec cet indicateur, ou ouvrir une nouvelle session MAPI où vous pouvez ouvrir la banque d'informations Exchange sur le serveur distant à l’aide de cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="1dad7-131">If you have already opened the cached message store, you must either close the store before you open it with this flag, or open a new MAPI session where you can open the Exchange store on the remote server by using this flag.</span></span>
      
  - <span data-ttu-id="1dad7-132">MDB_TEMPORARY: indique à MAPI que la Banque de messages n'est pas permanente et qu'elle ne doit pas être ajoutée à la table de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="1dad7-132">MDB_TEMPORARY: Instructs MAPI that the message store is not permanent and should not be added to the message store table.</span></span> <span data-ttu-id="1dad7-133">Cet indicateur est utilisé pour se connecter à la Banque de messages afin que les informations puissent être récupérées par programmation à partir de la section profil.</span><span class="sxs-lookup"><span data-stu-id="1dad7-133">This flag is used to log on to the message store so information can be retrieved programmatically from the profile section.</span></span> 
      
  - <span data-ttu-id="1dad7-134">MDB_WRITE: demande une autorisation d'accès en lecture/écriture à la Banque de messages.</span><span class="sxs-lookup"><span data-stu-id="1dad7-134">MDB_WRITE: Requests read/write permission to the message store.</span></span>
    
<span data-ttu-id="1dad7-135">_lppMDB_</span><span class="sxs-lookup"><span data-stu-id="1dad7-135">_lppMDB_</span></span>
  
> <span data-ttu-id="1dad7-136">remarquer Pointeur vers un pointeur de la Banque de messages.</span><span class="sxs-lookup"><span data-stu-id="1dad7-136">[out] Pointer to a pointer of the message store.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1dad7-137">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1dad7-137">Return value</span></span>

<span data-ttu-id="1dad7-138">S_OK</span><span class="sxs-lookup"><span data-stu-id="1dad7-138">S_OK</span></span> 
  
> <span data-ttu-id="1dad7-139">La Banque de messages a été ouverte.</span><span class="sxs-lookup"><span data-stu-id="1dad7-139">The message store was successfully opened.</span></span>
    
<span data-ttu-id="1dad7-140">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="1dad7-140">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="1dad7-141">Une tentative d'accès à une banque de messages pour laquelle l'utilisateur ne dispose pas d'autorisations suffisantes a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="1dad7-141">An attempt was made to access a message store for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="1dad7-142">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="1dad7-142">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="1dad7-143">La Banque de messages indiquée par _lpEntryID_ n'existe pas.</span><span class="sxs-lookup"><span data-stu-id="1dad7-143">The message store indicated by  _lpEntryID_ does not exist.</span></span> 
    
<span data-ttu-id="1dad7-144">MAPI_E_UNKNOWN_CPID</span><span class="sxs-lookup"><span data-stu-id="1dad7-144">MAPI_E_UNKNOWN_CPID</span></span> 
  
> <span data-ttu-id="1dad7-145">Le serveur n'est pas configuré pour prendre en charge la page de code du client.</span><span class="sxs-lookup"><span data-stu-id="1dad7-145">The server is not configured to support the client's code page.</span></span>
    
<span data-ttu-id="1dad7-146">MAPI_E_UNKNOWN_LCID</span><span class="sxs-lookup"><span data-stu-id="1dad7-146">MAPI_E_UNKNOWN_LCID</span></span> 
  
> <span data-ttu-id="1dad7-147">Le serveur n'est pas configuré pour prendre en charge les informations de paramètres régionaux du client.</span><span class="sxs-lookup"><span data-stu-id="1dad7-147">The server is not configured to support the client's locale information.</span></span>
    
<span data-ttu-id="1dad7-148">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="1dad7-148">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="1dad7-149">L'appel a réussi, mais le fournisseur de banque de messages contient des informations d'erreur disponibles.</span><span class="sxs-lookup"><span data-stu-id="1dad7-149">The call succeeded, but the message store provider has error information available.</span></span> <span data-ttu-id="1dad7-150">Lorsque cet avertissement est renvoyé, l'appel doit être géré comme réussi.</span><span class="sxs-lookup"><span data-stu-id="1dad7-150">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="1dad7-151">Pour obtenir les informations d'erreur du fournisseur, appelez la méthode [IMAPISession:: GetLastError](imapisession-getlasterror.md) .</span><span class="sxs-lookup"><span data-stu-id="1dad7-151">To get the error information from the provider, call the [IMAPISession::GetLastError](imapisession-getlasterror.md) method.</span></span> <span data-ttu-id="1dad7-152">Pour tester cet avertissement, utilisez la macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="1dad7-152">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="1dad7-153">Pour plus d'informations, consultez la rubrique [utilisation des macros pour la gestion des erreurs](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="1dad7-153">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1dad7-154">Remarques</span><span class="sxs-lookup"><span data-stu-id="1dad7-154">Remarks</span></span>

<span data-ttu-id="1dad7-155">La méthode **IMAPISession:: OpenMsgStore** ouvre une banque de messages particulière.</span><span class="sxs-lookup"><span data-stu-id="1dad7-155">The **IMAPISession::OpenMsgStore** method opens a particular message store.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="1dad7-156">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="1dad7-156">Notes to callers</span></span>

<span data-ttu-id="1dad7-157">Le niveau d'autorisation par défaut pour les banques de messages est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="1dad7-157">The default permission level for message stores is read-only.</span></span> <span data-ttu-id="1dad7-158">Si vous définissez l'indicateur MDB_WRITE, il se peut que vous ne soyez pas autorisé à accéder en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="1dad7-158">If you set the MDB_WRITE flag, you still might not be granted read/write permission.</span></span> <span data-ttu-id="1dad7-159">Le niveau d'accès final attribué par MAPI à la Banque de messages dépend de votre niveau d'autorisation, de la Banque de messages proprement dite et du fournisseur de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="1dad7-159">The final level of access that MAPI assigns to the message store depends on your permission level, the message store itself, and the message store provider.</span></span> 
  
<span data-ttu-id="1dad7-160">Si vous appelez **OpenMsgStore** pour ouvrir une banque de messages avec une autorisation en lecture seule, les opérations suivantes se produisent:</span><span class="sxs-lookup"><span data-stu-id="1dad7-160">If you call **OpenMsgStore** to open a message store with read-only permission, the following will occur:</span></span> 
  
- <span data-ttu-id="1dad7-161">La propriété **PR\_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) de la Banque ne dispose pas de\_l'ensemble de\_bits Store MODIFY_OK et Store CREATE_OK.</span><span class="sxs-lookup"><span data-stu-id="1dad7-161">The store's **PR\_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property will not have its STORE\_MODIFY_OK and STORE\_CREATE_OK bits set.</span></span> 
    
- <span data-ttu-id="1dad7-162">Les appels pour ouvrir l'un des messages ou dossiers d'une banque de messages à l'aide de [IMAPISession:: OpenEntry](imapisession-openentry.md) avec l'indicateur MAPI_MODIFY défini échoueront.</span><span class="sxs-lookup"><span data-stu-id="1dad7-162">Calls to open one of the message store's messages or folders by using [IMAPISession::OpenEntry](imapisession-openentry.md) with the MAPI_MODIFY flag set will fail.</span></span> 
    
- <span data-ttu-id="1dad7-163">Les appels pour ouvrir l'une des propriétés des messages ou dossiers d'une banque de messages à l'aide de [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) avec l'indicateur MAPI_MODIFY échoueront.</span><span class="sxs-lookup"><span data-stu-id="1dad7-163">Calls to open one of the properties of the message store's messages or folders by using [IMAPIProp::OpenProperty](imapiprop-openproperty.md) with the MAPI_MODIFY flag will fail.</span></span> 
    
- <span data-ttu-id="1dad7-164">Les appels à l'une des méthodes suivantes échouent:</span><span class="sxs-lookup"><span data-stu-id="1dad7-164">Calls to any of the following methods will fail:</span></span> 
    
  - [<span data-ttu-id="1dad7-165">IMAPIFolder::CreateMessage</span><span class="sxs-lookup"><span data-stu-id="1dad7-165">IMAPIFolder::CreateMessage</span></span>](imapifolder-createmessage.md)
    
  - [<span data-ttu-id="1dad7-166">IMAPIFolder::DeleteMessages</span><span class="sxs-lookup"><span data-stu-id="1dad7-166">IMAPIFolder::DeleteMessages</span></span>](imapifolder-deletemessages.md)
    
  - [<span data-ttu-id="1dad7-167">IMAPIFolder::CreateFolder</span><span class="sxs-lookup"><span data-stu-id="1dad7-167">IMAPIFolder::CreateFolder</span></span>](imapifolder-createfolder.md)
    
  - [<span data-ttu-id="1dad7-168">IMAPIFolder::DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="1dad7-168">IMAPIFolder::DeleteFolder</span></span>](imapifolder-deletefolder.md)
    
  - [<span data-ttu-id="1dad7-169">IMAPIFolder::SetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="1dad7-169">IMAPIFolder::SetMessageStatus</span></span>](imapifolder-setmessagestatus.md)
    
  - [<span data-ttu-id="1dad7-170">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="1dad7-170">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
    
  - [<span data-ttu-id="1dad7-171">IMAPIProp::DeleteProps</span><span class="sxs-lookup"><span data-stu-id="1dad7-171">IMAPIProp::DeleteProps</span></span>](imapiprop-deleteprops.md)
  
- <span data-ttu-id="1dad7-172">Les appels aux méthodes suivantes échouent si la destination du message copié est en lecture seule, si la destination est identique à la Banque de messages source ou s'il s'agit d'une autre banque en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="1dad7-172">Calls to the following methods will fail if the destination for the copied message is read-only, whether the destination is the same as the source message store or is another read-only store.</span></span>
    
  - [<span data-ttu-id="1dad7-173">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="1dad7-173">IMAPIFolder::CopyMessages</span></span>](imapifolder-copymessages.md)
    
  - [<span data-ttu-id="1dad7-174">IMAPIFolder::CopyFolder</span><span class="sxs-lookup"><span data-stu-id="1dad7-174">IMAPIFolder::CopyFolder</span></span>](imapifolder-copyfolder.md)
    
  - [<span data-ttu-id="1dad7-175">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="1dad7-175">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1dad7-176">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="1dad7-176">MFCMAPI reference</span></span>

<span data-ttu-id="1dad7-177">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="1dad7-177">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1dad7-178">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="1dad7-178">**File**</span></span>|<span data-ttu-id="1dad7-179">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="1dad7-179">**Function**</span></span>|<span data-ttu-id="1dad7-180">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="1dad7-180">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1dad7-181">MAPIStoreFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="1dad7-181">MAPIStoreFunctions.cpp</span></span>  <br/> |<span data-ttu-id="1dad7-182">CallOpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="1dad7-182">CallOpenMsgStore</span></span>  <br/> |<span data-ttu-id="1dad7-183">MFCMAPI utilise la méthode **IMAPISession:: OpenMsgStore** pour ouvrir une banque de messages.</span><span class="sxs-lookup"><span data-stu-id="1dad7-183">MFCMAPI uses the **IMAPISession::OpenMsgStore** method to open a message store.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1dad7-184">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1dad7-184">See also</span></span>

- [<span data-ttu-id="1dad7-185">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="1dad7-185">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)
- [<span data-ttu-id="1dad7-186">IMAPISession::GetLastError</span><span class="sxs-lookup"><span data-stu-id="1dad7-186">IMAPISession::GetLastError</span></span>](imapisession-getlasterror.md)
- [<span data-ttu-id="1dad7-187">IMAPISession::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="1dad7-187">IMAPISession::OpenEntry</span></span>](imapisession-openentry.md)
- [<span data-ttu-id="1dad7-188">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="1dad7-188">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
- [<span data-ttu-id="1dad7-189">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1dad7-189">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)
- [<span data-ttu-id="1dad7-190">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="1dad7-190">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
- [<span data-ttu-id="1dad7-191">Utilisation de macros pour la gestion des erreurs</span><span class="sxs-lookup"><span data-stu-id="1dad7-191">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

