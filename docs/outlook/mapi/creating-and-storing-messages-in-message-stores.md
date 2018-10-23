---
title: Création et stockage des messages dans des banques de messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cc74b31c-d7ed-4fcf-9535-a2f9222901b7
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: be718ea3ef4da91d2f85a0229f5a506198a2527f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589174"
---
# <a name="creating-and-storing-messages-in-message-stores"></a>Création et stockage des messages dans des banques de messages

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
La façon dont votre fournisseur de banques de messages crée et stocke les messages dans le mécanisme de stockage sous-jacent dépend fortement du mécanisme de stockage sous-jacent lui-même. En règle générale, vous devrez uniquement écrire du code pour conserver les propriétés d’un message et leurs valeurs.
  
Lorsque le fournisseur de banques de messages crée un message, il doit le créer avec les propriétés requises pour les messages. Une liste de ces propriétés est consultable dans la documentation relative à l’interface [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md). Après cela, les applications clientes ajoutent des propriétés supplémentaires avec les méthodes [IMAPIProp](imapipropiunknown.md). 
  
Lorsque le fournisseur de banques de messages enregistre un message dans le mécanisme de stockage sous-jacent, il doit effectuer une itération sur les propriétés du message et les enregistrer dans le mécanisme de stockage sous-jacent de façon à ce qu’elles puissent être récupérées entièrement si le message est ouvert ultérieurement.
  
MAPI exige que les propriétés sur les interfaces [IMessage](imessageimapiprop.md) soient traitées, ce qui signifie que les modifications apportées à celles-ci ne deviennent pas permanentes tant que la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) n’est pas appelée sur l’objet de message. Le fournisseur de banques de messages est responsable de l’implémentation de ce comportement. Cette opération n’est généralement pas compliquée. Elle consiste simplement à conserver les propriétés en mémoire pendant qu’elles sont modifiées et à les valider dans le mécanisme de stockage sous-jacent lorsque la méthode **SaveChanges** est appelée. 
  
Certaines propriétés sur les objets de message ont une sémantique spéciale pour les applications clientes par rapport à la méthode **SaveChanges**, comme suit : 
  
- Certaines propriétés doivent être en lecture/écriture avant que la méthode **SaveChanges** soit appelée, mais en lecture seule ensuite. Par exemple, la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) est initialement définie par l’application cliente qui crée le message (et est donc en lecture/écriture), mais ne peut pas être modifiée après le premier appel à **SaveChanges**.
    
- Certaines propriétés ont des relations spéciales avec les propriétés dans le dossier qui les contient ou avec les méthodes **IMAPIFolder**. Par exemple, la propriété **PR_MESSAGE_FLAGS** est liée aux indicateurs utilisés sur l’appel [IMAPIFolder::CreateMessage](imapifolder-createmessage.md). 
    
- Certaines propriétés peuvent ne pas être disponibles tant que **SaveChanges** n’est pas appelée pour la première fois. Par exemple, la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) peut ne pas être disponible tant que **SaveChanges** n’est pas appelée. 
    
- Certaines propriétés peuvent avoir des relations spéciales avec d’autres propriétés sur l’objet de message. Par exemple, la propriété **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) est généralement dérivée de la propriété **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) dans les fournisseurs de banques de messages prenant en charge les messages au format RTF.
    
- Certaines propriétés sont utilisées par plusieurs types d’objet liés à des banques de messages. Par exemple, la propriété **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) est requise sur les objets de dossier et de message ainsi que sur les objets de banque de messages.
    
Il incombe au fournisseur de banques de messages d’implémenter la sémantique correcte pour ces propriétés.
  
## <a name="see-also"></a>Voir aussi



[Implémentation des messages dans les banques de messages](implementing-messages-in-message-stores.md)

