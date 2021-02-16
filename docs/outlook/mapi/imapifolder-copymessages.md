---
title: IMAPIFolderCopyMessages
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.CopyMessages
api_type:
- COM
ms.assetid: 4c7d2110-3fcb-4b9f-bf20-1dc1a611161d
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 21aa28e1a2c11ee7361fb4921f8d527b3e3ceb44
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424454"
---
# <a name="imapifoldercopymessages"></a><span data-ttu-id="a8127-103">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="a8127-103">IMAPIFolder::CopyMessages</span></span>

  
  
<span data-ttu-id="a8127-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a8127-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a8127-105">Copie ou déplace un ou plusieurs messages.</span><span class="sxs-lookup"><span data-stu-id="a8127-105">Copies or moves one or more messages.</span></span>
  
```cpp
HRESULT CopyMessages(
  LPENTRYLIST lpMsgList,
  LPCIID lpInterface,
  LPVOID lpDestFolder,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="a8127-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a8127-106">Parameters</span></span>

 <span data-ttu-id="a8127-107">_lpMsgList_</span><span class="sxs-lookup"><span data-stu-id="a8127-107">_lpMsgList_</span></span>
  
> <span data-ttu-id="a8127-108">[in] Pointeur vers un tableau de structures [ENTRYLIST](entrylist.md) qui identifient le ou les messages à copier ou déplacer.</span><span class="sxs-lookup"><span data-stu-id="a8127-108">[in] A pointer to an array of [ENTRYLIST](entrylist.md) structures that identify the message or messages to copy or move.</span></span> 
    
 <span data-ttu-id="a8127-109">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="a8127-109">_lpInterface_</span></span>
  
> <span data-ttu-id="a8127-110">[in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder au dossier de destination pointé par le paramètre _lpDestFolder._</span><span class="sxs-lookup"><span data-stu-id="a8127-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the destination folder pointed to by the  _lpDestFolder_ parameter.</span></span> <span data-ttu-id="a8127-111">En passant NULL, le fournisseur de services retourne l’interface de dossier [standard, IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="a8127-111">Passing NULL results in the service provider returning the standard folder interface, [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="a8127-112">Les clients doivent passer la valeur NULL.</span><span class="sxs-lookup"><span data-stu-id="a8127-112">Clients must pass NULL.</span></span> <span data-ttu-id="a8127-113">D’autres appelants peuvent définir le paramètre  _lpInterface_ sur IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer ou IID_IMAPIFolder.</span><span class="sxs-lookup"><span data-stu-id="a8127-113">Other callers can set the  _lpInterface_ parameter to IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer, or IID_IMAPIFolder.</span></span> 
    
 <span data-ttu-id="a8127-114">_lpDestFolder_</span><span class="sxs-lookup"><span data-stu-id="a8127-114">_lpDestFolder_</span></span>
  
> <span data-ttu-id="a8127-115">[in] Pointeur vers le dossier ouvert pour recevoir les messages copiés ou déplacés.</span><span class="sxs-lookup"><span data-stu-id="a8127-115">[in] A pointer to the open folder to receive the copied or moved messages.</span></span>
    
 <span data-ttu-id="a8127-116">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="a8127-116">_ulUIParam_</span></span>
  
> <span data-ttu-id="a8127-117">[in] Poignée vers la fenêtre parente de toutes les boîtes de dialogue ou fenêtres affichées par cette méthode.</span><span class="sxs-lookup"><span data-stu-id="a8127-117">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span> <span data-ttu-id="a8127-118">Le _paramètre ulUIParam_ est ignoré, sauf si le client définit l’indicateur MESSAGE_DIALOG dans le paramètre _ulFlags_ et transmet null dans le paramètre _lpProgress._</span><span class="sxs-lookup"><span data-stu-id="a8127-118">The  _ulUIParam_ parameter is ignored unless the client sets the MESSAGE_DIALOG flag in the  _ulFlags_ parameter and passes NULL in the  _lpProgress_ parameter.</span></span> 
    
 <span data-ttu-id="a8127-119">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="a8127-119">_lpProgress_</span></span>
  
> <span data-ttu-id="a8127-120">[in] Pointeur vers un objet de progression qui affiche un indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="a8127-120">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="a8127-121">Si NULL est transmis dans  _lpProgress,_ le fournisseur de magasin de messages affiche un indicateur de progression à l’aide de l’implémentation de l’objet de progression MAPI.</span><span class="sxs-lookup"><span data-stu-id="a8127-121">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="a8127-122">Le  _paramètre lpProgress est_ ignoré, sauf si l’MESSAGE_DIALOG est définie dans  _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="a8127-122">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="a8127-123">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a8127-123">_ulFlags_</span></span>
  
> <span data-ttu-id="a8127-124">[in] Masque de bits d’indicateurs qui contrôle la façon dont l’opération de copie ou de déplacement est accomplie.</span><span class="sxs-lookup"><span data-stu-id="a8127-124">[in] A bitmask of flags that controls how the copy or move operation is accomplished.</span></span> <span data-ttu-id="a8127-125">Les indicateurs suivants peuvent être définies :</span><span class="sxs-lookup"><span data-stu-id="a8127-125">The following flags can be set:</span></span>
    
<span data-ttu-id="a8127-126">MAPI_DECLINE_OK</span><span class="sxs-lookup"><span data-stu-id="a8127-126">MAPI_DECLINE_OK</span></span> 
  
> <span data-ttu-id="a8127-127">Informe le fournisseur de magasin de messages de renvoyer immédiatement MAPI_E_DECLINE_COPY s’il implémente **IMAPIFolder::CopyMessages** en appelant la méthode [IMAPISupport::D oCopyTo](imapisupport-docopyto.md) ou [IMAPISupport::D oCopyProps](imapisupport-docopyprops.md) de l’objet de support.</span><span class="sxs-lookup"><span data-stu-id="a8127-127">Informs the message store provider to immediately return MAPI_E_DECLINE_COPY if it implements **IMAPIFolder::CopyMessages** by calling the support object's [IMAPISupport::DoCopyTo](imapisupport-docopyto.md) or [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md) method.</span></span> 
    
<span data-ttu-id="a8127-128">MESSAGE_DIALOG</span><span class="sxs-lookup"><span data-stu-id="a8127-128">MESSAGE_DIALOG</span></span> 
  
> <span data-ttu-id="a8127-129">Affiche un indicateur de progression au cours de l’opération.</span><span class="sxs-lookup"><span data-stu-id="a8127-129">Displays a progress indicator as the operation proceeds.</span></span>
    
<span data-ttu-id="a8127-130">MESSAGE_MOVE</span><span class="sxs-lookup"><span data-stu-id="a8127-130">MESSAGE_MOVE</span></span> 
  
> <span data-ttu-id="a8127-131">Le ou les messages doivent être déplacés au lieu d’être copiés.</span><span class="sxs-lookup"><span data-stu-id="a8127-131">The message or messages are to be moved instead of copied.</span></span> <span data-ttu-id="a8127-132">Si MESSAGE_MOVE n’est pas définie, les messages sont copiés.</span><span class="sxs-lookup"><span data-stu-id="a8127-132">If MESSAGE_MOVE is not set, the messages are copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a8127-133">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a8127-133">Return value</span></span>

<span data-ttu-id="a8127-134">S_OK</span><span class="sxs-lookup"><span data-stu-id="a8127-134">S_OK</span></span> 
  
> <span data-ttu-id="a8127-135">Le ou les messages ont été correctement copiés ou déplacés.</span><span class="sxs-lookup"><span data-stu-id="a8127-135">The message or messages have been successfully copied or moved.</span></span>
    
<span data-ttu-id="a8127-136">MAPI_E_DECLINE_COPY</span><span class="sxs-lookup"><span data-stu-id="a8127-136">MAPI_E_DECLINE_COPY</span></span> 
  
> <span data-ttu-id="a8127-137">Le fournisseur implémente cette méthode en appelant une méthode objet de support, et l’appelant a passé l’MAPI_DECLINE_OK’indicateur.</span><span class="sxs-lookup"><span data-stu-id="a8127-137">The provider implements this method by calling a support object method, and the caller has passed the MAPI_DECLINE_OK flag.</span></span>
    
<span data-ttu-id="a8127-138">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="a8127-138">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="a8127-139">L’appel a réussi, mais toutes les entrées n’ont pas été correctement copiées ou déplacées.</span><span class="sxs-lookup"><span data-stu-id="a8127-139">The call succeeded, but not all entries were successfully copied or moved.</span></span> <span data-ttu-id="a8127-140">Lorsque cet avertissement est renvoyé, l’appel doit être traité comme réussi.</span><span class="sxs-lookup"><span data-stu-id="a8127-140">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="a8127-141">Pour tester cet avertissement, utilisez la macro **HR_FAILED.**</span><span class="sxs-lookup"><span data-stu-id="a8127-141">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="a8127-142">Pour plus d’informations, voir [Utilisation de macros pour la gestion des erreurs.](using-macros-for-error-handling.md)</span><span class="sxs-lookup"><span data-stu-id="a8127-142">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a8127-143">Remarques</span><span class="sxs-lookup"><span data-stu-id="a8127-143">Remarks</span></span>

<span data-ttu-id="a8127-144">La **méthode IMAPIFolder::CopyMessages** copie ou déplace les messages vers un autre dossier.</span><span class="sxs-lookup"><span data-stu-id="a8127-144">The **IMAPIFolder::CopyMessages** method copies or moves messages to another folder.</span></span> 
  
<span data-ttu-id="a8127-145">Les messages ouverts avec une autorisation de lecture/écriture peuvent être déplacés ou copiés.</span><span class="sxs-lookup"><span data-stu-id="a8127-145">Messages that are opened with read/write permission can be moved or copied.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="a8127-146">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="a8127-146">Notes to implementers</span></span>

<span data-ttu-id="a8127-147">Si vous copiez des messages dans une autre magasin de messages sans utiliser la méthode [IMAPISupport::CopyMessages,](imapisupport-copymessages.md) vous devez d’abord appeler [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) avec l’indicateur GENERATE_RECEIPT_ONLY définie.</span><span class="sxs-lookup"><span data-stu-id="a8127-147">If you are copying messages to another message store without using the [IMAPISupport::CopyMessages](imapisupport-copymessages.md) method, you must first call [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) with the GENERATE_RECEIPT_ONLY flag set.</span></span> <span data-ttu-id="a8127-148">La boutique de messages de réception n’est pas chargée de générer des rapports de lecture pour les messages copiés ou déplacés.</span><span class="sxs-lookup"><span data-stu-id="a8127-148">The receiving message store is not responsible for generating read reports for the copied or moved messages.</span></span> <span data-ttu-id="a8127-149">Si vous appelez **IMAPISupport::CopyMessages** pour implémenter **IMAPIFolder::CopyMessages**, n’appelez **pas SetReadFlags**; MAPI l’appelle.</span><span class="sxs-lookup"><span data-stu-id="a8127-149">If you are calling **IMAPISupport::CopyMessages** to implement **IMAPIFolder::CopyMessages**, do not call **SetReadFlags**; MAPI will call it.</span></span> 
  
<span data-ttu-id="a8127-150">Votre implémentation peut déplacer ou copier les messages dans n’importe quel ordre et générer des rapports d’état de lecture dans n’importe quel ordre.</span><span class="sxs-lookup"><span data-stu-id="a8127-150">Your implementation can move or copy the messages in any order and generate read status reports in any order.</span></span> <span data-ttu-id="a8127-151">Autrement dit, vous pouvez terminer la copie des messages avant de générer les rapports d’état de lecture ou envoyer les rapports avant que votre implémentation ne démarre l’opération de copie.</span><span class="sxs-lookup"><span data-stu-id="a8127-151">That is, you can finish copying messages before generating any of the read status reports or send the reports before your implementation starts the copy operation.</span></span> <span data-ttu-id="a8127-152">Toutefois, les rapports de lecture doivent être envoyés pour que tous les messages soient copiés, que la copie réussisse ou non.</span><span class="sxs-lookup"><span data-stu-id="a8127-152">However, read reports should be sent for all messages to be copied, regardless of whether the copy is successful.</span></span>
  
<span data-ttu-id="a8127-153">Lorsque l’opération de copie ou de déplacement implique plusieurs messages, effectuez l’opération aussi complètement que possible.</span><span class="sxs-lookup"><span data-stu-id="a8127-153">When the copy or move operation involves more than one message, perform the operation as completely as possible.</span></span> <span data-ttu-id="a8127-154">N’arrêtez pas l’opération prématurément, sauf si une défaillance dépasse votre contrôle, par exemple un manque de mémoire, un manque d’espace disque ou une altération de la magasin de messages.</span><span class="sxs-lookup"><span data-stu-id="a8127-154">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span>
  
<span data-ttu-id="a8127-155">Essayez de conserver les identificateurs d’entrée entre les opérations de déplacement ou de copie.</span><span class="sxs-lookup"><span data-stu-id="a8127-155">Try to maintain entry identifiers across move or copy operations.</span></span> <span data-ttu-id="a8127-156">Vous devez également conserver les identificateurs d’entrée, bien que cela ne soit pas obligatoire.</span><span class="sxs-lookup"><span data-stu-id="a8127-156">You should also preserve entry identifiers, although it is not required.</span></span>
  
<span data-ttu-id="a8127-157">Envoyez des notifications lorsque vous déplacez ou copiez des messages afin que les clients soient avertis que leurs appels aux méthodes [IMAPIProp::SaveChanges](imapiprop-savechanges.md) des messages risquent d’échouer.</span><span class="sxs-lookup"><span data-stu-id="a8127-157">Send notifications when you move or copy messages so that clients are forewarned that their calls to the messages' [IMAPIProp::SaveChanges](imapiprop-savechanges.md) methods may fail.</span></span> 
  
<span data-ttu-id="a8127-158">N’incluez pas l’état d’un message dans l’opération de copie ou de déplacement.</span><span class="sxs-lookup"><span data-stu-id="a8127-158">Do not include a message's status in the copy or move operation.</span></span> <span data-ttu-id="a8127-159">Le déplacement ou la copie de l’état d’un message affecte grandement les performances.</span><span class="sxs-lookup"><span data-stu-id="a8127-159">Moving or copying a message status greatly affects performance.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="a8127-160">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="a8127-160">Notes to callers</span></span>

<span data-ttu-id="a8127-161">Utilisez **IMAPIFolder::CopyMessages** pour remplir les dossiers de résultats de recherche, où les messages sont souvent regroupés par dossier parent.</span><span class="sxs-lookup"><span data-stu-id="a8127-161">Use **IMAPIFolder::CopyMessages** to populate search-results folders, where messages are often grouped by parent folder.</span></span> 
  
<span data-ttu-id="a8127-162">Attendez-vous à ce que ces valeurs de retour se placent dans les conditions suivantes.</span><span class="sxs-lookup"><span data-stu-id="a8127-162">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="a8127-163">**Condition**</span><span class="sxs-lookup"><span data-stu-id="a8127-163">**Condition**</span></span>|<span data-ttu-id="a8127-164">**Valeur renvoy�e**</span><span class="sxs-lookup"><span data-stu-id="a8127-164">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a8127-165">**IMAPIFolder::CopyMessages** a correctement copié ou déplacé chaque message.</span><span class="sxs-lookup"><span data-stu-id="a8127-165">**IMAPIFolder::CopyMessages** has successfully copied or moved every message.</span></span>  <br/> |<span data-ttu-id="a8127-166">S_OK</span><span class="sxs-lookup"><span data-stu-id="a8127-166">S_OK</span></span>  <br/> |
|<span data-ttu-id="a8127-167">**IMAPIFolder::CopyMessages** n’a pas pu copier ou déplacer tous les messages.</span><span class="sxs-lookup"><span data-stu-id="a8127-167">**IMAPIFolder::CopyMessages** was unable to successfully copy or move every message.</span></span>  <br/> |<span data-ttu-id="a8127-168">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="a8127-168">MAPI_W_PARTIAL_COMPLETION</span></span>  <br/> |
|<span data-ttu-id="a8127-169">**IMAPIFolder::CopyMessages** n’a pas pu se terminer.</span><span class="sxs-lookup"><span data-stu-id="a8127-169">**IMAPIFolder::CopyMessages** was unable to complete.</span></span>  <br/> |<span data-ttu-id="a8127-170">Toute valeur d’erreur</span><span class="sxs-lookup"><span data-stu-id="a8127-170">Any error value</span></span>  <br/> |
   
<span data-ttu-id="a8127-171">Lorsque **IMAPIFolder::CopyMessages** ne peut pas se terminer, ne supposez pas qu’aucun travail n’a été effectué.</span><span class="sxs-lookup"><span data-stu-id="a8127-171">When **IMAPIFolder::CopyMessages** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="a8127-172">**IMAPIFolder::CopyMessages** a peut-être pu copier ou déplacer un ou plusieurs messages avant de rencontrer l’erreur.</span><span class="sxs-lookup"><span data-stu-id="a8127-172">**IMAPIFolder::CopyMessages** might have been able to copy or move one or more messages before encountering the error.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a8127-173">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a8127-173">See also</span></span>



[<span data-ttu-id="a8127-174">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="a8127-174">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)

