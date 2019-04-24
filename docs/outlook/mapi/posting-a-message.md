---
title: Publication d’un message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cc3e1546-e58b-413f-82d7-4efeb86b0000
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 2c174d48a19e23de725e1d5a1533130175f2ab00
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350749"
---
# <a name="posting-a-message"></a><span data-ttu-id="0936b-103">Publication d’un message</span><span class="sxs-lookup"><span data-stu-id="0936b-103">Posting a message</span></span>

<span data-ttu-id="0936b-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0936b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0936b-105">La publication d'un message est similaire à l'envoi d'un message.</span><span class="sxs-lookup"><span data-stu-id="0936b-105">Posting a message is similar to sending a message.</span></span> <span data-ttu-id="0936b-106">La différence principale est la destination.</span><span class="sxs-lookup"><span data-stu-id="0936b-106">The main difference is the destination.</span></span> <span data-ttu-id="0936b-107">Au lieu d'être dirigé vers un ou plusieurs destinataires dans un ou plusieurs systèmes de messagerie, un message publié reste dans un dossier dans la Banque de messages actuelle.</span><span class="sxs-lookup"><span data-stu-id="0936b-107">Rather than being directed to one or more recipients across one or more messaging systems, a posted message remains in a folder in the current message store.</span></span>
  
### <a name="to-post-a-message"></a><span data-ttu-id="0936b-108">Pour publier un message</span><span class="sxs-lookup"><span data-stu-id="0936b-108">To post a message</span></span>
  
1. <span data-ttu-id="0936b-109">Ouvrez le dossier de destination en appelant [IMsgStore:: OpenEntry](imsgstore-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="0936b-109">Open the destination folder by calling [IMsgStore::OpenEntry](imsgstore-openentry.md).</span></span> <span data-ttu-id="0936b-110">Si le dossier de destination est la boîte de réception, localisez l'identificateur d'entrée à transmettre à **OpenEntry** en appelant [IMsgStore:: GetReceiveFolder](imsgstore-getreceivefolder.md).</span><span class="sxs-lookup"><span data-stu-id="0936b-110">If the destination folder is the Inbox, locate the entry identifier to pass to **OpenEntry** by calling [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md).</span></span> 
    
2. <span data-ttu-id="0936b-111">Appelez [IMAPIFolder: CreateMessage](imapifolder-createmessage.md) pour créer le message.</span><span class="sxs-lookup"><span data-stu-id="0936b-111">Call [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) to create the message.</span></span> 
    
3. <span data-ttu-id="0936b-112">Appelez la méthode [IMAPIProp:: SetProps](imapiprop-setprops.md) du message pour définir:</span><span class="sxs-lookup"><span data-stu-id="0936b-112">Call the message's [IMAPIProp::SetProps](imapiprop-setprops.md) method to set:</span></span> 
    
   - <span data-ttu-id="0936b-113">L'indicateur MSGFLAG_READ dans la propriété **PidTagMessageFlags** ( [PR_MESSAGE_FLAGS](pidtagmessageflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="0936b-113">The MSGFLAG_READ flag in the **PidTagMessageFlags** ( [PR_MESSAGE_FLAGS](pidtagmessageflags-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="0936b-114">Propriétés **PR_SENDER** .</span><span class="sxs-lookup"><span data-stu-id="0936b-114">The **PR_SENDER** properties.</span></span> 
    
   - <span data-ttu-id="0936b-115">Propriétés **PR_SENT_REPRESENTING** .</span><span class="sxs-lookup"><span data-stu-id="0936b-115">The **PR_SENT_REPRESENTING** properties.</span></span> 
    
   - <span data-ttu-id="0936b-116">Propriété **PR_RECEIPT_TIME** ([PidTagReceiptTime](pidtagreceipttime-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="0936b-116">The **PR_RECEIPT_TIME** ([PidTagReceiptTime](pidtagreceipttime-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="0936b-117">Propriété **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) ou **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="0936b-117">The **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) or **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="0936b-118">Propriété **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="0936b-118">The **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="0936b-119">La propriété **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="0936b-119">The **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="0936b-120">Toutes les propriétés requises par la classe de message.</span><span class="sxs-lookup"><span data-stu-id="0936b-120">Any properties required by the message class.</span></span>
    
4. <span data-ttu-id="0936b-121">Appelez la méthode [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) du message pour enregistrer le message.</span><span class="sxs-lookup"><span data-stu-id="0936b-121">Call the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to save the message.</span></span> 
    
5. <span data-ttu-id="0936b-122">Si nécessaire, créez une pièce jointe, définissez ses propriétés et enregistrez-la.</span><span class="sxs-lookup"><span data-stu-id="0936b-122">If necessary, create an attachment, set its properties, and save it.</span></span> <span data-ttu-id="0936b-123">Pour plus d'informations sur l'ajout de pièces jointes aux messages, consultez [la rubrique Création d'une pièce jointe](creating-a-message-attachment.md).</span><span class="sxs-lookup"><span data-stu-id="0936b-123">For more information about adding attachments to messages, see [Creating a Message Attachment](creating-a-message-attachment.md).</span></span>
    
6. <span data-ttu-id="0936b-124">Appelez **IMessage:: SaveChanges** pour enregistrer le message.</span><span class="sxs-lookup"><span data-stu-id="0936b-124">Call **IMessage::SaveChanges** to save the message.</span></span> <span data-ttu-id="0936b-125">À ce stade, il apparaîtra dans la table des matières du dossier de destination.</span><span class="sxs-lookup"><span data-stu-id="0936b-125">At this point it will appear in the contents table of the destination folder.</span></span> 
    
<span data-ttu-id="0936b-126">Notez que vous ne créez pas de liste de destinataires.</span><span class="sxs-lookup"><span data-stu-id="0936b-126">Notice that you do not create a recipient list.</span></span> <span data-ttu-id="0936b-127">Au lieu de cela, vous définissez plusieurs propriétés qui sont normalement définies par un fournisseur de transport pour un message envoyé.</span><span class="sxs-lookup"><span data-stu-id="0936b-127">Instead, you set several properties that are normally set by a transport provider for a sent message.</span></span> 
  
<span data-ttu-id="0936b-128">Si vous souhaitez enregistrer un message par intermittence avant de l'afficher dans la table des matières du dossier visible, créez-le à la place dans un dossier masqué, tel que le dossier racine de la sous-arborescence IPM, puis déplacez-le vers le dossier cible.</span><span class="sxs-lookup"><span data-stu-id="0936b-128">If you want to save a message intermittently before having it appear in the contents table of the visible folder, create it instead in a hidden folder such as the root folder of the IPM subtree and then move it to the target folder.</span></span> 
  

