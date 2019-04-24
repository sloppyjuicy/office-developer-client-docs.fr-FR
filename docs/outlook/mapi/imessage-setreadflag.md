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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 874dba4aa18190792a52e29064155f5afa0ef44d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349265"
---
# <a name="imessagesetreadflag"></a><span data-ttu-id="64d1e-103">IMessage::SetReadFlag</span><span class="sxs-lookup"><span data-stu-id="64d1e-103">IMessage::SetReadFlag</span></span>

<span data-ttu-id="64d1e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="64d1e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="64d1e-105">Définit ou efface l'indicateur MSGFLAG_READ dans la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) du message et gère l'envoi des rapports de lecture.</span><span class="sxs-lookup"><span data-stu-id="64d1e-105">Sets or clears the MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of the message and manages the sending of read reports.</span></span>
  
```cpp
HRESULT SetReadFlag(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="64d1e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="64d1e-106">Parameters</span></span>

<span data-ttu-id="64d1e-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="64d1e-107">_ulFlags_</span></span>
  
> <span data-ttu-id="64d1e-108">dans Masque de réinitialisation des indicateurs qui contrôlent le paramètre de l'indicateur de lecture d'un message qui est l'indicateur MSGFLAG_READ du message dans sa propriété **PR_MESSAGE_FLAGS** et le traitement des rapports de lecture.</span><span class="sxs-lookup"><span data-stu-id="64d1e-108">[in] Bitmask of flags that controls the setting of a message's read flag that is, the message's MSGFLAG_READ flag in its **PR_MESSAGE_FLAGS** property and the processing of read reports.</span></span> <span data-ttu-id="64d1e-109">Les indicateurs suivants peuvent être définis:</span><span class="sxs-lookup"><span data-stu-id="64d1e-109">The following flags can be set:</span></span> 
    
  - <span data-ttu-id="64d1e-110">CLEAR_READ_FLAG: l'indicateur MSGFLAG_READ doit être effacé dans **PR_MESSAGE_FLAGS** et aucun rapport de lecture ne doit être envoyé.</span><span class="sxs-lookup"><span data-stu-id="64d1e-110">CLEAR_READ_FLAG: The MSGFLAG_READ flag should be cleared in **PR_MESSAGE_FLAGS** and no read report should be sent.</span></span> 
      
  - <span data-ttu-id="64d1e-111">CLEAR_NRN_PENDING: l'indicateur MSGFLAG_NRN_PENDING doit être effacé dans **PR_MESSAGE_FLAGS** et un rapport de non-lecture ne doit pas être envoyé.</span><span class="sxs-lookup"><span data-stu-id="64d1e-111">CLEAR_NRN_PENDING: The MSGFLAG_NRN_PENDING flag should be cleared in **PR_MESSAGE_FLAGS** and a non-read report should not be sent.</span></span> 
      
  - <span data-ttu-id="64d1e-112">CLEAR_RN_PENDING: l'indicateur MSGFLAG_RN_PENDING doit être effacé dans **PR_MESSAGE_FLAGS** et aucun rapport de lecture ne doit être envoyé.</span><span class="sxs-lookup"><span data-stu-id="64d1e-112">CLEAR_RN_PENDING: The MSGFLAG_RN_PENDING flag should be cleared in **PR_MESSAGE_FLAGS** and no read report should be sent.</span></span> 
      
  - <span data-ttu-id="64d1e-113">GENERATE_RECEIPT_ONLY: un rapport de lecture doit être envoyé s'il en est en attente, mais il ne doit y avoir aucune modification dans l'état de l'indicateur MSGFLAG_READ.</span><span class="sxs-lookup"><span data-stu-id="64d1e-113">GENERATE_RECEIPT_ONLY: A read report should be sent if one is pending, but there should be no change in the state of the MSGFLAG_READ flag.</span></span>
      
  - <span data-ttu-id="64d1e-114">MAPI_DEFERRED_ERRORS: permet à **SetReadFlag** de renvoyer correctement, éventuellement avant la fin de l'opération.</span><span class="sxs-lookup"><span data-stu-id="64d1e-114">MAPI_DEFERRED_ERRORS: Allows **SetReadFlag** to return successfully, possibly before the operation has completed.</span></span> 
      
  - <span data-ttu-id="64d1e-115">SUPPRESS_RECEIPT: un rapport de lecture en attente doit être annulé si un rapport de lecture a été demandé et que cet appel change l'état du message de non lu en lecture.</span><span class="sxs-lookup"><span data-stu-id="64d1e-115">SUPPRESS_RECEIPT: A pending read report should be canceled if a read report had been requested and this call changes the state of the message from unread to read.</span></span> <span data-ttu-id="64d1e-116">Si cet appel ne modifie pas l'état du message, le fournisseur de banque de messages peut ignorer cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="64d1e-116">If this call does not change the state of the message, the message store provider can ignore this flag.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="64d1e-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="64d1e-117">Return value</span></span>

<span data-ttu-id="64d1e-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="64d1e-118">S_OK</span></span> 
  
> <span data-ttu-id="64d1e-119">L'indicateur de lecture du message a été correctement défini ou désactivé.</span><span class="sxs-lookup"><span data-stu-id="64d1e-119">The message's read flag has been successfully set or cleared.</span></span>
    
<span data-ttu-id="64d1e-120">MAPI_E_NO_SUPPRESS</span><span class="sxs-lookup"><span data-stu-id="64d1e-120">MAPI_E_NO_SUPPRESS</span></span> 
  
> <span data-ttu-id="64d1e-121">Le fournisseur de banque de messages ne prend pas en charge la suppression des rapports lus.</span><span class="sxs-lookup"><span data-stu-id="64d1e-121">The message store provider does not support the suppression of read reports.</span></span>
    
<span data-ttu-id="64d1e-122">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="64d1e-122">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="64d1e-123">L'une des combinaisons d'indicateurs suivantes est définie dans le paramètre _ulFlags_ :</span><span class="sxs-lookup"><span data-stu-id="64d1e-123">One of the following combinations of flags is set in the  _ulFlags_ parameter:</span></span> 
    
   - <span data-ttu-id="64d1e-124">SUPPRESS_RECEIPT | CLEAR_READ_FLAG</span><span class="sxs-lookup"><span data-stu-id="64d1e-124">SUPPRESS_RECEIPT | CLEAR_READ_FLAG</span></span> 
    
   - <span data-ttu-id="64d1e-125">SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span><span class="sxs-lookup"><span data-stu-id="64d1e-125">SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span></span>
    
   - <span data-ttu-id="64d1e-126">CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span><span class="sxs-lookup"><span data-stu-id="64d1e-126">CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span></span>
    
## <a name="remarks"></a><span data-ttu-id="64d1e-127">Remarques</span><span class="sxs-lookup"><span data-stu-id="64d1e-127">Remarks</span></span>

<span data-ttu-id="64d1e-128">La méthode **IMessage:: SetReadFlag** définit ou efface l'indicateur MSGFLAG_READ du message dans la propriété **PR_MESSAGE_FLAGS** et appelle [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) pour enregistrer le message.</span><span class="sxs-lookup"><span data-stu-id="64d1e-128">The **IMessage::SetReadFlag** method sets or clears the message's MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** property and calls [IMAPIProp::SaveChanges](imapiprop-savechanges.md) to save the message.</span></span> <span data-ttu-id="64d1e-129">La définition de l'indicateur MSGFLAG_READ marque un message comme lu, ce qui n'indique pas nécessairement que le destinataire concerné a effectivement lu le message.</span><span class="sxs-lookup"><span data-stu-id="64d1e-129">Setting the MSGFLAG_READ flag marks a message as having been read, which does not necessarily indicate that the intended recipient has actually read the message.</span></span> 
  
<span data-ttu-id="64d1e-130">**SetReadFlags** gère également l'envoi des rapports de lecture.</span><span class="sxs-lookup"><span data-stu-id="64d1e-130">**SetReadFlags** also manages the sending of read reports.</span></span> <span data-ttu-id="64d1e-131">Un rapport de lecture est envoyé uniquement si l'expéditeur en a demandé un.</span><span class="sxs-lookup"><span data-stu-id="64d1e-131">A read report is sent only if the sender has requested one.</span></span> 
  
<span data-ttu-id="64d1e-132">L'indicateur de lecture ne peut pas être modifié pour:</span><span class="sxs-lookup"><span data-stu-id="64d1e-132">The read flag cannot be altered for:</span></span>
  
- <span data-ttu-id="64d1e-133">Messages qui n'existent pas.</span><span class="sxs-lookup"><span data-stu-id="64d1e-133">Messages that do not exist.</span></span>
    
- <span data-ttu-id="64d1e-134">Messages qui ont été déplacés ailleurs.</span><span class="sxs-lookup"><span data-stu-id="64d1e-134">Messages that have been moved elsewhere.</span></span>
    
- <span data-ttu-id="64d1e-135">Messages ouverts avec une autorisation en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="64d1e-135">Messages that are open with read/write permission.</span></span>
    
- <span data-ttu-id="64d1e-136">Messages actuellement envoyés.</span><span class="sxs-lookup"><span data-stu-id="64d1e-136">Messages that are currently submitted.</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="64d1e-137">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="64d1e-137">Notes to callers</span></span>

<span data-ttu-id="64d1e-138">Si aucun des indicateurs n'est défini dans le paramètre _ulFlags_ , les règles suivantes s'appliquent:</span><span class="sxs-lookup"><span data-stu-id="64d1e-138">If none of the flags are set in the  _ulFlags_ parameter, the following rules apply:</span></span> 
  
- <span data-ttu-id="64d1e-139">Si MSGFLAG_READ est déjà défini, ne faites rien.</span><span class="sxs-lookup"><span data-stu-id="64d1e-139">If MSGFLAG_READ is already set, do nothing.</span></span>
    
- <span data-ttu-id="64d1e-140">Si MSGFLAG_READ n'est pas défini, définissez-le et envoyez les rapports de lecture en attente si la propriété **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) est définie.</span><span class="sxs-lookup"><span data-stu-id="64d1e-140">If MSGFLAG_READ is not set, set it and send any pending read reports if the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property is set.</span></span>
    
<span data-ttu-id="64d1e-141">Si les deux indicateurs SUPPRESS_RECEIPT et GENERATE_RECEIPT_ONLY sont définis, le bit PR_READ_RECEIPT_REQUESTED, s'il est défini, doit être effacé et un rapport de lecture ne doit pas être envoyé.</span><span class="sxs-lookup"><span data-stu-id="64d1e-141">If both the SUPPRESS_RECEIPT and GENERATE_RECEIPT_ONLY flags are set, the PR_READ_RECEIPT_REQUESTED bit, if set, should be cleared and a read report should not be sent.</span></span>
  
<span data-ttu-id="64d1e-142">Lorsque l'indicateur SUPPRESS_RECEIPT est défini:</span><span class="sxs-lookup"><span data-stu-id="64d1e-142">When the SUPPRESS_RECEIPT flag is set:</span></span>
  
- <span data-ttu-id="64d1e-143">Si MSGFLAG_READ est déjà défini, ne faites rien.</span><span class="sxs-lookup"><span data-stu-id="64d1e-143">If MSGFLAG_READ is already set, do nothing.</span></span> 
    
- <span data-ttu-id="64d1e-144">Si MSGFLAG_READ n'est pas défini, définissez-le et annulez tous les rapports de lecture en attente.</span><span class="sxs-lookup"><span data-stu-id="64d1e-144">If MSGFLAG_READ is not set, set it and cancel any pending read reports.</span></span>
    
<span data-ttu-id="64d1e-145">Lorsque l'indicateur CLEAR_READ_FLAG est défini, effacez l'indicateur MSGFLAG_READ dans la propriété **PR_MESSAGE_FLAGS** de chaque message et n'envoyez aucun rapport de lecture.</span><span class="sxs-lookup"><span data-stu-id="64d1e-145">When the CLEAR_READ_FLAG flag is set, clear the MSGFLAG_READ flag in each message's **PR_MESSAGE_FLAGS** property and do not send any read reports.</span></span> 
  
<span data-ttu-id="64d1e-146">Lorsque l'indicateur GENERATE_RECEIPT_ONLY est défini, envoyez tous les rapports de lecture en attente.</span><span class="sxs-lookup"><span data-stu-id="64d1e-146">When the GENERATE_RECEIPT_ONLY flag is set, send any pending read reports.</span></span> <span data-ttu-id="64d1e-147">Ne définissez pas MSGFLAG_READ.</span><span class="sxs-lookup"><span data-stu-id="64d1e-147">Do not set or clear MSGFLAG_READ.</span></span>
  
<span data-ttu-id="64d1e-148">Lorsque les deux indicateurs SUPPRESS_RECEIPT et GENERATE_RECEIPT_ONLY sont définis, affectez la valeur FALSe à la propriété PR_READ_RECEIPT_REQUESTED si elle est définie et que vous ne souhaitez pas envoyer de rapport de lecture.</span><span class="sxs-lookup"><span data-stu-id="64d1e-148">When both the SUPPRESS_RECEIPT and GENERATE_RECEIPT_ONLY flags are set, set the PR_READ_RECEIPT_REQUESTED property to FALSE if it is set and do not send a read report.</span></span>
  
<span data-ttu-id="64d1e-149">Vous pouvez optimiser le comportement de rapport en supprimant la génération de rapports en lecture dans certaines conditions.</span><span class="sxs-lookup"><span data-stu-id="64d1e-149">You can optimize report behavior by suppressing the generation of read reports under certain conditions.</span></span> <span data-ttu-id="64d1e-150">Toutefois, si vous ne prenez pas en charge la suppression des rapports et qu'un client appelle **SetReadFlag** avec l'indicateur SUPPRESS_RECEIPT défini, retournez MAPI_E_NO_SUPPRESS.</span><span class="sxs-lookup"><span data-stu-id="64d1e-150">However, if you do not support the suppression of reports and a client calls **SetReadFlag** with the SUPPRESS_RECEIPT flag set, return MAPI_E_NO_SUPPRESS.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="64d1e-151">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="64d1e-151">MFCMAPI reference</span></span>

<span data-ttu-id="64d1e-152">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="64d1e-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="64d1e-153">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="64d1e-153">**File**</span></span>|<span data-ttu-id="64d1e-154">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="64d1e-154">**Function**</span></span>|<span data-ttu-id="64d1e-155">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="64d1e-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="64d1e-156">FolderDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="64d1e-156">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="64d1e-157">CFolderDlg:: OnSetReadFlag</span><span class="sxs-lookup"><span data-stu-id="64d1e-157">CFolderDlg::OnSetReadFlag</span></span>  <br/> |<span data-ttu-id="64d1e-158">MFCMAPI utilise la méthode **IMessage:: SetReadFlag** pour définir des indicateurs de lecture sur les messages sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="64d1e-158">MFCMAPI uses the **IMessage::SetReadFlag** method to set read flags on selected messages.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="64d1e-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="64d1e-159">See also</span></span>

- [<span data-ttu-id="64d1e-160">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="64d1e-160">IMAPIContainer::OpenEntry</span></span>](imapicontainer-openentry.md)  
- [<span data-ttu-id="64d1e-161">IMAPIFolder::SetReadFlags</span><span class="sxs-lookup"><span data-stu-id="64d1e-161">IMAPIFolder::SetReadFlags</span></span>](imapifolder-setreadflags.md)  
- [<span data-ttu-id="64d1e-162">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="64d1e-162">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)  
- [<span data-ttu-id="64d1e-163">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="64d1e-163">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md) 
- [<span data-ttu-id="64d1e-164">Propriété canonique PidTagMessageFlags</span><span class="sxs-lookup"><span data-stu-id="64d1e-164">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md) 
- [<span data-ttu-id="64d1e-165">IMessage : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="64d1e-165">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)
- [<span data-ttu-id="64d1e-166">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="64d1e-166">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

