---
title: Mappages et signatures de mappages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 773f6671-cc21-4d1f-a11d-308bc71c852d
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: b5c8fd8c757de995e2a2e4239be614cf171fcb44
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566186"
---
# <a name="mappings-and-mapping-signatures"></a>Mappages et signatures de mappages

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Lorsqu’un fournisseur de services prend en charge les propriétés nommées, chaque jeu de paires identificateur et le nom est appelé un mappage. Fournisseurs de services peuvent prendre en charge un mappage ou plusieurs. Qui est un fournisseur de banque de messages, par exemple, peut implémenter les méthodes **GetIDsFromNames** et **GetNamesFromIDs** pour toutes ses messages, dossier et objets de banque de messages pour fonctionner avec une seule liste de noms et de leurs identificateurs correspondants. Un autre fournisseur de banque de messages peut-être avoir une liste de tous les dossiers et les messages qu’il contient ou implémenter une liste unique pour chaque message et chaque dossier. Les fournisseurs de magasins de message qui utilisent un mappage unique pour chaque message ne doivent pas autoriser les propriétés nommées apparaissent dans les tables de contenu de dossier, car un nom de propriété donné, l’identificateur de la propriété sera différent à partir du message à. MAPI recommande que les fournisseurs de simplicité et fonctionnent avec une seule liste pour tous les objets, y compris les tables. 
  
Pour le mappage de tous les fournisseurs de services doivent fournir une signature de mappage. Une signature de mappage est une valeur binaire, généralement un GUID qui identifie de manière unique un ensemble d’identificateurs de propriété et les noms correspondants. Mappage des signatures sont stockés dans la propriété **PR_MAPPING_SIGNATURE** ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md)) d’un objet. Fournisseurs de services doivent changer la valeur de leur propriété **PR_MAPPING_SIGNATURE** chaque fois qu’une modification est apportée au mappage qu’il représente. Par exemple, **PR_MAPPING_SIGNATURE** doit être mis à jour si un nouvel identificateur est affecté à un nom ou un nouveau nom et identificateur paire est ajoutée. 
  
Clients fonctionnant avec les propriétés des objets nommées utilisent les propriétés des objets **PR_MAPPING_SIGNATURE** dans les opérations de comparaison et de copie. Pour comparer nommés identificateurs appartenant aux deux objets, les clients ne pas à l’aide de signatures de mappage doivent appeler [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) sur les deux objets pour récupérer les noms de chacun des identificateurs de propriété. À l’aide de signatures de mappage d’objets peut rendre cet appel inutile. Lorsque deux objets ont la même valeur pour leurs propriétés **PR_MAPPING_SIGNATURE** , ils utilisent le même mappage. Les identificateurs qui utilisent le même mappage peuvent être comparées directement. Fournisseurs de services qui implémentent [IMAPIProp::CopyTo](imapiprop-copyto.md) et [IMAPIProp::CopyProps](imapiprop-copyprops.md) peuvent également tirer parti de signature de mappage d’un objet. Lors de la copie des propriétés entre les objets nommées, les fournisseurs de services peuvent éviter l’étape de conversion lorsque les objets source et de destination ont la même signature de mappage. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIProp : IUnknown](imapipropiunknown.md)


[MAPI des propri�t�s nomm�e](mapi-named-properties.md)

