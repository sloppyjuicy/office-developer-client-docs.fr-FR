---
title: Mappages et signatures de mappage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 773f6671-cc21-4d1f-a11d-308bc71c852d
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: cd26ce4bc2da3da639b4a611fc9a69f39b13e5f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410013"
---
# <a name="mappings-and-mapping-signatures"></a>Mappages et signatures de mappage

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lorsqu’un fournisseur de services prend en charge les propriétés nommées, chaque ensemble de paires d’identificateurs et de noms est appelé mappage. Les fournisseurs de services peuvent prendre en charge un ou plusieurs mappages. Autrement dit, un fournisseur de magasin de messages, par exemple, peut implémenter les méthodes **GetIDsFromNames** et **GetNamesFromIDs** pour tous ses objets message, dossier et magasin de messages pour fonctionner avec une seule liste de noms et leurs identificateurs correspondants. Un autre fournisseur de magasins de messages peut avoir une liste pour chaque dossier et les messages qu’il contient, ou implémenter une liste unique pour chaque message et chaque dossier. Les fournisseurs de magasins de messages qui utilisent un mappage unique pour chaque message ne doivent pas autoriser les propriétés nommées à apparaître dans leurs tables de contenu de dossier, car pour un nom de propriété donné, l’identificateur de propriété diffère d’un message à l’autre. MAPI recommande aux fournisseurs de les conserver simples et de fonctionner avec une seule liste pour tous leurs objets, y compris les tableaux. 
  
Pour chaque mappage, les fournisseurs de services doivent fournir une signature de mappage. Une signature de mappage est une valeur binaire, généralement un GUID, qui identifie de manière unique un ensemble d’identificateurs de propriété et leurs noms correspondants. Les signatures de mappage sont stockées dans la propriété **PR_MAPPING_SIGNATURE** ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md)). Les fournisseurs de services doivent modifier la valeur de **leur propriété PR_MAPPING_SIGNATURE** chaque fois qu’une modification est apporté au mappage qu’elle représente. Par exemple, **PR_MAPPING_SIGNATURE** doit être mis à jour si un nouvel identificateur est affecté à un nom ou si une nouvelle paire de nom et d’identificateur est ajoutée. 
  
Les clients qui utilisent les propriétés nommées des objets utilisent les propriétés PR_MAPPING_SIGNATURE **des** objets dans les opérations de comparaison et de copie. Pour comparer les identificateurs de propriété nommés appartenant à deux objets, les clients qui n’utilisent pas de signatures de mappage doivent appeler [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) sur les deux objets pour récupérer les noms de chacun des identificateurs. L’utilisation des signatures de mappage d’objets peut rendre cet appel inutile. Lorsque deux objets ont la même valeur pour **PR_MAPPING_SIGNATURE** propriétés, ils utilisent le même mappage. Les identificateurs qui utilisent le même mappage peuvent être comparés directement. Les fournisseurs de services qui implémentent [IMAPIProp::CopyTo](imapiprop-copyto.md) et [IMAPIProp::CopyProps](imapiprop-copyprops.md) peuvent également tirer parti de la signature de mappage d’un objet. Lors de la copie de propriétés nommées entre des objets, les fournisseurs de services peuvent éviter l’étape de conversion lorsque les objets source et de destination ont la même signature de mappage. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIProp : IUnknown](imapipropiunknown.md)


[MAPI des propri�t�s nomm�e](mapi-named-properties.md)

