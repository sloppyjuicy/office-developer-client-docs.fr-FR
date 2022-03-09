---
title: Transmission et copie de propriétés nommées
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 37075cfc-461d-4983-9045-d9f1da6739be
ms.openlocfilehash: 9f305af5be2f19088b1df9990a2d82d8ade3fb53
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63373633"
---
# <a name="transmitting-and-copying-named-properties"></a>Transmission et copie de propriétés nommées

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Chaque fois qu’une propriété nommée est envoyée, déplacée ou copiée, le nom reste constant, mais l’identificateur doit changer pour adhérer au mappage de l’objet de destination. La seule exception à cette règle est lorsque la source et la destination ont la même signature de mappage, ce qui rend inutile le remappage.
  
Il incombe au fournisseur de transport de rema propres aux identificateurs appropriés qui fonctionnent à destination les noms des propriétés nommées transmises. Le fournisseur de transport d’envoi ne peut pas savoir quel est le mappage correct à la destination ; Il doit transmettre les noms et s’appuyer sur le fournisseur de transport de réception pour les matre aux identificateurs qui fonctionnent. L’implémentation MAPI de TNEF gère le remappage des propriétés nommées pour les fournisseurs de transport. Les fournisseurs de transport peuvent gérer le remappage manuellement ou utiliser l’implémentation TNEF. 
  
Un remappage similaire des propriétés nommées doit se produire lorsque ces propriétés sont copiées entre les magasins de messages. Toutefois, étant donné que les fournisseurs de magasins de messages peuvent récupérer le nom au mappage d’identificateur de la destination, ils peuvent remapage immédiatement les propriétés et ne pas avoir à compter sur la magasin de messages de destination. 
  
## <a name="see-also"></a>Voir aussi



[MAPI des propri�t�s nomm�e](mapi-named-properties.md)

