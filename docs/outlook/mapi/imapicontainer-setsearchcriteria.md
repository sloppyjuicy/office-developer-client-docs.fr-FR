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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: a6168e8fced2fff3a7f9d273e47ed2410ac4c010
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427198"
---
# <a name="imapicontainersetsearchcriteria"></a><span data-ttu-id="03bb7-103">IMAPIContainer::SetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="03bb7-103">IMAPIContainer::SetSearchCriteria</span></span>

  
  
<span data-ttu-id="03bb7-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="03bb7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="03bb7-105">Établit des critères de recherche pour le conteneur.</span><span class="sxs-lookup"><span data-stu-id="03bb7-105">Establishes search criteria for the container.</span></span>
  
```cpp
HRESULT SetSearchCriteria(
  LPSRestriction lpRestriction,
  LPENTRYLIST lpContainerList,
  ULONG ulSearchFlags
);
```

## <a name="parameters"></a><span data-ttu-id="03bb7-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="03bb7-106">Parameters</span></span>

 <span data-ttu-id="03bb7-107">_lpRestriction_</span><span class="sxs-lookup"><span data-stu-id="03bb7-107">_lpRestriction_</span></span>
  
> <span data-ttu-id="03bb7-108">[in] Pointeur vers une structure [SRestriction](srestriction.md) qui définit les critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="03bb7-108">[in] A pointer to an [SRestriction](srestriction.md) structure that defines the search criteria.</span></span> <span data-ttu-id="03bb7-109">Si LA VALEUR NULL est passée dans le paramètre  _lpRestriction,_ les critères de recherche les plus récemment utilisés pour ce conteneur sont utilisés à nouveau.</span><span class="sxs-lookup"><span data-stu-id="03bb7-109">If NULL is passed in the  _lpRestriction_ parameter, the search criteria that were used most recently for this container are used again.</span></span> <span data-ttu-id="03bb7-110">Null ne doit pas être transmis dans  _lpRestriction_ pour la première recherche dans un conteneur.</span><span class="sxs-lookup"><span data-stu-id="03bb7-110">NULL should not be passed in  _lpRestriction_ for the first search in a container.</span></span> 
    
 <span data-ttu-id="03bb7-111">_lpContainerList_</span><span class="sxs-lookup"><span data-stu-id="03bb7-111">_lpContainerList_</span></span>
  
> <span data-ttu-id="03bb7-112">[in] Pointeur vers un tableau d’identificateurs d’entrée qui représentent les conteneurs à inclure dans la recherche.</span><span class="sxs-lookup"><span data-stu-id="03bb7-112">[in] A pointer to an array of entry identifiers that represent containers to be included in the search.</span></span> <span data-ttu-id="03bb7-113">Si un client transmet la valeur NULL dans le paramètre  _lpContainerList,_ les identificateurs d’entrée utilisés le plus récemment pour rechercher ce conteneur sont utilisés pour la nouvelle recherche.</span><span class="sxs-lookup"><span data-stu-id="03bb7-113">If a client passes NULL in the  _lpContainerList_ parameter, the entry identifiers used most recently to search this container are used for the new search.</span></span> <span data-ttu-id="03bb7-114">Un client ne doit pas transmettre null dans  _lpContainerList_ pour la première recherche dans un conteneur.</span><span class="sxs-lookup"><span data-stu-id="03bb7-114">A client should not pass NULL in  _lpContainerList_ for the first search in a container.</span></span> 
    
 <span data-ttu-id="03bb7-115">_ulSearchFlags_</span><span class="sxs-lookup"><span data-stu-id="03bb7-115">_ulSearchFlags_</span></span>
  
> <span data-ttu-id="03bb7-116">[in] Masque de bits d’indicateurs qui contrôlent la façon dont la recherche est effectuée.</span><span class="sxs-lookup"><span data-stu-id="03bb7-116">[in] A bitmask of flags that control how the search is performed.</span></span> <span data-ttu-id="03bb7-117">Les indicateurs suivants peuvent être définies :</span><span class="sxs-lookup"><span data-stu-id="03bb7-117">The following flags can be set:</span></span>
    
<span data-ttu-id="03bb7-118">BACKGROUND_SEARCH</span><span class="sxs-lookup"><span data-stu-id="03bb7-118">BACKGROUND_SEARCH</span></span> 
  
> <span data-ttu-id="03bb7-119">La recherche doit s’exécuter selon une priorité normale par rapport aux autres recherches.</span><span class="sxs-lookup"><span data-stu-id="03bb7-119">The search should run at normal priority relative to other searches.</span></span> <span data-ttu-id="03bb7-120">Cet indicateur ne peut pas être définie en même temps que l’FOREGROUND_SEARCH’indicateur.</span><span class="sxs-lookup"><span data-stu-id="03bb7-120">This flag cannot be set at the same time as the FOREGROUND_SEARCH flag.</span></span>
    
<span data-ttu-id="03bb7-121">FOREGROUND_SEARCH</span><span class="sxs-lookup"><span data-stu-id="03bb7-121">FOREGROUND_SEARCH</span></span> 
  
> <span data-ttu-id="03bb7-122">La recherche doit s’exécuter avec une priorité élevée par rapport aux autres recherches.</span><span class="sxs-lookup"><span data-stu-id="03bb7-122">The search should run at high priority relative to other searches.</span></span> <span data-ttu-id="03bb7-123">Cet indicateur ne peut pas être définie en même temps que l’BACKGROUND_SEARCH’indicateur.</span><span class="sxs-lookup"><span data-stu-id="03bb7-123">This flag cannot be set at the same time as the BACKGROUND_SEARCH flag.</span></span>
    
<span data-ttu-id="03bb7-124">NON_CONTENT_INDEXED_SEARCH</span><span class="sxs-lookup"><span data-stu-id="03bb7-124">NON_CONTENT_INDEXED_SEARCH</span></span>
  
> <span data-ttu-id="03bb7-125">La recherche ne doit pas utiliser l’indexation de contenu pour rechercher des entrées correspondantes.</span><span class="sxs-lookup"><span data-stu-id="03bb7-125">The search should not use content indexing to find matching entries.</span></span> <span data-ttu-id="03bb7-126">Cet indicateur n’est valide que pour Exchange magasins.</span><span class="sxs-lookup"><span data-stu-id="03bb7-126">This flag is only valid for Exchange stores.</span></span>
    
<span data-ttu-id="03bb7-127">RECURSIVE_SEARCH</span><span class="sxs-lookup"><span data-stu-id="03bb7-127">RECURSIVE_SEARCH</span></span> 
  
> <span data-ttu-id="03bb7-128">La recherche doit inclure les conteneurs spécifiés dans le  _paramètre lpContainerList_ et tous leurs conteneurs enfants.</span><span class="sxs-lookup"><span data-stu-id="03bb7-128">The search should include the containers specified in the  _lpContainerList_ parameter and all their child containers.</span></span> <span data-ttu-id="03bb7-129">Cet indicateur ne peut pas être définie en même temps que l’SHALLOW_SEARCH’indicateur.</span><span class="sxs-lookup"><span data-stu-id="03bb7-129">This flag cannot be set at the same time as the SHALLOW_SEARCH flag.</span></span> 
    
<span data-ttu-id="03bb7-130">RESTART_SEARCH</span><span class="sxs-lookup"><span data-stu-id="03bb7-130">RESTART_SEARCH</span></span> 
  
> <span data-ttu-id="03bb7-131">La recherche doit être lancée s’il s’agit du premier appel à **SetSearchCriteria,** ou redémarré si la recherche est inactive.</span><span class="sxs-lookup"><span data-stu-id="03bb7-131">The search should be initiated if this is the first call to **SetSearchCriteria**, or restarted if the search is inactive.</span></span> <span data-ttu-id="03bb7-132">Cet indicateur ne peut pas être définie en même temps que l’STOP_SEARCH’indicateur.</span><span class="sxs-lookup"><span data-stu-id="03bb7-132">This flag cannot be set at the same time as the STOP_SEARCH flag.</span></span>
    
<span data-ttu-id="03bb7-133">SHALLOW_SEARCH</span><span class="sxs-lookup"><span data-stu-id="03bb7-133">SHALLOW_SEARCH</span></span> 
  
> <span data-ttu-id="03bb7-134">La recherche doit uniquement rechercher des entrées correspondantes dans les conteneurs spécifiés dans le _paramètre lpContainerList._</span><span class="sxs-lookup"><span data-stu-id="03bb7-134">The search should look only in the containers specified in the  _lpContainerList_ parameter for matching entries.</span></span> <span data-ttu-id="03bb7-135">Cet indicateur ne peut pas être définie en même temps que l’RECURSIVE_SEARCH’indicateur.</span><span class="sxs-lookup"><span data-stu-id="03bb7-135">This flag cannot be set at the same time as the RECURSIVE_SEARCH flag.</span></span> 
    
<span data-ttu-id="03bb7-136">STOP_SEARCH</span><span class="sxs-lookup"><span data-stu-id="03bb7-136">STOP_SEARCH</span></span> 
  
> <span data-ttu-id="03bb7-137">La recherche doit être arrêtée.</span><span class="sxs-lookup"><span data-stu-id="03bb7-137">The search should be stopped.</span></span> <span data-ttu-id="03bb7-138">Cet indicateur ne peut pas être définie en même temps que l’RESTART_SEARCH’indicateur.</span><span class="sxs-lookup"><span data-stu-id="03bb7-138">This flag cannot be set at the same time as the RESTART_SEARCH flag.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="03bb7-139">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="03bb7-139">Return value</span></span>

<span data-ttu-id="03bb7-140">S_OK</span><span class="sxs-lookup"><span data-stu-id="03bb7-140">S_OK</span></span> 
  
> <span data-ttu-id="03bb7-141">Les critères de recherche ont été correctement définis.</span><span class="sxs-lookup"><span data-stu-id="03bb7-141">The search criteria was successfully set.</span></span>
    
<span data-ttu-id="03bb7-142">MAPI_E_TOO_COMPLEX</span><span class="sxs-lookup"><span data-stu-id="03bb7-142">MAPI_E_TOO_COMPLEX</span></span> 
  
> <span data-ttu-id="03bb7-143">Le fournisseur de services ne prend pas en charge les critères de recherche spécifiés.</span><span class="sxs-lookup"><span data-stu-id="03bb7-143">The service provider does not support the specified search criteria.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="03bb7-144">Remarques</span><span class="sxs-lookup"><span data-stu-id="03bb7-144">Remarks</span></span>

<span data-ttu-id="03bb7-145">La **méthode IMAPIContainer::SetSearchCriteria** établit des critères de recherche pour un conteneur qui prend en charge les recherches, généralement un dossier de résultats de recherche.</span><span class="sxs-lookup"><span data-stu-id="03bb7-145">The **IMAPIContainer::SetSearchCriteria** method establishes search criteria for a container that supports searches, typically a search-results folder.</span></span> <span data-ttu-id="03bb7-146">Un dossier de résultats de recherche contient des liens vers les messages qui répondent aux critères de recherche . les messages réels sont toujours stockés à leur emplacement d’origine.</span><span class="sxs-lookup"><span data-stu-id="03bb7-146">A search-results folder contains links to the messages that meet the search criteria; the actual messages are still stored in their original locations.</span></span> <span data-ttu-id="03bb7-147">Les seules données uniques contenues dans un dossier de résultats de recherche sont sa table des matières.</span><span class="sxs-lookup"><span data-stu-id="03bb7-147">The only unique data that is contained in a search-results folder is its contents table.</span></span> <span data-ttu-id="03bb7-148">La table des matières d’un dossier de résultats de recherche contient le contenu fusionné de la magasin de messages après l’application de la restriction de recherche.</span><span class="sxs-lookup"><span data-stu-id="03bb7-148">The contents table of a search-results folder has the merged contents of the message store after the search restriction has been applied.</span></span> 
  
<span data-ttu-id="03bb7-149">Une opération de recherche ne fonctionne que sur cette table des matières fusionnée ; il ne recherche pas dans d’autres dossiers de résultats de recherche.</span><span class="sxs-lookup"><span data-stu-id="03bb7-149">A search operation works only on this merged contents table; it does not search through other search-results folders.</span></span> <span data-ttu-id="03bb7-150">Les résultats de la recherche retournent uniquement les messages qui correspondent aux critères de recherche . la hiérarchie de dossiers n’est pas renvoyée.</span><span class="sxs-lookup"><span data-stu-id="03bb7-150">The search results return only the messages that match the search criteria; the folder hierarchy is not returned.</span></span>
  
<span data-ttu-id="03bb7-151">Le contrôle est renvoyé au client une fois la recherche terminée.</span><span class="sxs-lookup"><span data-stu-id="03bb7-151">Control is returned to the client when the search has finished.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="03bb7-152">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="03bb7-152">Notes to implementers</span></span>

<span data-ttu-id="03bb7-153">Les conteneurs de carnet d’adresses établissent des critères de recherche en appliquant des restrictions à leurs tables de contenu.</span><span class="sxs-lookup"><span data-stu-id="03bb7-153">Address book containers establish search criteria by applying restrictions to their contents tables.</span></span> <span data-ttu-id="03bb7-154">Pour plus d’informations sur les critères de recherche et les conteneurs de carnet d’adresses, voir [Implementing Advanced Searching](implementing-advanced-searching.md).</span><span class="sxs-lookup"><span data-stu-id="03bb7-154">For more information about search criteria and address book containers, see [Implementing Advanced Searching](implementing-advanced-searching.md).</span></span>
  
<span data-ttu-id="03bb7-155">Vous devez prendre en charge les opérations d’ouverture, de copie, de déplacement et de suppression sur les messages dans les dossiers de résultats de recherche, et non sur le dossier de résultats de recherche lui-même.</span><span class="sxs-lookup"><span data-stu-id="03bb7-155">You should support open, copy, move, and delete operations on the messages within search-results folders, not on the search-results folder itself.</span></span> <span data-ttu-id="03bb7-156">N’autorisez pas la création ou la copie de messages dans un dossier de résultats de recherche.</span><span class="sxs-lookup"><span data-stu-id="03bb7-156">Do not allow messages to be created within or copied into a search-results folder.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="03bb7-157">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="03bb7-157">Notes to callers</span></span>

<span data-ttu-id="03bb7-158">Pour rechercher des destinataires de message, définissez  _lpRestriction_ de façon à pointer vers une restriction de sous-objet avec le membre **ulSubObject** dans la structure [SSubRestriction](ssubrestriction.md) définie sur **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="03bb7-158">To search for message recipients, set  _lpRestriction_ to point to a subobject restriction with the **ulSubObject** member in the [SSubRestriction](ssubrestriction.md) structure set to **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)).</span></span> <span data-ttu-id="03bb7-159">Pour rechercher des pièces jointes, définissez le membre **ulSubObject** sur **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="03bb7-159">To search for attachments, set the **ulSubObject** member to **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)).</span></span> <span data-ttu-id="03bb7-160">Définissez **le membre lpRes** pour qu’il pointe vers une restriction de propriété qui décrit les critères de recherche pour les destinataires ou les pièces jointes.</span><span class="sxs-lookup"><span data-stu-id="03bb7-160">Set the **lpRes** member to point to a property restriction that describes the search criteria for the recipients or attachments.</span></span> 
  
<span data-ttu-id="03bb7-161">Par exemple, pour rechercher des pièces jointes dont l’extension est .mss, définissez **ulSubObject** sur **PR_MESSAGE_ATTACHMENTS** et **lpRes** sur une restriction de propriété qui correspond à **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) avec .mss.</span><span class="sxs-lookup"><span data-stu-id="03bb7-161">For example, to look for file attachments that have the extension .mss, set **ulSubObject** to **PR_MESSAGE_ATTACHMENTS** and **lpRes** to a property restriction that matches **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) with .mss.</span></span>
  
<span data-ttu-id="03bb7-162">La définition FOREGROUND_SEARCH’indicateur dans le  _paramètre ulSearchFlags_ peut entraîner une diminution des performances du système.</span><span class="sxs-lookup"><span data-stu-id="03bb7-162">Setting the FOREGROUND_SEARCH flag in the  _ulSearchFlags_ parameter could cause a decrease in system performance.</span></span> 
  
<span data-ttu-id="03bb7-163">Vous pouvez utiliser **SetSearchCriteria** pour modifier les critères de recherche d’une recherche déjà en cours.</span><span class="sxs-lookup"><span data-stu-id="03bb7-163">You can use **SetSearchCriteria** to change the search criteria of a search already in progress.</span></span> <span data-ttu-id="03bb7-164">Vous pouvez spécifier de nouvelles restrictions, de nouvelles listes de dossiers à rechercher et une nouvelle priorité de recherche, telle que la mise à niveau d’une recherche vers une priorité plus élevée.</span><span class="sxs-lookup"><span data-stu-id="03bb7-164">You can specify new restrictions, new lists of folders to search, and a new search priority, such as upgrading a search to a higher priority.</span></span> <span data-ttu-id="03bb7-165">Les modifications apportées à la priorité de recherche n’entraînent pas le redémarrage d’une recherche existante, mais d’autres modifications apportées aux critères de recherche le peuvent.</span><span class="sxs-lookup"><span data-stu-id="03bb7-165">Changes in search priority do not cause an existing search to restart, but other changes to search criteria can.</span></span> 
  
<span data-ttu-id="03bb7-166">Lorsque vous utilisez un dossier de résultats de recherche, vous pouvez supprimer le dossier ou le laisser ouvert pour une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="03bb7-166">When you are through using a search-results folder, you can either delete the folder or let it remain open for later use.</span></span> <span data-ttu-id="03bb7-167">Si vous supprimez le dossier de résultats de recherche, seuls les liens de message sont supprimés.</span><span class="sxs-lookup"><span data-stu-id="03bb7-167">If you do delete the search-results folder, only message links are deleted.</span></span> <span data-ttu-id="03bb7-168">Les messages réels restent dans leurs dossiers parents.</span><span class="sxs-lookup"><span data-stu-id="03bb7-168">The actual messages remain in their parent folders.</span></span> 
  
<span data-ttu-id="03bb7-169">Pour plus d’informations sur les dossiers de résultats de recherche, voir [Dossiers de recherche MAPI.](mapi-search-folders.md)</span><span class="sxs-lookup"><span data-stu-id="03bb7-169">For more information about search-results folders, see [MAPI Search Folders](mapi-search-folders.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="03bb7-170">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="03bb7-170">MFCMAPI reference</span></span>

<span data-ttu-id="03bb7-171">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="03bb7-171">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="03bb7-172">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="03bb7-172">**File**</span></span>|<span data-ttu-id="03bb7-173">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="03bb7-173">**Function**</span></span>|<span data-ttu-id="03bb7-174">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="03bb7-174">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="03bb7-175">HierarchyTableDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="03bb7-175">HierarchyTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="03bb7-176">CHierarchyTableDlg::OnEditSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="03bb7-176">CHierarchyTableDlg::OnEditSearchCriteria</span></span>  <br/> |<span data-ttu-id="03bb7-177">MFCMAPI utilise la méthode **IMAPIContainer::SetSearchCriteria** pour écrire des critères de recherche pour un dossier après qu’un utilisateur l’a modifié.</span><span class="sxs-lookup"><span data-stu-id="03bb7-177">MFCMAPI uses the **IMAPIContainer::SetSearchCriteria** method to write search criteria for a folder after a user has edited it.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="03bb7-178">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="03bb7-178">See also</span></span>



[<span data-ttu-id="03bb7-179">IMAPIContainer::GetContentsTable</span><span class="sxs-lookup"><span data-stu-id="03bb7-179">IMAPIContainer::GetContentsTable</span></span>](imapicontainer-getcontentstable.md)
  
[<span data-ttu-id="03bb7-180">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="03bb7-180">IMAPIContainer::OpenEntry</span></span>](imapicontainer-openentry.md)
  
[<span data-ttu-id="03bb7-181">IMAPIFolder::CreateFolder</span><span class="sxs-lookup"><span data-stu-id="03bb7-181">IMAPIFolder::CreateFolder</span></span>](imapifolder-createfolder.md)
  
[<span data-ttu-id="03bb7-182">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="03bb7-182">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
  
[<span data-ttu-id="03bb7-183">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="03bb7-183">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="03bb7-184">SRestriction</span><span class="sxs-lookup"><span data-stu-id="03bb7-184">SRestriction</span></span>](srestriction.md)
  
[<span data-ttu-id="03bb7-185">SSubRestriction</span><span class="sxs-lookup"><span data-stu-id="03bb7-185">SSubRestriction</span></span>](ssubrestriction.md)
  
[<span data-ttu-id="03bb7-186">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="03bb7-186">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


[<span data-ttu-id="03bb7-187">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="03bb7-187">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

