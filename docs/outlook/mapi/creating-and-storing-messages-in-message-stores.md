---
title: Création et stockage des messages dans des banques de messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cc74b31c-d7ed-4fcf-9535-a2f9222901b7
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 7c923a330c542dff8b1bbc476461ccd21680a5b7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332899"
---
# <a name="creating-and-storing-messages-in-message-stores"></a><span data-ttu-id="ce70a-103">Création et stockage des messages dans des banques de messages</span><span class="sxs-lookup"><span data-stu-id="ce70a-103">Creating and Storing Messages in Message Stores</span></span>

  
  
<span data-ttu-id="ce70a-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ce70a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ce70a-p101">La façon dont votre fournisseur de banques de messages crée et stocke les messages dans le mécanisme de stockage sous-jacent dépend fortement du mécanisme de stockage sous-jacent lui-même. En règle générale, vous devrez uniquement écrire du code pour conserver les propriétés d’un message et leurs valeurs.</span><span class="sxs-lookup"><span data-stu-id="ce70a-p101">How your message store provider creates and stores messages in the underlying storage mechanism depends heavily on the underlying storage mechanism itself. In general, you need only to write code to preserve the properties of a message and their values.</span></span>
  
<span data-ttu-id="ce70a-p102">Lorsque le fournisseur de banques de messages crée un message, il doit le créer avec les propriétés requises pour les messages. Une liste de ces propriétés est consultable dans la documentation relative à l’interface [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md). Après cela, les applications clientes ajoutent des propriétés supplémentaires avec les méthodes [IMAPIProp](imapipropiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="ce70a-p102">When the message store provider creates a new message, the provider needs to create the message with the required properties for messages. A list of these properties can be found in the documentation for the [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md) interface. After that, client applications add any additional properties with [IMAPIProp](imapipropiunknown.md) methods.</span></span> 
  
<span data-ttu-id="ce70a-110">Lorsque le fournisseur de banques de messages enregistre un message dans le mécanisme de stockage sous-jacent, il doit effectuer une itération sur les propriétés du message et les enregistrer dans le mécanisme de stockage sous-jacent de façon à ce qu’elles puissent être récupérées entièrement si le message est ouvert ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="ce70a-110">When the message store provider saves a message to the underlying storage mechanism, the provider needs to iterate over the message's properties, and save them to the underlying storage mechanism such that they can be fully recovered if the message is later opened.</span></span>
  
<span data-ttu-id="ce70a-p103">MAPI exige que les propriétés sur les interfaces [IMessage](imessageimapiprop.md) soient traitées, ce qui signifie que les modifications apportées à celles-ci ne deviennent pas permanentes tant que la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) n’est pas appelée sur l’objet de message. Le fournisseur de banques de messages est responsable de l’implémentation de ce comportement. Cette opération n’est généralement pas compliquée. Elle consiste simplement à conserver les propriétés en mémoire pendant qu’elles sont modifiées et à les valider dans le mécanisme de stockage sous-jacent lorsque la méthode **SaveChanges** est appelée.</span><span class="sxs-lookup"><span data-stu-id="ce70a-p103">MAPI requires that the properties on [IMessage](imessageimapiprop.md) interfaces are transacted, meaning that changes made to them do not become permanent until the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method is called on the message object. The message store provider is responsible for implementing this behavior. Usually this is not difficult; it simply means holding properties in memory while they are being modified and committing them to the underlying storage mechanism when **SaveChanges** is called.</span></span> 
  
<span data-ttu-id="ce70a-114">Certaines propriétés sur les objets de message ont une sémantique spéciale pour les applications clientes par rapport à la méthode **SaveChanges**, comme suit :</span><span class="sxs-lookup"><span data-stu-id="ce70a-114">Some properties on message objects have special semantics for client applications with respect to the **SaveChanges** method, as follows:</span></span> 
  
- <span data-ttu-id="ce70a-115">Certaines propriétés doivent être en lecture/écriture avant que la méthode **SaveChanges** soit appelée, mais en lecture seule ensuite.</span><span class="sxs-lookup"><span data-stu-id="ce70a-115">Some properties should be read/write before **SaveChanges** is called, but read-only afterward.</span></span> <span data-ttu-id="ce70a-116">Par exemple, la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) est initialement définie par l’application cliente qui crée le message (et est donc en lecture/écriture), mais ne peut pas être modifiée après le premier appel à **SaveChanges**.</span><span class="sxs-lookup"><span data-stu-id="ce70a-116">For example, **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) is set initially by the client application that creates the message (and thus is read/write) but cannot be changed after the first call to **SaveChanges**.</span></span>
    
- <span data-ttu-id="ce70a-p105">Certaines propriétés ont des relations spéciales avec les propriétés dans le dossier qui les contient ou avec les méthodes **IMAPIFolder**. Par exemple, la propriété **PR_MESSAGE_FLAGS** est liée aux indicateurs utilisés sur l’appel [IMAPIFolder::CreateMessage](imapifolder-createmessage.md).</span><span class="sxs-lookup"><span data-stu-id="ce70a-p105">Some properties have special relations to properties on the folder they are in or to **IMAPIFolder** methods. For example, the **PR_MESSAGE_FLAGS** property is related to the flags used on the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) call.</span></span> 
    
- <span data-ttu-id="ce70a-119">Certaines propriétés peuvent ne pas être disponibles tant que **SaveChanges** n’est pas appelée pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="ce70a-119">Some properties may not be available until **SaveChanges** is called for the first time.</span></span> <span data-ttu-id="ce70a-120">Par exemple, la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) peut ne pas être disponible tant que **SaveChanges** n’est pas appelée.</span><span class="sxs-lookup"><span data-stu-id="ce70a-120">For example, the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property may not be available until **SaveChanges** is called.</span></span> 
    
- <span data-ttu-id="ce70a-121">Certaines propriétés peuvent avoir des relations spéciales avec d’autres propriétés sur l’objet de message.</span><span class="sxs-lookup"><span data-stu-id="ce70a-121">Some properties can have special relationships to other properties on the message object.</span></span> <span data-ttu-id="ce70a-122">Par exemple, la propriété **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) est généralement dérivée de la propriété **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) dans les fournisseurs de banques de messages prenant en charge les messages au format RTF.</span><span class="sxs-lookup"><span data-stu-id="ce70a-122">For example, the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property is usually derived from the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property in message store providers that support Rich Text Format messages.</span></span>
    
- <span data-ttu-id="ce70a-123">Certaines propriétés sont utilisées par plusieurs types d’objet liés à des banques de messages.</span><span class="sxs-lookup"><span data-stu-id="ce70a-123">Some properties are used by more than one object type related to message stores.</span></span> <span data-ttu-id="ce70a-124">Par exemple, la propriété **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) est requise sur les objets de dossier et de message ainsi que sur les objets de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="ce70a-124">For example, the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property is required on folder and message objects as well as message store objects.</span></span>
    
<span data-ttu-id="ce70a-125">Il incombe au fournisseur de banques de messages d’implémenter la sémantique correcte pour ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="ce70a-125">It is the responsibility of the message store provider to implement the correct semantics for such properties.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ce70a-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ce70a-126">See also</span></span>



[<span data-ttu-id="ce70a-127">Implémentation des messages dans les banques de messages</span><span class="sxs-lookup"><span data-stu-id="ce70a-127">Implementing Messages in Message Stores</span></span>](implementing-messages-in-message-stores.md)

