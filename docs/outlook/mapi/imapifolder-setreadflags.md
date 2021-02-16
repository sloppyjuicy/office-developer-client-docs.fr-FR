---
title: IMAPIFolderSetReadFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.SetReadFlags
api_type:
- COM
ms.assetid: 95a40c8a-0a8b-46c7-a07a-cbc6a7de8a3c
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 15504ecc88188ed7bc4eed0e64b1871dbc6a5e8d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406912"
---
# <a name="imapifoldersetreadflags"></a><span data-ttu-id="deee6-103">IMAPIFolder::SetReadFlags</span><span class="sxs-lookup"><span data-stu-id="deee6-103">IMAPIFolder::SetReadFlags</span></span>

<span data-ttu-id="deee6-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="deee6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="deee6-105">Définit ou désine l’indicateur MSGFLAG_READ dans la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) d’un ou plusieurs messages du dossier et gère l’envoi de rapports de lecture.</span><span class="sxs-lookup"><span data-stu-id="deee6-105">Sets or clears the MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of one or more of the folder's messages, and manages the sending of read reports.</span></span> 
  
```cpp
HRESULT SetReadFlags(
  LPENTRYLIST lpMsgList,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="deee6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="deee6-106">Parameters</span></span>

<span data-ttu-id="deee6-107">_lpMsgList_</span><span class="sxs-lookup"><span data-stu-id="deee6-107">_lpMsgList_</span></span>
  
> <span data-ttu-id="deee6-108">[in] Pointeur vers un tableau de structures [ENTRYLIST](entrylist.md) qui identifient le ou les messages qui ont des indicateurs de lecture à définir ou effacer.</span><span class="sxs-lookup"><span data-stu-id="deee6-108">[in] A pointer to an array of [ENTRYLIST](entrylist.md) structures that identify the message or messages that have read flags to set or clear.</span></span> <span data-ttu-id="deee6-109">Si  _lpMsgList_ est définie sur NULL, les indicateurs de lecture de tous les messages du dossier sont définies ou effacées.</span><span class="sxs-lookup"><span data-stu-id="deee6-109">If  _lpMsgList_ is set to NULL, the read flags for all the folder's messages are set or cleared.</span></span> 
    
<span data-ttu-id="deee6-110">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="deee6-110">_ulUIParam_</span></span>
  
> <span data-ttu-id="deee6-111">[in] Handle vers la fenêtre parent de l’indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="deee6-111">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="deee6-112">Le _paramètre ulUIParam_ est ignoré, sauf si l’MESSAGE_DIALOG est définie dans _le paramètre ulFlags._</span><span class="sxs-lookup"><span data-stu-id="deee6-112">The  _ulUIParam_ parameter is ignored unless the MESSAGE_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
<span data-ttu-id="deee6-113">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="deee6-113">_lpProgress_</span></span>
  
> <span data-ttu-id="deee6-114">[in] Pointeur vers un objet de progression qui affiche un indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="deee6-114">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="deee6-115">Si NULL est transmis dans  _lpProgress,_ le fournisseur de magasin de messages affiche un indicateur de progression à l’aide de l’implémentation de MAPI.</span><span class="sxs-lookup"><span data-stu-id="deee6-115">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using MAPI's implementation.</span></span> <span data-ttu-id="deee6-116">Le  _paramètre lpProgress est_ ignoré, sauf si l’MESSAGE_DIALOG est définie dans  _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="deee6-116">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in  _ulFlags_.</span></span>
    
<span data-ttu-id="deee6-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="deee6-117">_ulFlags_</span></span>
  
> <span data-ttu-id="deee6-118">[in] Masque de bits d’indicateurs qui contrôle la définition de l’indicateur de lecture d’un message et le traitement des rapports de lecture.</span><span class="sxs-lookup"><span data-stu-id="deee6-118">[in] A bitmask of flags that controls the setting of a message's read flag and the processing of read reports.</span></span> <span data-ttu-id="deee6-119">Les indicateurs suivants peuvent être définies :</span><span class="sxs-lookup"><span data-stu-id="deee6-119">The following flags can be set:</span></span>
    
  - <span data-ttu-id="deee6-120">CLEAR_READ_FLAG : l’indicateur MSGFLAG_READ doit être  effacé dans PR_MESSAGE_FLAGS et un rapport de lecture ne doit pas être envoyé.</span><span class="sxs-lookup"><span data-stu-id="deee6-120">CLEAR_READ_FLAG: The MSGFLAG_READ flag should be cleared in **PR_MESSAGE_FLAGS** and a read report should not be sent.</span></span> 
        
  - <span data-ttu-id="deee6-121">CLEAR_NRN_PENDING : l’indicateur MSGFLAG_NRN_PENDING doit être effacé  dans PR_MESSAGE_FLAGS et un rapport non lu ne doit pas être envoyé.</span><span class="sxs-lookup"><span data-stu-id="deee6-121">CLEAR_NRN_PENDING: The MSGFLAG_NRN_PENDING flag should be cleared in **PR_MESSAGE_FLAGS** and an unread report should not be sent.</span></span> 
        
  - <span data-ttu-id="deee6-122">CLEAR_RN_PENDING : l’indicateur MSGFLAG_RN_PENDING doit être  effacé dans PR_MESSAGE_FLAGS et un rapport de lecture ne doit pas être envoyé.</span><span class="sxs-lookup"><span data-stu-id="deee6-122">CLEAR_RN_PENDING: The MSGFLAG_RN_PENDING flag should be cleared in **PR_MESSAGE_FLAGS** and a read report should not be sent.</span></span> 
        
  - <span data-ttu-id="deee6-123">GENERATE_RECEIPT_ONLY : un rapport de lecture doit être envoyé s’il est en attente, mais l’état de l’indicateur MSGFLAG_READ ne doit pas être changé.</span><span class="sxs-lookup"><span data-stu-id="deee6-123">GENERATE_RECEIPT_ONLY: A read report should be sent if one is pending, but there should be no change in the state of the MSGFLAG_READ flag.</span></span>
        
  - <span data-ttu-id="deee6-124">MAPI_DEFERRED_ERRORS : permet à **SetReadFlags** de renvoyer correctement, éventuellement avant la fin de l’opération.</span><span class="sxs-lookup"><span data-stu-id="deee6-124">MAPI_DEFERRED_ERRORS: Allows **SetReadFlags** to return successfully, possibly before the operation has completed.</span></span> 
        
  - <span data-ttu-id="deee6-125">MESSAGE_DIALOG : affiche un indicateur de progression pendant la progression de l’opération.</span><span class="sxs-lookup"><span data-stu-id="deee6-125">MESSAGE_DIALOG: Displays a progress indicator while the operation proceeds.</span></span>
    
  - <span data-ttu-id="deee6-126">SUPPRESS_RECEIPT : un rapport de lecture en attente doit être annulé si un rapport de lecture a été demandé et que cet appel modifie l’état du message de non lu en lecture.</span><span class="sxs-lookup"><span data-stu-id="deee6-126">SUPPRESS_RECEIPT: A pending read report should be canceled if a read report had been requested and this call changes the state of the message from unread to read.</span></span> <span data-ttu-id="deee6-127">Si cet appel ne modifie pas l’état du message, le fournisseur de la boutique de messages peut ignorer cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="deee6-127">If this call does not change the state of the message, the message store provider can ignore this flag.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="deee6-128">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="deee6-128">Return values</span></span>

<span data-ttu-id="deee6-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="deee6-129">S_OK</span></span> 
  
> <span data-ttu-id="deee6-130">L’indicateur de lecture du ou des messages spécifiés a été correctement définie ou effacée.</span><span class="sxs-lookup"><span data-stu-id="deee6-130">The read flag for the specified message or messages was successfully set or cleared.</span></span>
    
<span data-ttu-id="deee6-131">MAPI_E_NO_SUPPRESS</span><span class="sxs-lookup"><span data-stu-id="deee6-131">MAPI_E_NO_SUPPRESS</span></span> 
  
> <span data-ttu-id="deee6-132">Le fournisseur de la boutique de messages ne prend pas en charge la suppression des rapports de lecture.</span><span class="sxs-lookup"><span data-stu-id="deee6-132">The message store provider does not support the suppression of read reports.</span></span>
    
<span data-ttu-id="deee6-133">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="deee6-133">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="deee6-134">L’une des combinaisons d’indicateurs incompatibles suivantes est définie dans le  _paramètre ulFlags_ :</span><span class="sxs-lookup"><span data-stu-id="deee6-134">One of the following incompatible combinations of flags is set in the  _ulFlags_ parameter:</span></span> 
    
   - <span data-ttu-id="deee6-135">SUPPRESS_RECEIPT | CLEAR_READ_FLAG</span><span class="sxs-lookup"><span data-stu-id="deee6-135">SUPPRESS_RECEIPT | CLEAR_READ_FLAG</span></span> 
    
   - <span data-ttu-id="deee6-136">SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span><span class="sxs-lookup"><span data-stu-id="deee6-136">SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span></span>
    
   - <span data-ttu-id="deee6-137">CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span><span class="sxs-lookup"><span data-stu-id="deee6-137">CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span></span>
    
<span data-ttu-id="deee6-138">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="deee6-138">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="deee6-139">L’appel a réussi, mais tous les messages n’ont pas été correctement traitées.</span><span class="sxs-lookup"><span data-stu-id="deee6-139">The call succeeded, but not all of the messages were successfully processed.</span></span> <span data-ttu-id="deee6-140">Lorsque cet avertissement est renvoyé, l’appel doit être traité comme réussi.</span><span class="sxs-lookup"><span data-stu-id="deee6-140">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="deee6-141">Pour tester cet avertissement, utilisez la macro **HR_FAILED.**</span><span class="sxs-lookup"><span data-stu-id="deee6-141">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="deee6-142">Pour plus d’informations, voir [Utilisation de macros pour la gestion des erreurs.](using-macros-for-error-handling.md)</span><span class="sxs-lookup"><span data-stu-id="deee6-142">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="deee6-143">Remarques</span><span class="sxs-lookup"><span data-stu-id="deee6-143">Remarks</span></span>

<span data-ttu-id="deee6-144">La **méthode IMAPIFolder::SetReadFlags** définit ou désinsiste l’indicateur MSGFLAG_READ dans la propriété **PR_MESSAGE_FLAGS** d’un ou plusieurs messages du dossier.</span><span class="sxs-lookup"><span data-stu-id="deee6-144">The **IMAPIFolder::SetReadFlags** method sets or clears the MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** property of one or more of the folder's messages.</span></span> <span data-ttu-id="deee6-145">La définition MSGFLAG_READ marque un message comme lu, ce qui n’indique pas nécessairement que le destinataire prévu a réellement lu le message.</span><span class="sxs-lookup"><span data-stu-id="deee6-145">Setting the MSGFLAG_READ flag marks a message as read, which does not necessarily indicate that the intended recipient has actually read the message.</span></span> 
  
<span data-ttu-id="deee6-146">**SetReadFlags gère** également l’envoi de rapports de lecture.</span><span class="sxs-lookup"><span data-stu-id="deee6-146">**SetReadFlags** also manages the sending of read reports.</span></span> 
  
<span data-ttu-id="deee6-147">L’indicateur de lecture ne peut pas être modifié pour les raisons suivantes :</span><span class="sxs-lookup"><span data-stu-id="deee6-147">The read flag cannot be changed for the following:</span></span>
  
- <span data-ttu-id="deee6-148">Messages qui n’existent pas.</span><span class="sxs-lookup"><span data-stu-id="deee6-148">Messages that do not exist.</span></span>
    
- <span data-ttu-id="deee6-149">Messages qui ont été déplacés ailleurs.</span><span class="sxs-lookup"><span data-stu-id="deee6-149">Messages that have been moved elsewhere.</span></span>
    
- <span data-ttu-id="deee6-150">Messages ouverts avec une autorisation de lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="deee6-150">Messages that are open with read/write permission.</span></span>
    
- <span data-ttu-id="deee6-151">Messages actuellement envoyés.</span><span class="sxs-lookup"><span data-stu-id="deee6-151">Messages that are currently submitted.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="deee6-152">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="deee6-152">Notes to implementers</span></span>

<span data-ttu-id="deee6-153">Vous pouvez décider de ne pas prendre en charge l’envoi de rapports de lecture et la demande de suppression des rapports de lecture.</span><span class="sxs-lookup"><span data-stu-id="deee6-153">You can decide not to support the sending of read reports and the request to suppress read reports.</span></span> <span data-ttu-id="deee6-154">Pour éviter la suppression d’un rapport de lecture, renvoyez MAPI_E_NO_SUPPRESS lorsque **SetReadFlags** est appelé avec SUPPRESS_RECEIPT définie dans le _paramètre ulFlags._</span><span class="sxs-lookup"><span data-stu-id="deee6-154">To avoid suppressing a read report, return MAPI_E_NO_SUPPRESS when **SetReadFlags** is called with SUPPRESS_RECEIPT set in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="deee6-155">Lorsque le  _paramètre lpMsgList_ pointe vers plusieurs messages, effectuez l’opération aussi complètement que possible pour chaque message.</span><span class="sxs-lookup"><span data-stu-id="deee6-155">When the  _lpMsgList_ parameter points to more than one message, perform the operation as completely as possible for each message.</span></span> <span data-ttu-id="deee6-156">N’arrêtez pas l’opération prématurément, sauf si une défaillance dépasse votre contrôle, par exemple un manque de mémoire, un manque d’espace disque ou une altération de la magasin de messages.</span><span class="sxs-lookup"><span data-stu-id="deee6-156">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span> 
  
<span data-ttu-id="deee6-157">Si aucun des indicateurs n’est paramétré dans  _le paramètre ulFlags,_ les règles suivantes s’appliquent :</span><span class="sxs-lookup"><span data-stu-id="deee6-157">If none of the flags are set in the  _ulFlags_ parameter, the following rules apply:</span></span> 
  
- <span data-ttu-id="deee6-158">Si MSGFLAG_READ est déjà définie, ne faites rien.</span><span class="sxs-lookup"><span data-stu-id="deee6-158">If MSGFLAG_READ is already set, do nothing.</span></span>
    
- <span data-ttu-id="deee6-159">Si MSGFLAG_READ n’est pas définie, définissez-la immédiatement et envoyez les rapports de lecture en attente si la propriété **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) est définie.</span><span class="sxs-lookup"><span data-stu-id="deee6-159">If MSGFLAG_READ is not set, set it immediately and send any pending read reports if the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property is set.</span></span>
    
<span data-ttu-id="deee6-160">Lorsque l’SUPPRESS_RECEIPT est définie, les règles suivantes s’appliquent :</span><span class="sxs-lookup"><span data-stu-id="deee6-160">When the SUPPRESS_RECEIPT flag is set, the following rules apply:</span></span>
  
- <span data-ttu-id="deee6-161">Si MSGFLAG_READ est déjà définie, ne faites rien.</span><span class="sxs-lookup"><span data-stu-id="deee6-161">If MSGFLAG_READ is already set, do nothing.</span></span> 
    
- <span data-ttu-id="deee6-162">Si MSGFLAG_READ n’est pas définie, définissez-la et annulez les rapports de lecture en attente.</span><span class="sxs-lookup"><span data-stu-id="deee6-162">If MSGFLAG_READ is not set, set it and cancel any pending read reports.</span></span>
    
<span data-ttu-id="deee6-163">Lorsque l’CLEAR_READ_FLAG est définie, effacer l’indicateur MSGFLAG_READ dans la  propriété PR_MESSAGE_FLAGS de chaque message et n’envoyez aucun rapport de lecture.</span><span class="sxs-lookup"><span data-stu-id="deee6-163">When the CLEAR_READ_FLAG flag is set, clear the MSGFLAG_READ flag in each message's **PR_MESSAGE_FLAGS** property and do not send any read reports.</span></span> 
  
<span data-ttu-id="deee6-164">Lorsque l’GENERATE_RECEIPT_ONLY est définie, envoyez les rapports de lecture en attente.</span><span class="sxs-lookup"><span data-stu-id="deee6-164">When the GENERATE_RECEIPT_ONLY flag is set, send any pending read reports.</span></span> <span data-ttu-id="deee6-165">Ne pas définir ou effacer les MSGFLAG_READ.</span><span class="sxs-lookup"><span data-stu-id="deee6-165">Do not set or clear MSGFLAG_READ.</span></span>
  
<span data-ttu-id="deee6-166">Lorsque les indicateurs SUPPRESS_RECEIPT et GENERATE_RECEIPT_ONLY sont tous deux définies, définissez PR_READ_RECEIPT_REQUESTED sur FALSE **si** elle est définie et n’envoyez pas de rapport de lecture.</span><span class="sxs-lookup"><span data-stu-id="deee6-166">When both the SUPPRESS_RECEIPT and GENERATE_RECEIPT_ONLY flags are set, set **PR_READ_RECEIPT_REQUESTED** to FALSE if it is set and do not send a read report.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="deee6-167">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="deee6-167">Notes to callers</span></span>

<span data-ttu-id="deee6-168">Attendez-vous à ce que ces valeurs de retour se placent dans les conditions suivantes.</span><span class="sxs-lookup"><span data-stu-id="deee6-168">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="deee6-169">**Condition**</span><span class="sxs-lookup"><span data-stu-id="deee6-169">**Condition**</span></span>|<span data-ttu-id="deee6-170">**Valeur renvoy�e**</span><span class="sxs-lookup"><span data-stu-id="deee6-170">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="deee6-171">**SetReadFlags a** correctement traitée chaque message.</span><span class="sxs-lookup"><span data-stu-id="deee6-171">**SetReadFlags** has successfully processed every message.</span></span>  <br/> |<span data-ttu-id="deee6-172">S_OK</span><span class="sxs-lookup"><span data-stu-id="deee6-172">S_OK</span></span>  <br/> |
|<span data-ttu-id="deee6-173">**SetReadFlags n’a** pas pu traiter correctement chaque message.</span><span class="sxs-lookup"><span data-stu-id="deee6-173">**SetReadFlags** was unable to successfully process every message.</span></span>  <br/> |<span data-ttu-id="deee6-174">MAPI_W_PARTIAL_COMPLETION ou MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="deee6-174">MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND</span></span>  <br/> |
|<span data-ttu-id="deee6-175">**SetReadFlags n’a** pas pu se terminer.</span><span class="sxs-lookup"><span data-stu-id="deee6-175">**SetReadFlags** was unable to complete.</span></span>  <br/> |<span data-ttu-id="deee6-176">Toute valeur d’erreur à l’exception MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="deee6-176">Any error value except MAPI_E_NOT_FOUND</span></span>  <br/> |
   
<span data-ttu-id="deee6-177">Lorsque **SetReadFlags ne** parvient pas à se terminer, ne supposez pas qu’aucun travail n’a été effectué.</span><span class="sxs-lookup"><span data-stu-id="deee6-177">When **SetReadFlags** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="deee6-178">**SetReadFlags** a peut-être pu définir ou effacer l’indicateur MSGFLAG_READ’un ou plusieurs des messages avant de rencontrer l’erreur.</span><span class="sxs-lookup"><span data-stu-id="deee6-178">**SetReadFlags** might have been able to set or clear the MSGFLAG_READ flag for one or more of the messages before encountering the error.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="deee6-179">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="deee6-179">MFCMAPI reference</span></span>

<span data-ttu-id="deee6-180">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="deee6-180">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="deee6-181">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="deee6-181">**File**</span></span>|<span data-ttu-id="deee6-182">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="deee6-182">**Function**</span></span>|<span data-ttu-id="deee6-183">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="deee6-183">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="deee6-184">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="deee6-184">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="deee6-185">CFolderDlg::OnSetReadFlag</span><span class="sxs-lookup"><span data-stu-id="deee6-185">CFolderDlg::OnSetReadFlag</span></span>  <br/> |<span data-ttu-id="deee6-186">MFCMAPI utilise la méthode **IMAPIFolder::SetReadFlags** pour définir manuellement l’état de lecture sur les messages spécifiés.</span><span class="sxs-lookup"><span data-stu-id="deee6-186">MFCMAPI uses the **IMAPIFolder::SetReadFlags** method to manually set the read status on the specified messages.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="deee6-187">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="deee6-187">See also</span></span>

- [<span data-ttu-id="deee6-188">ENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="deee6-188">ENTRYLIST</span></span>](entrylist.md) 
- [<span data-ttu-id="deee6-189">IMessage::SetReadFlag</span><span class="sxs-lookup"><span data-stu-id="deee6-189">IMessage::SetReadFlag</span></span>](imessage-setreadflag.md)  
- [<span data-ttu-id="deee6-190">Propriété canonique PidTagMessageFlags</span><span class="sxs-lookup"><span data-stu-id="deee6-190">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)  
- [<span data-ttu-id="deee6-191">Propriété canonique PidTagReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="deee6-191">PidTagReadReceiptRequested Canonical Property</span></span>](pidtagreadreceiptrequested-canonical-property.md)  
- [<span data-ttu-id="deee6-192">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="deee6-192">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
- [<span data-ttu-id="deee6-193">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="deee6-193">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)  
- [<span data-ttu-id="deee6-194">Utilisation de macros pour la gestion des erreurs</span><span class="sxs-lookup"><span data-stu-id="deee6-194">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

