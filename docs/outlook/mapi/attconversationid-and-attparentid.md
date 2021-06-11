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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410048"
---
# <a name="attconversationid-and-attparentid"></a><span data-ttu-id="86dd0-103">attConversationID et attParentID</span><span class="sxs-lookup"><span data-stu-id="86dd0-103">attConversationID and attParentID</span></span>

<span data-ttu-id="86dd0-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="86dd0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="86dd0-105">La Windows de conversation de messagerie workgroups 3.1 est une chaîne de texte.</span><span class="sxs-lookup"><span data-stu-id="86dd0-105">The Windows for Workgroups 3.1 Mail conversation key is a text string.</span></span> <span data-ttu-id="86dd0-106">L’équivalent MAPI est une valeur binaire.</span><span class="sxs-lookup"><span data-stu-id="86dd0-106">The MAPI equivalent is a binary value.</span></span> <span data-ttu-id="86dd0-107">Pour assurer la compatibilité ascendante, l’implémentation TNEF convertit les données binaires en texte et ajoute un caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="86dd0-107">To provide backward compatibility, the TNEF implementation converts the binary data to text and adds a terminating null character.</span></span>
  
> [!NOTE]
> <span data-ttu-id="86dd0-108">Les propriétés correspondantes dans MAPI sur lesquelles ces attributs TNEF sont mappés, PR_CONVERSATION_KEY et PR_PARENT_KEY, ont été dépréciées dans Microsoft Exchange Server : l’utilisation de **PR_CONVERSATION_KEY**, la propriété canonique [PidTagConversationKey](pidtagconversationkey-canonical-property.md), persiste dans Outlook uniquement, pour localiser **IPM. Messages MessageManager.**</span><span class="sxs-lookup"><span data-stu-id="86dd0-108">The corresponding properties in MAPI to which these TNEF attributes are mapped, PR_CONVERSATION_KEY and PR_PARENT_KEY, have been deprecated in Microsoft Exchange Server: Use of **PR_CONVERSATION_KEY**, the [PidTagConversationKey Canonical Property](pidtagconversationkey-canonical-property.md), persists in Outlook only, for locating **IPM.MessageManager** messages.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="86dd0-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="86dd0-109">Remarks</span></span>

<span data-ttu-id="86dd0-110">La **propriété PR_CONVERSATION_KEY** est le prédécesseur obsolète de la propriété canonique **PR_CONVERSATION_INDEX**, [PidTagConversationIndex](pidtagconversationindex-canonical-property.md) et **PR_CONVERSATION_TOPIC**, de la propriété canonique [PidTagConversationTopic](pidtagconversationtopic-canonical-property.md), qui doit être utilisée à la place.</span><span class="sxs-lookup"><span data-stu-id="86dd0-110">The **PR_CONVERSATION_KEY** property is the otherwise obsolete precursor of the **PR_CONVERSATION_INDEX**, [PidTagConversationIndex Canonical Property](pidtagconversationindex-canonical-property.md) and **PR_CONVERSATION_TOPIC**, [PidTagConversationTopic Canonical Property](pidtagconversationtopic-canonical-property.md), which should be used instead.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="86dd0-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="86dd0-111">See also</span></span>

- [<span data-ttu-id="86dd0-112">Sous-arbre IPM</span><span class="sxs-lookup"><span data-stu-id="86dd0-112">IPM Subtree</span></span>](ipm-subtree.md)
- [<span data-ttu-id="86dd0-113">Dossiers spéciaux MAPI</span><span class="sxs-lookup"><span data-stu-id="86dd0-113">MAPI Special Folders</span></span>](mapi-special-folders.md)

