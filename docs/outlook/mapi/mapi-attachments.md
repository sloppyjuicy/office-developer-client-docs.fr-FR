---
title: Pi�ces jointes MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6e6c6ad9-1e07-4234-a5ef-18020d7ce468
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: c6538f8fef7d8ccb87b6e6d9d2b9c68779ca8582
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784580"
---
# <a name="mapi-attachments"></a><span data-ttu-id="3cefe-103">Pi�ces jointes MAPI</span><span class="sxs-lookup"><span data-stu-id="3cefe-103">MAPI Attachments</span></span>

  
  
<span data-ttu-id="3cefe-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3cefe-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3cefe-105">Certains fournisseurs de banque de messages permettent aux clients d'associer l'ajout d'informations sous la forme de fichiers, des objets OLE, des messages ou des donn�es binaires avec des messages.</span><span class="sxs-lookup"><span data-stu-id="3cefe-105">Some message store providers enable clients to associate added information in the form of files, OLE objects, messages, or binary data with messages.</span></span> <span data-ttu-id="3cefe-106">Ajout d'informations est appel� une pi�ce jointe d'un message.</span><span class="sxs-lookup"><span data-stu-id="3cefe-106">This added information is called a message's attachment.</span></span> <span data-ttu-id="3cefe-107">�tant donn� que les pi�ces jointes sont cr��s, g�r�s et accessibles uniquement par le biais de leurs messages, ils sont consid�r�s comme message sous-objets.</span><span class="sxs-lookup"><span data-stu-id="3cefe-107">Because attachments are created, maintained, and accessed only through their messages, they are considered message subobjects.</span></span> <span data-ttu-id="3cefe-108">Au lieu d'avoir un identificateur d'entr�e pour l'acc�s, les pi�ces jointes ont un autre num�ro s�quentiel comme un num�ro de pi�ce jointe.</span><span class="sxs-lookup"><span data-stu-id="3cefe-108">Rather than having an entry identifier for access, attachments have a sequential number known as an attachment number.</span></span> <span data-ttu-id="3cefe-109">Ce num�ro identifie de mani�re unique la pi�ce jointe au sein de son message, mais pas n�cessairement au sein de la banque de messages.</span><span class="sxs-lookup"><span data-stu-id="3cefe-109">This number uniquely identifies the attachment within its message, but not necessarily within the message store.</span></span> <span data-ttu-id="3cefe-110">Deux messages diff�rents peuvent avoir diff�rentes pi�ces jointes ayant le m�me nombre de pi�ces jointes.</span><span class="sxs-lookup"><span data-stu-id="3cefe-110">Two different messages can have different attachments with the same attachment number.</span></span> <span data-ttu-id="3cefe-111">Les numéros de pièce jointe ne sont valides que tant que le message est ouvert et sont stockés dans la propriété **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="3cefe-111">Attachment numbers are only valid as long as the message is open and are stored in the **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="3cefe-p102">Pour acc�der � des informations r�capitulatives sur toutes les pi�ces jointes d'un message, les clients r�cup�rer sa table des pi�ces jointes. Le tableau de la pi�ce jointe consacr�e des informations que les clients peuvent utiliser pour acc�der � une pi�ce jointe directement, telles que son num�ro de pi�ce jointe et la cl� d'enregistrement. Les clients peuvent r�cup�rer un tableau des pi�ces jointes par :</span><span class="sxs-lookup"><span data-stu-id="3cefe-p102">To access summary information about all of a message's attachments, clients retrieve its attachment table. The attachment table includes information that clients can use to access an attachment directly, such as its attachment number and record key. Clients can retrieve an attachment table by:</span></span>
  
- <span data-ttu-id="3cefe-p103">Calling **IMessage::GetAttachmentTable**. For more information, see [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).</span><span class="sxs-lookup"><span data-stu-id="3cefe-p103">Calling **IMessage::GetAttachmentTable**. For more information, see [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).</span></span>
    
- <span data-ttu-id="3cefe-p104">Calling **IMAPIProp::OpenProperty**. For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span><span class="sxs-lookup"><span data-stu-id="3cefe-p104">Calling **IMAPIProp::OpenProperty**. For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span></span>
    
<span data-ttu-id="3cefe-119">Message store providers are expected to support both of these approaches.</span><span class="sxs-lookup"><span data-stu-id="3cefe-119">Message store providers are expected to support both of these approaches.</span></span> <span data-ttu-id="3cefe-120">L’approche **OpenProperty** requiert que l’appelant spécifiez IID_IMAPITable comme identificateur d’interface et **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) en tant que la balise de propriété.</span><span class="sxs-lookup"><span data-stu-id="3cefe-120">The **OpenProperty** approach requires that the caller specify IID_IMAPITable as the interface identifier and **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) as the property tag.</span></span> <span data-ttu-id="3cefe-121">**PR_MESSAGE_ATTACHMENTS** is a table object property that represents a message's attachment table.</span><span class="sxs-lookup"><span data-stu-id="3cefe-121">**PR_MESSAGE_ATTACHMENTS** is a table object property that represents a message's attachment table.</span></span> <span data-ttu-id="3cefe-122">Message store providers are required to set **PR_MESSAGE_ATTACHMENTS** for each message and include it in the array of property tags returned from the **IMAPIProp::GetPropList** method.</span><span class="sxs-lookup"><span data-stu-id="3cefe-122">Message store providers are required to set **PR_MESSAGE_ATTACHMENTS** for each message and include it in the array of property tags returned from the **IMAPIProp::GetPropList** method.</span></span> <span data-ttu-id="3cefe-123">For more information, see [IMAPIProp::GetPropList](imapiprop-getproplist.md).</span><span class="sxs-lookup"><span data-stu-id="3cefe-123">For more information, see [IMAPIProp::GetPropList](imapiprop-getproplist.md).</span></span>
  
 <span data-ttu-id="3cefe-124">**PR_MESSAGE_ATTACHMENTS** peuvent �tre utilis�es :</span><span class="sxs-lookup"><span data-stu-id="3cefe-124">**PR_MESSAGE_ATTACHMENTS** can be used:</span></span> 
  
- <span data-ttu-id="3cefe-125">Avec **IMAPIProp::OpenProperty** pour acc�der � une table de pi�ce jointe ou un destinataire.</span><span class="sxs-lookup"><span data-stu-id="3cefe-125">With **IMAPIProp::OpenProperty** to access an attachment or recipient table.</span></span> 
    
- <span data-ttu-id="3cefe-p106">With **IMAPIProp::CopyTo** or **IMAPIProp::CopyProps** to exclude or include attachments when copying. For more information, see [IMAPIProp::CopyTo](imapiprop-copyto.md) and [IMAPIProp::CopyProps](imapiprop-copyprops.md).</span><span class="sxs-lookup"><span data-stu-id="3cefe-p106">With **IMAPIProp::CopyTo** or **IMAPIProp::CopyProps** to exclude or include attachments when copying. For more information, see [IMAPIProp::CopyTo](imapiprop-copyto.md) and [IMAPIProp::CopyProps](imapiprop-copyprops.md).</span></span>
    
- <span data-ttu-id="3cefe-128">Une restriction sous-objet pour indiquer que la restriction de l'enfant doit appliquer aux pi�ces jointes.</span><span class="sxs-lookup"><span data-stu-id="3cefe-128">In a subobject restriction to indicate that the child restriction should apply to attachments.</span></span>
    
<span data-ttu-id="3cefe-129">For more information, see [Tables des pi�ces jointes](attachment-tables.md).</span><span class="sxs-lookup"><span data-stu-id="3cefe-129">For more information, see [Attachment Tables](attachment-tables.md).</span></span>
  

