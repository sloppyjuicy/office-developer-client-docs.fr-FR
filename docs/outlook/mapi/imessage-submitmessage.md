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
ms.openlocfilehash: 28786f483c4d2031c334d7b9697db7c5e627fe93
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437363"
---
# <a name="imessagesubmitmessage"></a><span data-ttu-id="1cd04-103">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="1cd04-103">IMessage::SubmitMessage</span></span>

  
  
<span data-ttu-id="1cd04-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1cd04-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1cd04-105">Enregistre toutes les propriétés du message et marque le message comme étant prêt à être envoyé.</span><span class="sxs-lookup"><span data-stu-id="1cd04-105">Saves all of the message's properties and marks the message as ready to be sent.</span></span>
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="1cd04-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1cd04-106">Parameters</span></span>

 <span data-ttu-id="1cd04-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1cd04-107">_ulFlags_</span></span>
  
> <span data-ttu-id="1cd04-108">dans Masque de des indicateurs utilisés pour contrôler le mode d'envoi d'un message.</span><span class="sxs-lookup"><span data-stu-id="1cd04-108">[in] Bitmask of flags used to control how a message is submitted.</span></span> <span data-ttu-id="1cd04-109">L'indicateur suivant peut être défini:</span><span class="sxs-lookup"><span data-stu-id="1cd04-109">The following flag can be set:</span></span>
    
<span data-ttu-id="1cd04-110">FORCE_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="1cd04-110">FORCE_SUBMIT</span></span> 
  
> <span data-ttu-id="1cd04-111">MAPI doit envoyer le message immédiatement.</span><span class="sxs-lookup"><span data-stu-id="1cd04-111">MAPI should submit the message immediately.</span></span> <span data-ttu-id="1cd04-112">Cet indicateur n'est pas en cours d'utilisation.</span><span class="sxs-lookup"><span data-stu-id="1cd04-112">This flag is not currently in use.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1cd04-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1cd04-113">Return value</span></span>

<span data-ttu-id="1cd04-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="1cd04-114">S_OK</span></span> 
  
> <span data-ttu-id="1cd04-115">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="1cd04-115">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="1cd04-116">MAPI_E_NO_RECIPIENTS</span><span class="sxs-lookup"><span data-stu-id="1cd04-116">MAPI_E_NO_RECIPIENTS</span></span> 
  
> <span data-ttu-id="1cd04-117">La table des destinataires du message est vide.</span><span class="sxs-lookup"><span data-stu-id="1cd04-117">The message's recipient table is empty.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1cd04-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="1cd04-118">Remarks</span></span>

<span data-ttu-id="1cd04-119">La méthode **IMessage:: SubmitMessage** marque un message comme étant prêt à être transmis.</span><span class="sxs-lookup"><span data-stu-id="1cd04-119">The **IMessage::SubmitMessage** method marks a message as ready to be transmitted.</span></span> <span data-ttu-id="1cd04-120">MAPI transmet des messages au système de messagerie sous-jacent dans l'ordre dans lequel ils sont marqués pour l'envoi.</span><span class="sxs-lookup"><span data-stu-id="1cd04-120">MAPI passes messages to the underlying messaging system in the order in which they are marked for sending.</span></span> <span data-ttu-id="1cd04-121">En raison de cette fonctionnalité, un message peut rester dans une banque de messages pendant un certain temps avant que le système de messagerie sous-jacent puisse le prendre en charge.</span><span class="sxs-lookup"><span data-stu-id="1cd04-121">Because of this functionality, a message might stay in a message store for some time before the underlying messaging system can take responsibility for it.</span></span> <span data-ttu-id="1cd04-122">L'ordre de réception à la destination se trouve dans le contrôle du système de messagerie sous-jacent et ne correspond pas nécessairement à l'ordre dans lequel les messages ont été envoyés.</span><span class="sxs-lookup"><span data-stu-id="1cd04-122">The order of receipt at the destination is in the underlying messaging system's control and does not necessarily match the order in which messages were sent.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="1cd04-123">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="1cd04-123">Notes to implementers</span></span>

<span data-ttu-id="1cd04-124">Appelez la méthode [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) du message pour l'enregistrer, puis vérifiez la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) du message.</span><span class="sxs-lookup"><span data-stu-id="1cd04-124">Call the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to save it and then check the message's **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span> <span data-ttu-id="1cd04-125">Si l'indicateur MSGFLAG_RESEND est défini, appelez [IMAPISupport::P reparesubmit](imapisupport-preparesubmit.md).</span><span class="sxs-lookup"><span data-stu-id="1cd04-125">If the MSGFLAG_RESEND flag is set, call [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md).</span></span> <span data-ttu-id="1cd04-126">**PrepareSubmit** met à jour le type de destinataire et la propriété **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) pour tous les destinataires dans le message de renvoi.</span><span class="sxs-lookup"><span data-stu-id="1cd04-126">**PrepareSubmit** updates the recipient type and **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property for all of the recipients in the resend message.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="1cd04-127">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="1cd04-127">Notes to callers</span></span>

<span data-ttu-id="1cd04-128">Lorsque **SubmitMessage** renvoie, tous les pointeurs vers le message et ses sous-objets associés les messages, les dossiers, les pièces jointes, les flux, les tables, etc., ne sont plus valides.</span><span class="sxs-lookup"><span data-stu-id="1cd04-128">When **SubmitMessage** returns, all pointers to the message and its associated subobjects messages, folders, attachments, streams, tables, and so on are no longer valid.</span></span> <span data-ttu-id="1cd04-129">MAPI n'autorise pas d'autres opérations sur ces pointeurs, à l'exception de l'appel de leurs méthodes **IUnknown:: Release** .</span><span class="sxs-lookup"><span data-stu-id="1cd04-129">MAPI does not permit any further operations on these pointers, except for calling their **IUnknown::Release** methods.</span></span> <span data-ttu-id="1cd04-130">MAPI est conçu de telle sorte qu'après l'appel de **SubmitMessage** , vous devez libérer le message et tous les sous-objets associés.</span><span class="sxs-lookup"><span data-stu-id="1cd04-130">MAPI is designed such that after **SubmitMessage** is called, you should release the message and all associated subobjects.</span></span> <span data-ttu-id="1cd04-131">Toutefois, si **SubmitMessage** renvoie une valeur d'erreur indiquant que les informations sont manquantes ou incorrectes, le message reste ouvert et les pointeurs restent valides.</span><span class="sxs-lookup"><span data-stu-id="1cd04-131">However, if **SubmitMessage** returns an error value indicating missing or invalid information, the message remains open and the pointers remain valid.</span></span> 
  
<span data-ttu-id="1cd04-132">Pour annuler une opération d'envoi, récupérez et stockez un pointeur vers la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) du message avant l'envoi du message.</span><span class="sxs-lookup"><span data-stu-id="1cd04-132">To cancel a send operation, get and store a pointer to the message's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property before the message is submitted.</span></span> <span data-ttu-id="1cd04-133">Étant donné que l'identificateur d'entrée d'un message n'est pas valide une fois que le message a été envoyé, il est nécessaire de l'enregistrer avant d'appeler **SubmitMessage**.</span><span class="sxs-lookup"><span data-stu-id="1cd04-133">Because a message's entry identifier is invalidated after the message has been submitted, it is necessary to save it before calling **SubmitMessage**.</span></span> <span data-ttu-id="1cd04-134">Pour annuler l'envoi, pointez le paramètre _lpEntryId_ vers cet identificateur d'entrée et appelez [IMsgStore:: AbortSubmit](imsgstore-abortsubmit.md).</span><span class="sxs-lookup"><span data-stu-id="1cd04-134">To cancel the send, point the  _lpEntryId_ parameter to this entry identifier and call [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1cd04-135">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="1cd04-135">MFCMAPI reference</span></span>

<span data-ttu-id="1cd04-136">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="1cd04-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1cd04-137">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="1cd04-137">**File**</span></span>|<span data-ttu-id="1cd04-138">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="1cd04-138">**Function**</span></span>|<span data-ttu-id="1cd04-139">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="1cd04-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1cd04-140">FolderDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="1cd04-140">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="1cd04-141">**CFolderDlg:: OnSubmitMessage**</span><span class="sxs-lookup"><span data-stu-id="1cd04-141">**CFolderDlg::OnSubmitMessage**</span></span> <br/> |<span data-ttu-id="1cd04-142">MFCMAPI utilise la méthode **IMessage:: SubmitMessage** pour envoyer le message sélectionné.</span><span class="sxs-lookup"><span data-stu-id="1cd04-142">MFCMAPI uses the **IMessage::SubmitMessage** method to submit the selected message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1cd04-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1cd04-143">See also</span></span>



[<span data-ttu-id="1cd04-144">IMsgStore::AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="1cd04-144">IMsgStore::AbortSubmit</span></span>](imsgstore-abortsubmit.md)
  
[<span data-ttu-id="1cd04-145">IMessage : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="1cd04-145">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)


[<span data-ttu-id="1cd04-146">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="1cd04-146">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

