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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: a52c0501040d77ddb8172b212bf341a08704dcc3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783741"
---
# <a name="imapifoldersetreadflags"></a><span data-ttu-id="c056f-103">IMAPIFolder::SetReadFlags</span><span class="sxs-lookup"><span data-stu-id="c056f-103">IMAPIFolder::SetReadFlags</span></span>

<span data-ttu-id="c056f-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c056f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c056f-105">Définit ou supprime l’indicateur MSGFLAG_READ dans la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) d’un ou plusieurs des messages du dossier et gère l’envoi de rapports de lecture.</span><span class="sxs-lookup"><span data-stu-id="c056f-105">Sets or clears the MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of one or more of the folder's messages, and manages the sending of read reports.</span></span> 
  
```cpp
HRESULT SetReadFlags(
  LPENTRYLIST lpMsgList,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="c056f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c056f-106">Parameters</span></span>

<span data-ttu-id="c056f-107">_lpMsgList_</span><span class="sxs-lookup"><span data-stu-id="c056f-107">_lpMsgList_</span></span>
  
> <span data-ttu-id="c056f-108">[in] Pointeur vers un tableau de structures [ENTRYLIST](entrylist.md) qui identifient l’ou les messages que vous ont lu les indicateurs pour définir ou supprimer.</span><span class="sxs-lookup"><span data-stu-id="c056f-108">[in] A pointer to an array of [ENTRYLIST](entrylist.md) structures that identify the message or messages that have read flags to set or clear.</span></span> <span data-ttu-id="c056f-109">Si _lpMsgList_ est défini sur NULL, la lecture indicateurs pour tous les messages du dossier sont configurés ou désactivés.</span><span class="sxs-lookup"><span data-stu-id="c056f-109">If  _lpMsgList_ is set to NULL, the read flags for all the folder's messages are set or cleared.</span></span> 
    
<span data-ttu-id="c056f-110">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="c056f-110">_ulUIParam_</span></span>
  
> <span data-ttu-id="c056f-111">[in] Un handle vers la fenêtre parent de l’indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="c056f-111">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="c056f-112">Le paramètre _ulUIParam_ est ignoré à moins que l’indicateur MESSAGE_DIALOG est défini dans le paramètre _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="c056f-112">The  _ulUIParam_ parameter is ignored unless the MESSAGE_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
<span data-ttu-id="c056f-113">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="c056f-113">_lpProgress_</span></span>
  
> <span data-ttu-id="c056f-114">[in] Pointeur vers un objet de progression qui affiche un indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="c056f-114">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="c056f-115">Si NULL est indiqué dans _lpProgress_, le fournisseur de banque de message affiche un indicateur de progression à l’aide de mise en œuvre de MAPI.</span><span class="sxs-lookup"><span data-stu-id="c056f-115">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using MAPI's implementation.</span></span> <span data-ttu-id="c056f-116">Le paramètre _lpProgress_ est ignoré à moins que l’indicateur MESSAGE_DIALOG est défini dans _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="c056f-116">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in  _ulFlags_.</span></span>
    
<span data-ttu-id="c056f-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c056f-117">_ulFlags_</span></span>
  
> <span data-ttu-id="c056f-118">[in] Un masque de bits d’indicateurs qui contrôlent la valeur d’indicateur de lecture d’un message et le traitement de lire des rapports.</span><span class="sxs-lookup"><span data-stu-id="c056f-118">[in] A bitmask of flags that controls the setting of a message's read flag and the processing of read reports.</span></span> <span data-ttu-id="c056f-119">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="c056f-119">The following flags can be set:</span></span>
    
  - <span data-ttu-id="c056f-120">CLEAR_READ_FLAG : L’indicateur MSGFLAG_READ doit être effacé dans **PR_MESSAGE_FLAGS** et un rapport de lecture ne doit pas être envoyé.</span><span class="sxs-lookup"><span data-stu-id="c056f-120">CLEAR_READ_FLAG: The MSGFLAG_READ flag should be cleared in **PR_MESSAGE_FLAGS** and a read report should not be sent.</span></span> 
        
  - <span data-ttu-id="c056f-121">CLEAR_NRN_PENDING : L’indicateur MSGFLAG_NRN_PENDING doit être effacé dans **PR_MESSAGE_FLAGS** et un rapport non lu ne doit pas être envoyé.</span><span class="sxs-lookup"><span data-stu-id="c056f-121">CLEAR_NRN_PENDING: The MSGFLAG_NRN_PENDING flag should be cleared in **PR_MESSAGE_FLAGS** and an unread report should not be sent.</span></span> 
        
  - <span data-ttu-id="c056f-122">CLEAR_RN_PENDING : L’indicateur MSGFLAG_RN_PENDING doit être effacé dans **PR_MESSAGE_FLAGS** et un rapport de lecture ne doit pas être envoyé.</span><span class="sxs-lookup"><span data-stu-id="c056f-122">CLEAR_RN_PENDING: The MSGFLAG_RN_PENDING flag should be cleared in **PR_MESSAGE_FLAGS** and a read report should not be sent.</span></span> 
        
  - <span data-ttu-id="c056f-123">GENERATE_RECEIPT_ONLY : Un rapport de lecture doit être envoyé si un est en attente, mais il ne doit y avoir aucune modification de l’état de l’indicateur MSGFLAG_READ.</span><span class="sxs-lookup"><span data-stu-id="c056f-123">GENERATE_RECEIPT_ONLY: A read report should be sent if one is pending, but there should be no change in the state of the MSGFLAG_READ flag.</span></span>
        
  - <span data-ttu-id="c056f-124">MAPI_DEFERRED_ERRORS : Permet de **SetReadFlags** renvoyer avec succès, éventuellement, avant la fin de l’opération.</span><span class="sxs-lookup"><span data-stu-id="c056f-124">MAPI_DEFERRED_ERRORS: Allows **SetReadFlags** to return successfully, possibly before the operation has completed.</span></span> 
        
  - <span data-ttu-id="c056f-125">MESSAGE_DIALOG : Affiche un indicateur de progression pendant que l’opération s’effectue.</span><span class="sxs-lookup"><span data-stu-id="c056f-125">MESSAGE_DIALOG: Displays a progress indicator while the operation proceeds.</span></span>
    
  - <span data-ttu-id="c056f-126">SUPPRESS_RECEIPT : Un rapport de lecture en attente doit être annulé si un rapport de lecture a été demandé et cet appel remplace l’état du message non lu à lire.</span><span class="sxs-lookup"><span data-stu-id="c056f-126">SUPPRESS_RECEIPT: A pending read report should be canceled if a read report had been requested and this call changes the state of the message from unread to read.</span></span> <span data-ttu-id="c056f-127">Si cet appel ne modifie pas l’état du message, le fournisseur de banque de message peut ignorer cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="c056f-127">If this call does not change the state of the message, the message store provider can ignore this flag.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="c056f-128">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="c056f-128">Return values</span></span>

<span data-ttu-id="c056f-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="c056f-129">S_OK</span></span> 
  
> <span data-ttu-id="c056f-130">L’indicateur de lecture pour l’ou les messages spécifié a été correctement configurée ou désactivée.</span><span class="sxs-lookup"><span data-stu-id="c056f-130">The read flag for the specified message or messages was successfully set or cleared.</span></span>
    
<span data-ttu-id="c056f-131">MAPI_E_NO_SUPPRESS</span><span class="sxs-lookup"><span data-stu-id="c056f-131">MAPI_E_NO_SUPPRESS</span></span> 
  
> <span data-ttu-id="c056f-132">Le fournisseur de banque de messages ne gère pas la suppression des rapports de lecture.</span><span class="sxs-lookup"><span data-stu-id="c056f-132">The message store provider does not support the suppression of read reports.</span></span>
    
<span data-ttu-id="c056f-133">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c056f-133">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="c056f-134">Une des combinaisons d’indicateurs incompatibles suivants est définie dans le paramètre _ulFlags_ :</span><span class="sxs-lookup"><span data-stu-id="c056f-134">One of the following incompatible combinations of flags is set in the  _ulFlags_ parameter:</span></span> 
    
   - <span data-ttu-id="c056f-135">SUPPRESS_RECEIPT | CLEAR_READ_FLAG</span><span class="sxs-lookup"><span data-stu-id="c056f-135">SUPPRESS_RECEIPT | CLEAR_READ_FLAG</span></span> 
    
   - <span data-ttu-id="c056f-136">SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span><span class="sxs-lookup"><span data-stu-id="c056f-136">SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span></span>
    
   - <span data-ttu-id="c056f-137">CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span><span class="sxs-lookup"><span data-stu-id="c056f-137">CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span></span>
    
<span data-ttu-id="c056f-138">MAPI_W_PARTIAL_COMPLETION SE PRODUIT</span><span class="sxs-lookup"><span data-stu-id="c056f-138">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="c056f-139">L’appel a réussi, mais pas tous les messages ont été traités.</span><span class="sxs-lookup"><span data-stu-id="c056f-139">The call succeeded, but not all of the messages were successfully processed.</span></span> <span data-ttu-id="c056f-140">Lorsque cet avertissement est renvoyé, l’appel doit être traité comme étant réussi.</span><span class="sxs-lookup"><span data-stu-id="c056f-140">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="c056f-141">Pour tester cet avertissement, utilisez la macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="c056f-141">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="c056f-142">Pour plus d’informations, consultez [Utilisation de Macros pour gérer les erreurs](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="c056f-142">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c056f-143">Remarques</span><span class="sxs-lookup"><span data-stu-id="c056f-143">Remarks</span></span>

<span data-ttu-id="c056f-144">La méthode **IMAPIFolder::SetReadFlags** Active ou désactive l’indicateur MSGFLAG_READ dans la propriété **PR_MESSAGE_FLAGS** d’une ou plusieurs des messages du dossier.</span><span class="sxs-lookup"><span data-stu-id="c056f-144">The **IMAPIFolder::SetReadFlags** method sets or clears the MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** property of one or more of the folder's messages.</span></span> <span data-ttu-id="c056f-145">Définition de l’indicateur MSGFLAG_READ marque un message comme lu, ce qui n’indique pas nécessairement que le destinataire a lu réellement le message.</span><span class="sxs-lookup"><span data-stu-id="c056f-145">Setting the MSGFLAG_READ flag marks a message as read, which does not necessarily indicate that the intended recipient has actually read the message.</span></span> 
  
<span data-ttu-id="c056f-146">**SetReadFlags** gère également l’envoi des rapports de lecture.</span><span class="sxs-lookup"><span data-stu-id="c056f-146">**SetReadFlags** also manages the sending of read reports.</span></span> 
  
<span data-ttu-id="c056f-147">L’indicateur de lecture ne peut pas être modifié pour les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="c056f-147">The read flag cannot be changed for the following:</span></span>
  
- <span data-ttu-id="c056f-148">Messages qui n’existent pas.</span><span class="sxs-lookup"><span data-stu-id="c056f-148">Messages that do not exist.</span></span>
    
- <span data-ttu-id="c056f-149">Les messages qui ont été déplacés vers un autre emplacement.</span><span class="sxs-lookup"><span data-stu-id="c056f-149">Messages that have been moved elsewhere.</span></span>
    
- <span data-ttu-id="c056f-150">Messages qui sont ouvertes avec l’autorisation de lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="c056f-150">Messages that are open with read/write permission.</span></span>
    
- <span data-ttu-id="c056f-151">Messages qui sont actuellement envoyées.</span><span class="sxs-lookup"><span data-stu-id="c056f-151">Messages that are currently submitted.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="c056f-152">Remarques destinées aux responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="c056f-152">Notes to implementers</span></span>

<span data-ttu-id="c056f-153">Vous décider de ne pas prendre en charge l’envoi de rapports de lecture et de la demande à supprimer les rapports de lecture.</span><span class="sxs-lookup"><span data-stu-id="c056f-153">You can decide not to support the sending of read reports and the request to suppress read reports.</span></span> <span data-ttu-id="c056f-154">Pour éviter la suppression d’un rapport de lecture, renvoyer MAPI_E_NO_SUPPRESS lorsque **SetReadFlags** est appelée avec SUPPRESS_RECEIPT dans le paramètre _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="c056f-154">To avoid suppressing a read report, return MAPI_E_NO_SUPPRESS when **SetReadFlags** is called with SUPPRESS_RECEIPT set in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="c056f-155">Lorsque le paramètre _lpMsgList_ pointe vers plus d’un message, effectuez l’opération complètement que possible pour chaque message.</span><span class="sxs-lookup"><span data-stu-id="c056f-155">When the  _lpMsgList_ parameter points to more than one message, perform the operation as completely as possible for each message.</span></span> <span data-ttu-id="c056f-156">N’arrêtez pas l’opération prématurément, sauf si une panne se produit qui est votre volonté, telles que le manque de mémoire, manque d’espace disque ou l’endommagement de la banque de messages.</span><span class="sxs-lookup"><span data-stu-id="c056f-156">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span> 
  
<span data-ttu-id="c056f-157">Si aucun des indicateurs sont définies dans le paramètre _ulFlags_ , les règles suivantes s’appliquent :</span><span class="sxs-lookup"><span data-stu-id="c056f-157">If none of the flags are set in the  _ulFlags_ parameter, the following rules apply:</span></span> 
  
- <span data-ttu-id="c056f-158">Si MSGFLAG_READ est déjà défini, ne faites rien.</span><span class="sxs-lookup"><span data-stu-id="c056f-158">If MSGFLAG_READ is already set, do nothing.</span></span>
    
- <span data-ttu-id="c056f-159">Si MSGFLAG_READ n’est pas défini, affectez-lui immédiatement et envoyer tout en attente de rapports de lecture si la valeur de la propriété **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="c056f-159">If MSGFLAG_READ is not set, set it immediately and send any pending read reports if the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property is set.</span></span>
    
<span data-ttu-id="c056f-160">Lorsque l’indicateur SUPPRESS_RECEIPT est défini, les règles suivantes s’appliquent :</span><span class="sxs-lookup"><span data-stu-id="c056f-160">When the SUPPRESS_RECEIPT flag is set, the following rules apply:</span></span>
  
- <span data-ttu-id="c056f-161">Si MSGFLAG_READ est déjà défini, ne faites rien.</span><span class="sxs-lookup"><span data-stu-id="c056f-161">If MSGFLAG_READ is already set, do nothing.</span></span> 
    
- <span data-ttu-id="c056f-162">Si MSGFLAG_READ n’est pas définie, définissez-la et annuler les en attente de rapports de lecture.</span><span class="sxs-lookup"><span data-stu-id="c056f-162">If MSGFLAG_READ is not set, set it and cancel any pending read reports.</span></span>
    
<span data-ttu-id="c056f-163">Lorsque l’indicateur CLEAR_READ_FLAG est défini, effacer l’indicateur MSGFLAG_READ dans la propriété **PR_MESSAGE_FLAGS** du chaque message et ne pas envoyer des rapports de lecture.</span><span class="sxs-lookup"><span data-stu-id="c056f-163">When the CLEAR_READ_FLAG flag is set, clear the MSGFLAG_READ flag in each message's **PR_MESSAGE_FLAGS** property and do not send any read reports.</span></span> 
  
<span data-ttu-id="c056f-164">Lorsque l’indicateur GENERATE_RECEIPT_ONLY est défini, envoyer des rapports de lecture en attente.</span><span class="sxs-lookup"><span data-stu-id="c056f-164">When the GENERATE_RECEIPT_ONLY flag is set, send any pending read reports.</span></span> <span data-ttu-id="c056f-165">Ne pas définir ou effacer MSGFLAG_READ.</span><span class="sxs-lookup"><span data-stu-id="c056f-165">Do not set or clear MSGFLAG_READ.</span></span>
  
<span data-ttu-id="c056f-166">Lorsque les indicateurs GENERATE_RECEIPT_ONLY et SUPPRESS_RECEIPT sont définies, la valeur **PR_READ_RECEIPT_REQUESTED** FALSE si elle est définie et ne pas envoyer un rapport de lecture.</span><span class="sxs-lookup"><span data-stu-id="c056f-166">When both the SUPPRESS_RECEIPT and GENERATE_RECEIPT_ONLY flags are set, set **PR_READ_RECEIPT_REQUESTED** to FALSE if it is set and do not send a read report.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="c056f-167">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="c056f-167">Notes to callers</span></span>

<span data-ttu-id="c056f-168">Prévoyez ces valeurs de retour dans les conditions suivantes.</span><span class="sxs-lookup"><span data-stu-id="c056f-168">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="c056f-169">**Condition**</span><span class="sxs-lookup"><span data-stu-id="c056f-169">**Condition**</span></span>|<span data-ttu-id="c056f-170">**Valeur renvoy�e**</span><span class="sxs-lookup"><span data-stu-id="c056f-170">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c056f-171">**SetReadFlags** a traité avec succès à chaque message.</span><span class="sxs-lookup"><span data-stu-id="c056f-171">**SetReadFlags** has successfully processed every message.</span></span>  <br/> |<span data-ttu-id="c056f-172">S_OK</span><span class="sxs-lookup"><span data-stu-id="c056f-172">S_OK</span></span>  <br/> |
|<span data-ttu-id="c056f-173">**SetReadFlags** n’a pas pu traiter correctement tous les messages.</span><span class="sxs-lookup"><span data-stu-id="c056f-173">**SetReadFlags** was unable to successfully process every message.</span></span>  <br/> |<span data-ttu-id="c056f-174">MAPI_W_PARTIAL_COMPLETION se produit ou MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="c056f-174">MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND</span></span>  <br/> |
|<span data-ttu-id="c056f-175">**SetReadFlags** n’a pas pu terminer.</span><span class="sxs-lookup"><span data-stu-id="c056f-175">**SetReadFlags** was unable to complete.</span></span>  <br/> |<span data-ttu-id="c056f-176">Une valeur d’erreur à l’exception MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="c056f-176">Any error value except MAPI_E_NOT_FOUND</span></span>  <br/> |
   
<span data-ttu-id="c056f-177">Lorsque **SetReadFlags** est impossible de terminer, ne supposent qu’aucun travail n’a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="c056f-177">When **SetReadFlags** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="c056f-178">**SetReadFlags** a pu définir ou effacer l’indicateur MSGFLAG_READ pour une ou plusieurs des messages avant de rencontrer l’erreur.</span><span class="sxs-lookup"><span data-stu-id="c056f-178">**SetReadFlags** might have been able to set or clear the MSGFLAG_READ flag for one or more of the messages before encountering the error.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="c056f-179">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="c056f-179">MFCMAPI reference</span></span>

<span data-ttu-id="c056f-180">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="c056f-180">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c056f-181">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="c056f-181">**File**</span></span>|<span data-ttu-id="c056f-182">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="c056f-182">**Function**</span></span>|<span data-ttu-id="c056f-183">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="c056f-183">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c056f-184">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="c056f-184">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="c056f-185">CFolderDlg::OnSetReadFlag</span><span class="sxs-lookup"><span data-stu-id="c056f-185">CFolderDlg::OnSetReadFlag</span></span>  <br/> |<span data-ttu-id="c056f-186">MFCMAPI utilise la méthode **IMAPIFolder::SetReadFlags** pour définir manuellement l’état de lecture sur les messages spécifiés.</span><span class="sxs-lookup"><span data-stu-id="c056f-186">MFCMAPI uses the **IMAPIFolder::SetReadFlags** method to manually set the read status on the specified messages.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c056f-187">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c056f-187">See also</span></span>

- [<span data-ttu-id="c056f-188">ENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="c056f-188">ENTRYLIST</span></span>](entrylist.md) 
- [<span data-ttu-id="c056f-189">IMessage::SetReadFlag</span><span class="sxs-lookup"><span data-stu-id="c056f-189">IMessage::SetReadFlag</span></span>](imessage-setreadflag.md)  
- [<span data-ttu-id="c056f-190">Propriété canonique PidTagMessageFlags</span><span class="sxs-lookup"><span data-stu-id="c056f-190">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)  
- [<span data-ttu-id="c056f-191">Propriété canonique PidTagReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="c056f-191">PidTagReadReceiptRequested Canonical Property</span></span>](pidtagreadreceiptrequested-canonical-property.md)  
- [<span data-ttu-id="c056f-192">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="c056f-192">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
- [<span data-ttu-id="c056f-193">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="c056f-193">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)  
- [<span data-ttu-id="c056f-194">Utilisation de Macros pour la gestion des erreurs</span><span class="sxs-lookup"><span data-stu-id="c056f-194">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

