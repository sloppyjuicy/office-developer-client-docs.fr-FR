---
title: L’enregistrement d’un Message dans la boîte de réception
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3df04d4e-7e80-4232-aadc-c05c99ab59cb
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 3c48ded73d924a400632a94feab65f7afca6e526
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787037"
---
# <a name="saving-a-message-in-the-inbox"></a><span data-ttu-id="9af4e-103">L’enregistrement d’un Message dans la boîte de réception</span><span class="sxs-lookup"><span data-stu-id="9af4e-103">Saving a Message in the Inbox</span></span>

  
  
<span data-ttu-id="9af4e-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9af4e-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="9af4e-105">**Pour stocker un message dans la boîte de réception sans les destinataires**</span><span class="sxs-lookup"><span data-stu-id="9af4e-105">**To store a message in the Inbox without any recipients**</span></span>
  
1. <span data-ttu-id="9af4e-106">Appelez [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) pour récupérer l’identificateur d’entrée de la boîte de réception.</span><span class="sxs-lookup"><span data-stu-id="9af4e-106">Call [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) to retrieve the entry identifier of the Inbox.</span></span> 
    
2. <span data-ttu-id="9af4e-107">Appelez [IMsgStore::OpenEntry](imsgstore-openentry.md) pour ouvrir la boîte de réception et de récupérer un pointeur vers elle.</span><span class="sxs-lookup"><span data-stu-id="9af4e-107">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) to open the Inbox and retrieve a pointer to it.</span></span> 
    
3. <span data-ttu-id="9af4e-108">Appelez la méthode de [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) de la boîte de réception pour créer le message.</span><span class="sxs-lookup"><span data-stu-id="9af4e-108">Call the Inbox's [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method to create the message.</span></span> 
    
4. <span data-ttu-id="9af4e-109">Appeler la méthode de [IMAPIProp::SetProps](imapiprop-setprops.md) du message pour ajouter la **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)), ou **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) et **PR_SUBJECT** ([ PidTagSubject](pidtagsubject-canonical-property.md)) Propriétés.</span><span class="sxs-lookup"><span data-stu-id="9af4e-109">Call the message's [IMAPIProp::SetProps](imapiprop-setprops.md) method to add the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)), or **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) and **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) properties.</span></span> 
    
5. <span data-ttu-id="9af4e-110">Créer chaque pièce jointe, définissez ses propriétés et enregistrez-le.</span><span class="sxs-lookup"><span data-stu-id="9af4e-110">Create each attachment, set its properties, and save it.</span></span> <span data-ttu-id="9af4e-111">Pour plus d’informations sur l’ajout de pièces jointes aux messages, consultez [Création d’une pièce jointe du Message](creating-a-message-attachment.md).</span><span class="sxs-lookup"><span data-stu-id="9af4e-111">For detailed information about adding attachments to messages, see [Creating a Message Attachment](creating-a-message-attachment.md).</span></span>
    
6. <span data-ttu-id="9af4e-112">Appelez **IMessage::SaveChanges** pour enregistrer le message.</span><span class="sxs-lookup"><span data-stu-id="9af4e-112">Call **IMessage::SaveChanges** to save the message.</span></span> <span data-ttu-id="9af4e-113">À ce stade, il apparaîtra dans le tableau contenu de la boîte de réception.</span><span class="sxs-lookup"><span data-stu-id="9af4e-113">At this point it will appear in the contents table of the Inbox.</span></span> 
    
<span data-ttu-id="9af4e-114">Si vous souhaitez enregistrer une intermittantly message avant de s’affichent dans le tableau contenu de la boîte de réception, créer à la place dans un dossier masqué, tel que le dossier racine de la sous-arborescence IPM et déplacer ensuite vers la boîte de réception.</span><span class="sxs-lookup"><span data-stu-id="9af4e-114">If you want to save a message intermittantly before having it appear in the contents table of the Inbox, create it instead in a hidden folder such as the root folder of the IPM subtree and then move it to the Inbox.</span></span> 
  

