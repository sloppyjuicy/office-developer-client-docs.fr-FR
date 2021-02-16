---
title: À propos des restrictions
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e119fa20-08b8-4c8d-93fc-56037220890d
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 139526937380273703a96f91f2bae02a79debc76
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433107"
---
# <a name="about-restrictions"></a>À propos des restrictions

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Une restriction est un moyen de limiter le nombre de lignes dans un affichage aux seules lignes avec des valeurs pour les colonnes qui correspondent à des critères spécifiques. Il existe de nombreuses possibilités d’utilisation des restrictions avec des tableaux. Les applications clientes peuvent utiliser des restrictions, par exemple, pour filtrer une table des matières pour les messages envoyés par une personne particulière, pour rechercher des lignes qui ne prenons pas en charge une propriété ou qui ont fixé une valeur spécifique à une propriété, ou pour rechercher des destinataires en double dans un message. 
  
Les [méthodes IMAPITable::Restrict](imapitable-restrict.md) et [IMAPITable::FindRow](imapitable-findrow.md) sont utilisées pour définir des restrictions sur une table. **Restrict** applique la restriction au tableau sans récupérer de lignes. Pour récupérer uniquement les lignes qui répondent à la restriction, un appel ultérieur à [IMAPITable::QueryRows](imapitable-queryrows.md) ou à une méthode similaire est requis. **FindRow** applique la restriction et récupère la première ligne du tableau qui correspond aux critères. **FindRow** applique une restriction temporaire, qui n’existe que pour la durée de l’appel, tandis que **Restrict** applique une restriction plus permanente. 
  
Certains clients peuvent créer une restriction à l’aide de colonnes qui ne sont pas dans le jeu de colonnes actuel. La prise en charge d’une telle restriction est facultative et les implémenteurs de tableau qui la prisent en charge ajoutent de la valeur, en particulier pour les tables des matières. Les implémenteurs de tableau qui ne la prisent pas en charge peuvent renvoyer la valeur MAPI_E_TOO_COMPLEX d’un appel Restrict ou la valeur MAPI_E_NOT_FOUND d’un **appel FindRow.**  
  
Les clients doivent savoir que, même si le fournisseur prend en charge les restrictions sur les colonnes qui ne font pas l’ensemble de colonnes actuel, ils obtiennent de meilleures performances globales en spécifiant les colonnes qu’ils ont l’intention d’utiliser dans leurs restrictions avec [IMAPITable::SetColumns](imapitable-setcolumns.md).
  
## <a name="see-also"></a>Voir aussi



[MAPI Tables](mapi-tables.md)

