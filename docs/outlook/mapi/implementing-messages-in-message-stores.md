---
title: L'impl�mentation des Messages dans les banques de messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: df5003d5-cbfe-40b2-a481-e2e11dce4b3e
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: c21fea9b0c8de96f427c4bcdfabfde3a0032f0c9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784188"
---
# <a name="implementing-messages-in-message-stores"></a><span data-ttu-id="0fee8-103">L'impl�mentation des Messages dans les banques de messages</span><span class="sxs-lookup"><span data-stu-id="0fee8-103">Implementing Messages in Message Stores</span></span>

  
  
<span data-ttu-id="0fee8-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0fee8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0fee8-p101">The [IMessage : IMAPIProp](imessageimapiprop.md) interface is similar to the [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md) interface in that both interfaces derive from the [IMAPIProp : IUnknown](imapipropiunknown.md) interface. Clients use the **IMAPIProp** methods to access the contents of a message. The **IMessage** interface supplies additional methods for manipulating messages (for example, adding attachments or modifying the recipients of a message). The methods in the **IMessage** interface modify attributes of messages that are not stored directly in the message's properties.</span><span class="sxs-lookup"><span data-stu-id="0fee8-p101">The [IMessage : IMAPIProp](imessageimapiprop.md) interface is similar to the [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md) interface in that both interfaces derive from the [IMAPIProp : IUnknown](imapipropiunknown.md) interface. Clients use the **IMAPIProp** methods to access the contents of a message. The **IMessage** interface supplies additional methods for manipulating messages (for example, adding attachments or modifying the recipients of a message). The methods in the **IMessage** interface modify attributes of messages that are not stored directly in the message's properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0fee8-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0fee8-109">See also</span></span>



[<span data-ttu-id="0fee8-110">Fonctionnalit�s de la banque de messages</span><span class="sxs-lookup"><span data-stu-id="0fee8-110">Message Store Features</span></span>](message-store-features.md)

