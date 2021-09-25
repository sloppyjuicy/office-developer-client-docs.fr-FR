---
title: Balises de propriété MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 380dad4c-7fbf-4c49-b67c-ab612c923499
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: c0fb964b74539ea05cb638add5d3c964a992c3d9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567136"
---
# <a name="mapi-property-tags"></a>Balises de propriété MAPI
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Une balise de propriété est un nombre 32 bits qui contient un identificateur de propriété unique en bits 16 à 31 et un type de propriété en bits 0 à 15, comme illustré ci-après. 
  
**Éléments de balise de propriété**
  
![Éléments de balise de propriété](media/amapi_10.gif "Éléments de balise de propriété")
  
Les balises de propriété sont utilisées pour identifier les propriétés MAPI et chaque propriété doit en avoir une, que la propriété soit définie par MAPI, un client ou un fournisseur de services. MAPI définit un ensemble de constantes de balise de propriété pour ses propriétés dans le fichier d’en-tête Mapitags.h ; ces propriétés sont appelées « propriétés définies par MAPI ». 
  
Les constantes de balise de propriété suivent une convention d’attribution de noms pour des raisons de cohérence et de simplicité d’utilisation. Le nom de chaque balise de propriété est en deux parties : un préfixe PR_ et une ou plusieurs chaînes de caractères qui décrivent le contenu de la propriété. Plusieurs chaînes de caractères sont séparées par des traits de soulignement. Par exemple, la balise de propriété pour le type d’adresse d’un destinataire de message est **PR \_ ADDRTYPE** ([PidTagOrgAddrtype](https://msdn.microsoft.com/library/d40b5707-e4d5-4746-88d4-8616a3789789%28Office.15%29.aspx)) et l’identificateur d’entrée pour le dossier désigné pour recevoir une copie de chaque message sortant est **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)).
  
Quelques macros sont disponibles pour vous aider à utiliser des balises de propriété, parmi PROP_TYPE [,](prop_type.md) [PROP_ID](prop_id.md)et [PROP_TAG](prop_tag.md). **PROP \_ TYPE** extrait le type de propriété de la balise de propriété ; **PROP \_ L’ID** extrait l’identificateur. **PROP_TAG** crée une balise de propriété à partir d’un type de propriété et d’un identificateur. 
  
## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble de la propriété MAPI](mapi-property-overview.md)

