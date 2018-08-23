---
title: Définition d’une position de table avec un filtre
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0d66124b-a018-4db4-b55b-a0e5ed467e14
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 6c4db9c67fc712143657fe66b86ea33ef2b9c272
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565591"
---
# <a name="setting-a-table-position-with-a-filter"></a>Définition d’une position de table avec un filtre

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Les utilisateurs de tableau peuvent déplacer le curseur à une ligne qui correspond à un ensemble de critères de filtre. Filtres peuvent reposer sur un grand nombre d’instructions telles que les valeurs de propriété de colonne, les masques de bits ou les sous-objets. Les filtres sont spécifiés dans MAPI à l’aide d’une structure [SRestriction](srestriction.md) . 
  
 **Pour positionner un tableau à la première ligne qui établit une correspondance avec les critères définis dans une restriction**
  
- Appelez la méthode [IMAPITable::FindRow](imapitable-findrow.md) . **FindRow** commençant par la ligne représentée par un signet particulier, recherche dans une direction avancer ou reculer pour localiser une ligne qui correspond aux critères spécifiés dans la restriction. **FindRow** peut être utile pour l’implémentation d’une barre de défilement est basée sur des chaînes de caractères, au lieu des fractions. Par exemple, un client peut appeler la mise en œuvre de MAPI de **FindRow** lors de la recherche par le biais du carnet d’adresses intégré pour permettre à un utilisateur, en entrant un ou plusieurs caractères, pour rechercher le premier nom commence par les caractères spécifiés. 
    
## <a name="see-also"></a>Voir aussi



[Tables MAPI](mapi-tables.md)

