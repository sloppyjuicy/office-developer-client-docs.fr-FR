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
ms.openlocfilehash: 3f3330c132abdf35d0e4f67775c03f7d2e9fcc76
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563988"
---
# <a name="handling-an-outgoing-message"></a><span data-ttu-id="8bcab-103">Gestion d’un message sortant</span><span class="sxs-lookup"><span data-stu-id="8bcab-103">Handling an outgoing message</span></span>

<span data-ttu-id="8bcab-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8bcab-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8bcab-105">Un message sortant est un message qui peut être envoyé à un ou plusieurs destinataires via un ou plusieurs systèmes de messagerie ou être publié dans un dossier dans une banque de messages.</span><span class="sxs-lookup"><span data-stu-id="8bcab-105">An outgoing message is a message that can be sent to one or more recipients across one or more messaging systems or be posted to a folder in a message store.</span></span>
  
## <a name="create-and-send-an-outgoing-message"></a><span data-ttu-id="8bcab-106">Créer et envoyer un message sortant</span><span class="sxs-lookup"><span data-stu-id="8bcab-106">Create and send an outgoing message</span></span>
  
1. <span data-ttu-id="8bcab-107">Ouvrez la banque de messages par défaut.</span><span class="sxs-lookup"><span data-stu-id="8bcab-107">Open the default message store.</span></span> <span data-ttu-id="8bcab-108">Pour plus d’informations, voir [l’ouverture d’une banque de messages](opening-a-message-store.md) et de [l’ouverture de la banque de messages par défaut](opening-the-default-message-store.md).</span><span class="sxs-lookup"><span data-stu-id="8bcab-108">For more information, see [Opening a Message Store](opening-a-message-store.md) and [Opening the Default Message Store](opening-the-default-message-store.md).</span></span>
    
2. <span data-ttu-id="8bcab-109">Ouvrez le dossier boîte d’envoi.</span><span class="sxs-lookup"><span data-stu-id="8bcab-109">Open the Outbox folder.</span></span> <span data-ttu-id="8bcab-110">Pour plus d’informations, consultez [ouverture d’un dossier de la banque de messages](opening-a-message-store-folder.md).</span><span class="sxs-lookup"><span data-stu-id="8bcab-110">For more information, see [Opening a Message Store Folder](opening-a-message-store-folder.md).</span></span>
    
3. <span data-ttu-id="8bcab-111">Appeler la méthode de **IMAPIFolder::CreateMessage** du dossier boîte d’envoi pour créer le nouveau message.</span><span class="sxs-lookup"><span data-stu-id="8bcab-111">Call the Outbox folder's **IMAPIFolder::CreateMessage** method to create the new message.</span></span> <span data-ttu-id="8bcab-112">Pour plus d’informations, voir [IMAPIFolder::CreateMessage](imapifolder-createmessage.md),</span><span class="sxs-lookup"><span data-stu-id="8bcab-112">For more information, see [IMAPIFolder::CreateMessage](imapifolder-createmessage.md),</span></span>
    
4. <span data-ttu-id="8bcab-113">Créer une liste de destinataires avec un ou plusieurs destinataires résolus.</span><span class="sxs-lookup"><span data-stu-id="8bcab-113">Create a recipient list with one or more resolved recipients.</span></span> <span data-ttu-id="8bcab-114">Pour plus d’informations, voir [Création d’une liste de destinataires](creating-a-recipient-list.md).</span><span class="sxs-lookup"><span data-stu-id="8bcab-114">For more information, see [Creating a Recipient List](creating-a-recipient-list.md).</span></span>
    
5. <span data-ttu-id="8bcab-115">Si vous le souhaitez, ajoutez un objet.</span><span class="sxs-lookup"><span data-stu-id="8bcab-115">Optionally, add a subject.</span></span> <span data-ttu-id="8bcab-116">Pour plus d’informations, consultez [Création d’un objet du Message](creating-a-message-subject.md).</span><span class="sxs-lookup"><span data-stu-id="8bcab-116">For more information, see [Creating a Message Subject](creating-a-message-subject.md).</span></span>
    
6. <span data-ttu-id="8bcab-117">Ajoutez le texte du message.</span><span class="sxs-lookup"><span data-stu-id="8bcab-117">Add the message text.</span></span> <span data-ttu-id="8bcab-118">Pour plus d’informations, voir [Création de texte du Message](creating-message-text.md).</span><span class="sxs-lookup"><span data-stu-id="8bcab-118">For more information, see [Creating Message Text](creating-message-text.md).</span></span>
    
7. <span data-ttu-id="8bcab-119">Si le texte du message est mis en forme, ajouter des informations de rendu.</span><span class="sxs-lookup"><span data-stu-id="8bcab-119">If the message text is formatted, add rendering information.</span></span> <span data-ttu-id="8bcab-120">Pour plus d’informations, voir [Ajout d’informations d’affichage au texte mis en forme](adding-rendering-information-to-formatted-text.md).</span><span class="sxs-lookup"><span data-stu-id="8bcab-120">For more information, see [Adding Rendering Information to Formatted Text](adding-rendering-information-to-formatted-text.md).</span></span>
    
8. <span data-ttu-id="8bcab-121">Si vous le souhaitez, ajoutez une ou plusieurs pièces jointes.</span><span class="sxs-lookup"><span data-stu-id="8bcab-121">Optionally, add one or more attachments.</span></span> <span data-ttu-id="8bcab-122">Pour plus d’informations, consultez [Création d’une pièce jointe du Message](creating-a-message-attachment.md).</span><span class="sxs-lookup"><span data-stu-id="8bcab-122">For more information, see [Creating a Message Attachment](creating-a-message-attachment.md).</span></span>
    
9. <span data-ttu-id="8bcab-123">Définir d’autres propriétés de message comme vous le souhaitez puis enregistrer et envoyer le message en appelant **IMessage::SubmitMessage**.</span><span class="sxs-lookup"><span data-stu-id="8bcab-123">Set other message properties as desired and then save and send the message by calling **IMessage::SubmitMessage**.</span></span> <span data-ttu-id="8bcab-124">Pour plus d’informations, voir [IMessage::SubmitMessage](imessage-submitmessage.md).</span><span class="sxs-lookup"><span data-stu-id="8bcab-124">For more information, see [IMessage::SubmitMessage](imessage-submitmessage.md).</span></span>
    
10. <span data-ttu-id="8bcab-125">Supprimer le message envoyé si le **PR\_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) propriété a la valeur TRUE ou les déplacer vers le dossier identifié par la propriété **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="8bcab-125">Delete the sent message if the **PR\_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) property is set to TRUE or move it to the folder identified by the **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="8bcab-126">Pour plus d’informations, voir [traitement d’un Message envoyé](processing-a-sent-message.md).</span><span class="sxs-lookup"><span data-stu-id="8bcab-126">For more information, see [Processing a Sent Message](processing-a-sent-message.md).</span></span>
    
<span data-ttu-id="8bcab-127">Si vous souhaitez intermittantly enregistrer le message avant de l’envoyer, appelez la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) du message.</span><span class="sxs-lookup"><span data-stu-id="8bcab-127">If you want to intermittantly save the message before sending it, call the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="8bcab-128">Pour plus d’informations, consultez la rubrique, [L’enregistrement d’un Message](saving-a-message.md) ou [l’envoi d’un Message](sending-a-message.md).</span><span class="sxs-lookup"><span data-stu-id="8bcab-128">For more information, see, [Saving a Message](saving-a-message.md) or [Sending a Message](sending-a-message.md).</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="8bcab-129">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="8bcab-129">In this section</span></span>

- <span data-ttu-id="8bcab-130">[Création d’une liste de destinataires](creating-a-recipient-list.md): explique comment créer une liste de destinataires.</span><span class="sxs-lookup"><span data-stu-id="8bcab-130">[Creating a Recipient List](creating-a-recipient-list.md): Describes how to create a recipient list.</span></span>
    
- <span data-ttu-id="8bcab-131">[Création d’un objet du Message](creating-a-message-subject.md): explique comment créer un objet facultative pour un message.</span><span class="sxs-lookup"><span data-stu-id="8bcab-131">[Creating a Message Subject](creating-a-message-subject.md): Describes how to create an optional subject for a message.</span></span>
    
- <span data-ttu-id="8bcab-132">[Création de texte du Message](creating-message-text.md): explique comment créer le texte du message.</span><span class="sxs-lookup"><span data-stu-id="8bcab-132">[Creating Message Text](creating-message-text.md): Describes how to create message text.</span></span>
    
- <span data-ttu-id="8bcab-133">[Ajout d’informations d’affichage au texte mis en forme](adding-rendering-information-to-formatted-text.md): décrit où dans le texte mis en forme une pièce jointe doit être affiché.</span><span class="sxs-lookup"><span data-stu-id="8bcab-133">[Adding Rendering Information to Formatted Text](adding-rendering-information-to-formatted-text.md): Describes where in formatted text an attachment is to be rendered.</span></span>
    
- <span data-ttu-id="8bcab-134">[Création d’une pièce jointe](creating-a-message-attachment.md): décrit comment créer des pièces jointes.</span><span class="sxs-lookup"><span data-stu-id="8bcab-134">[Creating a Message Attachment](creating-a-message-attachment.md): Describes how to create attachments.</span></span>
    
- <span data-ttu-id="8bcab-135">[L’enregistrement d’un Message](saving-a-message.md): décrit comment enregistrent les messages clients.</span><span class="sxs-lookup"><span data-stu-id="8bcab-135">[Saving a Message](saving-a-message.md): Describes how clients save messages.</span></span>
    
- <span data-ttu-id="8bcab-136">[Envoi d’un Message](sending-a-message.md): comment faire envoyer un message.</span><span class="sxs-lookup"><span data-stu-id="8bcab-136">[Sending a Message](sending-a-message.md): Describes how to send a message.</span></span>
    
- <span data-ttu-id="8bcab-137">[Traitement d’un Message envoyé](processing-a-sent-message.md): décrit l’envoi de messages peuvent être traités.</span><span class="sxs-lookup"><span data-stu-id="8bcab-137">[Processing a Sent Message](processing-a-sent-message.md): Describes how to sent messages can be processed.</span></span>
    

