---
title: IMessageSubmitMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.SubmitMessage
api_type:
- COM
ms.assetid: 9ce93469-c55d-48d1-9abb-a637716ed4f2
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 67c86f39898b4bd0c019b9b3095c9449e6e60b1b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567320"
---
# <a name="imessagesubmitmessage"></a><span data-ttu-id="0d33f-103">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="0d33f-103">IMessage::SubmitMessage</span></span>

  
  
<span data-ttu-id="0d33f-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0d33f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0d33f-105">Enregistre toutes les propriétés du message et marquer le message comme étant prêt à être envoyé.</span><span class="sxs-lookup"><span data-stu-id="0d33f-105">Saves all of the message's properties and marks the message as ready to be sent.</span></span>
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="0d33f-106">Param�tres</span><span class="sxs-lookup"><span data-stu-id="0d33f-106">Parameters</span></span>

 <span data-ttu-id="0d33f-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0d33f-107">_ulFlags_</span></span>
  
> <span data-ttu-id="0d33f-108">[in] Masque de bits d’indicateurs utilisés pour contrôler la façon dont un message est envoyé.</span><span class="sxs-lookup"><span data-stu-id="0d33f-108">[in] Bitmask of flags used to control how a message is submitted.</span></span> <span data-ttu-id="0d33f-109">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="0d33f-109">The following flag can be set:</span></span>
    
<span data-ttu-id="0d33f-110">FORCE_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="0d33f-110">FORCE_SUBMIT</span></span> 
  
> <span data-ttu-id="0d33f-111">MAPI doit envoyer le message immédiatement.</span><span class="sxs-lookup"><span data-stu-id="0d33f-111">MAPI should submit the message immediately.</span></span> <span data-ttu-id="0d33f-112">Cet indicateur n’est pas en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="0d33f-112">This flag is not currently in use.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0d33f-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0d33f-113">Return value</span></span>

<span data-ttu-id="0d33f-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="0d33f-114">S_OK</span></span> 
  
> <span data-ttu-id="0d33f-115">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="0d33f-115">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="0d33f-116">MAPI_E_NO_RECIPIENTS</span><span class="sxs-lookup"><span data-stu-id="0d33f-116">MAPI_E_NO_RECIPIENTS</span></span> 
  
> <span data-ttu-id="0d33f-117">Table des destinataires du message est vide.</span><span class="sxs-lookup"><span data-stu-id="0d33f-117">The message's recipient table is empty.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0d33f-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="0d33f-118">Remarks</span></span>

<span data-ttu-id="0d33f-119">La méthode **IMessage::SubmitMessage** marque un message comme prêts à être transmis.</span><span class="sxs-lookup"><span data-stu-id="0d33f-119">The **IMessage::SubmitMessage** method marks a message as ready to be transmitted.</span></span> <span data-ttu-id="0d33f-120">MAPI transmet les messages au système de messagerie sous-jacent dans l’ordre dans lequel ils sont marqués pour l’envoi.</span><span class="sxs-lookup"><span data-stu-id="0d33f-120">MAPI passes messages to the underlying messaging system in the order in which they are marked for sending.</span></span> <span data-ttu-id="0d33f-121">En raison de cette fonctionnalité, un message peut rester dans une banque de messages pendant un certain temps avant que le système de messagerie sous-jacent peut prendre la responsabilité de celui-ci.</span><span class="sxs-lookup"><span data-stu-id="0d33f-121">Because of this functionality, a message might stay in a message store for some time before the underlying messaging system can take responsibility for it.</span></span> <span data-ttu-id="0d33f-122">L’ordre de réception à la destination est le contrôle de votre système de messagerie sous-jacent et ne correspond pas nécessairement à l’ordre dans lequel les messages ont été envoyés.</span><span class="sxs-lookup"><span data-stu-id="0d33f-122">The order of receipt at the destination is in the underlying messaging system's control and does not necessarily match the order in which messages were sent.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="0d33f-123">Remarques à l’attention des responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="0d33f-123">Notes to implementers</span></span>

<span data-ttu-id="0d33f-124">Appelez la méthode de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) du message pour l’enregistrer, puis vérifiez la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) du message.</span><span class="sxs-lookup"><span data-stu-id="0d33f-124">Call the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to save it and then check the message's **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span> <span data-ttu-id="0d33f-125">Si l’indicateur MSGFLAG_RESEND est défini, appelez [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md).</span><span class="sxs-lookup"><span data-stu-id="0d33f-125">If the MSGFLAG_RESEND flag is set, call [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md).</span></span> <span data-ttu-id="0d33f-126">**PrepareSubmit** met à jour le type de destinataire et la propriété **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) pour tous les destinataires du message à renvoyer.</span><span class="sxs-lookup"><span data-stu-id="0d33f-126">**PrepareSubmit** updates the recipient type and **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property for all of the recipients in the resend message.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="0d33f-127">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="0d33f-127">Notes to callers</span></span>

<span data-ttu-id="0d33f-128">**SubmitMessage** retourne tous les pointeurs vers le message et ses messages associés sous-objets, dossiers, pièces jointes, flux, tableaux et ainsi de suite ne sont plus valides.</span><span class="sxs-lookup"><span data-stu-id="0d33f-128">When **SubmitMessage** returns, all pointers to the message and its associated subobjects messages, folders, attachments, streams, tables, and so on are no longer valid.</span></span> <span data-ttu-id="0d33f-129">MAPI ne permet pas d’opérations supplémentaires sur ces pointeurs, à l’exception de l’appel de leurs méthodes **IUnknown::Release** .</span><span class="sxs-lookup"><span data-stu-id="0d33f-129">MAPI does not permit any further operations on these pointers, except for calling their **IUnknown::Release** methods.</span></span> <span data-ttu-id="0d33f-130">MAPI est conçue pour qu’après avoir appelé **SubmitMessage** , vous devez libérer le message et tous les sous-objets.</span><span class="sxs-lookup"><span data-stu-id="0d33f-130">MAPI is designed such that after **SubmitMessage** is called, you should release the message and all associated subobjects.</span></span> <span data-ttu-id="0d33f-131">Toutefois, si **SubmitMessage** renvoie une valeur d’erreur indiquant les informations manquantes ou incorrectes, le message reste ouvert et les pointeurs restent valides.</span><span class="sxs-lookup"><span data-stu-id="0d33f-131">However, if **SubmitMessage** returns an error value indicating missing or invalid information, the message remains open and the pointers remain valid.</span></span> 
  
<span data-ttu-id="0d33f-132">Pour annuler une opération d’envoi, obtenir et de stocker un pointeur vers la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) du message avant l’envoi du message.</span><span class="sxs-lookup"><span data-stu-id="0d33f-132">To cancel a send operation, get and store a pointer to the message's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property before the message is submitted.</span></span> <span data-ttu-id="0d33f-133">Identificateur d’entrée d’un message est non valide après que le message a été envoyé, il est nécessaire pour l’enregistrer avant d’appeler **SubmitMessage**.</span><span class="sxs-lookup"><span data-stu-id="0d33f-133">Because a message's entry identifier is invalidated after the message has been submitted, it is necessary to save it before calling **SubmitMessage**.</span></span> <span data-ttu-id="0d33f-134">Pour annuler l’envoi, pointez sur le paramètre _lpEntryId_ cet identificateur d’entrée et appelez [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md).</span><span class="sxs-lookup"><span data-stu-id="0d33f-134">To cancel the send, point the  _lpEntryId_ parameter to this entry identifier and call [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="0d33f-135">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="0d33f-135">MFCMAPI reference</span></span>

<span data-ttu-id="0d33f-136">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="0d33f-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="0d33f-137">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="0d33f-137">**File**</span></span>|<span data-ttu-id="0d33f-138">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="0d33f-138">**Function**</span></span>|<span data-ttu-id="0d33f-139">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="0d33f-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0d33f-140">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="0d33f-140">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="0d33f-141">**CFolderDlg::OnSubmitMessage**</span><span class="sxs-lookup"><span data-stu-id="0d33f-141">**CFolderDlg::OnSubmitMessage**</span></span> <br/> |<span data-ttu-id="0d33f-142">MFCMAPI utilise la méthode **IMessage::SubmitMessage** pour envoyer le message sélectionné.</span><span class="sxs-lookup"><span data-stu-id="0d33f-142">MFCMAPI uses the **IMessage::SubmitMessage** method to submit the selected message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0d33f-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0d33f-143">See also</span></span>



[<span data-ttu-id="0d33f-144">IMsgStore::AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="0d33f-144">IMsgStore::AbortSubmit</span></span>](imsgstore-abortsubmit.md)
  
[<span data-ttu-id="0d33f-145">IMessage : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="0d33f-145">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)


[<span data-ttu-id="0d33f-146">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="0d33f-146">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

