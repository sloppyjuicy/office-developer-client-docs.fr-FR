---
title: Propriétés et objets MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0aebf536-dcfb-406d-86ac-65db98c78139
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 7ba58cc87b0eefe6c6ff70994d887d7f83e713b3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592401"
---
# <a name="mapi-objects-and-properties"></a>Propriétés et objets MAPI

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Certaines propriétés sont pris en charge par les différents types d’objets. Les propriétés suivantes sont des exemples de propriétés qui sont utilisées par plusieurs objets :
  
- **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) est un identificateur binaire utilisé pour ouvrir des objets.
    
- **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) est une constante utilisée pour identifier le type d’objet.
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) est une chaîne de caractères utilisée pour décrire un objet à l’utilisateur.
    
Autres propriétés pertinent pour un seul type d’objet. Les propriétés suivantes sont des exemples de propriétés qui s’appliquent à un type d’objet :
  
- **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) est une chaîne de caractères utilisée pour décrire le type d’un message.
    
- **PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md)) est un entier utilisé pour identifier une ligne dans une table.
    
- **PR_ATTACH_SIZE** ([PidTagAttachSize](pidtagattachsize-canonical-property.md)) est un entier utilisé pour stocker le nombre d’octets dans une pièce jointe.
    
Toujours les autres propriétés sont applicables uniquement pour un seul type d’objet dans un état particulier. Propriétés de ce type sont généralement des propriétés de message. Lorsque vous créez un message, son jeu de propriétés est très faible. Il est envoyé par un client à un destinataire dans le système de messagerie, augmente le nombre de propriétés nécessaires pour décrire le message. Certaines de ces propriétés ajoutées apparaissent uniquement sur le message comme il est envoyé alors que d’autres personnes apparaissent uniquement sur le message lors de son envoi. Les messages ont également des propriétés qui sont associées à la classe à laquelle ils appartiennent. Signaler des messages, par exemple, ont des propriétés qui ne sont pas pris en charge par les messages d’autres classes, tels que les messages de la note. 
  
Chaque objet a certaines propriétés requises et peut ou peut-être pas les autres propriétés facultatives. Les propriétés requises doit exister sur un objet que l’objet puisse être correctement enregistré avec la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) . Clients ou fournisseurs de services à l’aide d’un objet dépend de la disponibilité des propriétés requises après l’appel de **SaveChanges** . Autrement dit, ils peuvent être certain qu’un appel à la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) ou la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) de l’objet à récupérer ces propriétés réussira. 
  
Facultatives les propriétés, en fonction de l’implémentation de l’objet, peut ou ne peut pas être pris en charge par un objet. Un client ou fournisseur de services à l’aide de l’objet ne vous attendez pas les propriétés facultatives disponibles via les méthodes **GetProps** ou **OpenProperty** et pour définir des valeurs valides. 
  
Pour une liste ou des propriétés dans cette référence, voir [Propriétés MAPI](mapi-properties.md). Stockent les descriptions de propriétés qui appartiennent à chaque message et objets de carnet d’adresses, voir la description de l’interface standard de l’objet. Par exemple, les propriétés de dossier sont abordées avec **IMAPIFolder** et des propriétés utilisateur messagerie sont présentées avec **IMailUser**. Propriétés de message, y compris les propriétés de message d’état, sont décrites avec **IMessage** et dans la [Vue d’ensemble des propriétés de Message](message-properties-overview.md). Propriétés qui appartiennent à chacune des différents types de tables sont décrits dans la rubrique appropriée de [MAPI Tables](mapi-tables.md) . Par exemple, les propriétés de table de hiérarchie sont décrits dans les [Tables de hiérarchie](hierarchy-tables.md). Propriétés qui appartiennent aux serveurs de formulaire sont décrivant lors du [choix de la valeur de propriété d’un formulaire](choosing-a-form-s-property-set.md).
  
Lorsqu’un client ou fournisseur de services appelle la méthode **GetProps** d’un objet pour extraire plusieurs de ses propriétés et une de ces propriétés n’est pas disponible, **GetProps** renvoie l’avertissement MAPI_W_ERRORS_RETURNED. L’appel est considéré comme étant réussi, car certaines propriétés ont été retournés. Lorsqu’un client ou service fournisseur appelle **OpenProperty** et la propriété cible n’est pas disponible, la méthode échoue avec l’erreur MAPI_E_NOT_FOUND. Il est important de vérifier qu’une propriété demandée est retournée avant d’essayer de l’utiliser. 
  
En fonction de l’objet, le fournisseur de services en fournissant l’implémentation et la propriété, une propriété attribuable en lecture/écriture ou autorisation en lecture seule. Autorisation de lecture/écriture permet à un fournisseur de client ou le service à l’aide de la propriété pour modifier sa valeur ; autorisation en lecture seule permet uniquement le fournisseur de services propriétaire de l’objet apporter des modifications. 
  
Pour déterminer exactement quelles propriétés sont actuellement définies pour un objet, appelez [IMAPIProp::GetPropList](imapiprop-getproplist.md). La méthode **GetPropList** permet à un appelant de savoir ce qui est disponible avant une tentative d’ouvrir une propriété potentiellement inexistante. Car il n’existe aucun ensemble standard de propriétés qui prennent en charge de tous les objets d’un type spécifique, il est impossible à deviner ou non un objet prend en charge une propriété particulière. L’appel **GetPropList** élimine le travail. 
  
## <a name="see-also"></a>Voir aussi



[Propriétés et objets MAPI](mapi-objects-and-properties.md)

