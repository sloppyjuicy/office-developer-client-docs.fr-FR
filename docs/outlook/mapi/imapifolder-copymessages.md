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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: e6e9e9cefc75ffc78ee7beb47e89063ea1a66ce7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783722"
---
# <a name="imapifoldercopymessages"></a><span data-ttu-id="e6c20-103">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="e6c20-103">IMAPIFolder::CopyMessages</span></span>

  
  
<span data-ttu-id="e6c20-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e6c20-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e6c20-105">Copie ou déplace un ou plusieurs messages.</span><span class="sxs-lookup"><span data-stu-id="e6c20-105">Copies or moves one or more messages.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="e6c20-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e6c20-106">Parameters</span></span>

 <span data-ttu-id="e6c20-107">_lpMsgList_</span><span class="sxs-lookup"><span data-stu-id="e6c20-107">_lpMsgList_</span></span>
  
> <span data-ttu-id="e6c20-108">[in] Pointeur vers un tableau de structures [ENTRYLIST](entrylist.md) qui identifient l’ou les messages pour copier ou déplacer.</span><span class="sxs-lookup"><span data-stu-id="e6c20-108">[in] A pointer to an array of [ENTRYLIST](entrylist.md) structures that identify the message or messages to copy or move.</span></span> 
    
 <span data-ttu-id="e6c20-109">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="e6c20-109">_lpInterface_</span></span>
  
> <span data-ttu-id="e6c20-110">[in] Un pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder au dossier de destination indiqué par le paramètre _lpDestFolder_ .</span><span class="sxs-lookup"><span data-stu-id="e6c20-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the destination folder pointed to by the  _lpDestFolder_ parameter.</span></span> <span data-ttu-id="e6c20-111">Passant NULL entraîne le renvoi de l’interface de dossier standard, du fournisseur de services [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="e6c20-111">Passing NULL results in the service provider returning the standard folder interface, [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="e6c20-112">Les clients doivent passer la valeur NULL.</span><span class="sxs-lookup"><span data-stu-id="e6c20-112">Clients must pass NULL.</span></span> <span data-ttu-id="e6c20-113">Autres appelants peuvent de définir le paramètre _lpInterface_ IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer ou IID_IMAPIFolder.</span><span class="sxs-lookup"><span data-stu-id="e6c20-113">Other callers can set the  _lpInterface_ parameter to IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer, or IID_IMAPIFolder.</span></span> 
    
 <span data-ttu-id="e6c20-114">_lpDestFolder_</span><span class="sxs-lookup"><span data-stu-id="e6c20-114">_lpDestFolder_</span></span>
  
> <span data-ttu-id="e6c20-115">[in] Pointeur vers le dossier ouvert pour recevoir les messages copiés ou déplacées.</span><span class="sxs-lookup"><span data-stu-id="e6c20-115">[in] A pointer to the open folder to receive the copied or moved messages.</span></span>
    
 <span data-ttu-id="e6c20-116">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="e6c20-116">_ulUIParam_</span></span>
  
> <span data-ttu-id="e6c20-117">[in] Un handle vers la fenêtre parent des boîtes de dialogue ni windows cette méthode affiche.</span><span class="sxs-lookup"><span data-stu-id="e6c20-117">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span> <span data-ttu-id="e6c20-118">Le paramètre _ulUIParam_ est ignoré à moins que le client définit l’indicateur MESSAGE_DIALOG dans le paramètre _ulFlags_ et transmet la valeur NULL dans le paramètre _lpProgress_ .</span><span class="sxs-lookup"><span data-stu-id="e6c20-118">The  _ulUIParam_ parameter is ignored unless the client sets the MESSAGE_DIALOG flag in the  _ulFlags_ parameter and passes NULL in the  _lpProgress_ parameter.</span></span> 
    
 <span data-ttu-id="e6c20-119">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="e6c20-119">_lpProgress_</span></span>
  
> <span data-ttu-id="e6c20-120">[in] Pointeur vers un objet de progression qui affiche un indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="e6c20-120">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="e6c20-121">Si NULL est indiqué dans _lpProgress_, le fournisseur de banque de message affiche un indicateur de progression à l’aide de l’implémentation d’objet de progression MAPI.</span><span class="sxs-lookup"><span data-stu-id="e6c20-121">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="e6c20-122">Le paramètre _lpProgress_ est ignoré à moins que l’indicateur MESSAGE_DIALOG est défini dans _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="e6c20-122">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="e6c20-123">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e6c20-123">_ulFlags_</span></span>
  
> <span data-ttu-id="e6c20-124">[in] Masque de bits d’indicateurs qui contrôle la manière dont l’opération de copie ou de déplacement est effectuée.</span><span class="sxs-lookup"><span data-stu-id="e6c20-124">[in] A bitmask of flags that controls how the copy or move operation is accomplished.</span></span> <span data-ttu-id="e6c20-125">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="e6c20-125">The following flags can be set:</span></span>
    
<span data-ttu-id="e6c20-126">MAPI_DECLINE_OK</span><span class="sxs-lookup"><span data-stu-id="e6c20-126">MAPI_DECLINE_OK</span></span> 
  
> <span data-ttu-id="e6c20-127">Informe le fournisseur de banque de messages pour retourner immédiatement MAPI_E_DECLINE_COPY si elle implémente **IMAPIFolder::CopyMessages** en appelant la méthode [IMAPISupport::DoCopyTo](imapisupport-docopyto.md) ou [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md) de l’objet de la prise en charge.</span><span class="sxs-lookup"><span data-stu-id="e6c20-127">Informs the message store provider to immediately return MAPI_E_DECLINE_COPY if it implements **IMAPIFolder::CopyMessages** by calling the support object's [IMAPISupport::DoCopyTo](imapisupport-docopyto.md) or [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md) method.</span></span> 
    
<span data-ttu-id="e6c20-128">MESSAGE_DIALOG</span><span class="sxs-lookup"><span data-stu-id="e6c20-128">MESSAGE_DIALOG</span></span> 
  
> <span data-ttu-id="e6c20-129">Affiche un indicateur de progression de l’opération.</span><span class="sxs-lookup"><span data-stu-id="e6c20-129">Displays a progress indicator as the operation proceeds.</span></span>
    
<span data-ttu-id="e6c20-130">MESSAGE_MOVE</span><span class="sxs-lookup"><span data-stu-id="e6c20-130">MESSAGE_MOVE</span></span> 
  
> <span data-ttu-id="e6c20-131">L’ou les messages doivent être déplacés et non copiés.</span><span class="sxs-lookup"><span data-stu-id="e6c20-131">The message or messages are to be moved instead of copied.</span></span> <span data-ttu-id="e6c20-132">Si MESSAGE_MOVE n’est pas définie, les messages sont copiés.</span><span class="sxs-lookup"><span data-stu-id="e6c20-132">If MESSAGE_MOVE is not set, the messages are copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e6c20-133">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="e6c20-133">Return value</span></span>

<span data-ttu-id="e6c20-134">S_OK</span><span class="sxs-lookup"><span data-stu-id="e6c20-134">S_OK</span></span> 
  
> <span data-ttu-id="e6c20-135">L’ou les messages ont été correctement copiés ou déplacés.</span><span class="sxs-lookup"><span data-stu-id="e6c20-135">The message or messages have been successfully copied or moved.</span></span>
    
<span data-ttu-id="e6c20-136">MAPI_E_DECLINE_COPY</span><span class="sxs-lookup"><span data-stu-id="e6c20-136">MAPI_E_DECLINE_COPY</span></span> 
  
> <span data-ttu-id="e6c20-137">Le fournisseur implémente cette méthode en appelant une méthode de prise en charge de l’objet et l’appelant a passé l’indicateur MAPI_DECLINE_OK.</span><span class="sxs-lookup"><span data-stu-id="e6c20-137">The provider implements this method by calling a support object method, and the caller has passed the MAPI_DECLINE_OK flag.</span></span>
    
<span data-ttu-id="e6c20-138">MAPI_W_PARTIAL_COMPLETION SE PRODUIT</span><span class="sxs-lookup"><span data-stu-id="e6c20-138">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="e6c20-139">L’appel a réussi, mais pas toutes les entrées ont été correctement copiées ou déplacées.</span><span class="sxs-lookup"><span data-stu-id="e6c20-139">The call succeeded, but not all entries were successfully copied or moved.</span></span> <span data-ttu-id="e6c20-140">Lorsque cet avertissement est renvoyé, l’appel doit être traité comme étant réussi.</span><span class="sxs-lookup"><span data-stu-id="e6c20-140">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="e6c20-141">Pour tester cet avertissement, utilisez la macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="e6c20-141">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="e6c20-142">Pour plus d’informations, consultez [Utilisation de Macros pour gérer les erreurs](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="e6c20-142">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e6c20-143">Remarques</span><span class="sxs-lookup"><span data-stu-id="e6c20-143">Remarks</span></span>

<span data-ttu-id="e6c20-144">La méthode **IMAPIFolder::CopyMessages** copie ou déplace les messages vers un autre dossier.</span><span class="sxs-lookup"><span data-stu-id="e6c20-144">The **IMAPIFolder::CopyMessages** method copies or moves messages to another folder.</span></span> 
  
<span data-ttu-id="e6c20-145">Les messages qui sont ouvertes avec en lecture/écriture autorisation peut être déplacée ou copiée.</span><span class="sxs-lookup"><span data-stu-id="e6c20-145">Messages that are opened with read/write permission can be moved or copied.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="e6c20-146">Remarques destinées aux responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="e6c20-146">Notes to implementers</span></span>

<span data-ttu-id="e6c20-147">Si vous copiez les messages vers une autre banque de messages sans utiliser la méthode [IMAPISupport::CopyMessages](imapisupport-copymessages.md) , vous devez d’abord appeler [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) avec l’indicateur GENERATE_RECEIPT_ONLY.</span><span class="sxs-lookup"><span data-stu-id="e6c20-147">If you are copying messages to another message store without using the [IMAPISupport::CopyMessages](imapisupport-copymessages.md) method, you must first call [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) with the GENERATE_RECEIPT_ONLY flag set.</span></span> <span data-ttu-id="e6c20-148">La banque de message de réception n’est pas responsable de la génération de rapports de lecture pour les messages copiés ou déplacées.</span><span class="sxs-lookup"><span data-stu-id="e6c20-148">The receiving message store is not responsible for generating read reports for the copied or moved messages.</span></span> <span data-ttu-id="e6c20-149">Si vous appelez **IMAPISupport::CopyMessages** pour mettre en œuvre **IMAPIFolder::CopyMessages**, n’appelez pas **SetReadFlags**; MAPI est l’appeler.</span><span class="sxs-lookup"><span data-stu-id="e6c20-149">If you are calling **IMAPISupport::CopyMessages** to implement **IMAPIFolder::CopyMessages**, do not call **SetReadFlags**; MAPI will call it.</span></span> 
  
<span data-ttu-id="e6c20-150">Votre implémentation peut déplacer ou copier les messages dans n’importe quel ordre et générer des rapports d’état de lecture dans n’importe quel ordre.</span><span class="sxs-lookup"><span data-stu-id="e6c20-150">Your implementation can move or copy the messages in any order and generate read status reports in any order.</span></span> <span data-ttu-id="e6c20-151">Autrement dit, vous pouvez terminer la copie des messages avant de générer des rapports d’état de lecture ou envoyer les rapports avant que votre implémentation démarre l’opération de copie.</span><span class="sxs-lookup"><span data-stu-id="e6c20-151">That is, you can finish copying messages before generating any of the read status reports or send the reports before your implementation starts the copy operation.</span></span> <span data-ttu-id="e6c20-152">Toutefois, lire les rapports doivent être envoyés pour tous les messages à copier, indépendamment de si la copie a réussi.</span><span class="sxs-lookup"><span data-stu-id="e6c20-152">However, read reports should be sent for all messages to be copied, regardless of whether the copy is successful.</span></span>
  
<span data-ttu-id="e6c20-153">Lorsque l’opération de copie ou de déplacement implique plusieurs messages, effectuez l’opération complètement que possible.</span><span class="sxs-lookup"><span data-stu-id="e6c20-153">When the copy or move operation involves more than one message, perform the operation as completely as possible.</span></span> <span data-ttu-id="e6c20-154">N’arrêtez pas l’opération prématurément, sauf si une panne se produit qui est votre volonté, telles que le manque de mémoire, manque d’espace disque ou l’endommagement de la banque de messages.</span><span class="sxs-lookup"><span data-stu-id="e6c20-154">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span>
  
<span data-ttu-id="e6c20-155">Essayez de mettre à jour les identificateurs d’entrée pour les opérations de déplacement ou de copie.</span><span class="sxs-lookup"><span data-stu-id="e6c20-155">Try to maintain entry identifiers across move or copy operations.</span></span> <span data-ttu-id="e6c20-156">Vous devez également conserver les identificateurs d’entrée, bien qu’il ne soit pas requis.</span><span class="sxs-lookup"><span data-stu-id="e6c20-156">You should also preserve entry identifiers, although it is not required.</span></span>
  
<span data-ttu-id="e6c20-157">Envoyer des notifications lorsque vous déplacez ou copiez des messages afin que les clients sont avertis que leurs appels aux méthodes de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) des messages peuvent échouer.</span><span class="sxs-lookup"><span data-stu-id="e6c20-157">Send notifications when you move or copy messages so that clients are forewarned that their calls to the messages' [IMAPIProp::SaveChanges](imapiprop-savechanges.md) methods may fail.</span></span> 
  
<span data-ttu-id="e6c20-158">Ne pas inclure l’état d’un message dans la copie ou l’opération de déplacement.</span><span class="sxs-lookup"><span data-stu-id="e6c20-158">Do not include a message's status in the copy or move operation.</span></span> <span data-ttu-id="e6c20-159">Déplacement ou copie d’un état de message considérablement affecte les performances.</span><span class="sxs-lookup"><span data-stu-id="e6c20-159">Moving or copying a message status greatly affects performance.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="e6c20-160">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="e6c20-160">Notes to callers</span></span>

<span data-ttu-id="e6c20-161">**IMAPIFolder::CopyMessages** permet de remplir les dossiers des résultats de recherche, dans laquelle les messages sont souvent regroupés par dossier parent.</span><span class="sxs-lookup"><span data-stu-id="e6c20-161">Use **IMAPIFolder::CopyMessages** to populate search-results folders, where messages are often grouped by parent folder.</span></span> 
  
<span data-ttu-id="e6c20-162">Prévoyez ces valeurs de retour dans les conditions suivantes.</span><span class="sxs-lookup"><span data-stu-id="e6c20-162">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="e6c20-163">**Condition**</span><span class="sxs-lookup"><span data-stu-id="e6c20-163">**Condition**</span></span>|<span data-ttu-id="e6c20-164">**Valeur renvoy�e**</span><span class="sxs-lookup"><span data-stu-id="e6c20-164">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e6c20-165">**IMAPIFolder::CopyMessages** a été copié ou déplacé chaque message.</span><span class="sxs-lookup"><span data-stu-id="e6c20-165">**IMAPIFolder::CopyMessages** has successfully copied or moved every message.</span></span>  <br/> |<span data-ttu-id="e6c20-166">S_OK</span><span class="sxs-lookup"><span data-stu-id="e6c20-166">S_OK</span></span>  <br/> |
|<span data-ttu-id="e6c20-167">**IMAPIFolder::CopyMessages** n’a pas pu copier ou déplacer tous les messages.</span><span class="sxs-lookup"><span data-stu-id="e6c20-167">**IMAPIFolder::CopyMessages** was unable to successfully copy or move every message.</span></span>  <br/> |<span data-ttu-id="e6c20-168">MAPI_W_PARTIAL_COMPLETION SE PRODUIT</span><span class="sxs-lookup"><span data-stu-id="e6c20-168">MAPI_W_PARTIAL_COMPLETION</span></span>  <br/> |
|<span data-ttu-id="e6c20-169">**IMAPIFolder::CopyMessages** n’a pas pu terminer.</span><span class="sxs-lookup"><span data-stu-id="e6c20-169">**IMAPIFolder::CopyMessages** was unable to complete.</span></span>  <br/> |<span data-ttu-id="e6c20-170">Une valeur d’erreur</span><span class="sxs-lookup"><span data-stu-id="e6c20-170">Any error value</span></span>  <br/> |
   
<span data-ttu-id="e6c20-171">Lorsque **IMAPIFolder::CopyMessages** est impossible de terminer, ne supposent qu’aucun travail n’a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="e6c20-171">When **IMAPIFolder::CopyMessages** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="e6c20-172">**IMAPIFolder::CopyMessages** a pu copier ou déplacer un ou plusieurs messages avant de rencontrer l’erreur.</span><span class="sxs-lookup"><span data-stu-id="e6c20-172">**IMAPIFolder::CopyMessages** might have been able to copy or move one or more messages before encountering the error.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e6c20-173">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e6c20-173">See also</span></span>



[<span data-ttu-id="e6c20-174">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="e6c20-174">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)

