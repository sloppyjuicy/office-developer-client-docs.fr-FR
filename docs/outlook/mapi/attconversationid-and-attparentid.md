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
# <a name="attconversationid-and-attparentid"></a>attConversationID et attParentID

**S’applique à** : Outlook 2013 | Outlook 2016 
  
La clé de conversation de messagerie Windows pour Workgroups 3,1 est une chaîne de texte. L'équivalent MAPI est une valeur binaire. Pour assurer la compatibilité descendante, l'implémentation TNEF convertit les données binaires en texte et ajoute un caractère de fin null.
  
> [!NOTE]
> Les propriétés correspondantes dans MAPI auxquelles ces attributs TNEF sont mappés, PR_CONVERSATION_KEY et PR_PARENT_KEY, ont été déconseillées dans Microsoft Exchange Server: utilisation de **PR_CONVERSATION_KEY**, la propriété [canonique PidTagConversationKey Propriété](pidtagconversationkey-canonical-property.md)persiste dans Outlook uniquement, pour localiser **IPM. **Messages de MessageManager. 
  
## <a name="remarks"></a>Remarques

La propriété **PR_CONVERSATION_KEY** est le précurseur autrement obsolète de l' **PR_CONVERSATION_INDEX**, [propriété canonique PidTagConversationIndex](pidtagconversationindex-canonical-property.md) et **PR_CONVERSATION_TOPIC**, propriété canonique [PidTagConversationTopic Propriété](pidtagconversationtopic-canonical-property.md), qui doit être utilisée à la place.
  
## <a name="see-also"></a>Voir aussi

- [Sous-arborescence IPM](ipm-subtree.md)
- [Dossiers spéciaux MAPI](mapi-special-folders.md)

