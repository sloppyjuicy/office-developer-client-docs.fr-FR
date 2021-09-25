---
title: Vue d’ensemble de l’identificateur de propriété MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 957aa00f-23d8-4f3b-bbc2-7d54f17b47b5
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 83712c9a432c31e0a02d7eca39397a1bef92271d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59600812"
---
# <a name="mapi-property-identifier-overview"></a>Vue d’ensemble de l’identificateur de propriété MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Un identificateur de propriété est un nombre utilisé pour indiquer à quoi sert une propriété et qui en est responsable. Les identificateurs de propriété sont divisés par MAPI en plages ; où un identificateur se trouve dans la plage indique son utilisation et sa propriété. 
  
La plage d’identificateurs de propriété s’exécute de 0x0001 à 0xFFFF. Les identificateurs 0x0000 et 0xFFFF sont réservés dans tous les cas, ce qui signifie que ces identificateurs doivent rester inutilisés. La plage de propriétés définie par MAPI s’exécute de 0x0001 à 0x3FFF. Ces propriétés sont appelées propriétés définies par MAPI. La plage 0x4000 à 0x7FFF propriétés de message et de destinataire, et les clients ou fournisseurs de services peuvent définir des propriétés dans cette plage. Les propriétés de la plage 0x0001 à 0x7FFF sont appelées propriétés marquées. Au-0x8000 se trouve la plage des propriétés nommées ou des propriétés qui incluent un identificateur global unique (GUID) 32 bits et une chaîne de caractères Unicode ou une valeur numérique. Les clients peuvent utiliser des propriétés nommées pour personnaliser leur jeu de propriétés.
  
Les fournisseurs de services peuvent définir des propriétés de profil sécurisées dans la plage 0x67F0 par 0x67FF. Les propriétés de profil sécurisées sont utilisées pour les informations qui nécessitent une protection supplémentaire, telles que les mots de passe. Ces propriétés peuvent être masquées et chiffrées. Le fait que les propriétés sécurisées soient incluses ou non dans la liste par défaut des propriétés renvoyées par la méthode [IMAPIProp::GetPropList](imapiprop-getproplist.md) dépend de l’implémentation du fournisseur. Généralement, ces propriétés ne sont pas incluses. [L’interface IProfSect : IMAPIProp](iprofsectimapiprop.md) permet d’accéder aux propriétés d’une section de profil, y compris aux propriétés sécurisées. 
  
Certaines plages de propriétés sont limitées aux propriétés transmises ou nontransmitables. Les propriétés transférables sont transférées avec un message . les propriétés non transférables ne sont pas transférées avec un message. Les propriétés nontransmitables contiennent généralement des informations qui n’ont de valeur que pour les clients et les fournisseurs de services qui fonctionnent avec la session en cours. Ces propriétés ne seraient pas nécessairement utiles pour un autre système de messagerie et un autre ensemble de fournisseurs de services. Le concept de propriétés transmises s’applique principalement aux fournisseurs de transport. Pour déterminer si une propriété est transmise ou non, transmettez sa balise de propriété à la macro **FIsTransmittable,** définie dans le fichier d’en-tête Mapitags.h. 
  
Pour obtenir une description complète des plages d’identificateurs, voir [Plages d’identificateurs de propriété.](property-identifier-ranges.md)
  
## <a name="see-also"></a>Voir aussi



[Vue d’ensemble de la propriété MAPI](mapi-property-overview.md)

