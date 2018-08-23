---
title: Balises de propriété MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 380dad4c-7fbf-4c49-b67c-ab612c923499
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 314d2d6987a8bc669239652b83a31b5927723c68
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22562924"
---
# <a name="mapi-property-tags"></a>Balises de propriété MAPI
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Une balise de propriété est un nombre à 32 bits qui contient un identificateur de la propriété unique en bits 31 à 16 et un type de propriété dans les bits 0 à 15, comme indiqué dans l’illustration suivante. 
  
**Éléments de balise de propriété**
  
![Éléments de balise de propriété] (media/amapi_10.gif "Éléments de balise de propriété")
  
Balises de propriété sont utilisés pour identifier les propriétés MAPI et chaque propriété doit contenir un, indépendamment de si la propriété est définie par MAPI, un client ou un fournisseur de services. MAPI définit un ensemble de constantes de la propriété tag pour ses propriétés dans le fichier d’en-tête Mapitags.h ; Ces propriétés sont appelées « propriétés définies par le MAPI ». 
  
Les constantes de balise de propriété suivent une convention d’affectation de noms pour la cohérence et la facilité d’utilisation. Il existe deux composants sur le nom de chaque balise de propriété : un préfixe PR_ et un ou plusieurs chaînes de caractères qui décrivent le contenu de la propriété. Plusieurs chaînes de caractères sont séparés par des traits de soulignement. Par exemple, la balise de propriété pour le type d’adresse d’un destinataire du message est **PR\_ADDRTYPE** ([PidTagOrgAddrtype](http://msdn.microsoft.com/library/d40b5707-e4d5-4746-88d4-8616a3789789%28Office.15%29.aspx)) et l’identificateur d’entrée pour le dossier désigné pour recevoir une copie de chaque message sortant est **PR_IPM_SENTMAIL_ Propriété ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)).
  
Macros quelques sont disponibles pour aider à travailler avec des balises de propriété entre eux [PROP_TYPE](prop_type.md), [PROP_ID](prop_id.md)et [PROP_TAG](prop_tag.md). **PROPRIÉTÉS\_TYPE** extrait le type de propriété de la balise de propriété ; **Propriétés\_ID** extrait l’identificateur. **PROP_TAG** génère une balise de propriété à partir d’un identificateur et le type de propriété. 
  
## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble de la propriété MAPI](mapi-property-overview.md)

