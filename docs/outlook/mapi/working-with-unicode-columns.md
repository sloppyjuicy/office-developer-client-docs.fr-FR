---
title: Travailler avec des colonnes Unicode
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 2cd55464-263f-4f83-b874-524271773934
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 762d8acf3ad006380611025fcfce7675c4a3f0bc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59629430"
---
# <a name="working-with-unicode-columns"></a>Travailler avec des colonnes Unicode

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les chaînes de caractères des tableaux peuvent être représentées à l’aide de caractères 8 bits standard, qui sont des PT_STRING8 de type propriété, ou des caractères Unicode 16 bits, qui sont des caractères de type PT_UNICODE. Les implémenteurs de tableau sont libres de choisir si leurs tables peuvent prendre en charge les chaînes Unicode. Étant donné qu’Unicode ajoute de la valeur pour les clients et les fournisseurs de services en étendant l’ensemble de fonctionnalités, la prise en charge d’Unicode dans la mesure du possible est recommandée. 
  
De nombreuses méthodes de table acceptent un indicateur qui détermine si les valeurs de propriété de chaîne doivent être Unicode ou non. Lors de l’entrée, la spécification de l’indicateur MAPI_UNICODE indique à l’implémenteur de table que toutes les valeurs de propriété de chaîne transmises avec l’appel sont des chaînes Unicode et ont des types de propriétés PT_UNICODE. En sortie, cet indicateur indique que toutes les valeurs de propriété de chaîne renvoyées doivent être des chaînes Unicode, si possible. La signification de l’indicateur pour l’entrée ou la sortie dépend de la méthode. Les implémenteurs de tableau qui ne viennent pas en charge Unicode et qui sont passés à l’indicateur MAPI_UNICODE renvoyer la MAPI_E_BAD_CHAR_WIDTH valeur.
  
## <a name="see-also"></a>Voir aussi



[MAPI Tables](mapi-tables.md)

