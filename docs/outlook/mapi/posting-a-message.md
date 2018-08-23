---
title: Publier un message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cc3e1546-e58b-413f-82d7-4efeb86b0000
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 61e1039a89f47fe29f9b5a1ba9203cfc88d9797e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577519"
---
# <a name="posting-a-message"></a><span data-ttu-id="31c88-103">Publier un message</span><span class="sxs-lookup"><span data-stu-id="31c88-103">Posting a message</span></span>

<span data-ttu-id="31c88-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="31c88-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="31c88-105">Publier un message est similaire à l’envoi d’un message.</span><span class="sxs-lookup"><span data-stu-id="31c88-105">Posting a message is similar to sending a message.</span></span> <span data-ttu-id="31c88-106">La principale différence est la destination.</span><span class="sxs-lookup"><span data-stu-id="31c88-106">The main difference is the destination.</span></span> <span data-ttu-id="31c88-107">Au lieu d’être dirigées vers un ou plusieurs destinataires sur un ou plusieurs systèmes de messagerie, un message publié reste dans un dossier dans la banque de messages en cours.</span><span class="sxs-lookup"><span data-stu-id="31c88-107">Rather than being directed to one or more recipients across one or more messaging systems, a posted message remains in a folder in the current message store.</span></span>
  
### <a name="to-post-a-message"></a><span data-ttu-id="31c88-108">Pour envoyer un message</span><span class="sxs-lookup"><span data-stu-id="31c88-108">To post a message</span></span>
  
1. <span data-ttu-id="31c88-109">Ouvrez le dossier de destination en appelant [IMsgStore::OpenEntry](imsgstore-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="31c88-109">Open the destination folder by calling [IMsgStore::OpenEntry](imsgstore-openentry.md).</span></span> <span data-ttu-id="31c88-110">Si le dossier de destination est la boîte de réception, recherchez l’identificateur d’entrée à transmettre à **OpenEntry** en appelant [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md).</span><span class="sxs-lookup"><span data-stu-id="31c88-110">If the destination folder is the Inbox, locate the entry identifier to pass to **OpenEntry** by calling [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md).</span></span> 
    
2. <span data-ttu-id="31c88-111">Appelez [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) pour créer le message.</span><span class="sxs-lookup"><span data-stu-id="31c88-111">Call [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) to create the message.</span></span> 
    
3. <span data-ttu-id="31c88-112">Appeler la méthode de [IMAPIProp::SetProps](imapiprop-setprops.md) du message pour définir :</span><span class="sxs-lookup"><span data-stu-id="31c88-112">Call the message's [IMAPIProp::SetProps](imapiprop-setprops.md) method to set:</span></span> 
    
   - <span data-ttu-id="31c88-113">L’indicateur MSGFLAG_READ dans la propriété **PidTagMessageFlags** ( [PR_MESSAGE_FLAGS](pidtagmessageflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="31c88-113">The MSGFLAG_READ flag in the **PidTagMessageFlags** ( [PR_MESSAGE_FLAGS](pidtagmessageflags-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="31c88-114">Les propriétés **PR_SENDER** .</span><span class="sxs-lookup"><span data-stu-id="31c88-114">The **PR_SENDER** properties.</span></span> 
    
   - <span data-ttu-id="31c88-115">Les propriétés **PR_SENT_REPRESENTING** .</span><span class="sxs-lookup"><span data-stu-id="31c88-115">The **PR_SENT_REPRESENTING** properties.</span></span> 
    
   - <span data-ttu-id="31c88-116">La propriété **PR_RECEIPT_TIME** ([PidTagReceiptTime](pidtagreceipttime-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="31c88-116">The **PR_RECEIPT_TIME** ([PidTagReceiptTime](pidtagreceipttime-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="31c88-117">Le **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) ou la propriété **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="31c88-117">The **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) or **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="31c88-118">La propriété **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="31c88-118">The **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="31c88-119">La propriété **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="31c88-119">The **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="31c88-120">Toutes les propriétés requises par la classe de message.</span><span class="sxs-lookup"><span data-stu-id="31c88-120">Any properties required by the message class.</span></span>
    
4. <span data-ttu-id="31c88-121">Appelez la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) du message pour enregistrer le message.</span><span class="sxs-lookup"><span data-stu-id="31c88-121">Call the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to save the message.</span></span> 
    
5. <span data-ttu-id="31c88-122">Si nécessaire, créez une pièce jointe, définissez ses propriétés et enregistrez-le.</span><span class="sxs-lookup"><span data-stu-id="31c88-122">If necessary, create an attachment, set its properties, and save it.</span></span> <span data-ttu-id="31c88-123">Pour plus d’informations sur l’ajout de pièces jointes aux messages, consultez [Création d’une pièce jointe du Message](creating-a-message-attachment.md).</span><span class="sxs-lookup"><span data-stu-id="31c88-123">For more information about adding attachments to messages, see [Creating a Message Attachment](creating-a-message-attachment.md).</span></span>
    
6. <span data-ttu-id="31c88-124">Appelez **IMessage::SaveChanges** pour enregistrer le message.</span><span class="sxs-lookup"><span data-stu-id="31c88-124">Call **IMessage::SaveChanges** to save the message.</span></span> <span data-ttu-id="31c88-125">À ce stade, il apparaîtra dans le tableau contenu du dossier de destination.</span><span class="sxs-lookup"><span data-stu-id="31c88-125">At this point it will appear in the contents table of the destination folder.</span></span> 
    
<span data-ttu-id="31c88-126">Notez que vous ne créez pas d’une liste de destinataires.</span><span class="sxs-lookup"><span data-stu-id="31c88-126">Notice that you do not create a recipient list.</span></span> <span data-ttu-id="31c88-127">Au lieu de cela, vous définissez plusieurs propriétés qui sont normalement définies par un fournisseur de transport pour un message.</span><span class="sxs-lookup"><span data-stu-id="31c88-127">Instead, you set several properties that are normally set by a transport provider for a sent message.</span></span> 
  
<span data-ttu-id="31c88-128">Si vous souhaitez enregistrer un message par intermittence avant de s’affichent dans le tableau contenu du dossier visible, créer à la place dans un dossier masqué, tel que le dossier racine de la sous-arborescence IPM et déplacer ensuite vers le dossier cible.</span><span class="sxs-lookup"><span data-stu-id="31c88-128">If you want to save a message intermittently before having it appear in the contents table of the visible folder, create it instead in a hidden folder such as the root folder of the IPM subtree and then move it to the target folder.</span></span> 
  

