---
title: Propriétés et objets MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 0aebf536-dcfb-406d-86ac-65db98c78139
ms.openlocfilehash: 666d88ae38dc44f66f9b9328b8c851fb1b910b2a
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63372513"
---
# <a name="mapi-objects-and-properties"></a>Propriétés et objets MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Certaines propriétés sont pris en charge par de nombreux types d’objets différents. Les propriétés suivantes sont des exemples de propriétés utilisées par plusieurs objets :
  
- **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) est un identificateur binaire utilisé pour ouvrir des objets.
    
- **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) est une constante utilisée pour identifier le type d’objet.
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) est une chaîne de caractères utilisée pour décrire un objet à l’utilisateur.
    
D’autres propriétés sont logiques pour un seul type d’objet. Les propriétés suivantes sont des exemples de propriétés qui s’appliquent à un type d’objet :
  
- **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) est une chaîne de caractères utilisée pour décrire le type d’un message.
    
- **PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md)) est un entier utilisé pour identifier une ligne dans un tableau.
    
- **PR_ATTACH_SIZE** ([PidTagAttachSize](pidtagattachsize-canonical-property.md)) est un nombre d’octets utilisé pour stocker le nombre d’octets dans une pièce jointe.
    
D’autres propriétés ne s’appliquent qu’à un seul type d’objet dans un état particulier. Les propriétés de ce type sont généralement des propriétés de message. Lorsqu’un message est créé pour la première fois, son ensemble de propriétés est très petit. Quand il est envoyé par un client à un destinataire via le système de messagerie, le nombre de propriétés nécessaires pour décrire le message augmente. Certaines de ces propriétés ajoutées apparaissent uniquement sur le message lors de sa livraison, tandis que d’autres apparaissent uniquement sur le message lors de son envoi. Les messages ont également des propriétés associées à la classe à laquelle ils appartiennent. Les messages de rapport, par exemple, ont des propriétés qui ne sont pas pris en charge par les messages d’autres classes, telles que les messages de note. 
  
Chaque objet possède certaines propriétés requises et peut ou non avoir d’autres propriétés facultatives. Les propriétés requises sont des propriétés qui doivent exister sur un objet pour que l’objet puisse être enregistré avec succès avec sa méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) . Les clients ou fournisseurs de services qui utilisent un objet peuvent dépendre de la disponibilité des propriétés **requises après l’appel de SaveChanges** . Autrement dit, ils peuvent s’assurer qu’un appel à la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) ou [IMAPIProp::OpenProperty](imapiprop-openproperty.md) pour récupérer ces propriétés réussira. 
  
Les propriétés facultatives sont des propriétés qui, selon l’implémenteur de l’objet, peuvent ou non être pris en charge par un objet. Un client ou un fournisseur de services utilisant l’objet ne peut pas s’attendre à ce que les propriétés facultatives soient disponibles via les méthodes **GetProps** ou **OpenProperty** et qu’elles soient définies sur des valeurs valides. 
  
Pour obtenir une liste ou des propriétés dans cette référence, voir [Propriétés MAPI](mapi-properties.md). Vous pouvez trouver des descriptions des propriétés appartenant à chacun des objets du magasin de messages et du carnet d’adresses dans la discussion de l’interface standard de l’objet. Par exemple, les propriétés de dossier sont abordées avec **IMAPIFolder** et les propriétés utilisateur de messagerie sont abordées **avec IMailUser**. Les propriétés de message, y compris les propriétés de message de rapport, sont **décrites avec IMessage** et dans [Message Properties Overview](message-properties-overview.md). Les propriétés appartenant à chacun des différents types de tables sont décrites dans la rubrique Tableaux [MAPI](mapi-tables.md) appropriée. Par exemple, les propriétés d’une table hiérarchique sont décrites dans [tables hiérarchiques](hierarchy-tables.md). Les propriétés appartenant à des serveurs de formulaires sont décrivant dans [le choix du jeu de propriétés d’un formulaire](choosing-a-form-s-property-set.md).
  
Lorsqu’un client ou un fournisseur de services appelle la méthode **GetProps** d’un objet pour récupérer plusieurs de ses propriétés et que l’une de ces propriétés n’est pas disponible, **GetProps** renvoie l’avertissement MAPI_W_ERRORS_RETURNED. L’appel est considéré comme réussi, car certaines propriétés ont été renvoyées. Lorsqu’un client ou un fournisseur de services appelle **OpenProperty** et que la propriété cible n’est pas disponible, la méthode échoue avec l’erreur MAPI_E_NOT_FOUND. Il est important de vérifier qu’une propriété demandée est renvoyée avant d’essayer d’y travailler. 
  
Selon l’objet, le fournisseur de services fournissant l’implémentation et la propriété, une propriété peut avoir une autorisation en lecture/écriture ou en lecture seule. L’autorisation en lecture/écriture permet à un client ou à un fournisseur de services d’utiliser la propriété pour modifier sa valeur . L’autorisation en lecture seule permet uniquement au fournisseur de services propriétaire de l’objet d’apporter des modifications. 
  
Pour savoir exactement quelles propriétés sont actuellement définies pour un objet, appelez [IMAPIProp::GetPropList](imapiprop-getproplist.md). La **méthode GetPropList** permet à un appelant de savoir ce qui est disponible avant d’essayer d’ouvrir une propriété potentiellement inexistante. Étant donné qu’il n’existe pas d’ensemble standard de propriétés prise en charge par tous les objets d’un type spécifique, il est impossible de deviner si un objet prend en charge une propriété particulière. **L’appel de GetPropList** élimine le travail d’estimation. 
  
## <a name="see-also"></a>Voir aussi



[Propriétés et objets MAPI](mapi-objects-and-properties.md)

