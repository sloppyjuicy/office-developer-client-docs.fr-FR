---
title: Publication d’un message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cc3e1546-e58b-413f-82d7-4efeb86b0000
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 2c174d48a19e23de725e1d5a1533130175f2ab00
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429767"
---
# <a name="posting-a-message"></a><span data-ttu-id="aa3e5-103">Publication d’un message</span><span class="sxs-lookup"><span data-stu-id="aa3e5-103">Posting a message</span></span>

<span data-ttu-id="aa3e5-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aa3e5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aa3e5-105">La publication d’un message est similaire à l’envoi d’un message.</span><span class="sxs-lookup"><span data-stu-id="aa3e5-105">Posting a message is similar to sending a message.</span></span> <span data-ttu-id="aa3e5-106">La principale différence est la destination.</span><span class="sxs-lookup"><span data-stu-id="aa3e5-106">The main difference is the destination.</span></span> <span data-ttu-id="aa3e5-107">Au lieu d’être dirigé vers un ou plusieurs destinataires dans un ou plusieurs systèmes de messagerie, un message publié reste dans un dossier de la boutique de messages actuelle.</span><span class="sxs-lookup"><span data-stu-id="aa3e5-107">Rather than being directed to one or more recipients across one or more messaging systems, a posted message remains in a folder in the current message store.</span></span>
  
### <a name="to-post-a-message"></a><span data-ttu-id="aa3e5-108">Pour publier un message</span><span class="sxs-lookup"><span data-stu-id="aa3e5-108">To post a message</span></span>
  
1. <span data-ttu-id="aa3e5-109">Ouvrez le dossier de destination en appelant [IMsgStore::OpenEntry](imsgstore-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="aa3e5-109">Open the destination folder by calling [IMsgStore::OpenEntry](imsgstore-openentry.md).</span></span> <span data-ttu-id="aa3e5-110">Si le dossier de destination est la boîte de réception, recherchez l’identificateur d’entrée à transmettre à **OpenEntry** en appelant [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md).</span><span class="sxs-lookup"><span data-stu-id="aa3e5-110">If the destination folder is the Inbox, locate the entry identifier to pass to **OpenEntry** by calling [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md).</span></span> 
    
2. <span data-ttu-id="aa3e5-111">Appelez [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) pour créer le message.</span><span class="sxs-lookup"><span data-stu-id="aa3e5-111">Call [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) to create the message.</span></span> 
    
3. <span data-ttu-id="aa3e5-112">Appelez la méthode [IMAPIProp::SetProps](imapiprop-setprops.md) du message pour définir :</span><span class="sxs-lookup"><span data-stu-id="aa3e5-112">Call the message's [IMAPIProp::SetProps](imapiprop-setprops.md) method to set:</span></span> 
    
   - <span data-ttu-id="aa3e5-113">L MSGFLAG_READ de la **propriété PidTagMessageFlags** [(PR_MESSAGE_FLAGS).](pidtagmessageflags-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="aa3e5-113">The MSGFLAG_READ flag in the **PidTagMessageFlags** ( [PR_MESSAGE_FLAGS](pidtagmessageflags-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="aa3e5-114">Propriétés **PR_SENDER** propriétés.</span><span class="sxs-lookup"><span data-stu-id="aa3e5-114">The **PR_SENDER** properties.</span></span> 
    
   - <span data-ttu-id="aa3e5-115">Propriétés **PR_SENT_REPRESENTING** propriétés.</span><span class="sxs-lookup"><span data-stu-id="aa3e5-115">The **PR_SENT_REPRESENTING** properties.</span></span> 
    
   - <span data-ttu-id="aa3e5-116">Propriété **PR_RECEIPT_TIME** ([PidTagReceiptTime](pidtagreceipttime-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="aa3e5-116">The **PR_RECEIPT_TIME** ([PidTagReceiptTime](pidtagreceipttime-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="aa3e5-117">Propriété **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) ou **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="aa3e5-117">The **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) or **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="aa3e5-118">Propriété **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="aa3e5-118">The **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="aa3e5-119">Propriété **PR_MESSAGE_CLASS** ([PidTagMessageClass).](pidtagmessageclass-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="aa3e5-119">The **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="aa3e5-120">Toutes les propriétés requises par la classe de message.</span><span class="sxs-lookup"><span data-stu-id="aa3e5-120">Any properties required by the message class.</span></span>
    
4. <span data-ttu-id="aa3e5-121">Appelez la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) du message pour enregistrer le message.</span><span class="sxs-lookup"><span data-stu-id="aa3e5-121">Call the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to save the message.</span></span> 
    
5. <span data-ttu-id="aa3e5-122">Si nécessaire, créez une pièce jointe, définissez ses propriétés et enregistrez-la.</span><span class="sxs-lookup"><span data-stu-id="aa3e5-122">If necessary, create an attachment, set its properties, and save it.</span></span> <span data-ttu-id="aa3e5-123">Pour plus d’informations sur l’ajout de pièces jointes à des messages, voir [Création d’une pièce jointe de message.](creating-a-message-attachment.md)</span><span class="sxs-lookup"><span data-stu-id="aa3e5-123">For more information about adding attachments to messages, see [Creating a Message Attachment](creating-a-message-attachment.md).</span></span>
    
6. <span data-ttu-id="aa3e5-124">Appelez **IMessage::SaveChanges** pour enregistrer le message.</span><span class="sxs-lookup"><span data-stu-id="aa3e5-124">Call **IMessage::SaveChanges** to save the message.</span></span> <span data-ttu-id="aa3e5-125">À ce stade, elle apparaît dans la table des matières du dossier de destination.</span><span class="sxs-lookup"><span data-stu-id="aa3e5-125">At this point it will appear in the contents table of the destination folder.</span></span> 
    
<span data-ttu-id="aa3e5-126">Notez que vous ne créez pas de liste de destinataires.</span><span class="sxs-lookup"><span data-stu-id="aa3e5-126">Notice that you do not create a recipient list.</span></span> <span data-ttu-id="aa3e5-127">Au lieu de cela, vous définissez plusieurs propriétés qui sont normalement définies par un fournisseur de transport pour un message envoyé.</span><span class="sxs-lookup"><span data-stu-id="aa3e5-127">Instead, you set several properties that are normally set by a transport provider for a sent message.</span></span> 
  
<span data-ttu-id="aa3e5-128">Si vous souhaitez enregistrer un message par intermittence avant de le faire apparaître dans la table des matières du dossier visible, créez-le dans un dossier masqué tel que le dossier racine de la sous-arbre IPM, puis déplacez-le vers le dossier cible.</span><span class="sxs-lookup"><span data-stu-id="aa3e5-128">If you want to save a message intermittently before having it appear in the contents table of the visible folder, create it instead in a hidden folder such as the root folder of the IPM subtree and then move it to the target folder.</span></span> 
  

