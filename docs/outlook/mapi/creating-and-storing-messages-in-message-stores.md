---
title: Cr�ation et le stockage des Messages dans les banques de messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cc74b31c-d7ed-4fcf-9535-a2f9222901b7
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 32cfae36fb519654c1fb92d2f3b688c966f9288f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783108"
---
# <a name="creating-and-storing-messages-in-message-stores"></a><span data-ttu-id="ae909-103">Cr�ation et le stockage des Messages dans les banques de messages</span><span class="sxs-lookup"><span data-stu-id="ae909-103">Creating and Storing Messages in Message Stores</span></span>

  
  
<span data-ttu-id="ae909-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ae909-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ae909-p101">Comment votre fournisseur de banque de messages cr�e et stocke les messages dans le m�canisme de stockage sous-jacent d�pendent essentiellement le m�canisme de stockage sous-jacent lui-m�me. En r�gle g�n�rale, vous devez uniquement d'�crire du code afin de pr�server les propri�t�s d'un message et leurs valeurs.</span><span class="sxs-lookup"><span data-stu-id="ae909-p101">How your message store provider creates and stores messages in the underlying storage mechanism depends heavily on the underlying storage mechanism itself. In general, you need only to write code to preserve the properties of a message and their values.</span></span>
  
<span data-ttu-id="ae909-p102">Lors de la banque de messages fournisseur cr�e un nouveau message, le fournisseur a besoin cr�er le message avec les propri�t�s requises pour les messages. Vous trouverez une liste de ces propri�t�s dans la documentation relative � la [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md) interface. Apr�s cela, les applications clientes ajouter des propri�t�s suppl�mentaires avec les m�thodes [IMAPIProp](imapipropiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="ae909-p102">When the message store provider creates a new message, the provider needs to create the message with the required properties for messages. A list of these properties can be found in the documentation for the [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md) interface. After that, client applications add any additional properties with [IMAPIProp](imapipropiunknown.md) methods.</span></span> 
  
<span data-ttu-id="ae909-110">Lors de la banque de messages fournisseur enregistre un message dans le m�canisme de stockage sous-jacent, le fournisseur a besoin effectuer une it�ration sur les propri�t�s de message, puis enregistrez-les dans le m�canisme de stockage sous-jacent, tels qu'ils peuvent �tre enti�rement r�cup�r�s si le message est ouvert par la suite.</span><span class="sxs-lookup"><span data-stu-id="ae909-110">When the message store provider saves a message to the underlying storage mechanism, the provider needs to iterate over the message's properties, and save them to the underlying storage mechanism such that they can be fully recovered if the message is later opened.</span></span>
  
<span data-ttu-id="ae909-p103">MAPI exige que les propri�t�s sur les interfaces [IMessage](imessageimapiprop.md) sont trait�es, ce qui signifie que les modifications apport�es � leur ne sont pas d�finitive jusqu'� ce que la m�thode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) est appel�e sur l'objet du message. Le fournisseur de banque de messages est responsable de l'impl�mentation de ce comportement. Cela n'est g�n�ralement pas difficile ; Cela signifie simplement que contenant des propri�t�s en m�moire pendant qu'ils sont en cours de modification et les rendre permanentes dans le m�canisme de stockage sous-jacent lorsque **SaveChanges** est appel�e.</span><span class="sxs-lookup"><span data-stu-id="ae909-p103">MAPI requires that the properties on [IMessage](imessageimapiprop.md) interfaces are transacted, meaning that changes made to them do not become permanent until the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method is called on the message object. The message store provider is responsible for implementing this behavior. Usually this is not difficult; it simply means holding properties in memory while they are being modified and committing them to the underlying storage mechanism when **SaveChanges** is called.</span></span> 
  
<span data-ttu-id="ae909-114">Certaines propri�t�s d'objets de message ont une s�mantique sp�ciale pour les applications clientes par rapport � la m�thode **SaveChanges**, comme suit :</span><span class="sxs-lookup"><span data-stu-id="ae909-114">Some properties on message objects have special semantics for client applications with respect to the **SaveChanges** method, as follows:</span></span> 
  
- <span data-ttu-id="ae909-115">Certaines propri�t�s doivent �tre en lecture/�criture avant **SaveChanges** est appel�e, mais en lecture seule par la suite.</span><span class="sxs-lookup"><span data-stu-id="ae909-115">Some properties should be read/write before **SaveChanges** is called, but read-only afterward.</span></span> <span data-ttu-id="ae909-116">Par exemple, **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) est définie à l’origine par l’application cliente qui crée le message (et par conséquent est en lecture/écriture), mais ne peut pas être modifié après le premier appel à **SaveChanges**.</span><span class="sxs-lookup"><span data-stu-id="ae909-116">For example, **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) is set initially by the client application that creates the message (and thus is read/write) but cannot be changed after the first call to **SaveChanges**.</span></span>
    
- <span data-ttu-id="ae909-p105">Certaines propri�t�s ont des relations particuli�res aux propri�t�s sur le dossier qu'ils sont dans ou aux m�thodes de **IMAPIFolder**. Par exemple, la propri�t� **PR_MESSAGE_FLAGS** est li�e aux indicateurs utilis�s lors de l'appel de [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="ae909-p105">Some properties have special relations to properties on the folder they are in or to **IMAPIFolder** methods. For example, the **PR_MESSAGE_FLAGS** property is related to the flags used on the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) call.</span></span> 
    
- <span data-ttu-id="ae909-119">Certaines propri�t�s ne soient pas disponibles tant que **SaveChanges** est appel� pour la premi�re fois.</span><span class="sxs-lookup"><span data-stu-id="ae909-119">Some properties may not be available until **SaveChanges** is called for the first time.</span></span> <span data-ttu-id="ae909-120">Par exemple, la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) sera ne peut-être pas disponible avant **SaveChanges** est appelée.</span><span class="sxs-lookup"><span data-stu-id="ae909-120">For example, the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property may not be available until **SaveChanges** is called.</span></span> 
    
- <span data-ttu-id="ae909-121">Certaines propri�t�s peuvent avoir des relations sp�ciales � d'autres propri�t�s sur l'objet du message.</span><span class="sxs-lookup"><span data-stu-id="ae909-121">Some properties can have special relationships to other properties on the message object.</span></span> <span data-ttu-id="ae909-122">Par exemple, la propriété **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) est généralement dérivée de la propriété **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) dans les fournisseurs de magasins de message qui prennent en charge des messages au Format RTF.</span><span class="sxs-lookup"><span data-stu-id="ae909-122">For example, the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property is usually derived from the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property in message store providers that support Rich Text Format messages.</span></span>
    
- <span data-ttu-id="ae909-123">Certaines propri�t�s sont utilis�es par plusieurs types d'objet associ�s aux magasins de message.</span><span class="sxs-lookup"><span data-stu-id="ae909-123">Some properties are used by more than one object type related to message stores.</span></span> <span data-ttu-id="ae909-124">Par exemple, la propriété **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) est requis sur le dossier et les objets ainsi que message stocker des objets de message.</span><span class="sxs-lookup"><span data-stu-id="ae909-124">For example, the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property is required on folder and message objects as well as message store objects.</span></span>
    
<span data-ttu-id="ae909-125">Il est de la responsabilit� du fournisseur de banque de messages pour impl�menter la s�mantique appropri�e pour ces propri�t�s.</span><span class="sxs-lookup"><span data-stu-id="ae909-125">It is the responsibility of the message store provider to implement the correct semantics for such properties.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ae909-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ae909-126">See also</span></span>



[<span data-ttu-id="ae909-127">L'impl�mentation des Messages dans les banques de messages</span><span class="sxs-lookup"><span data-stu-id="ae909-127">Implementing Messages in Message Stores</span></span>](implementing-messages-in-message-stores.md)

