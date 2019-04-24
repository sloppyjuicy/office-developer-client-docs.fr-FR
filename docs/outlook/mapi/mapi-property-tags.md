---
title: Balises de propriété MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 380dad4c-7fbf-4c49-b67c-ab612c923499
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 96211d3b6e1e4dfbd4c93a98c8dd04de10eac884
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328233"
---
# <a name="mapi-property-tags"></a>Balises de propriété MAPI
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Une balise de propriété est un nombre de 32 bits qui contient un identificateur de propriété unique en bits 16 à 31 et un type de propriété en bits 0 à 15, comme indiqué dans l'illustration suivante. 
  
**Éléments de balise de propriété**
  
![Éléments] de baliSe de propriété (media/amapi_10.gif "Éléments") de baliSe de propriété
  
Les balises de propriété sont utilisées pour identifier les propriétés MAPI et chaque propriété doit en avoir un, que la propriété soit définie par MAPI, un client ou un fournisseur de services. MAPI définit un ensemble de constantes de balise de propriété pour ses propriétés dans le fichier d'en-tête Mapitags. h; ces propriétés sont désignées par le titre «propriétés définies par MAPI». 
  
Les constantes de balise property suivent une convention d'affectation de noms pour la cohérence et la facilité d'utilisation. Le nom de chaque balise de propriété se répartit en deux parties: un préfixe PR_ et une ou plusieurs chaînes de caractères qui décrivent le contenu de la propriété. Les chaînes de caractères multiples sont séparées par des traits de soulignement. Par exemple, la balise de propriété pour le type d'adresse d'un destinataire de message est **PR\_ADDRTYPE** ([PidTagOrgAddrtype](https://msdn.microsoft.com/library/d40b5707-e4d5-4746-88d4-8616a3789789%28Office.15%29.aspx)) et l'identificateur d'entrée du dossier désigné pour recevoir une copie de chaque message sortant est **PR_IPM_SENTMAIL_ ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)).
  
Quelques macros sont disponibles pour vous aider à utiliser les balises de propriété, parmi celles-ci [PROP_TYPE](prop_type.md), [PROP_ID](prop_id.md)et [PROP_TAG](prop_tag.md). **Type\_prop** extrait le type de propriété de la balise de propriété; **ID\_de prop** extrait l'identificateur. **PROP_TAG** crée une balise de propriété à partir d'un type et d'un identificateur de propriété. 
  
## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble de la propriété MAPI](mapi-property-overview.md)

