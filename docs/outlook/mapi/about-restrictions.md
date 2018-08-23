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
ms.openlocfilehash: 003655354ecac8e2910b3e6851da32c28ce31cfc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586452"
---
# <a name="about-restrictions"></a>À propos des restrictions

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Une restriction est un moyen de limiter le nombre de lignes dans un affichage uniquement aux lignes avec des valeurs pour les colonnes qui correspondent à des critères spécifiques. Il existe plusieurs opportunités différentes pour des tableaux à l’aide de restrictions. Les applications clientes peuvent utiliser restrictions, par exemple, pour filtrer un tableau de contenu pour les messages envoyés par une personne particulière, pour rechercher des lignes qui ne prennent pas en charge une propriété ou ont défini une propriété à une valeur spécifique, ou pour rechercher des destinataires en double dans un Message. 
  
Les méthodes [IMAPITable](imapitable-restrict.md) et [IMAPITable::FindRow](imapitable-findrow.md) sont utilisés pour définir des restrictions sur une table. **Restrict** applique la restriction à la table sans récupérer toutes les lignes. Pour récupérer uniquement les lignes qui répondent à la restriction, un appel ultérieur à [IMAPITable::QueryRows](imapitable-queryrows.md) ou une méthode similaire est nécessaire. **FindRow** applique la restriction et récupère la première ligne dans le tableau qui correspond aux critères. **FindRow** applique une restriction temporaire, qui est uniquement à la durée de l’appel, alors que **Restrict** applique une restriction permanente. 
  
Certains clients peuvent générer une restriction à l’aide de colonnes qui sont définies pas dans la colonne en cours. Prise en charge une telle restriction est facultative et l’implémentation de tableau qui prennent en charge ajouter la valeur, en particulier pour les tables des matières. L’implémentation de tableau qui ne prennent pas en charge qu’il peut renvoyer la valeur MAPI_E_TOO_COMPLEX à partir d’un appel de **restreindre** ou la valeur MAPI_E_NOT_FOUND à partir d’un appel **FindRow** . 
  
Les clients doivent être conscient que, même si le fournisseur ne prend pas en charge les restrictions sur les colonnes pas dans le jeu actuel de la colonne, ils obtenir globale de meilleures performances en spécifiant les colonnes qu'ils souhaitent dans leurs restrictions avec [IMAPITable::SetColumns](imapitable-setcolumns.md) .
  
## <a name="see-also"></a>Voir aussi



[Tables MAPI](mapi-tables.md)

