---
title: IMessageSetReadFlag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.SetReadFlag
api_type:
- COM
ms.assetid: 2d02ebf6-bb8b-42bb-9bd0-870dbae9aeb4
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 40815f1df597a8fb1fd8adef3dcc09323e946d30
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592961"
---
# <a name="imessagesetreadflag"></a><span data-ttu-id="f466a-103">IMessage::SetReadFlag</span><span class="sxs-lookup"><span data-stu-id="f466a-103">IMessage::SetReadFlag</span></span>

<span data-ttu-id="f466a-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f466a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f466a-105">Définit ou supprime l’indicateur MSGFLAG_READ dans la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) du message et gère l’envoi de rapports de lecture.</span><span class="sxs-lookup"><span data-stu-id="f466a-105">Sets or clears the MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of the message and manages the sending of read reports.</span></span>
  
```cpp
HRESULT SetReadFlag(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="f466a-106">Param�tres</span><span class="sxs-lookup"><span data-stu-id="f466a-106">Parameters</span></span>

<span data-ttu-id="f466a-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f466a-107">_ulFlags_</span></span>
  
> <span data-ttu-id="f466a-108">[in] Masque de bits d’indicateurs qui contrôle le paramétrage de la lecture d’un message drapeau, du message MSGFLAG_READ dans sa propriété **PR_MESSAGE_FLAGS** et le traitement des rapports de lecture.</span><span class="sxs-lookup"><span data-stu-id="f466a-108">[in] Bitmask of flags that controls the setting of a message's read flag that is, the message's MSGFLAG_READ flag in its **PR_MESSAGE_FLAGS** property and the processing of read reports.</span></span> <span data-ttu-id="f466a-109">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="f466a-109">The following flags can be set:</span></span> 
    
  - <span data-ttu-id="f466a-110">CLEAR_READ_FLAG : L’indicateur MSGFLAG_READ doit être effacé dans **PR_MESSAGE_FLAGS** et aucun rapport de lecture ne doit être envoyé.</span><span class="sxs-lookup"><span data-stu-id="f466a-110">CLEAR_READ_FLAG: The MSGFLAG_READ flag should be cleared in **PR_MESSAGE_FLAGS** and no read report should be sent.</span></span> 
      
  - <span data-ttu-id="f466a-111">CLEAR_NRN_PENDING : L’indicateur MSGFLAG_NRN_PENDING doit être désactivée dans **PR_MESSAGE_FLAGS** et un rapport de non-lecture ne doit pas être envoyé.</span><span class="sxs-lookup"><span data-stu-id="f466a-111">CLEAR_NRN_PENDING: The MSGFLAG_NRN_PENDING flag should be cleared in **PR_MESSAGE_FLAGS** and a non-read report should not be sent.</span></span> 
      
  - <span data-ttu-id="f466a-112">CLEAR_RN_PENDING : L’indicateur MSGFLAG_RN_PENDING doit être effacé dans **PR_MESSAGE_FLAGS** et aucun rapport de lecture ne doit être envoyé.</span><span class="sxs-lookup"><span data-stu-id="f466a-112">CLEAR_RN_PENDING: The MSGFLAG_RN_PENDING flag should be cleared in **PR_MESSAGE_FLAGS** and no read report should be sent.</span></span> 
      
  - <span data-ttu-id="f466a-113">GENERATE_RECEIPT_ONLY : Un rapport de lecture doit être envoyé si un est en attente, mais il ne doit y avoir aucune modification de l’état de l’indicateur MSGFLAG_READ.</span><span class="sxs-lookup"><span data-stu-id="f466a-113">GENERATE_RECEIPT_ONLY: A read report should be sent if one is pending, but there should be no change in the state of the MSGFLAG_READ flag.</span></span>
      
  - <span data-ttu-id="f466a-114">MAPI_DEFERRED_ERRORS : Permet de **SetReadFlag** renvoyer avec succès, éventuellement, avant la fin de l’opération.</span><span class="sxs-lookup"><span data-stu-id="f466a-114">MAPI_DEFERRED_ERRORS: Allows **SetReadFlag** to return successfully, possibly before the operation has completed.</span></span> 
      
  - <span data-ttu-id="f466a-115">SUPPRESS_RECEIPT : Un rapport de lecture en attente doit être annulé si un rapport de lecture a été demandé et cet appel remplace l’état du message non lu à lire.</span><span class="sxs-lookup"><span data-stu-id="f466a-115">SUPPRESS_RECEIPT: A pending read report should be canceled if a read report had been requested and this call changes the state of the message from unread to read.</span></span> <span data-ttu-id="f466a-116">Si cet appel ne modifie pas l’état du message, le fournisseur de banque de message peut ignorer cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="f466a-116">If this call does not change the state of the message, the message store provider can ignore this flag.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f466a-117">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="f466a-117">Return value</span></span>

<span data-ttu-id="f466a-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="f466a-118">S_OK</span></span> 
  
> <span data-ttu-id="f466a-119">Indicateur de lecture du message a été configurée ou désactivée.</span><span class="sxs-lookup"><span data-stu-id="f466a-119">The message's read flag has been successfully set or cleared.</span></span>
    
<span data-ttu-id="f466a-120">MAPI_E_NO_SUPPRESS</span><span class="sxs-lookup"><span data-stu-id="f466a-120">MAPI_E_NO_SUPPRESS</span></span> 
  
> <span data-ttu-id="f466a-121">Le fournisseur de banque de messages ne gère pas la suppression des rapports de lecture.</span><span class="sxs-lookup"><span data-stu-id="f466a-121">The message store provider does not support the suppression of read reports.</span></span>
    
<span data-ttu-id="f466a-122">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f466a-122">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="f466a-123">Une des combinaisons d’indicateurs suivants est définie dans le paramètre _ulFlags_ :</span><span class="sxs-lookup"><span data-stu-id="f466a-123">One of the following combinations of flags is set in the  _ulFlags_ parameter:</span></span> 
    
   - <span data-ttu-id="f466a-124">SUPPRESS_RECEIPT | CLEAR_READ_FLAG</span><span class="sxs-lookup"><span data-stu-id="f466a-124">SUPPRESS_RECEIPT | CLEAR_READ_FLAG</span></span> 
    
   - <span data-ttu-id="f466a-125">SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span><span class="sxs-lookup"><span data-stu-id="f466a-125">SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span></span>
    
   - <span data-ttu-id="f466a-126">CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span><span class="sxs-lookup"><span data-stu-id="f466a-126">CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f466a-127">Remarques</span><span class="sxs-lookup"><span data-stu-id="f466a-127">Remarks</span></span>

<span data-ttu-id="f466a-128">La méthode **IMessage::SetReadFlag** définit ou efface l’indicateur MSGFLAG_READ du message dans la propriété **PR_MESSAGE_FLAGS** et les appels [IMAPIProp::SaveChanges](imapiprop-savechanges.md) pour enregistrer le message.</span><span class="sxs-lookup"><span data-stu-id="f466a-128">The **IMessage::SetReadFlag** method sets or clears the message's MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** property and calls [IMAPIProp::SaveChanges](imapiprop-savechanges.md) to save the message.</span></span> <span data-ttu-id="f466a-129">Définition de l’indicateur MSGFLAG_READ marque un message comme ayant été lu, ce qui n’indique pas nécessairement que le destinataire a lu réellement le message.</span><span class="sxs-lookup"><span data-stu-id="f466a-129">Setting the MSGFLAG_READ flag marks a message as having been read, which does not necessarily indicate that the intended recipient has actually read the message.</span></span> 
  
<span data-ttu-id="f466a-130">**SetReadFlags** gère également l’envoi des rapports de lecture.</span><span class="sxs-lookup"><span data-stu-id="f466a-130">**SetReadFlags** also manages the sending of read reports.</span></span> <span data-ttu-id="f466a-131">Un rapport de lecture est envoyé uniquement si l’expéditeur a demandé une.</span><span class="sxs-lookup"><span data-stu-id="f466a-131">A read report is sent only if the sender has requested one.</span></span> 
  
<span data-ttu-id="f466a-132">L’indicateur de lecture ne peut pas être modifié pour :</span><span class="sxs-lookup"><span data-stu-id="f466a-132">The read flag cannot be altered for:</span></span>
  
- <span data-ttu-id="f466a-133">Messages qui n’existent pas.</span><span class="sxs-lookup"><span data-stu-id="f466a-133">Messages that do not exist.</span></span>
    
- <span data-ttu-id="f466a-134">Les messages qui ont été déplacés vers un autre emplacement.</span><span class="sxs-lookup"><span data-stu-id="f466a-134">Messages that have been moved elsewhere.</span></span>
    
- <span data-ttu-id="f466a-135">Messages qui sont ouvertes avec l’autorisation de lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="f466a-135">Messages that are open with read/write permission.</span></span>
    
- <span data-ttu-id="f466a-136">Messages qui sont actuellement envoyées.</span><span class="sxs-lookup"><span data-stu-id="f466a-136">Messages that are currently submitted.</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="f466a-137">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="f466a-137">Notes to callers</span></span>

<span data-ttu-id="f466a-138">Si aucun des indicateurs sont définies dans le paramètre _ulFlags_ , les règles suivantes s’appliquent :</span><span class="sxs-lookup"><span data-stu-id="f466a-138">If none of the flags are set in the  _ulFlags_ parameter, the following rules apply:</span></span> 
  
- <span data-ttu-id="f466a-139">Si MSGFLAG_READ est déjà défini, ne faites rien.</span><span class="sxs-lookup"><span data-stu-id="f466a-139">If MSGFLAG_READ is already set, do nothing.</span></span>
    
- <span data-ttu-id="f466a-140">Si MSGFLAG_READ n’est pas définie, définissez-la et envoyer les en attente de rapports de lecture si la valeur de la propriété **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="f466a-140">If MSGFLAG_READ is not set, set it and send any pending read reports if the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property is set.</span></span>
    
<span data-ttu-id="f466a-141">Si les indicateurs GENERATE_RECEIPT_ONLY et SUPPRESS_RECEIPT sont définies, la PR_READ_RECEIPT_REQUESTED bit, s’il est défini, doit être désactivée et un rapport de lecture ne doit pas être envoyé.</span><span class="sxs-lookup"><span data-stu-id="f466a-141">If both the SUPPRESS_RECEIPT and GENERATE_RECEIPT_ONLY flags are set, the PR_READ_RECEIPT_REQUESTED bit, if set, should be cleared and a read report should not be sent.</span></span>
  
<span data-ttu-id="f466a-142">Lorsque l’indicateur SUPPRESS_RECEIPT est défini :</span><span class="sxs-lookup"><span data-stu-id="f466a-142">When the SUPPRESS_RECEIPT flag is set:</span></span>
  
- <span data-ttu-id="f466a-143">Si MSGFLAG_READ est déjà défini, ne faites rien.</span><span class="sxs-lookup"><span data-stu-id="f466a-143">If MSGFLAG_READ is already set, do nothing.</span></span> 
    
- <span data-ttu-id="f466a-144">Si MSGFLAG_READ n’est pas définie, définissez-la et annuler les en attente de rapports de lecture.</span><span class="sxs-lookup"><span data-stu-id="f466a-144">If MSGFLAG_READ is not set, set it and cancel any pending read reports.</span></span>
    
<span data-ttu-id="f466a-145">Lorsque l’indicateur CLEAR_READ_FLAG est défini, effacer l’indicateur MSGFLAG_READ dans la propriété **PR_MESSAGE_FLAGS** du chaque message et ne pas envoyer des rapports de lecture.</span><span class="sxs-lookup"><span data-stu-id="f466a-145">When the CLEAR_READ_FLAG flag is set, clear the MSGFLAG_READ flag in each message's **PR_MESSAGE_FLAGS** property and do not send any read reports.</span></span> 
  
<span data-ttu-id="f466a-146">Lorsque l’indicateur GENERATE_RECEIPT_ONLY est défini, envoyer des rapports de lecture en attente.</span><span class="sxs-lookup"><span data-stu-id="f466a-146">When the GENERATE_RECEIPT_ONLY flag is set, send any pending read reports.</span></span> <span data-ttu-id="f466a-147">Ne pas définir ou effacer MSGFLAG_READ.</span><span class="sxs-lookup"><span data-stu-id="f466a-147">Do not set or clear MSGFLAG_READ.</span></span>
  
<span data-ttu-id="f466a-148">Lorsque les indicateurs GENERATE_RECEIPT_ONLY et SUPPRESS_RECEIPT sont définis, définir la propriété PR_READ_RECEIPT_REQUESTED sur FALSE si elle est définie et ne pas envoyer un rapport de lecture.</span><span class="sxs-lookup"><span data-stu-id="f466a-148">When both the SUPPRESS_RECEIPT and GENERATE_RECEIPT_ONLY flags are set, set the PR_READ_RECEIPT_REQUESTED property to FALSE if it is set and do not send a read report.</span></span>
  
<span data-ttu-id="f466a-149">Vous pouvez optimiser le comportement de rapport en supprimant la génération de rapports de lecture sous certaines conditions.</span><span class="sxs-lookup"><span data-stu-id="f466a-149">You can optimize report behavior by suppressing the generation of read reports under certain conditions.</span></span> <span data-ttu-id="f466a-150">Toutefois, si vous ne prennent pas en charge la suppression des rapports et un client appelle **SetReadFlag** avec l’indicateur SUPPRESS_RECEIPT, retourner MAPI_E_NO_SUPPRESS.</span><span class="sxs-lookup"><span data-stu-id="f466a-150">However, if you do not support the suppression of reports and a client calls **SetReadFlag** with the SUPPRESS_RECEIPT flag set, return MAPI_E_NO_SUPPRESS.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f466a-151">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="f466a-151">MFCMAPI reference</span></span>

<span data-ttu-id="f466a-152">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="f466a-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f466a-153">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="f466a-153">**File**</span></span>|<span data-ttu-id="f466a-154">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="f466a-154">**Function**</span></span>|<span data-ttu-id="f466a-155">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="f466a-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f466a-156">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="f466a-156">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="f466a-157">CFolderDlg::OnSetReadFlag</span><span class="sxs-lookup"><span data-stu-id="f466a-157">CFolderDlg::OnSetReadFlag</span></span>  <br/> |<span data-ttu-id="f466a-158">MFCMAPI utilise la méthode **IMessage::SetReadFlag** pour définir des indicateurs de lecture sur les messages sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="f466a-158">MFCMAPI uses the **IMessage::SetReadFlag** method to set read flags on selected messages.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f466a-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f466a-159">See also</span></span>

- [<span data-ttu-id="f466a-160">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="f466a-160">IMAPIContainer::OpenEntry</span></span>](imapicontainer-openentry.md)  
- [<span data-ttu-id="f466a-161">IMAPIFolder::SetReadFlags</span><span class="sxs-lookup"><span data-stu-id="f466a-161">IMAPIFolder::SetReadFlags</span></span>](imapifolder-setreadflags.md)  
- [<span data-ttu-id="f466a-162">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="f466a-162">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)  
- [<span data-ttu-id="f466a-163">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="f466a-163">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md) 
- [<span data-ttu-id="f466a-164">Propriété canonique PidTagMessageFlags</span><span class="sxs-lookup"><span data-stu-id="f466a-164">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md) 
- [<span data-ttu-id="f466a-165">IMessage : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="f466a-165">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)
- [<span data-ttu-id="f466a-166">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="f466a-166">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

