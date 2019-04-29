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
  
Une restriction permet de limiter le nombre de lignes d'un affichage aux seules lignes dont les valeurs correspondent à des critères spécifiques. Il existe de nombreuses opportunités différentes pour l'utilisation de restrictions avec des tables. Les applications clientes peuvent utiliser des restrictions, par exemple, pour filtrer une table de contenu pour les messages envoyés par une personne particulière, pour rechercher des lignes qui ne prennent pas en charge une propriété ou ont défini une propriété sur une valeur spécifique, ou pour rechercher des destinataires en double dans un Message. 
  
Les méthodes [IMAPITable](imapitable-restrict.md) :: Restrict et [IMAPITable:: FindRow](imapitable-findrow.md) permettent de définir des restrictions sur une table. **** La méthode Restrict applique la restriction à la table sans récupérer de ligne. Pour récupérer uniquement les lignes qui satisfont à la restriction, un appel suivant à [IMAPITable:: QueryRows](imapitable-queryrows.md) ou une méthode similaire est requise. **FindRow** applique la restriction et récupère la première ligne du tableau qui correspond aux critères. **FindRow** applique une restriction temporaire, qui existe uniquement pendant la durée de l'appel, tandis que **restrict** applique une restriction permanente plus permanente. 
  
Certains clients peuvent créer une restriction à l'aide de colonnes qui ne figurent pas dans le jeu de colonnes actuel. La prise en charge d'une restriction de ce type est facultative et les implémenteurs de tableau qui le prennent en charge ajoutent une valeur ajoutée, en particulier pour les tables des matières. Les implémenteurs de tableau qui ne le prennent pas en charge peuvent renvoyer la **** valeur MAPI_E_TOO_COMPLEX à partir d'un appel de la propriété restrict ou de la valeur MAPI_E_NOT_FOUND à partir d'un appel **FindRow** . 
  
Les clients doivent savoir que, même si le fournisseur prend en charge les restrictions sur les colonnes qui ne figurent pas dans le jeu de colonnes actuel, il obtiendra de meilleures performances globales en spécifiant les colonnes qu'ils entendent utiliser dans leurs restrictions avec la fonction [IMAPITable:: SetColumns](imapitable-setcolumns.md) .
  
## <a name="see-also"></a>Voir aussi



[Tables MAPI](mapi-tables.md)

