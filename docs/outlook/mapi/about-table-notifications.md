---
title: À propos des notifications de tableau
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 00c9c6c2-fc21-4b9c-91fa-629450a22d37
ms.openlocfilehash: 4b7bbc06f5a96b02749ef7a99923bc608c3bce8e
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63372394"
---
# <a name="about-table-notifications"></a>À propos des notifications de tableau

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les clients s’appuient souvent sur les notifications de tableau pour découvrir les modifications apportées aux objets au lieu de s’inscrire pour recevoir des notifications directement à partir des objets. Les modifications types qui entraînent l’envoi de notifications incluent l’ajout, la suppression ou la modification d’une ligne et toute erreur critique. Lorsque les notifications arrivent, les clients peuvent déterminer s’il faut effectuer un autre appel pour recharger la table. 
  
Étant donné que les notifications de tableau sont asynchrones, il existe quelques problèmes qui peuvent rendre la gestion des notifications moins simple :
  
- Les données transmises dans la structure [de TABLE_NOTIFICATION](table_notification.md) peuvent ne pas représenter l’état le plus actuel de la table. Par exemple, un client peut apporter une modification à un message, puis décider de le supprimer. Le fournisseur de magasins de messages qui implémente la table des matières qui incluait le message envoie deux notifications : un événement TABLE_ROW_MODIFIED suivi d’un TABLE_ROW_DELETED de messagerie. Selon la façon dont le fournisseur de la boutique de messages times les notifications, le client peut recevoir la notification TABLE_ROW_MODIFIED après la suppression de la ligne. 
    
- Le jeu de colonnes inclus dans une notification peut être différent du jeu de colonnes actuel du tableau. MAPI exige que le jeu de colonnes de notification corresponde à l’ensemble de colonnes en vigueur au moment où la notification a été générée. Étant donné qu’il est possible pour un client d’appeler [IMAPITable::SetColumns](imapitable-setcolumns.md) pour modifier le jeu de colonnes à tout moment, y compris après une notification, les deux ensembles de colonnes peuvent ne pas être synchronisés. 
    
- Les notifications de tableau sont envoyées uniquement pour les lignes qui font partie de l’affichage. Autrement dit, si une ligne est exclue de l’affichage en raison d’une restriction ou parce que le tableau est dans un état de réduire, aucune notification n’est envoyée si cette ligne change. En outre, aucune notification n’est envoyée pour informer un client d’un changement d’état de catégorie.
    
Les clients doivent savoir que toutes les tables ne gèrent pas la notification TABLE_SORT_DONE et doivent être prêts à gérer cette condition en :
  
1. Forcer le tri à être synchrone.
    
2. Rechargez les lignes du tableau lorsque [la table IMAPITable::SortTable est](imapitable-sorttable.md) de retour. 
    
## <a name="see-also"></a>Voir aussi



[MAPI Tables](mapi-tables.md)

