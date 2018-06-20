---
title: Vue d’ensemble des propriétés de message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 447f54de-9f0d-4f73-89b6-bed9cfea9c15
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 78e2f63746a866603bc2392fbe5c8bb25d3f38c5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784887"
---
# <a name="message-properties-overview"></a>Vue d’ensemble des propriétés de message

  
  
**S’applique à**: Outlook 
  
MAPI divise en trois types de plusieurs propriétés de message :
  
- Propriétés de contenu de message.
    
- Propriétés de transmission ou enveloppe de message.
    
- Propriétés de destinataire de message.
    
Propriétés de message contenues décrivent le texte d’un message. Chaque classe de message possède son propre jeu de propriétés de contenu. MAPI définissant les propriétés de contenu pour les messages de rapport et de la note ; Ce sont les clients et les fournisseurs de magasins de message qui prennent en charge ces classes de messages pour définir les propriétés de manière appropriée pour leurs implémentations. **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) et **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) sont des exemples de propriétés de contenu pour les messages de la note. **PR_BODY** contient le contenu non mis en forme d’une note, tandis que **PR_RTF_COMPRESSED** contient la version compressée du contenu mis en forme d’une note. Pour plus d’informations sur les plages d’identificateur de propriété, voir la [Propriété identificateur de plages](property-identifier-ranges.md).
  
Pour les nouvelles classes de message, clients pouvant définir des propriétés spécifiques au contenu de deux façons :
  
- Dans la plage de propriétés de contenu de classe de message personnalisé à l’aide des identificateurs de propriété : 0x6800 via 0x7BFF.
    
- À l’aide des propriétés qui ont des identificateurs qui peuvent être classées dans les 0 x 8000 0xFFFE plage nommées.
    
La plage d’identificateurs de propriétés de contenu de classe de message personnalisé est disponible pour tout client qui crée une classe de message personnalisé. Par conséquent, un identificateur de propriété dans cette plage peut être utilisé pour plusieurs classes de message. Les utilisateurs des propriétés dans cette plage ne peut pas faire des suppositions quant le comportement des propriétés. 
  
Pour les propriétés nommées, les clients créer un nom qui spécifie un jeu de propriétés et une chaîne de caractères ou une valeur numérique pour chaque nouvelle propriété. Ensuite, les clients associer la propriété avec un identificateur de la plage de la propriété nommée. Les utilisateurs des propriétés nommées y accéder par nom ou l’identificateur via les méthodes [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) et [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) . 
  
Propriétés d’enveloppe fournissent des informations qui sont utilisées pour transmettre un message à partir d’un destinataire à une autre. Comme avec les propriétés de contenu de message, il est possible pour les clients ou fournisseurs de services définir leurs propres propriétés d’enveloppe complètent celles qui définit MAPI. Clients et fournisseurs de transport définir les propriétés d’enveloppe qui définit MAPI basées sur la définition MAPI propose. Fournisseurs de transport qui implémentent des fonctionnalités spécifiques peuvent définir leurs propres propriétés d’enveloppe pour exposer les fonctionnalités aux clients. MAPI met de côté une plage d’identificateurs de propriété peut être utilisée pour ces propriétés spéciales défini par le fournisseur. Fournisseurs de transport implémentent généralement une page de propriétés spéciale pour afficher ces propriétés et activer des clients pour les modifier. **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) et **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) sont des exemples de propriétés d’enveloppe. Pour plus d’informations, voir [Propriété identificateur de plages](property-identifier-ranges.md).
  
Propriétés de destinataire décrivent la destination d’un message envoyé. Un destinataire peut être un utilisateur de messagerie, liste de distribution ou d’un ordinateur. Propriétés de destinataire sont définies par MAPI et définies par les fournisseurs de services. Certaines propriétés de destinataire sont pris en charge par les fournisseurs de carnet d’adresses pour leur utilisateur de messagerie et les objets de liste de distribution ; autres propriétés de destinataire sont pris en charge par les clients, les fournisseurs de magasins de message ou des fournisseurs de transport. Par exemple, tous les destinataires nécessitent une adresse et un type d’adresse ; Il s’agit des propriétés gérées par un fournisseur de carnet d’adresses lorsque le destinataire est stocké dans un de ses conteneurs. Destinataires ont également un type, **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)), qui identifie un destinataire en tant qu’un principal, copie carbone ou destinataires en copie carbone invisible.
  
De nombreuses propriétés de message sont facultatifs, ce qui signifie que les clients ne peuvent pas attendais disponibles ou défini à des valeurs valides. Certaines propriétés de message sont requis mais disponible uniquement lorsqu’un message est dans un état particulier. Par exemple, un message nouvellement créé n’est pas nécessaire de posséder un identificateur d’entrée jusqu'à une fois que le message a été enregistré, et il n’est pas nécessaire d’avoir une classe de message jusqu'à ce que le message est prêt à être envoyé. Les clients doivent toujours vérifier les résultats de leurs appels [IMAPIProp::GetProps](imapiprop-getprops.md) et [IMAPIProp::OpenProperty](imapiprop-openproperty.md) et ont des valeurs par défaut prêts en tant que sauvegarde au cas où une propriété demandée n’est pas disponible. 
  
La plupart des propriétés de message pour définissent des fournisseurs de services sont en lecture seule aux clients. 
  
## <a name="see-also"></a>Voir aussi



[Messages MAPI](mapi-messages.md)

