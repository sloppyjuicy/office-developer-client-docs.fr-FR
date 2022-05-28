---
title: attConversationID et attParentID
description: Décrit les attributs ConversationID et ParentID.
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: bed36900-e44d-434b-a4f2-d10f2d6f70da
ms.openlocfilehash: 5c58fe7118acbfa3fed2d9212ec1aca1af30ec60
ms.sourcegitcommit: 8c8e4ac05a6612dd5c815ab18ba40e56a6ba839d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2022
ms.locfileid: "65770844"
---
# <a name="attconversationid-and-attparentid"></a>attConversationID et attParentID

**S’applique à** : Outlook 2013 | Outlook 2016 
  
La Windows pour workgroups 3.1 Mail conversation key est une chaîne de texte. L’équivalent MAPI est une valeur binaire. Pour assurer la compatibilité descendante, l’implémentation TNEF convertit les données binaires en texte et ajoute un caractère Null de fin.
  
> [!NOTE]
> Les propriétés correspondantes dans MAPI auxquelles ces attributs TNEF sont mappés, PR_CONVERSATION_KEY et PR_PARENT_KEY, ont été dépréciées dans Microsoft Exchange Server : l’utilisation de **PR_CONVERSATION_KEY**, propriété [canonique PidTagConversationKey](pidtagconversationkey-canonical-property.md), persiste dans Outlook uniquement, pour localiser **IPM. Messages MessageManager**. 
  
## <a name="remarks"></a>Remarques

La propriété **PR_CONVERSATION_KEY** est le précurseur par ailleurs obsolète de la **PR_CONVERSATION_INDEX**, [propriété canonique PidTagConversationIndex](pidtagconversationindex-canonical-property.md) et **PR_CONVERSATION_TOPIC**, [propriété canonique PidTagConversationTopic](pidtagconversationtopic-canonical-property.md), qui doit être utilisée à la place.
  
## <a name="see-also"></a>Voir aussi

- [Sous-arborescence IPM](ipm-subtree.md)
- [Dossiers spéciaux MAPI](mapi-special-folders.md)

