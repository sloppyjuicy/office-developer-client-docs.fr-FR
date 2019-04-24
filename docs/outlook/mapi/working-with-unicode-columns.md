---
title: Utilisation des colonnes Unicode
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2cd55464-263f-4f83-b874-524271773934
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 76d1afb750dc81b889ca8e5eb3639145c061bfc2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325570"
---
# <a name="working-with-unicode-columns"></a>Utilisation des colonnes Unicode

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les chaînes de caractères dans les tableaux peuvent être représentées à l'aide de caractères standard 8 bits, qui sont des types de propriété PT_STRING8 ou des caractères Unicode 16 bits, dont le type de propriété est PT_UNICODE. Les implémenteurs de tableaux sont libres de choisir si leurs tables prennent en charge les chaînes Unicode. Étant donné qu'Unicode ajoute de la valeur pour les clients et les fournisseurs de services en étendant le jeu de fonctionnalités, la prise en charge d'Unicode est, autant possible, recommandée. 
  
De nombreuses méthodes de table acceptent un indicateur qui indique si les valeurs de propriété de chaîne sont supposées être Unicode. Lors de l'entrée, la spécification de l'indicateur MAPI_UNICODE indique à l'implémenteur de tableau que toutes les valeurs de propriété de chaîne transmises avec l'appel sont des chaînes Unicode et ont des types de propriété PT_UNICODE. Lors de la sortie, cet indicateur indique que toutes les valeurs de propriété de chaîne renvoyées doivent être des chaînes Unicode, si possible. Le fait que l'indicateur ait une signification pour l'entrée ou la sortie dépend de la méthode. Les implémenteurs de tableau qui ne prennent pas en charge Unicode et qui sont transmis à l'indicateur MAPI_UNICODE renvoient la valeur MAPI_E_BAD_CHAR_WIDTH.
  
## <a name="see-also"></a>Voir aussi



[Tables MAPI](mapi-tables.md)

