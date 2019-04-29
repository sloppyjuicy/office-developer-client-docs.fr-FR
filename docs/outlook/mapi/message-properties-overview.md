---
title: Vue d'ensemble des propriétés de message
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
# <a name="message-properties-overview"></a>Vue d'ensemble des propriétés de message

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
MAPI divise les propriétés des messages en trois types:
  
- Propriétés du contenu du message.
    
- Transmission de messages, ou enveloppe, propriétés.
    
- Propriétés du destinataire du message.
    
Les propriétés de contenu de message décrivent le texte d'un message. Chaque classe de message possède son propre ensemble de propriétés de contenu. MAPI définit les propriétés de contenu des notes et des messages de rapport; Il revient aux clients et aux fournisseurs de banques de messages qui gèrent ces classes de messages à définir correctement les propriétés pour leurs implémentations. **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) et **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) sont des exemples de propriétés de contenu pour les messages de note. **PR_BODY** contient le contenu non mis en forme d'une note, tandis que **PR_RTF_COMPRESSED** contient la version compressée du contenu mis en forme d'une note. Pour plus d'informations sur les plages d'identificateurs de propriétés, consultez la rubrique [Property identifier Ranges](property-identifier-ranges.md).
  
Pour les nouvelles classes de message, les clients peuvent définir des propriétés spécifiques au contenu de l'une des deux façons suivantes:
  
- En utilisant des identificateurs de propriété dans la plage de propriétés de contenu de classe de message personnalisée: 0x6800 à 0x7BFF.
    
- À l'aide de propriétés nommées qui ont des identificateurs compris dans la plage 0x8000 à 0xFFFE.
    
La plage d'identificateur pour les propriétés de contenu de classe de message personnalisées est disponible pour tout client qui crée une classe de message personnalisée. Par conséquent, un identificateur de propriété dans cette plage peut être utilisé pour plusieurs classes de message. Les utilisateurs des propriétés de cette plage ne peuvent pas faire des suppositions quant au comportement des propriétés. 
  
Pour les propriétés nommées, les clients créent un nom qui spécifie un jeu de propriétés et soit une chaîne de caractères, soit une valeur numérique pour chaque nouvelle propriété. Les clients associent ensuite la propriété à un identificateur dans la plage de propriétés nommées. Les utilisateurs de propriétés nommées y accèdent par nom ou par identificateur via les méthodes [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) et [IMAPIProp:: GetNamesFromIDs](imapiprop-getnamesfromids.md) . 
  
Les propriétés d'enveloppe fournissent des informations qui permettent de transmettre un message d'un destinataire à un autre. Comme pour les propriétés de contenu de message, il est possible pour les clients ou les fournisseurs de services de définir leurs propres propriétés d'enveloppe afin de compléter celles définies par MAPI. Les clients et les fournisseurs de transport définissent les propriétés d'enveloppe que MAPI définit en fonction de la définition fournie par MAPI. Les fournisseurs de transport qui implémentent des fonctionnalités spéciales peuvent définir leurs propres propriétés d'enveloppe pour exposer ces fonctionnalités aux clients. MAPI met de côté une plage d'identificateurs de propriétés qui peuvent être utilisées pour ces propriétés spéciales définies par le fournisseur. Les fournisseurs de transport implémentent généralement une page de propriétés spéciale pour afficher ces propriétés et permettre aux clients de les modifier. **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) et **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) sont des exemples de propriétés d'enveloppe. Pour plus d'informations, reportez-vous à la rubrique [Property identifier Ranges](property-identifier-ranges.md).
  
Les propriétés des destinataires décrivent la destination d'un message envoyé. Un destinataire peut être un utilisateur de messagerie, une liste de distribution ou un ordinateur. Les propriétés de destinataire sont définies par MAPI et définies par les fournisseurs de services. Certaines propriétés de destinataire sont prises en charge par les fournisseurs de carnet d'adresses pour leur utilisateur de messagerie et leurs objets de liste de distribution; les autres propriétés de destinataire sont prises en charge par les clients, les fournisseurs de banques de messages ou les fournisseurs de transport. Par exemple, tous les destinataires nécessitent une adresse et un type d'adresse; Il s'agit des propriétés gérées par un fournisseur de carnets d'adresses lorsque le destinataire est stocké dans l'un de ses conteneurs. Les destinataires ont également un type, **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)), qui identifie un destinataire comme un destinataire principal, une copie carbone ou un destinataire en copie carbone invisible.
  
De nombreuses propriétés de message sont facultatives, ce qui signifie que les clients ne peuvent pas s'attendre à être disponibles ou définis sur des valeurs valides. Certaines propriétés de message sont requises mais disponibles uniquement lorsqu'un message est dans un état particulier. Par exemple, un message nouvellement créé ne doit pas obligatoirement avoir un identificateur d'entrée tant que le message n'a pas été enregistré, et il n'est pas nécessaire d'avoir une classe de message tant que le message n'est pas prêt à être soumis. Les clients doivent toujours vérifier les résultats de leurs appels [IMAPIProp:: GetProps](imapiprop-getprops.md) et [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) et avoir des valeurs par défaut prêtes comme sauvegarde au cas où une propriété demandée n'est pas disponible. 
  
La plupart des propriétés de message définies par les fournisseurs de services sont en lecture seule pour les clients. 
  
## <a name="see-also"></a>Voir aussi



[Messages MAPI](mapi-messages.md)

