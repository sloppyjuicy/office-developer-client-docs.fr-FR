---
title: À propos des notifications de table
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 00c9c6c2-fc21-4b9c-91fa-629450a22d37
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 9a42ed1e196e8ac498ab5889b4419ff407db4748
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321839"
---
# <a name="about-table-notifications"></a>À propos des notifications de table

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les clients s'appuient souvent sur des notifications de table pour découvrir les modifications apportées aux objets au lieu de s'inscrire pour recevoir des notifications directement à partir des objets. Les modifications classiques qui provoquent l'envoi de notifications incluent l'ajout, la suppression ou la modification d'une ligne et d'une erreur critique. Lorsque les notifications arrivent, les clients peuvent déterminer s'il faut effectuer un autre appel pour recharger la table. 
  
Étant donné que les notifications de table sont asynchrones, il existe quelques problèmes qui permettent de gérer les notifications de manière moins directe:
  
- Les données transmises dans la structure [TABLE_NOTIFICATION](table_notification.md) ne représentent pas nécessairement l'état le plus récent de la table. Par exemple, un client peut modifier un message, puis décider de le supprimer. Le fournisseur de banque de messages implémentant la table de contenu qui inclut le message envoie deux notifications: un événement TABLE_ROW_MODIFIED suivi d'un événement TABLE_ROW_DELETED. En fonction de la fréquence de notification du fournisseur de banque de messages, le client peut recevoir la notification TABLE_ROW_MODIFIED après la suppression de la ligne. 
    
- Le jeu de colonnes inclus avec une notification peut être différent de l'ensemble de colonnes actuel de la table. MAPI exige que le jeu de colonnes de notification corresponde au jeu de colonnes qui était en vigueur lors de la génération de la notification. Dans la mesure où un client peut appeler [IMAPITable:: SetColumns](imapitable-setcolumns.md) pour modifier le jeu de colonnes à tout moment, y compris après une notification, les deux jeux de colonnes peuvent ne pas être synchronisés. 
    
- Les notifications de table sont envoyées uniquement pour les lignes qui font partie de l'affichage. Autrement dit, si une ligne est exclue de la vue en raison d'une restriction ou parce que le tableau est réduit, aucune notification n'est envoyée si cette ligne est modifiée. Par ailleurs, aucune notification n'est envoyée pour informer un client de la modification de l'état de la catégorie.
    
Les clients doivent savoir que toutes les tables ne prennent pas en charge la notification TABLE_SORT_DONE et doivent être prêtes à gérer cette condition en procédant comme suit:
  
1. Forcer le tri en mode synchrone.
    
2. Rechargement des lignes de la table lorsque la méthode [IMAPITable:: SortTable](imapitable-sorttable.md) renvoie. 
    
## <a name="see-also"></a>Voir aussi



[Tables MAPI](mapi-tables.md)

