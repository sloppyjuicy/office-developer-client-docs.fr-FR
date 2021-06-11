---
title: Vue d’ensemble des propriétés de message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 447f54de-9f0d-4f73-89b6-bed9cfea9c15
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 515b4637f99b806c5c5bc6304f107f62ca6d9091
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420247"
---
# <a name="message-properties-overview"></a>Vue d’ensemble des propriétés de message

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
MAPI divise les propriétés de message en trois types :
  
- Propriétés de contenu de message.
    
- Propriétés de transmission de message, ou d’enveloppe.
    
- Propriétés du destinataire du message.
    
Les propriétés de contenu de message décrivent le texte d’un message. Chaque classe de message possède son propre ensemble de propriétés de contenu. MAPI définit les propriétés de contenu pour les messages de note et de rapport ; C’est aux clients et aux fournisseurs de magasins de messages qui gèrent ces classes de messages de définir les propriétés appropriées pour leurs implémentations. **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) et **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) sont des exemples de propriétés de contenu pour les messages de note. **PR_BODY** contient le contenu non formaté d’une note, tandis que **PR_RTF_COMPRESSED** contient la version compressée du contenu formaté d’une note. Pour plus d’informations sur les plages d’identificateurs de propriété, voir [Plages d’identificateurs de propriété.](property-identifier-ranges.md)
  
Pour les nouvelles classes de message, les clients peuvent définir des propriétés spécifiques au contenu de deux manières :
  
- En utilisant des identificateurs de propriétés dans la plage de propriétés de contenu de classe de message personnalisée : 0x6800 à 0x7BFF.
    
- En utilisant des propriétés nommées qui ont des identificateurs qui se 0x8000 par 0xFFFE plage.
    
La plage d’identificateurs pour les propriétés de contenu de classe de message personnalisée est disponible pour tout client qui crée une classe de message personnalisée. Par conséquent, un identificateur de propriété dans cette plage peut être utilisé pour plusieurs classes de message. Les utilisateurs des propriétés de cette plage ne peuvent pas faire d’hypothèses sur le comportement des propriétés. 
  
Pour les propriétés nommées, les clients créent un nom qui spécifie un jeu de propriétés et une chaîne de caractères ou une valeur numérique pour chaque nouvelle propriété. Les clients associent ensuite la propriété à un identificateur dans la plage de propriétés nommée. Les utilisateurs de propriétés nommées y accèdent par leur nom ou leur identificateur via les méthodes [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) et [IMAPIProp::GetNamesFromIDs.](imapiprop-getnamesfromids.md) 
  
Les propriétés d’enveloppe fournissent des informations qui sont utilisées pour transmettre un message d’un destinataire à un autre. Comme pour les propriétés de contenu de message, il est possible pour les clients ou les fournisseurs de services de définir leurs propres propriétés d’enveloppe pour compléter celles définies par MAPI. Les clients et les fournisseurs de transport définissent les propriétés d’enveloppe que MAPI définit en fonction de la définition que MAPI fournit. Les fournisseurs de transport qui implémentent des fonctionnalités spéciales peuvent définir leurs propres propriétés d’enveloppe pour exposer ces fonctionnalités aux clients. MAPI met de côté une plage d’identificateurs de propriétés qui peuvent être utilisés pour ces propriétés spécifiques définies par un fournisseur. Les fournisseurs de transport implémentent généralement une page de propriétés spéciale pour afficher ces propriétés et permettre aux clients de les modifier. **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) et **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) sont des exemples de propriétés d’enveloppe. Pour plus d’informations, [voir Plages d’identificateurs de propriété.](property-identifier-ranges.md)
  
Les propriétés du destinataire décrivent la destination d’un message envoyé. Un destinataire peut être un utilisateur de messagerie, une liste de distribution ou un ordinateur. Les propriétés de destinataire sont définies par MAPI et définies par les fournisseurs de services. Certaines propriétés de destinataire sont pris en charge par les fournisseurs de carnets d’adresses pour leurs objets d’utilisateur de messagerie et de liste de distribution ; d’autres propriétés de destinataire sont pris en charge par les clients, les fournisseurs de magasins de messages ou les fournisseurs de transport. Par exemple, tous les destinataires nécessitent une adresse et un type d’adresse . Il s’agit des propriétés conservées par un fournisseur de carnet d’adresses lorsque le destinataire est stocké dans l’un de ses conteneurs. Les destinataires ont également un type, **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)), qui identifie un destinataire en tant que destinataire principal, en copie carbone ou en copie carbone non voyante.
  
De nombreuses propriétés de message sont facultatives, ce qui signifie que les clients ne peuvent pas s’attendre à ce qu’elles soient disponibles ou définies sur des valeurs valides. Certaines propriétés de message sont requises, mais disponibles uniquement lorsqu’un message se trouve dans un état particulier. Par exemple, un message nouvellement créé ne doit pas avoir d’identificateur d’entrée tant que le message n’a pas été enregistré et il n’est pas nécessaire d’avoir une classe de message tant que le message n’est pas prêt à être envoyé. Les clients doivent toujours vérifier les résultats de leurs appels [IMAPIProp::GetProps](imapiprop-getprops.md) et [IMAPIProp::OpenProperty](imapiprop-openproperty.md) et avoir des valeurs par défaut prêtes en tant que sauvegarde au cas où une propriété demandée serait indisponible. 
  
La plupart des propriétés de message définies par les fournisseurs de services sont en lecture seule pour les clients. 
  
## <a name="see-also"></a>Voir aussi



[MAPI Messages](mapi-messages.md)

