---
title: Mappages et signatures de mappages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 773f6671-cc21-4d1f-a11d-308bc71c852d
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: cd26ce4bc2da3da639b4a611fc9a69f39b13e5f3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357637"
---
# <a name="mappings-and-mapping-signatures"></a>Mappages et signatures de mappages

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lorsqu'un fournisseur de services prend en charge les propriétés nommées, chaque ensemble d'identificateurs et de paires de noms est appelé mappage. Les fournisseurs de services peuvent prendre en charge un ou plusieurs mappages. En d'autres, un fournisseur de banque de messages, par exemple, peut implémenter les méthodes **GetIDsFromNames** et **GetNamesFromIDs** pour tous ses objets message, Folder et Store de messages afin qu'ils fonctionnent avec une seule liste de noms et leurs identificateurs correspondants. Un autre fournisseur de banque de messages peut avoir une liste pour chaque dossier et les messages qu'il contient, ou implémenter une liste unique pour chaque message et chaque dossier. Les fournisseurs de banques de messages qui utilisent un mappage unique pour chaque message ne doivent pas autoriser les propriétés nommées à apparaître dans leurs tables de contenu de dossier, car pour un nom de propriété donné, l'identificateur de propriété diffère d'un message à l'autres. MAPI recommande aux fournisseurs de simplifier et d'utiliser une seule liste pour tous leurs objets, y compris les tables. 
  
Pour chaque mappage, les fournisseurs de services doivent fournir une signature de mappage. Une signature de mappage est une valeur binaire, généralement un GUID, qui identifie de manière unique un ensemble d'identificateurs de propriétés et leurs noms correspondants. Les signatures de mappage sont stockées dans la propriété **PR_MAPPING_SIGNATURE** ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md)) d'un objet. Les fournisseurs de services doivent modifier la valeur de leur propriété **PR_MAPPING_SIGNATURE** chaque fois qu'une modification est apportée au mappage qu'elle représente. Par exemple, **PR_MAPPING_SIGNATURE** doit être mis à jour si un nouvel identificateur est affecté à un nom ou si une paire nom/identificateur est ajoutée. 
  
Les clients qui travaillent avec les propriétés nommées des objets utilisent les propriétés **PR_MAPPING_SIGNATURE** des objets dans les opérations de comparaison et de copie. Pour comparer des identificateurs de propriétés nommées appartenant à deux objets, les clients qui n'utilisent pas de signatures de mappage doivent appeler [IMAPIProp:: GetNamesFromIDs](imapiprop-getnamesfromids.md) sur les deux objets pour récupérer les noms de chacun des identificateurs. L'utilisation des signatures de mappage d'objets peut rendre cet appel inutile. Lorsque deux objets ont la même valeur pour leurs propriétés **PR_MAPPING_SIGNATURE** , ils utilisent le même mappage. Les identificateurs qui utilisent le même mappage peuvent être comparés directement. Les fournisseurs de services qui implémentent [IMAPIProp:: CopyTo](imapiprop-copyto.md) et [IMAPIProp:: CopyProps](imapiprop-copyprops.md) peuvent également tirer parti de la signature de mappage d'un objet. Lors de la copie de propriétés nommées entre des objets, les fournisseurs de services peuvent éviter l'étape de conversion lorsque les objets source et de destination ont la même signature de mappage. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIProp : IUnknown](imapipropiunknown.md)


[MAPI des propri�t�s nomm�e](mapi-named-properties.md)

