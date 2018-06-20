---
title: À propos des Notifications de Table
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 00c9c6c2-fc21-4b9c-91fa-629450a22d37
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 3dfc67c8bcd899396da5371c614fd221cd9b2251
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782852"
---
# <a name="about-table-notifications"></a>À propos des Notifications de Table

  
  
**S’applique à**: Outlook 
  
Clients dépendent souvent des notifications de table pour découvrir des modifications apportées aux objets au lieu d’inscription pour recevoir des notifications directement à partir des objets. Les modifications classiques qui provoquent des notifications soient envoyées incluent l’ajout, la suppression ou la modification d’une ligne et toute erreur critique. Lors de l’arrivent de notifications, clients peuvent déterminer s’il faut effectuer un autre appel recharger le tableau. 
  
Étant donné que les notifications de table sont asynchrones, il existe quelques problèmes qui peuvent rendre la gestion des notifications moins simple :
  
- Les données transmises dans la structure [TABLE_NOTIFICATION](table_notification.md) ne peuvent pas représenter état le plus récent de la table. Par exemple, un client peut apporter une modification à un message et décidez ensuite de le supprimer. Le fournisseur de banque de messages l’implémentation de la table de contenu comprenant le message envoie des notifications de deux : un événement TABLE_ROW_MODIFIED suivi d’un événement TABLE_ROW_DELETED. Selon la façon dont le fournisseur de banque de messages heures notifications, le client peut recevoir la notification de TABLE_ROW_MODIFIED après la suppression de la ligne. 
    
- La colonne incluse avec une notification peut être différente de l’ensemble de colonnes de la table en cours. MAPI exige que le jeu de colonnes de notification à l’ensemble de colonnes qui était en vigueur au moment de la notification a été générée. Car il est possible pour un client appeler [IMAPITable::SetColumns](imapitable-setcolumns.md) pour modifier la colonne définie à tout moment, y compris après une notification — les jeux de deux colonnes ne peuvent pas être synchronisées. 
    
- Notifications de table sont envoyées uniquement pour les lignes qui font partie de l’affichage. Autrement dit, si une ligne est exclue de l’affichage en raison d’une restriction ou la table est dans un état réduit, aucune notification n’est envoyée si cette ligne change. En outre, aucun notifications ne sont envoyées à informer un client sur un changement d’état de la catégorie.
    
Clients Sachez que toutes les tables ne prennent en charge la notification TABLE_SORT_DONE et doivent être préparés à gérer cette condition par :
  
1. Forcer le tri être synchrone.
    
2. Recharger les lignes de la table lorsque [IMAPITable::SortTable](imapitable-sorttable.md) est retournée. 
    
## <a name="see-also"></a>Voir aussi



[Tables MAPI](mapi-tables.md)

