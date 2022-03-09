---
title: Cr�ation et le stockage des Messages dans les banques de messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: cc74b31c-d7ed-4fcf-9535-a2f9222901b7
ms.openlocfilehash: b5e8dd51ab102b31cfc3b13e283d2c54c69f215a
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63371162"
---
# <a name="creating-and-storing-messages-in-message-stores"></a>Création et stockage des messages dans des banques de messages

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
La façon dont votre fournisseur de banques de messages crée et stocke les messages dans le mécanisme de stockage sous-jacent dépend fortement du mécanisme de stockage sous-jacent lui-même. En règle générale, vous devrez uniquement écrire du code pour conserver les propriétés d’un message et leurs valeurs.
  
Lors de la banque de messages fournisseur cr�e un nouveau message, le fournisseur a besoin cr�er le message avec les propri�t�s requises pour les messages. Vous trouverez une liste de ces propri�t�s dans la documentation relative � la [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md) interface. Apr�s cela, les applications clientes ajouter des propri�t�s suppl�mentaires avec les m�thodes [IMAPIProp](imapipropiunknown.md) . 
  
Lors de la banque de messages fournisseur enregistre un message dans le m�canisme de stockage sous-jacent, le fournisseur a besoin effectuer une it�ration sur les propri�t�s de message, puis enregistrez-les dans le m�canisme de stockage sous-jacent, tels qu'ils peuvent �tre enti�rement r�cup�r�s si le message est ouvert par la suite.
  
MAPI exige que les propri�t�s sur les interfaces [IMessage](imessageimapiprop.md) sont trait�es, ce qui signifie que les modifications apport�es � leur ne sont pas d�finitive jusqu'� ce que la m�thode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) est appel�e sur l'objet du message. Le fournisseur de banque de messages est responsable de l'impl�mentation de ce comportement. Cela n'est g�n�ralement pas difficile ; Cela signifie simplement que contenant des propri�t�s en m�moire pendant qu'ils sont en cours de modification et les rendre permanentes dans le m�canisme de stockage sous-jacent lorsque **SaveChanges** est appel�e. 
  
Certaines propri�t�s d'objets de message ont une s�mantique sp�ciale pour les applications clientes par rapport � la m�thode **SaveChanges**, comme suit : 
  
- Certaines propriétés doivent être en lecture/écriture avant que la méthode **SaveChanges** soit appelée, mais en lecture seule ensuite. Par exemple, la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) est initialement définie par l’application cliente qui crée le message (et est donc en lecture/écriture), mais ne peut pas être modifiée après le premier appel à **SaveChanges**.
    
- Certaines propriétés ont des relations spéciales avec les propriétés dans le dossier qui les contient ou avec les méthodes **IMAPIFolder**. Par exemple, la propriété **PR_MESSAGE_FLAGS** est liée aux indicateurs utilisés sur l’appel [IMAPIFolder::CreateMessage](imapifolder-createmessage.md). 
    
- Certaines propriétés peuvent ne pas être disponibles tant que **SaveChanges** n’est pas appelée pour la première fois. Par exemple, la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) peut ne pas être disponible tant que **SaveChanges** n’est pas appelée. 
    
- Certaines propriétés peuvent avoir des relations spéciales avec d’autres propriétés sur l’objet de message. Par exemple, la propriété **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) est généralement dérivée de la propriété **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) dans les fournisseurs de banques de messages prenant en charge les messages au format RTF.
    
- Certaines propriétés sont utilisées par plusieurs types d’objet liés à des banques de messages. Par exemple, la propriété **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) est requise sur les objets de dossier et de message ainsi que sur les objets de banque de messages.
    
Il incombe au fournisseur de banques de messages d’implémenter la sémantique correcte pour ces propriétés.
  
## <a name="see-also"></a>Voir aussi



[Implémentation des messages dans les banques de messages](implementing-messages-in-message-stores.md)

