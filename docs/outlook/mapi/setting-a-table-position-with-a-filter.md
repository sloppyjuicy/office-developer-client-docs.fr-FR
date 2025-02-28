---
title: Définition d’une position de tableau avec un filtre
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 0d66124b-a018-4db4-b55b-a0e5ed467e14
ms.openlocfilehash: 5f1e37b36a8210fdf969964c1e82d8a961d712a3
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63379338"
---
# <a name="setting-a-table-position-with-a-filter"></a>Définition d’une position de tableau avec un filtre

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les utilisateurs du tableau peuvent déplacer le curseur vers une ligne qui correspond à un ensemble de critères de filtre. Les filtres peuvent être basés sur diverses recommandations telles que les valeurs des propriétés de colonne, les masques de bits ou les sous-objets. Les filtres sont spécifiés dans MAPI à l’aide d’une structure [SRestriction](srestriction.md) . 
  
 **Pour positionner une table sur la première ligne qui correspond aux critères établis dans une restriction**
  
- Appelez [la méthode IMAPITable::FindRow](imapitable-findrow.md) . À partir de la ligne représentée par un signet particulier, **FindRow** recherche dans un sens avant ou arrière pour rechercher une ligne qui correspond aux critères spécifiés dans la restriction. **FindRow peut** être utile pour implémenter une barre de défilement basée sur des chaînes de caractères, plutôt que sur des valeurs fractionnaires. Par exemple, un client peut appeler l’implémentation mapi de **FindRow** lors de la recherche dans le carnet d’adresses intégré pour permettre à un utilisateur, en entrant un ou plusieurs caractères, de localiser le prénom qui commence par les caractères spécifiés. 
    
## <a name="see-also"></a>Voir aussi



[MAPI Tables](mapi-tables.md)

