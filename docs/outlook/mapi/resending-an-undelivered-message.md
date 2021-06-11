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
ms.openlocfilehash: ddd0c1419531b0822bb98df51f47e12e63dcf242
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432666"
---
# <a name="resending-an-undelivered-message"></a><span data-ttu-id="108be-103">Renvoi d’un message non remis</span><span class="sxs-lookup"><span data-stu-id="108be-103">Resending an undelivered message</span></span>
  
<span data-ttu-id="108be-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="108be-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="108be-105">Un fournisseur de transport envoie une rapport de non-remise (NDR) lorsqu’il ne peut pas remettre correctement un message que vous avez envoyé.</span><span class="sxs-lookup"><span data-stu-id="108be-105">A transport provider sends a non-delivery report (NDR) when it cannot successfully deliver a message that you have submitted.</span></span> <span data-ttu-id="108be-106">C’est au client de décider si les utilisateurs peuvent tenter de renvoyer ces messages non envoyés.</span><span class="sxs-lookup"><span data-stu-id="108be-106">It is up to the client whether or not users can attempt to resend these undelivered messages.</span></span> <span data-ttu-id="108be-107">Si vous vous chargez de renvoyer des messages, vous pouvez utiliser un formulaire fourni par MAPI ou implémenter le vôtre.</span><span class="sxs-lookup"><span data-stu-id="108be-107">If you support resending messages, you can either use a form provided by MAPI or implement your own.</span></span> <span data-ttu-id="108be-108">Le formulaire MAPI affiche les noms des destinataires en échec et la raison de l’échec de remise, si possible, et inclut un bouton qui, lorsqu’il est sélectionné, permet à un utilisateur de renvoyer le message.</span><span class="sxs-lookup"><span data-stu-id="108be-108">The MAPI form displays the names of the failed recipients and the reason for the delivery failure, if possible, and includes a button that, when selected, allows a user to resend the message.</span></span>
  
<span data-ttu-id="108be-109">Lorsqu’un message de nouvelle réception est reçu, il doit ressembler exactement au message d’origine.</span><span class="sxs-lookup"><span data-stu-id="108be-109">When a resent message is received, it should look exactly like the original message.</span></span> <span data-ttu-id="108be-110">Le destinataire ne doit pas être en mesure de différencier un message remis lors de sa première tentative de transmission ou d’une tentative ultérieure.</span><span class="sxs-lookup"><span data-stu-id="108be-110">The recipient should be unable to differentiate between a message that was delivered on its first attempt at transmission or a subsequent attempt.</span></span> <span data-ttu-id="108be-111">Les réponses à ce message doivent fonctionner exactement comme si le message avait été envoyé avec succès la première fois.</span><span class="sxs-lookup"><span data-stu-id="108be-111">Replies on this message should work exactly as if the message had been sent successfully the first time.</span></span>
  
### <a name="to-resend-an-undelivered-message"></a><span data-ttu-id="108be-112">Pour renvoyer un message non reçu</span><span class="sxs-lookup"><span data-stu-id="108be-112">To resend an undelivered message</span></span>
  
1. <span data-ttu-id="108be-113">Appelez [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) pour créer un message.</span><span class="sxs-lookup"><span data-stu-id="108be-113">Call [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) to create a new message.</span></span> 
    
2. <span data-ttu-id="108be-114">Copiez toutes les propriétés du message d’origine, à l’exception de la propriété \*\* PR_MESSAGE_RECIPIENTS \*\* ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)), et des propriétés **PR_SENDER** et **PR_SENT_REPRESENTING.**</span><span class="sxs-lookup"><span data-stu-id="108be-114">Copy all of the properties from the original message, excluding the \*\* PR_MESSAGE_RECIPIENTS \*\* ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property, and the **PR_SENDER** and **PR_SENT_REPRESENTING** properties.</span></span> <span data-ttu-id="108be-115">A effectuer les modifications de propriété suivantes :</span><span class="sxs-lookup"><span data-stu-id="108be-115">Make the following property modifications:</span></span> 
    
   - <span data-ttu-id="108be-116">Définissez **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) à la propriété \*\*PR_ORIG_MESSAGE_CLASS \*\* ([PidTagOriginalMessageClass](pidtagoriginalmessageclass-canonical-property.md)) de l’état.</span><span class="sxs-lookup"><span data-stu-id="108be-116">Set **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) to the report's \*\*PR_ORIG_MESSAGE_CLASS \*\* ([PidTagOriginalMessageClass](pidtagoriginalmessageclass-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="108be-117">Définissez MSGFLAG_RESEND’indicateur **de** PR_MESSAGE_FLAGS ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="108be-117">Set the MSGFLAG_RESEND flag in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="108be-118">Définissez **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)) sur la propriété PR_ENTRYID **(** [PidTagEntryId](pidtagentryid-canonical-property.md)) du message d’origine.</span><span class="sxs-lookup"><span data-stu-id="108be-118">Set **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)) to the original message's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="108be-119">Pour chaque destinataire, définissez MAPI_SUBMITTED la propriété **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="108be-119">For each recipient, set MAPI_SUBMITTED in the **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) property.</span></span> 
    
   - <span data-ttu-id="108be-120">Dupliquer chaque destinataire en échec.</span><span class="sxs-lookup"><span data-stu-id="108be-120">Duplicate each failed recipient.</span></span> <span data-ttu-id="108be-121">Modifiez **la PR_RECIPIENT_TYPE** du destinataire dupliqué en MAPI_P1.</span><span class="sxs-lookup"><span data-stu-id="108be-121">Change the **PR_RECIPIENT_TYPE** property for the duplicated recipient to MAPI_P1.</span></span> <span data-ttu-id="108be-122">Par conséquent, pour chaque destinataire ayant échoué, il existe désormais deux entrées dans la table des destinataires : une avec **PR_RECIPIENT_TYPE** définie sur sa valeur d’origine et l’autre avec **PR_RECIPIENT_TYPE** définie sur MAPI_P1.</span><span class="sxs-lookup"><span data-stu-id="108be-122">Therefore, for each failed recipient there are now two entries in the recipient table: one with **PR_RECIPIENT_TYPE** set to its original value and the other with **PR_RECIPIENT_TYPE** set to MAPI_P1.</span></span> 
    
3. <span data-ttu-id="108be-123">Appelez [ScCreateConversationIndex](sccreateconversationindex.md) pour configurer le suivi des conversations si vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="108be-123">Call [ScCreateConversationIndex](sccreateconversationindex.md) to set up conversation tracking if desired.</span></span> 
    
4. <span data-ttu-id="108be-124">Appelez la méthode [IMessage::ModifyRecipients](imessage-modifyrecipients.md) du nouveau message pour mettre à jour la liste des destinataires.</span><span class="sxs-lookup"><span data-stu-id="108be-124">Call the new message's [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method to update the recipient list.</span></span> 
    
5. <span data-ttu-id="108be-125">Appelez [IMessage::SubmitMessage](imessage-submitmessage.md) pour enregistrer et envoyer le nouveau message.</span><span class="sxs-lookup"><span data-stu-id="108be-125">Call [IMessage::SubmitMessage](imessage-submitmessage.md) to save and send the new message.</span></span> 
    

