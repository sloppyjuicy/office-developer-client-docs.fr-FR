---
title: Enregistrement d’un message dans la boîte de réception
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3df04d4e-7e80-4232-aadc-c05c99ab59cb
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 672a9df55ce711b88451a517a2813c9ad8c599ce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407892"
---
# <a name="saving-a-message-in-the-inbox"></a><span data-ttu-id="b369a-103">Enregistrement d’un message dans la boîte de réception</span><span class="sxs-lookup"><span data-stu-id="b369a-103">Saving a Message in the Inbox</span></span>

  
  
<span data-ttu-id="b369a-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b369a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="b369a-105">**Pour stocker un message dans la boîte de réception sans destinataire**</span><span class="sxs-lookup"><span data-stu-id="b369a-105">**To store a message in the Inbox without any recipients**</span></span>
  
1. <span data-ttu-id="b369a-106">Appelez [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) pour récupérer l’identificateur d’entrée de la boîte de réception.</span><span class="sxs-lookup"><span data-stu-id="b369a-106">Call [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) to retrieve the entry identifier of the Inbox.</span></span> 
    
2. <span data-ttu-id="b369a-107">Appelez [IMsgStore::OpenEntry](imsgstore-openentry.md) pour ouvrir la boîte de réception et récupérer un pointeur vers celui-ci.</span><span class="sxs-lookup"><span data-stu-id="b369a-107">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) to open the Inbox and retrieve a pointer to it.</span></span> 
    
3. <span data-ttu-id="b369a-108">Appelez la méthode [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) de la boîte de réception pour créer le message.</span><span class="sxs-lookup"><span data-stu-id="b369a-108">Call the Inbox's [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method to create the message.</span></span> 
    
4. <span data-ttu-id="b369a-109">Appelez la méthode [IMAPIProp::SetProps](imapiprop-setprops.md) du message pour ajouter les propriétés **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) ou **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) et **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b369a-109">Call the message's [IMAPIProp::SetProps](imapiprop-setprops.md) method to add the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)), or **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) and **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) properties.</span></span> 
    
5. <span data-ttu-id="b369a-110">Créez chaque pièce jointe, définissez ses propriétés et enregistrez-la.</span><span class="sxs-lookup"><span data-stu-id="b369a-110">Create each attachment, set its properties, and save it.</span></span> <span data-ttu-id="b369a-111">Pour plus d’informations sur l’ajout de pièces jointes à des messages, voir [Création d’une pièce jointe de message.](creating-a-message-attachment.md)</span><span class="sxs-lookup"><span data-stu-id="b369a-111">For detailed information about adding attachments to messages, see [Creating a Message Attachment](creating-a-message-attachment.md).</span></span>
    
6. <span data-ttu-id="b369a-112">Appelez **IMessage::SaveChanges** pour enregistrer le message.</span><span class="sxs-lookup"><span data-stu-id="b369a-112">Call **IMessage::SaveChanges** to save the message.</span></span> <span data-ttu-id="b369a-113">À ce stade, elle apparaît dans la table des matières de la Boîte de réception.</span><span class="sxs-lookup"><span data-stu-id="b369a-113">At this point it will appear in the contents table of the Inbox.</span></span> 
    
<span data-ttu-id="b369a-114">Si vous souhaitez enregistrer un message entremettants avant de le faire apparaître dans la table des matières de la boîte de réception, créez-le dans un dossier masqué tel que le dossier racine de la sous-arbre IPM, puis déplacez-le dans la boîte de réception.</span><span class="sxs-lookup"><span data-stu-id="b369a-114">If you want to save a message intermittantly before having it appear in the contents table of the Inbox, create it instead in a hidden folder such as the root folder of the IPM subtree and then move it to the Inbox.</span></span> 
  

