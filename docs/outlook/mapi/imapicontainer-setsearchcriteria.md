---
title: IMAPIContainerSetSearchCriteria
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer.SetSearchCriteria
api_type:
- COM
ms.assetid: b5eb1841-e450-4024-aeaa-3b5a492ddb99
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 93578300e2520dda4a9621b05ac6a79c54eca2ef
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19783708"
---
# <a name="imapicontainersetsearchcriteria"></a><span data-ttu-id="7b3cd-103">IMAPIContainer::SetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="7b3cd-103">IMAPIContainer::SetSearchCriteria</span></span>

  
  
<span data-ttu-id="7b3cd-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7b3cd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7b3cd-105">Définit les critères de recherche pour le conteneur.</span><span class="sxs-lookup"><span data-stu-id="7b3cd-105">Establishes search criteria for the container.</span></span>
  
```cpp
HRESULT SetSearchCriteria(
  LPSRestriction lpRestriction,
  LPENTRYLIST lpContainerList,
  ULONG ulSearchFlags
);
```

## <a name="parameters"></a><span data-ttu-id="7b3cd-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7b3cd-106">Parameters</span></span>

 <span data-ttu-id="7b3cd-107">_lpRestriction_</span><span class="sxs-lookup"><span data-stu-id="7b3cd-107">_lpRestriction_</span></span>
  
> <span data-ttu-id="7b3cd-108">[in] Pointeur vers une structure [SRestriction](srestriction.md) qui définit les critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="7b3cd-108">[in] A pointer to an [SRestriction](srestriction.md) structure that defines the search criteria.</span></span> <span data-ttu-id="7b3cd-109">Si NULL est indiqué dans le paramètre _lpRestriction_ , les critères de recherche qui ont été utilisés récemment pour ce conteneur sont utilisés à nouveau.</span><span class="sxs-lookup"><span data-stu-id="7b3cd-109">If NULL is passed in the  _lpRestriction_ parameter, the search criteria that were used most recently for this container are used again.</span></span> <span data-ttu-id="7b3cd-110">NULL ne doit pas être passé dans _lpRestriction_ pour la première recherche dans un conteneur.</span><span class="sxs-lookup"><span data-stu-id="7b3cd-110">NULL should not be passed in  _lpRestriction_ for the first search in a container.</span></span> 
    
 <span data-ttu-id="7b3cd-111">_lpContainerList_</span><span class="sxs-lookup"><span data-stu-id="7b3cd-111">_lpContainerList_</span></span>
  
> <span data-ttu-id="7b3cd-112">[in] Pointeur vers un tableau d’identificateurs d’entrée qui représentent les conteneurs à inclure dans la recherche.</span><span class="sxs-lookup"><span data-stu-id="7b3cd-112">[in] A pointer to an array of entry identifiers that represent containers to be included in the search.</span></span> <span data-ttu-id="7b3cd-113">Si un client passe NULL dans le paramètre _lpContainerList_ , les identificateurs d’entrée plus récemment utilisés pour rechercher ce conteneur sont utilisés pour la recherche.</span><span class="sxs-lookup"><span data-stu-id="7b3cd-113">If a client passes NULL in the  _lpContainerList_ parameter, the entry identifiers used most recently to search this container are used for the new search.</span></span> <span data-ttu-id="7b3cd-114">Un client ne doit pas passer NULL dans _lpContainerList_ pour la première recherche dans un conteneur.</span><span class="sxs-lookup"><span data-stu-id="7b3cd-114">A client should not pass NULL in  _lpContainerList_ for the first search in a container.</span></span> 
    
 <span data-ttu-id="7b3cd-115">_ulSearchFlags_</span><span class="sxs-lookup"><span data-stu-id="7b3cd-115">_ulSearchFlags_</span></span>
  
> <span data-ttu-id="7b3cd-116">[in] Masque de bits d’indicateurs qui contrôlent la façon dont la recherche est effectuée.</span><span class="sxs-lookup"><span data-stu-id="7b3cd-116">[in] A bitmask of flags that control how the search is performed.</span></span> <span data-ttu-id="7b3cd-117">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="7b3cd-117">The following flags can be set:</span></span>
    
<span data-ttu-id="7b3cd-118">BACKGROUND_SEARCH</span><span class="sxs-lookup"><span data-stu-id="7b3cd-118">BACKGROUND_SEARCH</span></span> 
  
> <span data-ttu-id="7b3cd-119">La recherche doit être exécutée à une priorité normale par rapport à d’autres critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="7b3cd-119">The search should run at normal priority relative to other searches.</span></span> <span data-ttu-id="7b3cd-120">Cet indicateur ne peut pas être défini en même temps que l’indicateur FOREGROUND_SEARCH.</span><span class="sxs-lookup"><span data-stu-id="7b3cd-120">This flag cannot be set at the same time as the FOREGROUND_SEARCH flag.</span></span>
    
<span data-ttu-id="7b3cd-121">FOREGROUND_SEARCH</span><span class="sxs-lookup"><span data-stu-id="7b3cd-121">FOREGROUND_SEARCH</span></span> 
  
> <span data-ttu-id="7b3cd-122">La recherche doit être exécutée à priorité élevée par rapport à d’autres critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="7b3cd-122">The search should run at high priority relative to other searches.</span></span> <span data-ttu-id="7b3cd-123">Cet indicateur ne peut pas être défini en même temps que l’indicateur BACKGROUND_SEARCH.</span><span class="sxs-lookup"><span data-stu-id="7b3cd-123">This flag cannot be set at the same time as the BACKGROUND_SEARCH flag.</span></span>
    
<span data-ttu-id="7b3cd-124">NON_CONTENT_INDEXED_SEARCH</span><span class="sxs-lookup"><span data-stu-id="7b3cd-124">NON_CONTENT_INDEXED_SEARCH</span></span>
  
> <span data-ttu-id="7b3cd-125">La recherche ne doit pas utiliser l’indexation de contenu pour rechercher des entrées correspondantes.</span><span class="sxs-lookup"><span data-stu-id="7b3cd-125">The search should not use content indexing to find matching entries.</span></span> <span data-ttu-id="7b3cd-126">Cet indicateur n’est valide pour les banques Exchange.</span><span class="sxs-lookup"><span data-stu-id="7b3cd-126">This flag is only valid for Exchange stores.</span></span>
    
<span data-ttu-id="7b3cd-127">RECURSIVE_SEARCH</span><span class="sxs-lookup"><span data-stu-id="7b3cd-127">RECURSIVE_SEARCH</span></span> 
  
> <span data-ttu-id="7b3cd-128">La recherche doit inclure les conteneurs spécifiés dans le paramètre _lpContainerList_ et tous les conteneurs de leurs enfants.</span><span class="sxs-lookup"><span data-stu-id="7b3cd-128">The search should include the containers specified in the  _lpContainerList_ parameter and all their child containers.</span></span> <span data-ttu-id="7b3cd-129">Cet indicateur ne peut pas être défini en même temps que l’indicateur SHALLOW_SEARCH.</span><span class="sxs-lookup"><span data-stu-id="7b3cd-129">This flag cannot be set at the same time as the SHALLOW_SEARCH flag.</span></span> 
    
<span data-ttu-id="7b3cd-130">RESTART_SEARCH</span><span class="sxs-lookup"><span data-stu-id="7b3cd-130">RESTART_SEARCH</span></span> 
  
> <span data-ttu-id="7b3cd-131">La recherche doit être lancée s’il s’agit du premier appel à **SetSearchCriteria**ou redémarrée si la recherche est inactive.</span><span class="sxs-lookup"><span data-stu-id="7b3cd-131">The search should be initiated if this is the first call to **SetSearchCriteria**, or restarted if the search is inactive.</span></span> <span data-ttu-id="7b3cd-132">Cet indicateur ne peut pas être défini en même temps que l’indicateur STOP_SEARCH.</span><span class="sxs-lookup"><span data-stu-id="7b3cd-132">This flag cannot be set at the same time as the STOP_SEARCH flag.</span></span>
    
<span data-ttu-id="7b3cd-133">SHALLOW_SEARCH</span><span class="sxs-lookup"><span data-stu-id="7b3cd-133">SHALLOW_SEARCH</span></span> 
  
> <span data-ttu-id="7b3cd-134">La recherche porte uniquement dans les conteneurs spécifiés dans le paramètre _lpContainerList_ pour la correspondance des entrées.</span><span class="sxs-lookup"><span data-stu-id="7b3cd-134">The search should look only in the containers specified in the  _lpContainerList_ parameter for matching entries.</span></span> <span data-ttu-id="7b3cd-135">Cet indicateur ne peut pas être défini en même temps que l’indicateur RECURSIVE_SEARCH.</span><span class="sxs-lookup"><span data-stu-id="7b3cd-135">This flag cannot be set at the same time as the RECURSIVE_SEARCH flag.</span></span> 
    
<span data-ttu-id="7b3cd-136">STOP_SEARCH</span><span class="sxs-lookup"><span data-stu-id="7b3cd-136">STOP_SEARCH</span></span> 
  
> <span data-ttu-id="7b3cd-137">La recherche doit être arrêtée.</span><span class="sxs-lookup"><span data-stu-id="7b3cd-137">The search should be stopped.</span></span> <span data-ttu-id="7b3cd-138">Cet indicateur ne peut pas être défini en même temps que l’indicateur RESTART_SEARCH.</span><span class="sxs-lookup"><span data-stu-id="7b3cd-138">This flag cannot be set at the same time as the RESTART_SEARCH flag.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7b3cd-139">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="7b3cd-139">Return value</span></span>

<span data-ttu-id="7b3cd-140">S_OK</span><span class="sxs-lookup"><span data-stu-id="7b3cd-140">S_OK</span></span> 
  
> <span data-ttu-id="7b3cd-141">Les critères de recherche a été défini.</span><span class="sxs-lookup"><span data-stu-id="7b3cd-141">The search criteria was successfully set.</span></span>
    
<span data-ttu-id="7b3cd-142">MAPI_E_TOO_COMPLEX</span><span class="sxs-lookup"><span data-stu-id="7b3cd-142">MAPI_E_TOO_COMPLEX</span></span> 
  
> <span data-ttu-id="7b3cd-143">Le fournisseur de services ne gère pas les critères de recherche spécifiée.</span><span class="sxs-lookup"><span data-stu-id="7b3cd-143">The service provider does not support the specified search criteria.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7b3cd-144">Note</span><span class="sxs-lookup"><span data-stu-id="7b3cd-144">Remarks</span></span>

<span data-ttu-id="7b3cd-145">La méthode **IMAPIContainer::SetSearchCriteria** établit les critères de recherche pour un conteneur qui prend en charge les recherches, généralement un dossier de résultats de recherche.</span><span class="sxs-lookup"><span data-stu-id="7b3cd-145">The **IMAPIContainer::SetSearchCriteria** method establishes search criteria for a container that supports searches, typically a search-results folder.</span></span> <span data-ttu-id="7b3cd-146">Un dossier de résultats de recherche contient des liens vers les messages qui répondent aux critères de recherche ; les messages réels sont toujours stockés dans leurs emplacements d’origine.</span><span class="sxs-lookup"><span data-stu-id="7b3cd-146">A search-results folder contains links to the messages that meet the search criteria; the actual messages are still stored in their original locations.</span></span> <span data-ttu-id="7b3cd-147">Les données uniquement uniques qui se trouve dans un dossier de résultats de recherche sont sa table des matières.</span><span class="sxs-lookup"><span data-stu-id="7b3cd-147">The only unique data that is contained in a search-results folder is its contents table.</span></span> <span data-ttu-id="7b3cd-148">La table des matières d’un dossier de résultats de recherche a le contenu de la banque de messages fusionné après que la restriction de recherche a été appliquée.</span><span class="sxs-lookup"><span data-stu-id="7b3cd-148">The contents table of a search-results folder has the merged contents of the message store after the search restriction has been applied.</span></span> 
  
<span data-ttu-id="7b3cd-149">Une opération de recherche fonctionne uniquement sur ce tableau contenu fusionné ; Il ne recherche pas les autres dossiers de résultats de recherche.</span><span class="sxs-lookup"><span data-stu-id="7b3cd-149">A search operation works only on this merged contents table; it does not search through other search-results folders.</span></span> <span data-ttu-id="7b3cd-150">Les résultats de recherche retournent uniquement les messages qui correspondent aux critères de recherche ; la hiérarchie de dossiers n’est pas retournée.</span><span class="sxs-lookup"><span data-stu-id="7b3cd-150">The search results return only the messages that match the search criteria; the folder hierarchy is not returned.</span></span>
  
<span data-ttu-id="7b3cd-151">Contrôle est renvoyé au client lors de la recherche est terminée.</span><span class="sxs-lookup"><span data-stu-id="7b3cd-151">Control is returned to the client when the search has finished.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="7b3cd-152">Remarques destinées aux responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="7b3cd-152">Notes to implementers</span></span>

<span data-ttu-id="7b3cd-153">Conteneurs de carnet d’adresses établissent des critères de recherche en appliquant des restrictions à leurs tables de contenu.</span><span class="sxs-lookup"><span data-stu-id="7b3cd-153">Address book containers establish search criteria by applying restrictions to their contents tables.</span></span> <span data-ttu-id="7b3cd-154">Pour plus d’informations sur les critères de recherche et les conteneurs de carnet d’adresses, voir [Implémentation de la recherche avancée](implementing-advanced-searching.md).</span><span class="sxs-lookup"><span data-stu-id="7b3cd-154">For more information about search criteria and address book containers, see [Implementing Advanced Searching](implementing-advanced-searching.md).</span></span>
  
<span data-ttu-id="7b3cd-155">Doit prendre en charge open, copier, déplacer et supprimer des opérations sur les messages dans les dossiers de résultats de recherche, et non sur le dossier de résultats de recherche proprement dite.</span><span class="sxs-lookup"><span data-stu-id="7b3cd-155">You should support open, copy, move, and delete operations on the messages within search-results folders, not on the search-results folder itself.</span></span> <span data-ttu-id="7b3cd-156">Ne pas autoriser les messages créés dans ou copiées dans un dossier de résultats de recherche.</span><span class="sxs-lookup"><span data-stu-id="7b3cd-156">Do not allow messages to be created within or copied into a search-results folder.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="7b3cd-157">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="7b3cd-157">Notes to callers</span></span>

<span data-ttu-id="7b3cd-158">Pour rechercher des destinataires du message, la valeur _lpRestriction_ pour pointer vers une restriction sous-objet avec le membre **ulSubObject** de la structure [SSubRestriction](ssubrestriction.md) défini sur **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="7b3cd-158">To search for message recipients, set  _lpRestriction_ to point to a subobject restriction with the **ulSubObject** member in the [SSubRestriction](ssubrestriction.md) structure set to **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)).</span></span> <span data-ttu-id="7b3cd-159">Pour rechercher des pièces jointes, la valeur du membre **ulSubObject** **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="7b3cd-159">To search for attachments, set the **ulSubObject** member to **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)).</span></span> <span data-ttu-id="7b3cd-160">Définissez le membre **lpRes** pour pointer vers une restriction de propriété qui décrit les critères de recherche pour les destinataires ou les pièces jointes.</span><span class="sxs-lookup"><span data-stu-id="7b3cd-160">Set the **lpRes** member to point to a property restriction that describes the search criteria for the recipients or attachments.</span></span> 
  
<span data-ttu-id="7b3cd-161">Par exemple, pour rechercher des pièces jointes ayant l’extension .mss, la valeur **ulSubObject** **PR_MESSAGE_ATTACHMENTS** et **lpRes** à une restriction de propriété qui correspond à **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md) ) avec. mss.</span><span class="sxs-lookup"><span data-stu-id="7b3cd-161">For example, to look for file attachments that have the extension .mss, set **ulSubObject** to **PR_MESSAGE_ATTACHMENTS** and **lpRes** to a property restriction that matches **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) with .mss.</span></span>
  
<span data-ttu-id="7b3cd-162">Définition de l’indicateur FOREGROUND_SEARCH dans le paramètre _ulSearchFlags_ peut entraîner une diminution des performances du système.</span><span class="sxs-lookup"><span data-stu-id="7b3cd-162">Setting the FOREGROUND_SEARCH flag in the  _ulSearchFlags_ parameter could cause a decrease in system performance.</span></span> 
  
<span data-ttu-id="7b3cd-163">Vous pouvez utiliser **SetSearchCriteria** pour modifier les critères de recherche d’une recherche en cours.</span><span class="sxs-lookup"><span data-stu-id="7b3cd-163">You can use **SetSearchCriteria** to change the search criteria of a search already in progress.</span></span> <span data-ttu-id="7b3cd-164">Vous pouvez spécifier de nouvelles restrictions, de nouvelles listes de dossiers à rechercher et une nouvelle priorité de la recherche, tels que la mise à niveau d’une recherche à une priorité plus élevée.</span><span class="sxs-lookup"><span data-stu-id="7b3cd-164">You can specify new restrictions, new lists of folders to search, and a new search priority, such as upgrading a search to a higher priority.</span></span> <span data-ttu-id="7b3cd-165">Modifications apportées à la priorité de la recherche ne provoquent pas une recherche existante à redémarrer, mais les autres modifications apportées aux critères de recherche peuvent.</span><span class="sxs-lookup"><span data-stu-id="7b3cd-165">Changes in search priority do not cause an existing search to restart, but other changes to search criteria can.</span></span> 
  
<span data-ttu-id="7b3cd-166">Lorsque vous êtes à l’aide d’un dossier de résultats de recherche, vous pouvez supprimer le dossier ou laissez-le restent ouverts pour une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="7b3cd-166">When you are through using a search-results folder, you can either delete the folder or let it remain open for later use.</span></span> <span data-ttu-id="7b3cd-167">Si vous ne supprimez pas le dossier de résultats de recherche, uniquement les liaisons de message sont supprimés.</span><span class="sxs-lookup"><span data-stu-id="7b3cd-167">If you do delete the search-results folder, only message links are deleted.</span></span> <span data-ttu-id="7b3cd-168">Les messages restent dans leurs dossiers parents.</span><span class="sxs-lookup"><span data-stu-id="7b3cd-168">The actual messages remain in their parent folders.</span></span> 
  
<span data-ttu-id="7b3cd-169">Pour plus d’informations sur les dossiers des résultats de recherche, voir [Dossiers de recherche MAPI](mapi-search-folders.md).</span><span class="sxs-lookup"><span data-stu-id="7b3cd-169">For more information about search-results folders, see [MAPI Search Folders](mapi-search-folders.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="7b3cd-170">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="7b3cd-170">MFCMAPI reference</span></span>

<span data-ttu-id="7b3cd-171">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="7b3cd-171">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="7b3cd-172">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="7b3cd-172">**File**</span></span>|<span data-ttu-id="7b3cd-173">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="7b3cd-173">**Function**</span></span>|<span data-ttu-id="7b3cd-174">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="7b3cd-174">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7b3cd-175">HierarchyTableDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="7b3cd-175">HierarchyTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="7b3cd-176">CHierarchyTableDlg::OnEditSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="7b3cd-176">CHierarchyTableDlg::OnEditSearchCriteria</span></span>  <br/> |<span data-ttu-id="7b3cd-177">MFCMAPI utilise la méthode **IMAPIContainer::SetSearchCriteria** pour écrire les critères de recherche pour un dossier après qu’un utilisateur a le modifiée.</span><span class="sxs-lookup"><span data-stu-id="7b3cd-177">MFCMAPI uses the **IMAPIContainer::SetSearchCriteria** method to write search criteria for a folder after a user has edited it.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7b3cd-178">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7b3cd-178">See also</span></span>



[<span data-ttu-id="7b3cd-179">IMAPIContainer::GetContentsTable</span><span class="sxs-lookup"><span data-stu-id="7b3cd-179">IMAPIContainer::GetContentsTable</span></span>](imapicontainer-getcontentstable.md)
  
[<span data-ttu-id="7b3cd-180">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="7b3cd-180">IMAPIContainer::OpenEntry</span></span>](imapicontainer-openentry.md)
  
[<span data-ttu-id="7b3cd-181">IMAPIFolder::CreateFolder</span><span class="sxs-lookup"><span data-stu-id="7b3cd-181">IMAPIFolder::CreateFolder</span></span>](imapifolder-createfolder.md)
  
[<span data-ttu-id="7b3cd-182">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="7b3cd-182">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
  
[<span data-ttu-id="7b3cd-183">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="7b3cd-183">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="7b3cd-184">SRestriction</span><span class="sxs-lookup"><span data-stu-id="7b3cd-184">SRestriction</span></span>](srestriction.md)
  
[<span data-ttu-id="7b3cd-185">SSubRestriction</span><span class="sxs-lookup"><span data-stu-id="7b3cd-185">SSubRestriction</span></span>](ssubrestriction.md)
  
[<span data-ttu-id="7b3cd-186">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="7b3cd-186">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


[<span data-ttu-id="7b3cd-187">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="7b3cd-187">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

