---
title: Noms de propriétés et jeux de propriétés
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cb216f5c-c965-4372-a15b-82090a410266
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 0272464d9a397f169b27aa15c80a17b49a3e9977
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571828"
---
# <a name="property-names-and-property-sets"></a>Noms de propriétés et jeux de propriétés

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Le nom de chaque propriété nommée comporte deux parties :
  
- Un identificateur global unique, ou le GUID, qui spécifie un jeu de propriétés.
    
- Une chaîne de caractères Unicode ou une valeur numérique 32 bits. 
    
Noms des propriétés nommées sont décrites à l’aide d’une structure [MAPINAMEID](mapinameid.md) . Cette structure contient un membre de jeu de propriétés, un membre pour indiquer le nom de format numérique ou chaîne et un membre pour identifier le format est utilisé. Étant donné que le jeu de propriétés fait partie du nom de la propriété, il n’est pas facultatif. MAPI a défini plusieurs jeux de propriétés pour une utilisation par les clients et les fournisseurs de service, mais si un ensemble existant de la propriété est inapproprié, un nouveau jeu de propriétés peut être défini. Clients et fournisseurs de services peuvent définir leurs propres jeux de propriétés en appelant la fonction [CoCreateGUID](http://msdn.microsoft.com/en-us/library/ms688568.aspx) . Ces jeux de propriétés est généralement créés pour les applications clientes personnalisées. 
  
Jeux de propriétés de MAPI sont représentés par l’une des constantes suivantes :
  
PS_MAPI
  
PS_PUBLIC_STRINGS
  
PS_ROUTING_EMAIL_ADDRESSES
  
PS_ROUTING_ADDRTYPE
  
PS_ROUTING_SEARCH_KEY
  
PS_ROUTING_DISPLAY_NAME
  
PS_ROUTING_ENTRYID
  
Le jeu de propriétés PS_MAPI est réservé. Il est utilisé par les fournisseurs de services pour générer des noms des propriétés avec des identificateurs au-dessous de la plage de la propriété nommée. Le jeu de propriétés PS_PUBLIC_STRINGS est utilisé par les clients pour les propriétés nommées de messages IPM. Étant donné que les propriétés nommées dans le jeu de propriétés PS_PUBLIC_STRINGS apparaissent dans l’interface utilisateur d’un client, messages non telles que celles qui appartiennent à la classe de message IPC Évitez de créer des propriétés avec ce jeu de propriétés nommées. Au lieu de cela, ils doivent créer des propriétés de la plage de spécifiques à la classe de message, 0x6800 via 0x7FFF.
  
Les autres jeux de propriétés contiennent des propriétés nommées décrivant les destinataires qui sont généralement des membres d’une liste de routage. Contenant le même type d’informations que les propriétés qui sont associées aux propriétés de la liste de destinataires, les propriétés de ces jeux de propriétés sont entendent par des passerelles nécessiter un mappage pour un système de messagerie cible. Car il existe cinq types d’informations pour décrire les propriétés, MAPI a défini cinq jeux de propriétés différentes. Un client envoie un message qui doit inclure une adresse et le type d’adresse pour ses membres de la liste Routage affecte une propriété nommée pour chaque membre de la PS_ROUTING_EMAIL_ADDRESSES et la propriété PS_ROUTING_ADDRTYPE définit. Cela garantit que l’adresse et le type d’adresse viabilité lorsque envoyé à un système de messagerie étranger.
  
## <a name="see-also"></a>Voir aussi



[MAPI des propri�t�s nomm�e](mapi-named-properties.md)

