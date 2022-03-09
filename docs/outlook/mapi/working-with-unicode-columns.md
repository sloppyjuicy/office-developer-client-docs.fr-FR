---
title: Travailler avec des colonnes Unicode
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 2cd55464-263f-4f83-b874-524271773934
ms.openlocfilehash: 378b9381cedf5b7f1e315e416e76c266fd8eafd4
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63374214"
---
# <a name="working-with-unicode-columns"></a>Travailler avec des colonnes Unicode

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les chaînes de caractères des tableaux peuvent être représentées à l’aide de caractères 8 bits standard, qui sont des PT_STRING8 de type propriété, ou des caractères Unicode 16 bits, qui sont des caractères de type PT_UNICODE. Les implémenteurs de tableau sont libres de choisir si leurs tables peuvent ou non prendre en charge les chaînes Unicode. Étant donné qu’Unicode ajoute de la valeur pour les clients et les fournisseurs de services en étendant l’ensemble de fonctionnalités, la prise en charge d’Unicode dans la mesure du possible est recommandée. 
  
De nombreuses méthodes de table acceptent un indicateur qui détermine si les valeurs de propriété de chaîne doivent être unicode. Lors de l’entrée, la spécification de l’indicateur MAPI_UNICODE indique à l’implémenteur de table que toutes les valeurs de propriété de chaîne transmises avec l’appel sont des chaînes Unicode et ont des types de propriétés PT_UNICODE. En sortie, cet indicateur indique que toutes les valeurs de propriété de chaîne renvoyées doivent être des chaînes Unicode, si possible. La signification de l’indicateur pour l’entrée ou la sortie dépend de la méthode. Les implémenteurs de tableau qui ne viennent pas en charge Unicode et qui sont passés à l’indicateur MAPI_UNICODE renvoyer la MAPI_E_BAD_CHAR_WIDTH valeur.
  
## <a name="see-also"></a>Voir aussi



[MAPI Tables](mapi-tables.md)

