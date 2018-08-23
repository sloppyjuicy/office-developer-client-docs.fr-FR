---
title: Renvoi d’un message non remis
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 71768db3-a107-47c6-8e6b-775e8d40ac36
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: cdb1ef3cf6db2a1b63b68a105867aa6624b80c2c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588894"
---
# <a name="resending-an-undelivered-message"></a><span data-ttu-id="5444f-103">Renvoi d’un message non remis</span><span class="sxs-lookup"><span data-stu-id="5444f-103">Resending an undelivered message</span></span>
  
<span data-ttu-id="5444f-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5444f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5444f-105">Un fournisseur de transport envoie un rapport de non-remise (NDR) lorsqu’il ne peut pas remettre avec succès un message que vous avez soumis.</span><span class="sxs-lookup"><span data-stu-id="5444f-105">A transport provider sends a non-delivery report (NDR) when it cannot successfully deliver a message that you have submitted.</span></span> <span data-ttu-id="5444f-106">C’est le client ou non les utilisateurs peuvent tenter de renvoyer ces messages non remis.</span><span class="sxs-lookup"><span data-stu-id="5444f-106">It is up to the client whether or not users can attempt to resend these undelivered messages.</span></span> <span data-ttu-id="5444f-107">Si vous prenez en charge le renvoi de messages, vous pouvez utiliser un formulaire fourni par MAPI ou implémenter votre propre.</span><span class="sxs-lookup"><span data-stu-id="5444f-107">If you support resending messages, you can either use a form provided by MAPI or implement your own.</span></span> <span data-ttu-id="5444f-108">Le formulaire MAPI affiche les noms des destinataires ayant échoués et la raison de l’échec de remise, dans la mesure du possible et inclut un bouton qui, lorsque sélectionnée, permet à un utilisateur de renvoyer le message.</span><span class="sxs-lookup"><span data-stu-id="5444f-108">The MAPI form displays the names of the failed recipients and the reason for the delivery failure, if possible, and includes a button that, when selected, allows a user to resend the message.</span></span>
  
<span data-ttu-id="5444f-109">Lorsqu’un message récente est reçu, il doit se présenter exactement comme le message d’origine.</span><span class="sxs-lookup"><span data-stu-id="5444f-109">When a resent message is received, it should look exactly like the original message.</span></span> <span data-ttu-id="5444f-110">Le destinataire doit être impossible de faire la distinction entre un message qui a été remis sur sa première tentative de transmission ou d’une nouvelle tentative.</span><span class="sxs-lookup"><span data-stu-id="5444f-110">The recipient should be unable to differentiate between a message that was delivered on its first attempt at transmission or a subsequent attempt.</span></span> <span data-ttu-id="5444f-111">Réponses de ce message devraient fonctionner comme si le message a été envoyé correctement la première fois.</span><span class="sxs-lookup"><span data-stu-id="5444f-111">Replies on this message should work exactly as if the message had been sent successfully the first time.</span></span>
  
### <a name="to-resend-an-undelivered-message"></a><span data-ttu-id="5444f-112">Pour renvoyer un message non remis</span><span class="sxs-lookup"><span data-stu-id="5444f-112">To resend an undelivered message</span></span>
  
1. <span data-ttu-id="5444f-113">Appelez [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) pour créer un nouveau message.</span><span class="sxs-lookup"><span data-stu-id="5444f-113">Call [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) to create a new message.</span></span> 
    
2. <span data-ttu-id="5444f-114">Copier toutes les propriétés à partir du message d’origine, à l’exclusion de la ** PR_MESSAGE_RECIPIENTS **, propriété ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) et les propriétés **PR_SENDER** et **PR_SENT_REPRESENTING** .</span><span class="sxs-lookup"><span data-stu-id="5444f-114">Copy all of the properties from the original message, excluding the ** PR_MESSAGE_RECIPIENTS ** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property, and the **PR_SENDER** and **PR_SENT_REPRESENTING** properties.</span></span> <span data-ttu-id="5444f-115">Apportez les modifications de propriété suivantes :</span><span class="sxs-lookup"><span data-stu-id="5444f-115">Make the following property modifications:</span></span> 
    
   - <span data-ttu-id="5444f-116">La valeur de l’état **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) ** PR_ORIG_MESSAGE_CLASS ** propriété ([PidTagOriginalMessageClass](pidtagoriginalmessageclass-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="5444f-116">Set **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) to the report's **PR_ORIG_MESSAGE_CLASS ** ([PidTagOriginalMessageClass](pidtagoriginalmessageclass-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="5444f-117">Définir l’indicateur MSGFLAG_RESEND dans la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="5444f-117">Set the MSGFLAG_RESEND flag in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="5444f-118">La valeur **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)) la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) du message d’origine.</span><span class="sxs-lookup"><span data-stu-id="5444f-118">Set **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)) to the original message's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="5444f-119">Pour chaque destinataire, définissez MAPI_SUBMITTED dans la propriété **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="5444f-119">For each recipient, set MAPI_SUBMITTED in the **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) property.</span></span> 
    
   - <span data-ttu-id="5444f-120">En double chaque destinataire ayant échoué.</span><span class="sxs-lookup"><span data-stu-id="5444f-120">Duplicate each failed recipient.</span></span> <span data-ttu-id="5444f-121">Modifier la propriété **PR_RECIPIENT_TYPE** pour le destinataire dupliqué à MAPI_P1.</span><span class="sxs-lookup"><span data-stu-id="5444f-121">Change the **PR_RECIPIENT_TYPE** property for the duplicated recipient to MAPI_P1.</span></span> <span data-ttu-id="5444f-122">Par conséquent, pour chaque destinataire ayant échoué il existe maintenant deux entrées dans la table de destinataires : une avec **PR_RECIPIENT_TYPE** défini à sa valeur d’origine et l’autre avec **PR_RECIPIENT_TYPE** défini à MAPI_P1.</span><span class="sxs-lookup"><span data-stu-id="5444f-122">Therefore, for each failed recipient there are now two entries in the recipient table: one with **PR_RECIPIENT_TYPE** set to its original value and the other with **PR_RECIPIENT_TYPE** set to MAPI_P1.</span></span> 
    
3. <span data-ttu-id="5444f-123">Appelez [ScCreateConversationIndex](sccreateconversationindex.md) pour configurer la conversation si vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="5444f-123">Call [ScCreateConversationIndex](sccreateconversationindex.md) to set up conversation tracking if desired.</span></span> 
    
4. <span data-ttu-id="5444f-124">Appeler la méthode de [IMessage::ModifyRecipients](imessage-modifyrecipients.md) du nouveau message pour mettre à jour la liste des destinataires.</span><span class="sxs-lookup"><span data-stu-id="5444f-124">Call the new message's [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method to update the recipient list.</span></span> 
    
5. <span data-ttu-id="5444f-125">Appelez [IMessage::SubmitMessage](imessage-submitmessage.md) pour enregistrer et envoyer le nouveau message.</span><span class="sxs-lookup"><span data-stu-id="5444f-125">Call [IMessage::SubmitMessage](imessage-submitmessage.md) to save and send the new message.</span></span> 
    

