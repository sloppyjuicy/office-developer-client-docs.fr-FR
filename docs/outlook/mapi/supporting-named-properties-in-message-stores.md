---
title: Prise en charge des propri�t�s nomm�es dans des magasins de Message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a1c73bb5-b44a-4ec6-89e4-0e2228572b2d
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 235683d8565732034f868dd71e4f2047ffe76f09
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569840"
---
# <a name="supporting-named-properties-in-message-stores"></a><span data-ttu-id="48353-103">Prise en charge des propri�t�s nomm�es dans des magasins de Message</span><span class="sxs-lookup"><span data-stu-id="48353-103">Supporting Named Properties in Message Stores</span></span>

  
  
<span data-ttu-id="48353-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="48353-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="48353-p101">Message objects can have properties in them that are not in the set of properties defined by MAPI. Such properties can be unnamed or named. Unnamed properties must reside in a range of property identifiers defined by MAPI. Named custom properties reside in a different range of property identifiers defined by MAPI. They are typically used by custom message types. Your message store provider must support named properties if it is to be used as the default message store. Supporting named properties means implementing the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) and [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) methods, and implementing one or more mapping signatures that identify what names go with what property identifiers. For more information, see [D�finition des nouvelles propri�t�s MAPI](defining-new-mapi-properties.md) and [Prise en charge des propri�t�s nomm�es](supporting-named-properties.md).</span><span class="sxs-lookup"><span data-stu-id="48353-p101">Message objects can have properties in them that are not in the set of properties defined by MAPI. Such properties can be unnamed or named. Unnamed properties must reside in a range of property identifiers defined by MAPI. Named custom properties reside in a different range of property identifiers defined by MAPI. They are typically used by custom message types. Your message store provider must support named properties if it is to be used as the default message store. Supporting named properties means implementing the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) and [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) methods, and implementing one or more mapping signatures that identify what names go with what property identifiers. For more information, see [Defining New MAPI Properties](defining-new-mapi-properties.md) and [Supporting Named Properties](supporting-named-properties.md).</span></span>
  
<span data-ttu-id="48353-p102">Fournisseurs qui prennent en charge de nomm�e propri�t�s utiliser une signature de mappage unique pour tous les objets dans la banque d'informations de base de la plupart des messages. Cela a deux avantages. Tout d'abord, il est plus simple � impl�menter des signatures de mappage s'il en existe uniquement pour suivre. Deuxi�mement, si tous les objets dans la banque de messages utilisent la m�me signature de mappage, les applications clientes sont assur�es que tous les identificateurs de propri�t� sur les messages de la banque de messages font r�f�rent � la m�me propri�t� nomm�e. Cela permet aux applications de client afficher les colonnes de propri�t�s nomm�es dans son interface d'affichage de dossier.</span><span class="sxs-lookup"><span data-stu-id="48353-p102">Most message store providers that support named properties use a single mapping signature for all objects in the message store. This has two benefits. First, it is simpler to implement mapping signatures if there is only one to keep track of. Second, if all objects in the message store use the same mapping signature, client applications are assured that all property identifiers on messages in the message store actually refer to the same named property. This enables client applications to display columns for named properties in their folder view interface.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="48353-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="48353-118">See also</span></span>



[<span data-ttu-id="48353-119">L'impl�mentation des Messages dans les banques de messages</span><span class="sxs-lookup"><span data-stu-id="48353-119">Implementing Messages in Message Stores</span></span>](implementing-messages-in-message-stores.md)

