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
ms.openlocfilehash: 1c225712e354d72b79313ee4c3f36da55f11b0a3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587515"
---
# <a name="transmitting-and-copying-named-properties"></a>Transmission et copie des propriétés nommées

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Envoi d’une propriété nommée, déplacé ou copié, le nom reste constant, mais l’identificateur doit changer pour respecter le mappage de l’objet de destination. La seule exception à cette règle est lors de la source et destination ont la même signature de mappage, rendant remappage inutile.
  
Il est de la responsabilité du fournisseur de transport pour remapper les noms des propriétés nommées transmises aux identificateurs appropriés qui fonctionnent à la destination. Le fournisseur de transport envoi ne peut pas savoir quel est le mappage correct à la destination ; Il doit transmettre les noms et s’appuient sur le fournisseur de transport de réception pour les mapper aux identificateurs qui fonctionnent. L’implémentation MAPI du format TNEF gère la reconfiguration des propriétés nommées fournisseurs de transport. Fournisseurs de transport peuvent gérer le remappage manuellement ou utiliser la mise en œuvre TNEF. 
  
Un remappage similaire des propriétés nommées doit se produire lorsque ces propriétés sont copiées entre les magasins de message. Toutefois, étant donné que les fournisseurs de magasins de message peuvent récupérer le nom pour le mappage d’identificateur de la destination, ils peuvent remapper les propriétés immédiatement et n’ont pas à s’appuyer sur la banque de messages de destination. 
  
## <a name="see-also"></a>Voir aussi



[MAPI des propri�t�s nomm�e](mapi-named-properties.md)

