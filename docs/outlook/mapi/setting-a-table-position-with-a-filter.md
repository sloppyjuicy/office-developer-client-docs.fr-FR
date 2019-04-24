---
title: Définition d'une position de table avec un filtre
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0d66124b-a018-4db4-b55b-a0e5ed467e14
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 6b21d6746baf438af438787d966d9af886d4a74f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316043"
---
# <a name="setting-a-table-position-with-a-filter"></a>Définition d'une position de table avec un filtre

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Tableau les utilisateurs peuvent déplacer le curseur vers une ligne qui correspond à un ensemble de critères de filtre. Les filtres peuvent être basés sur diverses instructions, telles que des valeurs de propriété de colonne, des masques de réplication ou des sous-objets. Les filtres sont spécifiés dans MAPI à l'aide d'une structure [SRestriction](srestriction.md) . 
  
 **Positionnement d'une table sur la première ligne correspondant aux critères établis dans une restriction**
  
- Appelez la méthode [IMAPITable:: FindRow](imapitable-findrow.md) . En commençant par la ligne représentée par un signet particulier, **FindRow** recherche dans une direction vers l'avant ou vers l'arrière pour trouver une ligne qui correspond aux critères spécifiés dans la restriction. **FindRow** peut être utile pour implémenter une barre de défilement basée sur des chaînes de caractères, au lieu de valeurs fractionnaires. Par exemple, un client peut appeler la mise en œuvre de **FindRow** par MAPI lors de la recherche dans le carnet d'adresses intégré pour permettre à un utilisateur, en entrant un ou plusieurs caractères, de localiser le prénom qui commence par les caractères spécifiés. 
    
## <a name="see-also"></a>Voir aussi



[Tables MAPI](mapi-tables.md)

