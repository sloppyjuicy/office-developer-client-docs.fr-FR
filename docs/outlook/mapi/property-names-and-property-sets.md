---
title: Noms de propriétés et jeux de propriétés
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cb216f5c-c965-4372-a15b-82090a410266
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: fa9d6afcaf1b360f37e8c8873c9d1a823fcd4888
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328545"
---
# <a name="property-names-and-property-sets"></a>Noms de propriétés et jeux de propriétés

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Le nom de chaque propriété nommée se compose de deux parties:
  
- Identificateur global unique, ou GUID, qui spécifie un jeu de propriétés.
    
- Chaîne de caractères Unicode ou valeur numérique 32 bits. 
    
Les noms des propriétés nommées sont décrits à l'aide d'une structure [MAPINAMEID](mapinameid.md) . Cette structure contient un membre de jeu de propriétés, un membre pour spécifier le nom au format numérique ou chaîne, ainsi qu'un membre pour identifier le format utilisé. Étant donné que le jeu de propriétés fait partie du nom de la propriété, il n'est pas facultatif. MAPI a défini plusieurs jeux de propriétés pour les clients et les fournisseurs de services, mais si un jeu de propriétés existant n'est pas approprié, un nouveau jeu de propriétés peut être défini. Les clients et les fournisseurs de services peuvent définir leurs propres jeux de propriétés en appelant la fonction [CoCreateGUID](https://msdn.microsoft.com/library/ms688568.aspx) . En règle générale, ces jeux de propriétés sont créés pour les applications clientes personnalisées. 
  
Les jeux de propriétés de MAPI sont représentés par les constantes suivantes:
  
PS_MAPI
  
PS_PUBLIC_STRINGS
  
PS_ROUTING_EMAIL_ADDRESSES
  
PS_ROUTING_ADDRTYPE
  
PS_ROUTING_SEARCH_KEY
  
PS_ROUTING_DISPLAY_NAME
  
PS_ROUTING_ENTRYID
  
Le jeu de propriétés PS_MAPI est réservé; Il est utilisé par les fournisseurs de services pour générer des noms pour les propriétés avec des identificateurs au-dessous de la plage de propriétés nommées. Le jeu de propriétés PS_PUBLIC_STRINGS est utilisé par les clients pour les propriétés nommées des messages IPM. Étant donné que les propriétés nommées dans le jeu de propriétés PS_PUBLIC_STRINGS s'affichent dans l'interface utilisateur d'un client, les messages invisibles, tels que ceux qui appartiennent à la classe de message IPC, doivent éviter de créer des propriétés nommées avec ce jeu de propriétés. Au lieu de cela, ils doivent créer des propriétés dans la plage spécifique à la classe de message, 0x6800 via 0x7FFF.
  
Les autres jeux de propriétés contiennent des propriétés nommées, qui décrivent les destinataires qui sont généralement membres d'une liste de routage. Contenant le même type d'informations que les propriétés associées aux propriétés de la liste de destinataires, les propriétés de ces jeux de propriétés sont comprises par les passerelles pour exiger le mappage pour un système de messagerie cible. Étant donné qu'il existe cinq types d'informations pour la description des propriétés, MAPI a défini cinq jeux de propriétés différents. Un client qui envoie un message qui doit inclure une adresse et un type d'adresse pour ses membres de la liste de routage affecte une propriété nommée pour chaque membre dans les jeux de propriétés PS_ROUTING_EMAIL_ADDRESSES et PS_ROUTING_ADDRTYPE. Cela garantit que l'adresse et le type d'adresse demeurent viables lors de l'envoi à un système de messagerie étranger.
  
## <a name="see-also"></a>Voir aussi



[MAPI des propri�t�s nomm�e](mapi-named-properties.md)

