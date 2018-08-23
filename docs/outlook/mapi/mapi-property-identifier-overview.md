---
title: Vue d’ensemble d’identificateur de propriété MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 957aa00f-23d8-4f3b-bbc2-7d54f17b47b5
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 8cf2f08a69ee87c40789b764596e514c91483c2e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563155"
---
# <a name="mapi-property-identifier-overview"></a>Vue d’ensemble d’identificateur de propriété MAPI

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Un identificateur de propriété est un nombre qui est utilisé pour indiquer qu’une propriété est utilisée pour et qui est responsable. Identificateurs de propriété sont divisées par MAPI plages ; où un identificateur fait partie de la plage indique son utilisation et propriété. 
  
La plage d’identificateurs de propriété ne s’exécute à partir de 0 x 0001 0xFFFF. Identificateurs de propriété 0 x 0000 et 0xFFFF sont réservés dans tous les cas, ce qui signifie que ces identificateurs doivent demeurer inutilisés. La plage de propriétés définies par MAPI s’exécute de 0 x 0001 à 0x3FFF. Ces propriétés sont appelées propriétés MAPI. La plage 0 x 4000 à 0x7FFF appartient à un message et des propriétés de destinataire, et des clients ou fournisseurs de services peuvent définir les propriétés dans cette plage. Propriétés de la plage de 0 x 0001 à 0x7FFF sont appelées propriétés avec balise. Au-delà de 0 x 8000 est la plage de ce qui est appelé propriétés nommées, ou des propriétés qui incluent un identificateur global unique de 32 bits (GUID) et une chaîne de caractères Unicode ou valeur numérique. Clients peuvent utiliser des propriétés nommées pour personnaliser leur jeu de propriétés.
  
Fournisseurs de services peuvent définir des propriétés de profil sécurisé dans la plage 0x67F0 via 0x67FF. Sécurisation du profil de propriétés sont utilisées pour plus d’informations qui requiert une protection supplémentaire, telles que les mots de passe. Ces propriétés peuvent être masquées et chiffrées. Ou non les propriétés sécurisées sont incluses dans la liste par défaut des propriétés renvoyées par la méthode [IMAPIProp::GetPropList](imapiprop-getproplist.md) dépend de l’implémentation du fournisseur. Généralement ces propriétés ne sont pas incluses. La [IProfSect : IMAPIProp](iprofsectimapiprop.md) interface est utilisée pour accéder aux propriétés d’une section de profil, y compris les propriétés d’informations sécurisé. 
  
Certains des plages de propriété sont limitées aux propriétés transmissible ou nontransmittable. Propriétés transmissible sont transférées avec un message ; propriétés nontransmittable ne sont pas transférées avec un message. Propriétés Nontransmittable contient généralement des informations qui sont uniquement pour les clients et les fournisseurs de service d’utilisation de la session en cours. Ces propriétés pas nécessairement serait utiles à un autre système de messagerie et un autre jeu de fournisseurs de services. Le concept des propriétés transmissible s’applique principalement aux fournisseurs de transport. Pour déterminer si une propriété est transmissible ou non, passez la balise de propriété à la macro **FIsTransmittable** , définie dans le fichier d’en-tête Mapitags.h. 
  
Pour une description complète des plages identificateur, voir [Propriété identificateur de plages](property-identifier-ranges.md).
  
## <a name="see-also"></a>Voir aussi



[Vue d’ensemble de la propriété MAPI](mapi-property-overview.md)

