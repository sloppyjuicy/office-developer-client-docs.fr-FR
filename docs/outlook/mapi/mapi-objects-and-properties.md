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
ms.openlocfilehash: 7fef84b7519c7a9d6373198283e903fba4fd0780
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411210"
---
# <a name="mapi-objects-and-properties"></a>Propriétés et objets MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Certaines propriétés sont prises en charge par de nombreux types d'objets. Les propriétés suivantes sont des exemples de propriétés utilisées par plusieurs objets:
  
- **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) est un identificateur binaire utilisé pour ouvrir des objets.
    
- **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) est une constante utilisée pour identifier le type d'objet.
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) est une chaîne de caractères utilisée pour décrire un objet à l'utilisateur.
    
D'autres propriétés ont un sens pour un seul type d'objet. Les propriétés suivantes sont des exemples de propriétés qui s'appliquent à un type d'objet:
  
- **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) est une chaîne de caractères utilisée pour décrire le type d'un message.
    
- **PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md)) est un entier utilisé pour identifier une ligne dans un tableau.
    
- **PR_ATTACH_SIZE** ([PidTagAttachSize](pidtagattachsize-canonical-property.md)) est un entier utilisé pour stocker le nombre d'octets d'une pièce jointe.
    
Les autres propriétés ne s'appliquent qu'à un seul type d'objet dans un état particulier. Les propriétés de ce type sont généralement des propriétés de message. Lorsqu'un message est créé pour la première fois, son ensemble de propriétés est très petit. Lorsqu'il est envoyé par un client à un destinataire via le système de messagerie, le nombre de propriétés nécessaires pour décrire le message augmente. Certaines de ces propriétés ajoutées apparaissent uniquement sur le message lors de sa remise, tandis que d'autres apparaissent uniquement sur le message lors de son envoi. Les messages ont également des propriétés associées à la classe à laquelle ils appartiennent. Les messages de rapport, par exemple, ont des propriétés qui ne sont pas prises en charge par les messages d'autres classes, tels que les messages de note. 
  
Chaque objet possède des propriétés obligatoires et peut avoir d'autres propriétés facultatives ou non. Les propriétés obligatoires sont des propriétés qui doivent exister sur un objet pour pouvoir être enregistrées avec la méthode [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) . Les clients ou fournisseurs de services qui utilisent un objet peuvent dépendre de la disponibilité des propriétés requises après l'appel de **SaveChanges** . Autrement dit, ils peuvent s'assurer qu'un appel à la méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) ou [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) pour récupérer ces propriétés réussit. 
  
Les propriétés facultatives sont des propriétés qui, en fonction de l'implémentation de l'objet, peuvent ou non être prises en charge par un objet. Un client ou un fournisseur de services qui utilise l'objet ne peut pas s'attendre à ce que les propriétés facultatives soient disponibles via les méthodes **GetProps** ou **OpenProperty** et soient définies sur des valeurs valides. 
  
Pour obtenir une liste ou des propriétés dans la référence This, consultez la rubrique [MAPI Properties](mapi-properties.md). Vous trouverez des descriptions des propriétés appartenant à chacun des objets de banque de messages et de carnet d'adresses dans la rubrique relative à l'interface standard de l'objet. Par exemple, les propriétés de dossier sont abordées avec **IMAPIFolder** et les propriétés de l'utilisateur de messagerie sont traitées avec **IMailUser**. Les propriétés de message, y compris les propriétés de message de rapport, sont décrites avec **IMessage** et in [message Properties Overview](message-properties-overview.md). Les propriétés appartenant à chacun des différents types de tables sont décrites dans la rubrique [tables MAPI](mapi-tables.md) appropriées. Par exemple, les propriétés de la table de hiérarchie sont décrites dans la rubrique [tables de hiérarchie](hierarchy-tables.md). Les propriétés appartenant aux serveurs de formulaires décrivent [le choix du jeu de propriétés d'un formulaire](choosing-a-form-s-property-set.md).
  
Lorsqu'un client ou un fournisseur de services appelle la méthode **GetProps** d'un objet pour récupérer plusieurs de ses propriétés et que l'une de ces propriétés n'est pas disponible, **GETPROPS** renvoie le MAPI_W_ERRORS_RETURNED d'avertissement. L'appel est considéré comme réussi, car certaines propriétés ont été renvoyées. Lorsqu'un client ou un fournisseur de services appelle **OpenProperty** et que la propriété cible n'est pas disponible, la méthode échoue avec l'erreur MAPI_E_NOT_FOUND. Il est important de vérifier qu'une propriété demandée est renvoyée avant d'essayer de l'utiliser. 
  
En fonction de l'objet, du fournisseur de services qui fournit l'implémentation et de la propriété, une propriété peut avoir une autorisation en lecture/écriture ou en lecture seule. L'autorisation de lecture/écriture permet à un client ou un fournisseur de services qui utilise la propriété de modifier sa valeur; l'autorisation en lecture seule permet uniquement au fournisseur de services d'effectuer des modifications. 
  
Pour savoir exactement quelles propriétés sont actuellement définies pour un objet, appelez [IMAPIProp:: GetPropList](imapiprop-getproplist.md). La méthode **GetPropList** permet à un appelant de rechercher les éléments disponibles avant d'ouvrir une propriété potentiellement inexistante. Étant donné qu'il n'existe aucun ensemble standard de propriétés pris en charge par tous les objets d'un type spécifique, il est impossible de déterminer si un objet prend ou non en charge une propriété particulière. L'appel de **GetPropList** élimine le travail de découverte. 
  
## <a name="see-also"></a>Voir aussi



[Propriétés et objets MAPI](mapi-objects-and-properties.md)

