---
title: Gestion d’un message sortant
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f40c2e0b-1a35-4901-868f-af6c191c921e
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 07785ac82c41108b4333b3c370e3d2f5bfd1426a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407626"
---
# <a name="handling-an-outgoing-message"></a><span data-ttu-id="3a057-103">Gestion d’un message sortant</span><span class="sxs-lookup"><span data-stu-id="3a057-103">Handling an outgoing message</span></span>

<span data-ttu-id="3a057-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3a057-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3a057-105">Un message sortant est un message qui peut être envoyé à un ou plusieurs destinataires dans un ou plusieurs systèmes de messagerie ou être publié dans un dossier d'une banque de messages.</span><span class="sxs-lookup"><span data-stu-id="3a057-105">An outgoing message is a message that can be sent to one or more recipients across one or more messaging systems or be posted to a folder in a message store.</span></span>
  
## <a name="create-and-send-an-outgoing-message"></a><span data-ttu-id="3a057-106">Créer et envoyer un message sortant</span><span class="sxs-lookup"><span data-stu-id="3a057-106">Create and send an outgoing message</span></span>
  
1. <span data-ttu-id="3a057-107">Ouvrez la Banque de messages par défaut.</span><span class="sxs-lookup"><span data-stu-id="3a057-107">Open the default message store.</span></span> <span data-ttu-id="3a057-108">Pour plus d'informations, consultez la rubrique [ouverture d'une banque de messages](opening-a-message-store.md) et [ouverture de la Banque de messages par défaut](opening-the-default-message-store.md).</span><span class="sxs-lookup"><span data-stu-id="3a057-108">For more information, see [Opening a Message Store](opening-a-message-store.md) and [Opening the Default Message Store](opening-the-default-message-store.md).</span></span>
    
2. <span data-ttu-id="3a057-109">Ouvrez le dossier boîte d'envoi.</span><span class="sxs-lookup"><span data-stu-id="3a057-109">Open the Outbox folder.</span></span> <span data-ttu-id="3a057-110">Pour plus d'informations, consultez [la rubrique ouverture d'un dossier de banque de messages](opening-a-message-store-folder.md).</span><span class="sxs-lookup"><span data-stu-id="3a057-110">For more information, see [Opening a Message Store Folder](opening-a-message-store-folder.md).</span></span>
    
3. <span data-ttu-id="3a057-111">Appelez la méthode **IMAPIFolder:: CreateMessage** du dossier boîte d'envoi pour créer le nouveau message.</span><span class="sxs-lookup"><span data-stu-id="3a057-111">Call the Outbox folder's **IMAPIFolder::CreateMessage** method to create the new message.</span></span> <span data-ttu-id="3a057-112">Pour plus d'informations, voir [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md),</span><span class="sxs-lookup"><span data-stu-id="3a057-112">For more information, see [IMAPIFolder::CreateMessage](imapifolder-createmessage.md),</span></span>
    
4. <span data-ttu-id="3a057-113">Créer une liste de destinataires avec un ou plusieurs destinataires résolus.</span><span class="sxs-lookup"><span data-stu-id="3a057-113">Create a recipient list with one or more resolved recipients.</span></span> <span data-ttu-id="3a057-114">Pour plus d'informations, consultez [la rubrique Création d'une liste de destinataires](creating-a-recipient-list.md).</span><span class="sxs-lookup"><span data-stu-id="3a057-114">For more information, see [Creating a Recipient List](creating-a-recipient-list.md).</span></span>
    
5. <span data-ttu-id="3a057-115">Si vous le souhaitez, ajoutez un objet.</span><span class="sxs-lookup"><span data-stu-id="3a057-115">Optionally, add a subject.</span></span> <span data-ttu-id="3a057-116">Pour plus d'informations, consultez [la rubrique Création d'un objet de message](creating-a-message-subject.md).</span><span class="sxs-lookup"><span data-stu-id="3a057-116">For more information, see [Creating a Message Subject](creating-a-message-subject.md).</span></span>
    
6. <span data-ttu-id="3a057-117">Ajoutez le texte du message.</span><span class="sxs-lookup"><span data-stu-id="3a057-117">Add the message text.</span></span> <span data-ttu-id="3a057-118">Pour plus d'informations, consultez la rubrique [création de texte de message](creating-message-text.md).</span><span class="sxs-lookup"><span data-stu-id="3a057-118">For more information, see [Creating Message Text](creating-message-text.md).</span></span>
    
7. <span data-ttu-id="3a057-119">Si le texte du message est mis en forme, ajoutez des informations de rendu.</span><span class="sxs-lookup"><span data-stu-id="3a057-119">If the message text is formatted, add rendering information.</span></span> <span data-ttu-id="3a057-120">Pour plus d'informations, consultez la rubrique [Ajout d'informations de rendu au texte mis en forme](adding-rendering-information-to-formatted-text.md).</span><span class="sxs-lookup"><span data-stu-id="3a057-120">For more information, see [Adding Rendering Information to Formatted Text](adding-rendering-information-to-formatted-text.md).</span></span>
    
8. <span data-ttu-id="3a057-121">Si vous le souhaitez, ajoutez une ou plusieurs pièces jointes.</span><span class="sxs-lookup"><span data-stu-id="3a057-121">Optionally, add one or more attachments.</span></span> <span data-ttu-id="3a057-122">Pour plus d'informations, consultez [la rubrique Création d'une pièce jointe](creating-a-message-attachment.md).</span><span class="sxs-lookup"><span data-stu-id="3a057-122">For more information, see [Creating a Message Attachment](creating-a-message-attachment.md).</span></span>
    
9. <span data-ttu-id="3a057-123">Définissez d'autres propriétés de message si vous le souhaitez, puis enregistrez et envoyez le message en appelant **IMessage:: SubmitMessage**.</span><span class="sxs-lookup"><span data-stu-id="3a057-123">Set other message properties as desired and then save and send the message by calling **IMessage::SubmitMessage**.</span></span> <span data-ttu-id="3a057-124">Pour plus d'informations, consultez [IMessage:: SubmitMessage](imessage-submitmessage.md).</span><span class="sxs-lookup"><span data-stu-id="3a057-124">For more information, see [IMessage::SubmitMessage](imessage-submitmessage.md).</span></span>
    
10. <span data-ttu-id="3a057-125">Supprimez le message envoyé si **la\_propriété PR DELETE_AFTER_SUBMIT** ([PIDTAGDELETEAFTERSUBMIT](pidtagdeleteaftersubmit-canonical-property.md)) est définie sur true ou déplacez-la dans le dossier identifié par la propriété **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="3a057-125">Delete the sent message if the **PR\_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) property is set to TRUE or move it to the folder identified by the **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="3a057-126">Pour plus d'informations, consultez [la rubrique traitement d'un message envoyé](processing-a-sent-message.md).</span><span class="sxs-lookup"><span data-stu-id="3a057-126">For more information, see [Processing a Sent Message](processing-a-sent-message.md).</span></span>
    
<span data-ttu-id="3a057-127">Si vous souhaitez intermittantly enregistrer le message avant de l'envoyer, appelez la méthode [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) du message.</span><span class="sxs-lookup"><span data-stu-id="3a057-127">If you want to intermittantly save the message before sending it, call the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="3a057-128">Pour plus d'informations, reportez-vous à [la rubrique enregistrement d'un message](saving-a-message.md) ou [envoi d'un message](sending-a-message.md).</span><span class="sxs-lookup"><span data-stu-id="3a057-128">For more information, see, [Saving a Message](saving-a-message.md) or [Sending a Message](sending-a-message.md).</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="3a057-129">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="3a057-129">In this section</span></span>

- <span data-ttu-id="3a057-130">[Création d'une liste](creating-a-recipient-list.md)de destinataires: décrit comment créer une liste de destinataires.</span><span class="sxs-lookup"><span data-stu-id="3a057-130">[Creating a Recipient List](creating-a-recipient-list.md): Describes how to create a recipient list.</span></span>
    
- <span data-ttu-id="3a057-131">[Création d'un objet de message](creating-a-message-subject.md): explique comment créer un objet facultatif pour un message.</span><span class="sxs-lookup"><span data-stu-id="3a057-131">[Creating a Message Subject](creating-a-message-subject.md): Describes how to create an optional subject for a message.</span></span>
    
- <span data-ttu-id="3a057-132">[Création](creating-message-text.md)d'un texte de message: explique comment créer un texte de message.</span><span class="sxs-lookup"><span data-stu-id="3a057-132">[Creating Message Text](creating-message-text.md): Describes how to create message text.</span></span>
    
- <span data-ttu-id="3a057-133">[Ajout d'informations de rendu au texte mis en forme](adding-rendering-information-to-formatted-text.md): décrit l'emplacement du texte mis en forme d'une pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="3a057-133">[Adding Rendering Information to Formatted Text](adding-rendering-information-to-formatted-text.md): Describes where in formatted text an attachment is to be rendered.</span></span>
    
- <span data-ttu-id="3a057-134">[Création d'une pièce jointe de message](creating-a-message-attachment.md): explique comment créer des pièces jointes.</span><span class="sxs-lookup"><span data-stu-id="3a057-134">[Creating a Message Attachment](creating-a-message-attachment.md): Describes how to create attachments.</span></span>
    
- <span data-ttu-id="3a057-135">[Enregistrement d'un message](saving-a-message.md): décrit la manière dont les clients enregistrent les messages.</span><span class="sxs-lookup"><span data-stu-id="3a057-135">[Saving a Message](saving-a-message.md): Describes how clients save messages.</span></span>
    
- <span data-ttu-id="3a057-136">[Envoi d'un message](sending-a-message.md): décrit comment envoyer un message.</span><span class="sxs-lookup"><span data-stu-id="3a057-136">[Sending a Message](sending-a-message.md): Describes how to send a message.</span></span>
    
- <span data-ttu-id="3a057-137">[Traitement d'un message envoyé](processing-a-sent-message.md): décrit comment les messages envoyés peuvent être traités.</span><span class="sxs-lookup"><span data-stu-id="3a057-137">[Processing a Sent Message](processing-a-sent-message.md): Describes how to sent messages can be processed.</span></span>
    

