---
title: Utilisation de colonnes Unicode
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2cd55464-263f-4f83-b874-524271773934
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 9f1fd2d4e4bfdc9ccbbb771fedf1141769c8c8ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787467"
---
# <a name="working-with-unicode-columns"></a>Utilisation de colonnes Unicode

  
  
**S’applique à**: Outlook 
  
Chaînes de caractères dans les tableaux peuvent être représentées à l’aide de caractères 8 bits standard, qui sont de type de propriété PT_STRING8, ou caractères Unicode 16 bits, qui sont du type de la propriété PT_UNICODE. L’implémentation de la table est libres de choisir ou non leurs tables de prise en charge des chaînes Unicode. Étant donné que Unicode ajoute la valeur pour les clients et les fournisseurs de services en étendant le jeu de fonctionnalités, prenant en charge Unicode dans la mesure du possible est recommandée. 
  
De nombreuses méthodes de table acceptent un indicateur qui détermine si les valeurs de propriété de chaîne sont supposés être Unicode. À l’entrée, spécifier l’indicateur MAPI_UNICODE indique à l’implémentation de la table que toutes les valeurs de propriété de chaîne transmises avec l’appel sont des chaînes Unicode et dont les types de propriété de PT_UNICODE. Dans la sortie, cet indicateur indique que toutes les valeurs de propriété de chaîne renvoyée doivent être chaînes Unicode, si possible. Si l’indicateur a une signification d’entrée ou de sortie dépend de la méthode. L’implémentation de tableau qui ne prennent pas en charge Unicode et est transmise à l’indicateur MAPI_UNICODE renvoie la valeur MAPI_E_BAD_CHAR_WIDTH.
  
## <a name="see-also"></a>Voir aussi



[Tables MAPI](mapi-tables.md)

