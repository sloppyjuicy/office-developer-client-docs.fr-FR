---
title: Transmission et copie de propriétés nommées
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 37075cfc-461d-4983-9045-d9f1da6739be
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 9e040277b82c0a946fbb55907ce823301351c44f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578458"
---
# <a name="transmitting-and-copying-named-properties"></a>Transmission et copie de propriétés nommées

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Chaque fois qu’une propriété nommée est envoyée, déplacée ou copiée, le nom reste constant, mais l’identificateur doit changer pour adhérer au mappage de l’objet de destination. La seule exception à cette règle est lorsque la source et la destination ont la même signature de mappage, ce qui rend inutile le remappage.
  
Il incombe au fournisseur de transport de remama les noms des propriétés nommées transmises aux identificateurs appropriés qui fonctionnent à la destination. Le fournisseur de transport d’envoi ne peut pas savoir quel est le mappage correct à la destination ; Il doit transmettre les noms et s’appuyer sur le fournisseur de transport de réception pour les ma mapmettre aux identificateurs qui fonctionnent. L’implémentation MAPI de TNEF gère le remappage des propriétés nommées pour les fournisseurs de transport. Les fournisseurs de transport peuvent gérer le remappage manuellement ou utiliser l’implémentation TNEF. 
  
Un remappage similaire des propriétés nommées doit se produire lorsque ces propriétés sont copiées entre les magasins de messages. Toutefois, étant donné que les fournisseurs de magasins de messages peuvent récupérer le nom au mappage d’identificateur de la destination, ils peuvent remapage immédiatement les propriétés sans avoir à compter sur la boutique de messages de destination. 
  
## <a name="see-also"></a>Voir aussi



[MAPI des propri�t�s nomm�e](mapi-named-properties.md)

