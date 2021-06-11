---
title: IXPLogonStartMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.StartMessage
api_type:
- COM
ms.assetid: 83c349f7-dcac-4268-befe-fb2bc0cd9c50
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 00273d5572fa0c12a9501a1620db11ea087fd5d1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427604"
---
# <a name="ixplogonstartmessage"></a><span data-ttu-id="4bd0b-103">IXPLogon::StartMessage</span><span class="sxs-lookup"><span data-stu-id="4bd0b-103">IXPLogon::StartMessage</span></span>

  
  
<span data-ttu-id="4bd0b-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4bd0b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4bd0b-105">Lance le transfert d’un message entrant du fournisseur de transport vers lepooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="4bd0b-105">Initiates the transfer of an inbound message from the transport provider to the MAPI spooler.</span></span>
  
```cpp
HRESULT StartMessage(
  ULONG ulFlags,
  LPMESSAGE lpMessage,
  ULONG FAR * lpulMsgRef
);
```

## <a name="parameters"></a><span data-ttu-id="4bd0b-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="4bd0b-106">Parameters</span></span>

 <span data-ttu-id="4bd0b-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4bd0b-107">_ulFlags_</span></span>
  
> <span data-ttu-id="4bd0b-108">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="4bd0b-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="4bd0b-109">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="4bd0b-109">_lpMessage_</span></span>
  
> <span data-ttu-id="4bd0b-110">[in] Pointeur vers un objet de message (représentant le message entrant) qui dispose d’une autorisation de lecture/écriture, qui est utilisé par le fournisseur de transport pour accéder à ce message et le manipuler.</span><span class="sxs-lookup"><span data-stu-id="4bd0b-110">[in] A pointer to a message object (representing the inbound message) that has read/write permission, which is used by the transport provider to access and manipulate that message.</span></span> <span data-ttu-id="4bd0b-111">Cet objet reste valide jusqu’à ce que le fournisseur de transport retourne de l’appel à **IXPLogon::StartMessage**.</span><span class="sxs-lookup"><span data-stu-id="4bd0b-111">This object remains valid until after the transport provider returns from the call to **IXPLogon::StartMessage**.</span></span>
    
 <span data-ttu-id="4bd0b-112">_lpulMsgRef_</span><span class="sxs-lookup"><span data-stu-id="4bd0b-112">_lpulMsgRef_</span></span>
  
> <span data-ttu-id="4bd0b-113">[out] Pointeur vers une valeur de référence affectée au message.</span><span class="sxs-lookup"><span data-stu-id="4bd0b-113">[out] A pointer to a reference value assigned to the message.</span></span> <span data-ttu-id="4bd0b-114">Lepooler MAPI initialise cette valeur sur 1 avant de retourner le pointeur au fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="4bd0b-114">The MAPI spooler initializes this value to 1 before it returns the pointer to the transport provider.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4bd0b-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4bd0b-115">Return value</span></span>

<span data-ttu-id="4bd0b-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="4bd0b-116">S_OK</span></span> 
  
> <span data-ttu-id="4bd0b-117">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="4bd0b-117">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4bd0b-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="4bd0b-118">Remarks</span></span>

<span data-ttu-id="4bd0b-119">Lepooler MAPI appelle la méthode **IXPLogon::StartMessage** pour initier le transfert d’un message entrant du fournisseur de transport vers lepooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="4bd0b-119">The MAPI spooler calls the **IXPLogon::StartMessage** method to initiate the transfer of an inbound message from the transport provider to the MAPI spooler.</span></span> <span data-ttu-id="4bd0b-120">Avant que le fournisseur de transport commence à utiliser le message pointé par _lpMessage,_ il doit stocker une référence de message dans le paramètre _lpulMsgRef_ pour une utilisation potentielle par un appel à la méthode [IXPLogon::TransportNotify.](ixplogon-transportnotify.md)</span><span class="sxs-lookup"><span data-stu-id="4bd0b-120">Before the transport provider starts to use the message pointed to by  _lpMessage_, it should store a message reference in the  _lpulMsgRef_ parameter for potential use by a call to the [IXPLogon::TransportNotify](ixplogon-transportnotify.md) method.</span></span> 
  
<span data-ttu-id="4bd0b-121">Lors **d’un appel StartMessage,** lepooler MAPI traite les méthodes pour les objets ouverts lors du transfert du message et traite également les pièces jointes.</span><span class="sxs-lookup"><span data-stu-id="4bd0b-121">During a **StartMessage** call, the MAPI spooler processes methods for objects opened during the transfer of the message, and it also processes any attachments.</span></span> <span data-ttu-id="4bd0b-122">Ce traitement peut prendre beaucoup de temps.</span><span class="sxs-lookup"><span data-stu-id="4bd0b-122">This processing can take a long time.</span></span> <span data-ttu-id="4bd0b-123">Les fournisseurs de transport peuvent appeler fréquemment la fonction de rappel [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) pour lepooler MAPI pendant ce traitement pour libérer du temps processeur pour d’autres tâches système.</span><span class="sxs-lookup"><span data-stu-id="4bd0b-123">Transport providers can call the [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) callback function for the MAPI spooler frequently during this processing to release CPU time for other system tasks.</span></span> 
  
<span data-ttu-id="4bd0b-124">Tous les destinataires de la table des destinataires créée par le fournisseur de transport pour le message doivent contenir toutes les propriétés d’adressare requises.</span><span class="sxs-lookup"><span data-stu-id="4bd0b-124">All recipients in the recipient table that the transport provider creates for the message must contain all required addressing properties.</span></span> <span data-ttu-id="4bd0b-125">Si nécessaire, le fournisseur peut construire un destinataire personnalisé pour représenter un destinataire particulier.</span><span class="sxs-lookup"><span data-stu-id="4bd0b-125">If necessary, the provider can construct a custom recipient to represent a particular recipient.</span></span> <span data-ttu-id="4bd0b-126">Toutefois, si le fournisseur peut produire une entrée de destinataire qui inclut plus d’informations, il doit le faire.</span><span class="sxs-lookup"><span data-stu-id="4bd0b-126">However, if the provider can produce a recipient entry that includes more information, it should do so.</span></span> <span data-ttu-id="4bd0b-127">Par exemple, si un fournisseur de transport dispose de suffisamment d’informations sur le format de destinataire d’un fournisseur de carnet d’adresses pour créer un identificateur d’entrée valide pour un destinataire pour ce format, il doit créer l’identificateur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="4bd0b-127">For example, if a transport provider has enough information about an address book provider's recipient format that it can build a valid entry identifier for a recipient for that format, it should build the entry identifier.</span></span>
  
<span data-ttu-id="4bd0b-128">Si des propriétés nontransmitables sont reçues, le fournisseur de transport ne doit pas les stocker dans le nouveau message.</span><span class="sxs-lookup"><span data-stu-id="4bd0b-128">If any nontransmittable properties are received, the transport provider should not store them in the new message.</span></span> <span data-ttu-id="4bd0b-129">Toutefois, le fournisseur de transport doit stocker toutes les propriétés transmises qu’il reçoit dans le nouveau message.</span><span class="sxs-lookup"><span data-stu-id="4bd0b-129">However, the transport provider should store all transmittable properties it receives in the new message.</span></span>
  
<span data-ttu-id="4bd0b-130">Si le message entrant est un rapport de remise ou de remise et que le fournisseur de transport ne peut pas utiliser la méthode [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) pour générer le rapport à partir du message d’origine, le fournisseur doit lui-même remplir le message avec les propriétés appropriées.</span><span class="sxs-lookup"><span data-stu-id="4bd0b-130">If the incoming message is a delivery report or a nondelivery report and the transport provider is unable to use the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method to generate the report from the original message, the provider should itself populate the message with the appropriate properties.</span></span> <span data-ttu-id="4bd0b-131">Toutefois, le fournisseur de transport ne peut pas définir la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="4bd0b-131">However, the transport provider cannot set the message's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="4bd0b-132">Pour enregistrer le message entrant dans la boutique de messages MAPI appropriée après le traitement, le fournisseur de transport appelle la méthode [IMAPIProp::SaveChanges.](imapiprop-savechanges.md)</span><span class="sxs-lookup"><span data-stu-id="4bd0b-132">To save the incoming message in the appropriate MAPI message store after processing, the transport provider calls the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="4bd0b-133">Si le fournisseur de transport n’a aucun message à transmettre aupooler MAPI, il peut arrêter le message entrant en revenant de l’appel **StartMessage** sans appeler **SaveChanges**.</span><span class="sxs-lookup"><span data-stu-id="4bd0b-133">If the transport provider does not have any messages to pass to the MAPI spooler, it can stop the incoming message by returning from the **StartMessage** call without calling **SaveChanges**.</span></span>
  
<span data-ttu-id="4bd0b-134">Tous les objets que le fournisseur de transport ouvre lors d’un appel **StartMessage** doivent être libérés avant d’être retournés.</span><span class="sxs-lookup"><span data-stu-id="4bd0b-134">All objects that the transport provider opens during a **StartMessage** call should be released before returning.</span></span> <span data-ttu-id="4bd0b-135">Toutefois, le fournisseur ne doit pas libérer l’objet message que lepooler MAPI a transmis à l’origine dans le _paramètre lpMessage._</span><span class="sxs-lookup"><span data-stu-id="4bd0b-135">However, the provider should not release the message object that the MAPI spooler originally passed in the  _lpMessage_ parameter.</span></span> 
  
<span data-ttu-id="4bd0b-136">Si **StartMessage renvoie** une erreur, le message en cours est libéré sans que les modifications ne sont enregistrées et est perdu.</span><span class="sxs-lookup"><span data-stu-id="4bd0b-136">If **StartMessage** returns an error, the message in process is released without having changes saved and is lost.</span></span> <span data-ttu-id="4bd0b-137">Dans ce cas, le fournisseur de transport doit transmettre l’indicateur NOTIFY_CRITICAL_ERROR avec un appel à la méthode [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) et appeler la méthode [IXPLogon::P élément](ixplogon-poll.md) pour informer lepooler MAPI qu’il se trouve dans une condition d’erreur grave.</span><span class="sxs-lookup"><span data-stu-id="4bd0b-137">In this case, the transport provider should pass the NOTIFY_CRITICAL_ERROR flag with a call to the [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) method and call the [IXPLogon::Poll](ixplogon-poll.md) method to notify the MAPI spooler that it is in a severe error condition.</span></span> 
  
<span data-ttu-id="4bd0b-138">Pour plus d’informations, [voir Interaction avec le spooler MAPI.](interacting-with-the-mapi-spooler.md)</span><span class="sxs-lookup"><span data-stu-id="4bd0b-138">For more information, see [Interacting with the MAPI Spooler](interacting-with-the-mapi-spooler.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4bd0b-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4bd0b-139">See also</span></span>



[<span data-ttu-id="4bd0b-140">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="4bd0b-140">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="4bd0b-141">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="4bd0b-141">IMAPISupport::SpoolerNotify</span></span>](imapisupport-spoolernotify.md)
  
[<span data-ttu-id="4bd0b-142">IMAPISupport::SpoolerYield</span><span class="sxs-lookup"><span data-stu-id="4bd0b-142">IMAPISupport::SpoolerYield</span></span>](imapisupport-spooleryield.md)
  
[<span data-ttu-id="4bd0b-143">IMAPISupport::StatusRecips</span><span class="sxs-lookup"><span data-stu-id="4bd0b-143">IMAPISupport::StatusRecips</span></span>](imapisupport-statusrecips.md)
  
[<span data-ttu-id="4bd0b-144">IMessage::GetRecipientTable</span><span class="sxs-lookup"><span data-stu-id="4bd0b-144">IMessage::GetRecipientTable</span></span>](imessage-getrecipienttable.md)
  
[<span data-ttu-id="4bd0b-145">IXPLogon::Poll</span><span class="sxs-lookup"><span data-stu-id="4bd0b-145">IXPLogon::Poll</span></span>](ixplogon-poll.md)
  
[<span data-ttu-id="4bd0b-146">IXPLogon::TransportNotify</span><span class="sxs-lookup"><span data-stu-id="4bd0b-146">IXPLogon::TransportNotify</span></span>](ixplogon-transportnotify.md)
  
[<span data-ttu-id="4bd0b-147">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4bd0b-147">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

