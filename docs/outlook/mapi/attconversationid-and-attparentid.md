---
title: attConversationID et attParentID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bed36900-e44d-434b-a4f2-d10f2d6f70da
description: Dernière modification le 12 mars 2013
ms.openlocfilehash: c5880aefe7c2dba2e5e4c5405aae2020bb86c711
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318416"
---
# <a name="attconversationid-and-attparentid"></a><span data-ttu-id="1af62-103">attConversationID et attParentID</span><span class="sxs-lookup"><span data-stu-id="1af62-103">attConversationID and attParentID</span></span>

<span data-ttu-id="1af62-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1af62-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1af62-105">La clé de conversation de messagerie Windows pour Workgroups 3,1 est une chaîne de texte.</span><span class="sxs-lookup"><span data-stu-id="1af62-105">The Windows for Workgroups 3.1 Mail conversation key is a text string.</span></span> <span data-ttu-id="1af62-106">L'équivalent MAPI est une valeur binaire.</span><span class="sxs-lookup"><span data-stu-id="1af62-106">The MAPI equivalent is a binary value.</span></span> <span data-ttu-id="1af62-107">Pour assurer la compatibilité descendante, l'implémentation TNEF convertit les données binaires en texte et ajoute un caractère de fin null.</span><span class="sxs-lookup"><span data-stu-id="1af62-107">To provide backward compatibility, the TNEF implementation converts the binary data to text and adds a terminating null character.</span></span>
  
> [!NOTE]
> <span data-ttu-id="1af62-108">Les propriétés correspondantes dans MAPI auxquelles ces attributs TNEF sont mappés, PR_CONVERSATION_KEY et PR_PARENT_KEY, ont été déconseillées dans Microsoft Exchange Server: utilisation de **PR_CONVERSATION_KEY**, la propriété [canonique PidTagConversationKey Propriété](pidtagconversationkey-canonical-property.md)persiste dans Outlook uniquement, pour localiser \*\*IPM. \*\*Messages de MessageManager.</span><span class="sxs-lookup"><span data-stu-id="1af62-108">The corresponding properties in MAPI to which these TNEF attributes are mapped, PR_CONVERSATION_KEY and PR_PARENT_KEY, have been deprecated in Microsoft Exchange Server: Use of **PR_CONVERSATION_KEY**, the [PidTagConversationKey Canonical Property](pidtagconversationkey-canonical-property.md), persists in Outlook only, for locating **IPM.MessageManager** messages.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="1af62-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="1af62-109">Remarks</span></span>

<span data-ttu-id="1af62-110">La propriété **PR_CONVERSATION_KEY** est le précurseur autrement obsolète de l' **PR_CONVERSATION_INDEX**, [propriété canonique PidTagConversationIndex](pidtagconversationindex-canonical-property.md) et **PR_CONVERSATION_TOPIC**, propriété canonique [PidTagConversationTopic Propriété](pidtagconversationtopic-canonical-property.md), qui doit être utilisée à la place.</span><span class="sxs-lookup"><span data-stu-id="1af62-110">The **PR_CONVERSATION_KEY** property is the otherwise obsolete precursor of the **PR_CONVERSATION_INDEX**, [PidTagConversationIndex Canonical Property](pidtagconversationindex-canonical-property.md) and **PR_CONVERSATION_TOPIC**, [PidTagConversationTopic Canonical Property](pidtagconversationtopic-canonical-property.md), which should be used instead.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1af62-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1af62-111">See also</span></span>

- [<span data-ttu-id="1af62-112">Sous-arborescence IPM</span><span class="sxs-lookup"><span data-stu-id="1af62-112">IPM Subtree</span></span>](ipm-subtree.md)
- [<span data-ttu-id="1af62-113">Dossiers spéciaux MAPI</span><span class="sxs-lookup"><span data-stu-id="1af62-113">MAPI Special Folders</span></span>](mapi-special-folders.md)

