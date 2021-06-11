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
# <a name="attconversationid-and-attparentid"></a>attConversationID et attParentID

**S’applique à** : Outlook 2013 | Outlook 2016 
  
La Windows de conversation de messagerie workgroups 3.1 est une chaîne de texte. L’équivalent MAPI est une valeur binaire. Pour assurer la compatibilité ascendante, l’implémentation TNEF convertit les données binaires en texte et ajoute un caractère null de fin.
  
> [!NOTE]
> Les propriétés correspondantes dans MAPI sur lesquelles ces attributs TNEF sont mappés, PR_CONVERSATION_KEY et PR_PARENT_KEY, ont été dépréciées dans Microsoft Exchange Server : l’utilisation de **PR_CONVERSATION_KEY**, la propriété canonique [PidTagConversationKey](pidtagconversationkey-canonical-property.md), persiste dans Outlook uniquement, pour localiser **IPM. Messages MessageManager.** 
  
## <a name="remarks"></a>Remarques

La **propriété PR_CONVERSATION_KEY** est le prédécesseur obsolète de la propriété canonique **PR_CONVERSATION_INDEX**, [PidTagConversationIndex](pidtagconversationindex-canonical-property.md) et **PR_CONVERSATION_TOPIC**, de la propriété canonique [PidTagConversationTopic](pidtagconversationtopic-canonical-property.md), qui doit être utilisée à la place.
  
## <a name="see-also"></a>Voir aussi

- [Sous-arbre IPM](ipm-subtree.md)
- [Dossiers spéciaux MAPI](mapi-special-folders.md)

