---
title: Définition d’une position de tableau avec un filtre
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0d66124b-a018-4db4-b55b-a0e5ed467e14
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 6b21d6746baf438af438787d966d9af886d4a74f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425469"
---
# <a name="setting-a-table-position-with-a-filter"></a>Définition d’une position de tableau avec un filtre

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les utilisateurs du tableau peuvent déplacer le curseur vers une ligne qui correspond à un ensemble de critères de filtre. Les filtres peuvent être basés sur diverses recommandations, telles que des valeurs de propriété de colonne, des masques de bits ou des sous-objets. Les filtres sont spécifiés dans MAPI à l’aide d’une structure [SRestriction.](srestriction.md) 
  
 **Pour positionner une table sur la première ligne qui correspond aux critères établis dans une restriction**
  
- Appelez [la méthode IMAPITable::FindRow.](imapitable-findrow.md) À partir de la ligne représentée par un signet particulier, **FindRow** recherche dans un sens avant ou arrière pour rechercher une ligne qui correspond aux critères spécifiés dans la restriction. **FindRow** peut être utile pour implémenter une barre de défilement basée sur des chaînes de caractères, plutôt que sur des valeurs fractionnaires. Par exemple, un client peut appeler l’implémentation mapi de **FindRow** lors de la recherche dans le carnet d’adresses intégré pour permettre à un utilisateur, en entrant un ou plusieurs caractères, de localiser le prénom qui commence par les caractères spécifiés. 
    
## <a name="see-also"></a>Voir aussi



[MAPI Tables](mapi-tables.md)

