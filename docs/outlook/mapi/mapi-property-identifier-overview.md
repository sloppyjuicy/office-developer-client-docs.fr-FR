---
title: Vue d'ensemble de l'identificateur de propriété MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 957aa00f-23d8-4f3b-bbc2-7d54f17b47b5
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 29626f49365a0f37f1e13d965c62bfd5ad0fb774
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328184"
---
# <a name="mapi-property-identifier-overview"></a>Vue d'ensemble de l'identificateur de propriété MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Un identificateur de propriété est un nombre qui est utilisé pour indiquer ce à quoi une propriété est utilisée et qui est responsable de celle-ci. Les identificateurs de propriétés sont divisés par MAPI en plages; l'emplacement où se trouve un identificateur dans la plage indique son utilisation et sa propriété. 
  
La plage d'identificateurs de propriétés s'exécute de 0x0001 à 0xFFFF. Les identificateurs de propriété 0x0000 et 0xFFFF sont réservés dans tous les cas, ce qui signifie que ces identificateurs doivent rester inutilisés. La plage de propriétés définie par MAPI s'exécute à partir de 0x0001 vers 0x3FFF. Ces propriétés sont désignées par le titre «propriétés MAPI». La plage 0x4000 à 0x7FFF appartient aux propriétés des messages et des destinataires, et les clients ou les fournisseurs de services peuvent définir des propriétés dans cette plage. Les propriétés de la plage 0x0001 à 0x7FFF sont appelées propriétés marquées. Au-delà de 0x8000 se trouve la plage pour ce qui est appelé propriétés nommées, ou les propriétés qui incluent un GUID (globally unique identifier) 32 bits et soit une chaîne de caractères, soit une valeur numérique. Les clients peuvent utiliser les propriétés nommées pour personnaliser leur jeu de propriétés.
  
Les fournisseurs de services peuvent définir des propriétés de profil sécurisées dans la plage 0x67F0 à 0x67FF. Les propriétés de profil sécurisé sont utilisées pour les informations qui nécessitent une protection supplémentaire, comme les mots de passe. Ces propriétés peuvent être masquées et chiffrées. Les propriétés sécurisées incluses ou non dans la liste par défaut des propriétés retournées par la méthode [IMAPIProp:: GetPropList](imapiprop-getproplist.md) dépendent de l'implémentation du fournisseur. En règle générale, ces propriétés ne sont pas incluses. L'interface [IProfSect: IMAPIProp](iprofsectimapiprop.md) est utilisée pour accéder aux propriétés d'une section de profil, y compris les propriétés sécurisées. 
  
Certaines plages de propriétés sont limitées aux propriétés transmissibles ou non transmissibles. Les propriétés transmissibles sont transférées avec un message; les propriétés non transmissibles ne sont pas transférées avec un message. Les propriétés non transmissibles contiennent généralement des informations qui sont de la valeur uniquement pour les clients et les fournisseurs de services fonctionnant avec la session en cours. Ces propriétés ne sont pas nécessairement utiles à un autre système de messagerie et un autre ensemble de fournisseurs de services. Le concept de propriétés transmissibles s'applique principalement aux fournisseurs de transport. Pour déterminer si une propriété est transmissible ou non, transmettez sa balise de propriété à la macro **FIsTransmittable** , définie dans le fichier d'en-tête Mapitags. h. 
  
Pour obtenir une description complète des plages d'identificateurs, voir la rubrique [Property identifier Ranges](property-identifier-ranges.md).
  
## <a name="see-also"></a>Voir aussi



[Vue d’ensemble de la propriété MAPI](mapi-property-overview.md)

