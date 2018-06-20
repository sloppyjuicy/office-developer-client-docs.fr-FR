---
title: attConversationID et attParentID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bed36900-e44d-434b-a4f2-d10f2d6f70da
description: 'Dernière modification : 12 mars 2013'
ms.openlocfilehash: 2fd3e66e3171c677465a533ede3001cd0b28c8aa
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782944"
---
# <a name="attconversationid-and-attparentid"></a><span data-ttu-id="74666-103">attConversationID et attParentID</span><span class="sxs-lookup"><span data-stu-id="74666-103">attConversationID and attParentID</span></span>

<span data-ttu-id="74666-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="74666-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="74666-105">Les fenêtres de clé de conversation de messagerie 3.1 de groupes de travail est une chaîne de texte.</span><span class="sxs-lookup"><span data-stu-id="74666-105">The Windows for Workgroups 3.1 Mail conversation key is a text string.</span></span> <span data-ttu-id="74666-106">L’équivalent MAPI est une valeur binaire.</span><span class="sxs-lookup"><span data-stu-id="74666-106">The MAPI equivalent is a binary value.</span></span> <span data-ttu-id="74666-107">Pour des raisons de compatibilité descendante, l’implémentation TNEF convertit les données binaires en texte et ajoute un caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="74666-107">To provide backward compatibility, the TNEF implementation converts the binary data to text and adds a terminating null character.</span></span>
  
> [!NOTE]
> <span data-ttu-id="74666-108">Les propriétés correspondantes dans MAPI pour lequel ces attributs TNEF sont mappées, PR_CONVERSATION_KEY et PR_PARENT_KEY, ont été désapprouvés dans Microsoft Exchange Server : utilisation de **PR_CONVERSATION_KEY**, le [PidTagConversationKey canonique Propriété](pidtagconversationkey-canonical-property.md), persiste dans Outlook uniquement, qui permettent de rechercher **IPM. MessageManager** messages.</span><span class="sxs-lookup"><span data-stu-id="74666-108">The corresponding properties in MAPI to which these TNEF attributes are mapped, PR_CONVERSATION_KEY and PR_PARENT_KEY, have been deprecated in Microsoft Exchange Server: Use of **PR_CONVERSATION_KEY**, the [PidTagConversationKey Canonical Property](pidtagconversationkey-canonical-property.md), persists in Outlook only, for locating **IPM.MessageManager** messages.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="74666-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="74666-109">Remarks</span></span>

<span data-ttu-id="74666-110">La propriété **PR_CONVERSATION_KEY** est le précurseur sinon obsolète des **PR_CONVERSATION_INDEX**, [Propriété canonique PidTagConversationIndex](pidtagconversationindex-canonical-property.md) et **PR_CONVERSATION_TOPIC**, [PidTagConversationTopic canonique Propriété](pidtagconversationtopic-canonical-property.md), qui doit être utilisé à la place.</span><span class="sxs-lookup"><span data-stu-id="74666-110">The **PR_CONVERSATION_KEY** property is the otherwise obsolete precursor of the **PR_CONVERSATION_INDEX**, [PidTagConversationIndex Canonical Property](pidtagconversationindex-canonical-property.md) and **PR_CONVERSATION_TOPIC**, [PidTagConversationTopic Canonical Property](pidtagconversationtopic-canonical-property.md), which should be used instead.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="74666-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="74666-111">See also</span></span>

- [<span data-ttu-id="74666-112">Sous-arborescence IPM</span><span class="sxs-lookup"><span data-stu-id="74666-112">IPM Subtree</span></span>](ipm-subtree.md)
- [<span data-ttu-id="74666-113">Dossiers spéciaux MAPI</span><span class="sxs-lookup"><span data-stu-id="74666-113">MAPI Special Folders</span></span>](mapi-special-folders.md)

