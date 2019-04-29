---
title: Transmission et copie des propriétés nommées
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 37075cfc-461d-4983-9045-d9f1da6739be
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 6534e7344a62717e406c112249d26407b0852d93
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437776"
---
# <a name="transmitting-and-copying-named-properties"></a>Transmission et copie des propriétés nommées

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Chaque fois qu'une propriété nommée est envoyée, déplacée ou copiée, le nom reste constant, mais l'identificateur doit être modifié pour adhérer au mappage de l'objet de destination. La seule exception à cette règle est lorsque la source et la destination ont la même signature de mappage, ce qui rend superflu le remappage.
  
Il incombe au fournisseur de transport de remapper les noms des propriétés nommées transmises à des identificateurs appropriés qui fonctionnent à la destination. Le fournisseur de transport d'envoi ne peut pas savoir quel mappage correct se trouve à la destination; il doit transmettre les noms et s'appuyer sur le fournisseur de transport de réception pour les mapper aux identificateurs qui fonctionnent. L'implémentation MAPI de TNEF gère le remappage des propriétés nommées pour les fournisseurs de transport. Les fournisseurs de transport peuvent gérer manuellement le remappage ou utiliser l'implémentation TNEF. 
  
Un remappage similaire des propriétés nommées doit se produire lorsque ces propriétés sont copiées entre des magasins de messages. Toutefois, étant donné que les fournisseurs de banques de messages peuvent récupérer le mappage du nom au identificateur de la destination, ils peuvent remapper les propriétés immédiatement et ne pas avoir à se reposer sur la Banque de messages de destination. 
  
## <a name="see-also"></a>Voir aussi



[MAPI des propri�t�s nomm�e](mapi-named-properties.md)

