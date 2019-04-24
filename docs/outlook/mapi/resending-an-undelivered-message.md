---
title: Renvoi d’un message non remis
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 71768db3-a107-47c6-8e6b-775e8d40ac36
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: ddd0c1419531b0822bb98df51f47e12e63dcf242
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328678"
---
# <a name="resending-an-undelivered-message"></a><span data-ttu-id="52ea3-103">Renvoi d’un message non remis</span><span class="sxs-lookup"><span data-stu-id="52ea3-103">Resending an undelivered message</span></span>
  
<span data-ttu-id="52ea3-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="52ea3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="52ea3-105">Un fournisseur de transport envoie une notification d'échec de remise lorsqu'il ne parvient pas à remettre un message que vous avez envoyé.</span><span class="sxs-lookup"><span data-stu-id="52ea3-105">A transport provider sends a non-delivery report (NDR) when it cannot successfully deliver a message that you have submitted.</span></span> <span data-ttu-id="52ea3-106">Il revient au client si les utilisateurs peuvent essayer de renvoyer ces messages non remis.</span><span class="sxs-lookup"><span data-stu-id="52ea3-106">It is up to the client whether or not users can attempt to resend these undelivered messages.</span></span> <span data-ttu-id="52ea3-107">Si vous prenez en charge la retransmission des messages, vous pouvez soit utiliser un formulaire fourni par MAPI, soit implémenter votre propre message.</span><span class="sxs-lookup"><span data-stu-id="52ea3-107">If you support resending messages, you can either use a form provided by MAPI or implement your own.</span></span> <span data-ttu-id="52ea3-108">Le formulaire MAPI affiche les noms des destinataires ayant échoué et la raison de l'échec de remise, si possible, et inclut un bouton qui, lorsqu'il est sélectionné, permet à un utilisateur de renvoyer le message.</span><span class="sxs-lookup"><span data-stu-id="52ea3-108">The MAPI form displays the names of the failed recipients and the reason for the delivery failure, if possible, and includes a button that, when selected, allows a user to resend the message.</span></span>
  
<span data-ttu-id="52ea3-109">Lorsqu'un message renvoyé est reçu, il doit ressembler exactement au message d'origine.</span><span class="sxs-lookup"><span data-stu-id="52ea3-109">When a resent message is received, it should look exactly like the original message.</span></span> <span data-ttu-id="52ea3-110">Le destinataire ne doit pas faire la différence entre un message qui a été remis lors de sa première tentative de transmission ou une tentative ultérieure.</span><span class="sxs-lookup"><span data-stu-id="52ea3-110">The recipient should be unable to differentiate between a message that was delivered on its first attempt at transmission or a subsequent attempt.</span></span> <span data-ttu-id="52ea3-111">Les réponses sur ce message doivent fonctionner exactement comme si le message avait été envoyé avec succès la première fois.</span><span class="sxs-lookup"><span data-stu-id="52ea3-111">Replies on this message should work exactly as if the message had been sent successfully the first time.</span></span>
  
### <a name="to-resend-an-undelivered-message"></a><span data-ttu-id="52ea3-112">Pour renvoyer un message non remis</span><span class="sxs-lookup"><span data-stu-id="52ea3-112">To resend an undelivered message</span></span>
  
1. <span data-ttu-id="52ea3-113">Appelez [IMAPIFolder: CreateMessage](imapifolder-createmessage.md) pour créer un message.</span><span class="sxs-lookup"><span data-stu-id="52ea3-113">Call [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) to create a new message.</span></span> 
    
2. <span data-ttu-id="52ea3-114">Copiez toutes les propriétés du message d'origine, à l'exception de la propriété \* \* PR_MESSAGE_RECIPIENTS \* \* ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)), ainsi que les propriétés **PR_SENDER** et **PR_SENT_REPRESENTING** .</span><span class="sxs-lookup"><span data-stu-id="52ea3-114">Copy all of the properties from the original message, excluding the \*\* PR_MESSAGE_RECIPIENTS \*\* ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property, and the **PR_SENDER** and **PR_SENT_REPRESENTING** properties.</span></span> <span data-ttu-id="52ea3-115">Effectuez les modifications de propriétés suivantes:</span><span class="sxs-lookup"><span data-stu-id="52ea3-115">Make the following property modifications:</span></span> 
    
   - <span data-ttu-id="52ea3-116">Définissez **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) sur la propriété \* \* PR_ORIG_MESSAGE_CLASS \* \* ([PidTagOriginalMessageClass](pidtagoriginalmessageclass-canonical-property.md)) de l'État.</span><span class="sxs-lookup"><span data-stu-id="52ea3-116">Set **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) to the report's \*\*PR_ORIG_MESSAGE_CLASS \*\* ([PidTagOriginalMessageClass](pidtagoriginalmessageclass-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="52ea3-117">Définissez l'indicateur MSGFLAG_RESEND dans la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="52ea3-117">Set the MSGFLAG_RESEND flag in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="52ea3-118">Définissez **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)) sur la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) du message d'origine.</span><span class="sxs-lookup"><span data-stu-id="52ea3-118">Set **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)) to the original message's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="52ea3-119">Pour chaque destinataire, définissez MAPI_SUBMITTED dans la propriété **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="52ea3-119">For each recipient, set MAPI_SUBMITTED in the **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) property.</span></span> 
    
   - <span data-ttu-id="52ea3-120">Dupliquez chaque destinataire ayant échoué.</span><span class="sxs-lookup"><span data-stu-id="52ea3-120">Duplicate each failed recipient.</span></span> <span data-ttu-id="52ea3-121">Modifiez la propriété **PR_RECIPIENT_TYPE** pour le destinataire DUPLIQUÉ vers MAPI_P1.</span><span class="sxs-lookup"><span data-stu-id="52ea3-121">Change the **PR_RECIPIENT_TYPE** property for the duplicated recipient to MAPI_P1.</span></span> <span data-ttu-id="52ea3-122">Par conséquent, pour chaque destinataire ayant échoué, il y a maintenant deux entrées dans la table des destinataires: une avec **PR_RECIPIENT_TYPE** définie à sa valeur d'origine et l'autre avec **PR_RECIPIENT_TYPE** défini sur MAPI_P1.</span><span class="sxs-lookup"><span data-stu-id="52ea3-122">Therefore, for each failed recipient there are now two entries in the recipient table: one with **PR_RECIPIENT_TYPE** set to its original value and the other with **PR_RECIPIENT_TYPE** set to MAPI_P1.</span></span> 
    
3. <span data-ttu-id="52ea3-123">Appelez [ScCreateConversationIndex](sccreateconversationindex.md) pour configurer le suivi des conversations si vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="52ea3-123">Call [ScCreateConversationIndex](sccreateconversationindex.md) to set up conversation tracking if desired.</span></span> 
    
4. <span data-ttu-id="52ea3-124">Appelez la méthode [IMessage:: ModifyRecipients](imessage-modifyrecipients.md) du nouveau message pour mettre à jour la liste des destinataires.</span><span class="sxs-lookup"><span data-stu-id="52ea3-124">Call the new message's [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method to update the recipient list.</span></span> 
    
5. <span data-ttu-id="52ea3-125">Appelez [IMessage:: SubmitMessage](imessage-submitmessage.md) pour enregistrer et envoyer le nouveau message.</span><span class="sxs-lookup"><span data-stu-id="52ea3-125">Call [IMessage::SubmitMessage](imessage-submitmessage.md) to save and send the new message.</span></span> 
    

