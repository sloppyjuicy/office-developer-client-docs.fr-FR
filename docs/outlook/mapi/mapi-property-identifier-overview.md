---
title: Vue d’ensemble de l’identificateur de propriété MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 957aa00f-23d8-4f3b-bbc2-7d54f17b47b5
ms.openlocfilehash: daab1f72b997b37a6a8a1e4eec5ff47f2536da63
ms.sourcegitcommit: b8c11491410ea058cfb559c2b83030d94c072bd7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/13/2022
ms.locfileid: "66755568"
---
# <a name="mapi-property-identifier-overview"></a>Vue d’ensemble de l’identificateur de propriété MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Un identificateur de propriété est un nombre utilisé pour indiquer à quoi une propriété est utilisée et qui en est responsable. Les identificateurs de propriété sont divisés par MAPI en plages ; où un identificateur se trouve dans la plage indique son utilisation et sa propriété. 
  
La plage d’identificateurs de propriétés s’exécute de 0x0001 à 0xFFFF. Les identificateurs de propriété 0x0000 et 0xFFFF sont réservés dans tous les cas, ce qui signifie que ces identificateurs doivent rester inutilisés. La plage de propriétés définies par MAPI s’exécute de 0x0001 à 0x3FFF. Ces propriétés sont appelées propriétés définies par MAPI. La plage 0x4000 à 0x7FFF appartient aux propriétés de message et de destinataire, et les clients ou fournisseurs de services peuvent définir des propriétés dans cette plage. Les propriétés de la plage de 0x0001 à 0x7FFF sont appelées propriétés marquées. Au-delà de 0x8000 se trouve la plage de propriétés nommées, ou propriétés qui incluent un identificateur global unique (GUID) 128 bits et une chaîne de caractères Unicode ou une valeur numérique 32 bits. Les clients peuvent utiliser des propriétés nommées pour personnaliser leur jeu de propriétés.
  
Les fournisseurs de services peuvent définir des propriétés de profil sécurisées dans la plage 0x67F0 via 0x67FF. Les propriétés de profil sécurisé sont utilisées pour les informations qui nécessitent une protection supplémentaire, telles que les mots de passe. Ces propriétés peuvent être masquées et chiffrées. La présence ou non de propriétés sécurisées dans la liste par défaut des propriétés retournées par la méthode [IMAPIProp::GetPropList](imapiprop-getproplist.md) dépend de l’implémentation du fournisseur. En règle générale, ces propriétés ne sont pas incluses. L’interface [IProfSect : IMAPIProp](iprofsectimapiprop.md) est utilisée pour accéder aux propriétés d’une section de profil, y compris les propriétés sécurisées. 
  
Certaines plages de propriétés sont limitées aux propriétés transmissibles ou non transférables. Les propriétés transmissibles sont transférées avec un message ; Les propriétés non transférables ne sont pas transférées avec un message. Les propriétés non transférables contiennent généralement des informations qui sont de valeur uniquement pour les clients et les fournisseurs de services qui opèrent avec la session active. Ces propriétés ne seraient pas nécessairement utiles à un autre système de messagerie et à un autre ensemble de fournisseurs de services. Le concept de propriétés transmissibles s’applique principalement aux fournisseurs de transport. Pour déterminer si une propriété peut être transmise ou non, transmettez sa balise de propriété à la macro **FIsTransmittable** , définie dans le fichier d’en-tête Mapitags.h. 
  
Pour obtenir une description complète des plages d’identificateurs, consultez [Plages d’identificateurs de propriétés](property-identifier-ranges.md).
  
## <a name="see-also"></a>Voir aussi



[Vue d’ensemble de la propriété MAPI](mapi-property-overview.md)

