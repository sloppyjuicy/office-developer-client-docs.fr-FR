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
ms.openlocfilehash: 14b93a952e4776716c333dc730144b55bcc61259
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582713"
---
# <a name="attconversationid-and-attparentid"></a>attConversationID et attParentID

**S’applique à**: Outlook 2013 | Outlook 2016 
  
Les fenêtres de clé de conversation de messagerie 3.1 de groupes de travail est une chaîne de texte. L’équivalent MAPI est une valeur binaire. Pour des raisons de compatibilité descendante, l’implémentation TNEF convertit les données binaires en texte et ajoute un caractère null de fin.
  
> [!NOTE]
> Les propriétés correspondantes dans MAPI pour lequel ces attributs TNEF sont mappées, PR_CONVERSATION_KEY et PR_PARENT_KEY, ont été désapprouvés dans Microsoft Exchange Server : utilisation de **PR_CONVERSATION_KEY**, le [PidTagConversationKey canonique Propriété](pidtagconversationkey-canonical-property.md), persiste dans Outlook uniquement, qui permettent de rechercher **IPM. MessageManager** messages. 
  
## <a name="remarks"></a>Remarques

La propriété **PR_CONVERSATION_KEY** est le précurseur sinon obsolète des **PR_CONVERSATION_INDEX**, [Propriété canonique PidTagConversationIndex](pidtagconversationindex-canonical-property.md) et **PR_CONVERSATION_TOPIC**, [PidTagConversationTopic canonique Propriété](pidtagconversationtopic-canonical-property.md), qui doit être utilisé à la place.
  
## <a name="see-also"></a>Voir aussi

- [Sous-arborescence IPM](ipm-subtree.md)
- [Dossiers sp�ciaux MAPI](mapi-special-folders.md)

