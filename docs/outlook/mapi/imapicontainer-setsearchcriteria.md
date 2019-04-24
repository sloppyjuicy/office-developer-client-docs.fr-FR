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
ms.openlocfilehash: a6168e8fced2fff3a7f9d273e47ed2410ac4c010
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350966"
---
# <a name="imapicontainersetsearchcriteria"></a><span data-ttu-id="41c86-103">IMAPIContainer::SetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="41c86-103">IMAPIContainer::SetSearchCriteria</span></span>

  
  
<span data-ttu-id="41c86-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="41c86-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="41c86-105">Établit les critères de recherche pour le conteneur.</span><span class="sxs-lookup"><span data-stu-id="41c86-105">Establishes search criteria for the container.</span></span>
  
```cpp
HRESULT SetSearchCriteria(
  LPSRestriction lpRestriction,
  LPENTRYLIST lpContainerList,
  ULONG ulSearchFlags
);
```

## <a name="parameters"></a><span data-ttu-id="41c86-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="41c86-106">Parameters</span></span>

 <span data-ttu-id="41c86-107">_lpRestriction_</span><span class="sxs-lookup"><span data-stu-id="41c86-107">_lpRestriction_</span></span>
  
> <span data-ttu-id="41c86-108">dans Pointeur vers une structure [SRestriction](srestriction.md) qui définit les critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="41c86-108">[in] A pointer to an [SRestriction](srestriction.md) structure that defines the search criteria.</span></span> <span data-ttu-id="41c86-109">Si la valeur NULL est transmise au paramètre _lpRestriction_ , les critères de recherche utilisés le plus récemment pour ce conteneur sont réutilisés.</span><span class="sxs-lookup"><span data-stu-id="41c86-109">If NULL is passed in the  _lpRestriction_ parameter, the search criteria that were used most recently for this container are used again.</span></span> <span data-ttu-id="41c86-110">NULL ne doit pas être passé dans _lpRestriction_ pour la première recherche dans un conteneur.</span><span class="sxs-lookup"><span data-stu-id="41c86-110">NULL should not be passed in  _lpRestriction_ for the first search in a container.</span></span> 
    
 <span data-ttu-id="41c86-111">_lpContainerList_</span><span class="sxs-lookup"><span data-stu-id="41c86-111">_lpContainerList_</span></span>
  
> <span data-ttu-id="41c86-112">dans Pointeur vers un tableau d'identificateurs d'entrée qui représentent des conteneurs à inclure dans la recherche.</span><span class="sxs-lookup"><span data-stu-id="41c86-112">[in] A pointer to an array of entry identifiers that represent containers to be included in the search.</span></span> <span data-ttu-id="41c86-113">Si un client transmet NULL dans le paramètre _lpContainerList_ , les identificateurs d'entrée utilisés le plus récemment pour rechercher ce conteneur sont utilisés pour la nouvelle recherche.</span><span class="sxs-lookup"><span data-stu-id="41c86-113">If a client passes NULL in the  _lpContainerList_ parameter, the entry identifiers used most recently to search this container are used for the new search.</span></span> <span data-ttu-id="41c86-114">Un client ne doit pas transmettre NULL dans _lpContainerList_ pour la première recherche dans un conteneur.</span><span class="sxs-lookup"><span data-stu-id="41c86-114">A client should not pass NULL in  _lpContainerList_ for the first search in a container.</span></span> 
    
 <span data-ttu-id="41c86-115">_ulSearchFlags_</span><span class="sxs-lookup"><span data-stu-id="41c86-115">_ulSearchFlags_</span></span>
  
> <span data-ttu-id="41c86-116">dans Masque de des indicateurs qui contrôlent le mode d'exécution de la recherche.</span><span class="sxs-lookup"><span data-stu-id="41c86-116">[in] A bitmask of flags that control how the search is performed.</span></span> <span data-ttu-id="41c86-117">Les indicateurs suivants peuvent être définis:</span><span class="sxs-lookup"><span data-stu-id="41c86-117">The following flags can be set:</span></span>
    
<span data-ttu-id="41c86-118">BACKGROUND_SEARCH</span><span class="sxs-lookup"><span data-stu-id="41c86-118">BACKGROUND_SEARCH</span></span> 
  
> <span data-ttu-id="41c86-119">La recherche doit être exécutée à une priorité normale par rapport à d'autres recherches.</span><span class="sxs-lookup"><span data-stu-id="41c86-119">The search should run at normal priority relative to other searches.</span></span> <span data-ttu-id="41c86-120">Cet indicateur ne peut pas être défini en même temps que l'indicateur FOREGROUND_SEARCH.</span><span class="sxs-lookup"><span data-stu-id="41c86-120">This flag cannot be set at the same time as the FOREGROUND_SEARCH flag.</span></span>
    
<span data-ttu-id="41c86-121">FOREGROUND_SEARCH</span><span class="sxs-lookup"><span data-stu-id="41c86-121">FOREGROUND_SEARCH</span></span> 
  
> <span data-ttu-id="41c86-122">La recherche doit s'exécuter à un niveau de priorité élevé par rapport à d'autres recherches.</span><span class="sxs-lookup"><span data-stu-id="41c86-122">The search should run at high priority relative to other searches.</span></span> <span data-ttu-id="41c86-123">Cet indicateur ne peut pas être défini en même temps que l'indicateur BACKGROUND_SEARCH.</span><span class="sxs-lookup"><span data-stu-id="41c86-123">This flag cannot be set at the same time as the BACKGROUND_SEARCH flag.</span></span>
    
<span data-ttu-id="41c86-124">NON_CONTENT_INDEXED_SEARCH</span><span class="sxs-lookup"><span data-stu-id="41c86-124">NON_CONTENT_INDEXED_SEARCH</span></span>
  
> <span data-ttu-id="41c86-125">La recherche ne doit pas utiliser l'indexation de contenu pour rechercher des entrées correspondantes.</span><span class="sxs-lookup"><span data-stu-id="41c86-125">The search should not use content indexing to find matching entries.</span></span> <span data-ttu-id="41c86-126">Cet indicateur est valide uniquement pour les banques Exchange.</span><span class="sxs-lookup"><span data-stu-id="41c86-126">This flag is only valid for Exchange stores.</span></span>
    
<span data-ttu-id="41c86-127">RECURSIVE_SEARCH</span><span class="sxs-lookup"><span data-stu-id="41c86-127">RECURSIVE_SEARCH</span></span> 
  
> <span data-ttu-id="41c86-128">La recherche doit inclure les conteneurs spécifiés dans le paramètre _lpContainerList_ et tous leurs conteneurs enfants.</span><span class="sxs-lookup"><span data-stu-id="41c86-128">The search should include the containers specified in the  _lpContainerList_ parameter and all their child containers.</span></span> <span data-ttu-id="41c86-129">Cet indicateur ne peut pas être défini en même temps que l'indicateur SHALLOW_SEARCH.</span><span class="sxs-lookup"><span data-stu-id="41c86-129">This flag cannot be set at the same time as the SHALLOW_SEARCH flag.</span></span> 
    
<span data-ttu-id="41c86-130">RESTART_SEARCH</span><span class="sxs-lookup"><span data-stu-id="41c86-130">RESTART_SEARCH</span></span> 
  
> <span data-ttu-id="41c86-131">La recherche doit être lancée s'il s'agit du premier appel à **SetSearchCriteria**ou si la recherche est inactive.</span><span class="sxs-lookup"><span data-stu-id="41c86-131">The search should be initiated if this is the first call to **SetSearchCriteria**, or restarted if the search is inactive.</span></span> <span data-ttu-id="41c86-132">Cet indicateur ne peut pas être défini en même temps que l'indicateur STOP_SEARCH.</span><span class="sxs-lookup"><span data-stu-id="41c86-132">This flag cannot be set at the same time as the STOP_SEARCH flag.</span></span>
    
<span data-ttu-id="41c86-133">SHALLOW_SEARCH</span><span class="sxs-lookup"><span data-stu-id="41c86-133">SHALLOW_SEARCH</span></span> 
  
> <span data-ttu-id="41c86-134">La recherche doit rechercher uniquement dans les conteneurs spécifiés dans le paramètre _lpContainerList_ pour les entrées correspondantes.</span><span class="sxs-lookup"><span data-stu-id="41c86-134">The search should look only in the containers specified in the  _lpContainerList_ parameter for matching entries.</span></span> <span data-ttu-id="41c86-135">Cet indicateur ne peut pas être défini en même temps que l'indicateur RECURSIVE_SEARCH.</span><span class="sxs-lookup"><span data-stu-id="41c86-135">This flag cannot be set at the same time as the RECURSIVE_SEARCH flag.</span></span> 
    
<span data-ttu-id="41c86-136">STOP_SEARCH</span><span class="sxs-lookup"><span data-stu-id="41c86-136">STOP_SEARCH</span></span> 
  
> <span data-ttu-id="41c86-137">La recherche doit être arrêtée.</span><span class="sxs-lookup"><span data-stu-id="41c86-137">The search should be stopped.</span></span> <span data-ttu-id="41c86-138">Cet indicateur ne peut pas être défini en même temps que l'indicateur RESTART_SEARCH.</span><span class="sxs-lookup"><span data-stu-id="41c86-138">This flag cannot be set at the same time as the RESTART_SEARCH flag.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="41c86-139">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="41c86-139">Return value</span></span>

<span data-ttu-id="41c86-140">S_OK</span><span class="sxs-lookup"><span data-stu-id="41c86-140">S_OK</span></span> 
  
> <span data-ttu-id="41c86-141">Les critères de recherche ont été correctement définis.</span><span class="sxs-lookup"><span data-stu-id="41c86-141">The search criteria was successfully set.</span></span>
    
<span data-ttu-id="41c86-142">MAPI_E_TOO_COMPLEX</span><span class="sxs-lookup"><span data-stu-id="41c86-142">MAPI_E_TOO_COMPLEX</span></span> 
  
> <span data-ttu-id="41c86-143">Le fournisseur de services ne prend pas en charge les critères de recherche spécifiés.</span><span class="sxs-lookup"><span data-stu-id="41c86-143">The service provider does not support the specified search criteria.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="41c86-144">Remarques</span><span class="sxs-lookup"><span data-stu-id="41c86-144">Remarks</span></span>

<span data-ttu-id="41c86-145">La méthode **IMAPIContainer:: SetSearchCriteria** établit les critères de recherche pour un conteneur qui prend en charge les recherches, généralement un dossier de résultats de recherche.</span><span class="sxs-lookup"><span data-stu-id="41c86-145">The **IMAPIContainer::SetSearchCriteria** method establishes search criteria for a container that supports searches, typically a search-results folder.</span></span> <span data-ttu-id="41c86-146">Un dossier de résultats de recherche contient des liens vers les messages qui répondent aux critères de recherche; les messages réels sont toujours stockés dans leurs emplacements d'origine.</span><span class="sxs-lookup"><span data-stu-id="41c86-146">A search-results folder contains links to the messages that meet the search criteria; the actual messages are still stored in their original locations.</span></span> <span data-ttu-id="41c86-147">Les seules données uniques contenues dans un dossier de résultats de recherche est sa table des matières.</span><span class="sxs-lookup"><span data-stu-id="41c86-147">The only unique data that is contained in a search-results folder is its contents table.</span></span> <span data-ttu-id="41c86-148">La table de contenu d'un dossier Search-Results a le contenu fusionné de la Banque de messages une fois que la restriction de recherche a été appliquée.</span><span class="sxs-lookup"><span data-stu-id="41c86-148">The contents table of a search-results folder has the merged contents of the message store after the search restriction has been applied.</span></span> 
  
<span data-ttu-id="41c86-149">Une opération de recherche ne fonctionne que sur cette table de contenu fusionné; il ne recherche pas dans d'autres dossiers de résultats de recherche.</span><span class="sxs-lookup"><span data-stu-id="41c86-149">A search operation works only on this merged contents table; it does not search through other search-results folders.</span></span> <span data-ttu-id="41c86-150">Les résultats de la recherche renvoient uniquement les messages qui correspondent aux critères de recherche; la hiérarchie de dossiers n'est pas renvoyée.</span><span class="sxs-lookup"><span data-stu-id="41c86-150">The search results return only the messages that match the search criteria; the folder hierarchy is not returned.</span></span>
  
<span data-ttu-id="41c86-151">Le contrôle est renvoyé au client lorsque la recherche est terminée.</span><span class="sxs-lookup"><span data-stu-id="41c86-151">Control is returned to the client when the search has finished.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="41c86-152">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="41c86-152">Notes to implementers</span></span>

<span data-ttu-id="41c86-153">Les conteneurs du carnet d'adresses établissent des critères de recherche en appliquant des restrictions à leurs tables de contenu.</span><span class="sxs-lookup"><span data-stu-id="41c86-153">Address book containers establish search criteria by applying restrictions to their contents tables.</span></span> <span data-ttu-id="41c86-154">Pour plus d'informations sur les critères de recherche et les conteneurs du carnet d'adresses, consultez la rubrique implémentation de la [recherche avancée](implementing-advanced-searching.md).</span><span class="sxs-lookup"><span data-stu-id="41c86-154">For more information about search criteria and address book containers, see [Implementing Advanced Searching](implementing-advanced-searching.md).</span></span>
  
<span data-ttu-id="41c86-155">Vous devez prendre en charge les opérations d'ouverture, de copie, de déplacement et de suppression des messages dans les dossiers de résultats de recherche, et non dans le dossier de résultats de recherche lui-même.</span><span class="sxs-lookup"><span data-stu-id="41c86-155">You should support open, copy, move, and delete operations on the messages within search-results folders, not on the search-results folder itself.</span></span> <span data-ttu-id="41c86-156">Ne pas autoriser la création ou la copie de messages dans un dossier de résultats de recherche.</span><span class="sxs-lookup"><span data-stu-id="41c86-156">Do not allow messages to be created within or copied into a search-results folder.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="41c86-157">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="41c86-157">Notes to callers</span></span>

<span data-ttu-id="41c86-158">Pour rechercher des destinataires de message, définissez _lpRestriction_ de sorte qu'il pointe vers une restriction de sous-objet avec le membre **ulSubObject** dans la structure [SSubRestriction](ssubrestriction.md) définie sur **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="41c86-158">To search for message recipients, set  _lpRestriction_ to point to a subobject restriction with the **ulSubObject** member in the [SSubRestriction](ssubrestriction.md) structure set to **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)).</span></span> <span data-ttu-id="41c86-159">Pour rechercher des pièces jointes, définissez le membre **ulSubObject** sur **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="41c86-159">To search for attachments, set the **ulSubObject** member to **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)).</span></span> <span data-ttu-id="41c86-160">Définissez le membre **lpRes** de sorte qu'il pointe vers une restriction de propriété qui décrit les critères de recherche pour les destinataires ou les pièces jointes.</span><span class="sxs-lookup"><span data-stu-id="41c86-160">Set the **lpRes** member to point to a property restriction that describes the search criteria for the recipients or attachments.</span></span> 
  
<span data-ttu-id="41c86-161">Par exemple, pour rechercher des pièces jointes portant l'extension. MSS, définissez **ulSubObject** sur **PR_MESSAGE_ATTACHMENTS** et **lpRes** sur une restriction de propriété qui correspond à **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md) ) avec. MSS.</span><span class="sxs-lookup"><span data-stu-id="41c86-161">For example, to look for file attachments that have the extension .mss, set **ulSubObject** to **PR_MESSAGE_ATTACHMENTS** and **lpRes** to a property restriction that matches **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) with .mss.</span></span>
  
<span data-ttu-id="41c86-162">La définition de l'indicateur FOREGROUND_SEARCH dans le paramètre _ulSearchFlags_ peut entraîner une diminution des performances du système.</span><span class="sxs-lookup"><span data-stu-id="41c86-162">Setting the FOREGROUND_SEARCH flag in the  _ulSearchFlags_ parameter could cause a decrease in system performance.</span></span> 
  
<span data-ttu-id="41c86-163">Vous pouvez utiliser **SetSearchCriteria** pour modifier les critères de recherche d'une recherche déjà en cours.</span><span class="sxs-lookup"><span data-stu-id="41c86-163">You can use **SetSearchCriteria** to change the search criteria of a search already in progress.</span></span> <span data-ttu-id="41c86-164">Vous pouvez spécifier de nouvelles restrictions, de nouvelles listes de dossiers à rechercher et une nouvelle priorité de recherche, telle que la mise à niveau d'une recherche vers une priorité plus élevée.</span><span class="sxs-lookup"><span data-stu-id="41c86-164">You can specify new restrictions, new lists of folders to search, and a new search priority, such as upgrading a search to a higher priority.</span></span> <span data-ttu-id="41c86-165">Les modifications apPortées à la priorité de recherche ne provoquent pas le redémarrage d'une recherche existante, mais d'autres modifications des critères de recherche peuvent.</span><span class="sxs-lookup"><span data-stu-id="41c86-165">Changes in search priority do not cause an existing search to restart, but other changes to search criteria can.</span></span> 
  
<span data-ttu-id="41c86-166">Lorsque vous utilisez un dossier Search-Results, vous pouvez supprimer le dossier ou le laisser ouvert en vue d'une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="41c86-166">When you are through using a search-results folder, you can either delete the folder or let it remain open for later use.</span></span> <span data-ttu-id="41c86-167">Si vous supprimez le dossier Search-Results, seuls les liens de message sont supprimés.</span><span class="sxs-lookup"><span data-stu-id="41c86-167">If you do delete the search-results folder, only message links are deleted.</span></span> <span data-ttu-id="41c86-168">Les messages réels restent dans leurs dossiers parents.</span><span class="sxs-lookup"><span data-stu-id="41c86-168">The actual messages remain in their parent folders.</span></span> 
  
<span data-ttu-id="41c86-169">Pour plus d'informations sur les dossiers de résultats de recherche, consultez la rubrique [MAPI Search Folders](mapi-search-folders.md).</span><span class="sxs-lookup"><span data-stu-id="41c86-169">For more information about search-results folders, see [MAPI Search Folders](mapi-search-folders.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="41c86-170">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="41c86-170">MFCMAPI reference</span></span>

<span data-ttu-id="41c86-171">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="41c86-171">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="41c86-172">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="41c86-172">**File**</span></span>|<span data-ttu-id="41c86-173">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="41c86-173">**Function**</span></span>|<span data-ttu-id="41c86-174">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="41c86-174">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="41c86-175">HierarchyTableDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="41c86-175">HierarchyTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="41c86-176">CHierarchyTableDlg:: OnEditSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="41c86-176">CHierarchyTableDlg::OnEditSearchCriteria</span></span>  <br/> |<span data-ttu-id="41c86-177">MFCMAPI utilise la méthode **IMAPIContainer:: SetSearchCriteria** pour écrire des critères de recherche pour un dossier après qu'un utilisateur l'a modifié.</span><span class="sxs-lookup"><span data-stu-id="41c86-177">MFCMAPI uses the **IMAPIContainer::SetSearchCriteria** method to write search criteria for a folder after a user has edited it.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="41c86-178">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="41c86-178">See also</span></span>



[<span data-ttu-id="41c86-179">IMAPIContainer::GetContentsTable</span><span class="sxs-lookup"><span data-stu-id="41c86-179">IMAPIContainer::GetContentsTable</span></span>](imapicontainer-getcontentstable.md)
  
[<span data-ttu-id="41c86-180">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="41c86-180">IMAPIContainer::OpenEntry</span></span>](imapicontainer-openentry.md)
  
[<span data-ttu-id="41c86-181">IMAPIFolder::CreateFolder</span><span class="sxs-lookup"><span data-stu-id="41c86-181">IMAPIFolder::CreateFolder</span></span>](imapifolder-createfolder.md)
  
[<span data-ttu-id="41c86-182">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="41c86-182">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
  
[<span data-ttu-id="41c86-183">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="41c86-183">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="41c86-184">SRestriction</span><span class="sxs-lookup"><span data-stu-id="41c86-184">SRestriction</span></span>](srestriction.md)
  
[<span data-ttu-id="41c86-185">SSubRestriction</span><span class="sxs-lookup"><span data-stu-id="41c86-185">SSubRestriction</span></span>](ssubrestriction.md)
  
[<span data-ttu-id="41c86-186">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="41c86-186">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


[<span data-ttu-id="41c86-187">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="41c86-187">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

