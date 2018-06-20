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
# <a name="about-table-notifications"></a><span data-ttu-id="1eaad-103">À propos des Notifications de Table</span><span class="sxs-lookup"><span data-stu-id="1eaad-103">About Table Notifications</span></span>

  
  
<span data-ttu-id="1eaad-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1eaad-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1eaad-105">Clients dépendent souvent des notifications de table pour découvrir des modifications apportées aux objets au lieu d’inscription pour recevoir des notifications directement à partir des objets.</span><span class="sxs-lookup"><span data-stu-id="1eaad-105">Clients often rely on table notifications to learn of changes to objects instead of registering to receive notifications directly from the objects.</span></span> <span data-ttu-id="1eaad-106">Les modifications classiques qui provoquent des notifications soient envoyées incluent l’ajout, la suppression ou la modification d’une ligne et toute erreur critique.</span><span class="sxs-lookup"><span data-stu-id="1eaad-106">Typical changes that cause notifications to be sent include the addition, deletion, or modification of a row and any critical error.</span></span> <span data-ttu-id="1eaad-107">Lors de l’arrivent de notifications, clients peuvent déterminer s’il faut effectuer un autre appel recharger le tableau.</span><span class="sxs-lookup"><span data-stu-id="1eaad-107">When notifications arrive, clients can determine whether to make another call to reload the table.</span></span> 
  
<span data-ttu-id="1eaad-108">Étant donné que les notifications de table sont asynchrones, il existe quelques problèmes qui peuvent rendre la gestion des notifications moins simple :</span><span class="sxs-lookup"><span data-stu-id="1eaad-108">Because table notifications are asynchronous, there are a few issues that can make handling notifications less than straightforward:</span></span>
  
- <span data-ttu-id="1eaad-109">Les données transmises dans la structure [TABLE_NOTIFICATION](table_notification.md) ne peuvent pas représenter état le plus récent de la table.</span><span class="sxs-lookup"><span data-stu-id="1eaad-109">The data passed in the [TABLE_NOTIFICATION](table_notification.md) structure might not represent the table's most current state.</span></span> <span data-ttu-id="1eaad-110">Par exemple, un client peut apporter une modification à un message et décidez ensuite de le supprimer.</span><span class="sxs-lookup"><span data-stu-id="1eaad-110">For example, a client might make a change to a message and then decide to delete it.</span></span> <span data-ttu-id="1eaad-111">Le fournisseur de banque de messages l’implémentation de la table de contenu comprenant le message envoie des notifications de deux : un événement TABLE_ROW_MODIFIED suivi d’un événement TABLE_ROW_DELETED.</span><span class="sxs-lookup"><span data-stu-id="1eaad-111">The message store provider implementing the contents table that included the message sends two notifications: a TABLE_ROW_MODIFIED event followed by a TABLE_ROW_DELETED event.</span></span> <span data-ttu-id="1eaad-112">Selon la façon dont le fournisseur de banque de messages heures notifications, le client peut recevoir la notification de TABLE_ROW_MODIFIED après la suppression de la ligne.</span><span class="sxs-lookup"><span data-stu-id="1eaad-112">Depending on how the message store provider times notifications, the client might receive the TABLE_ROW_MODIFIED notification after the deletion of the row.</span></span> 
    
- <span data-ttu-id="1eaad-113">La colonne incluse avec une notification peut être différente de l’ensemble de colonnes de la table en cours.</span><span class="sxs-lookup"><span data-stu-id="1eaad-113">The column set included with a notification might be different from the table's current column set.</span></span> <span data-ttu-id="1eaad-114">MAPI exige que le jeu de colonnes de notification à l’ensemble de colonnes qui était en vigueur au moment de la notification a été générée.</span><span class="sxs-lookup"><span data-stu-id="1eaad-114">MAPI requires that the notification column set match the column set that was in effect at the time that the notification was generated.</span></span> <span data-ttu-id="1eaad-115">Car il est possible pour un client appeler [IMAPITable::SetColumns](imapitable-setcolumns.md) pour modifier la colonne définie à tout moment, y compris après une notification — les jeux de deux colonnes ne peuvent pas être synchronisées.</span><span class="sxs-lookup"><span data-stu-id="1eaad-115">Because it is possible for a client to call [IMAPITable::SetColumns](imapitable-setcolumns.md) to alter the column set at any time — including after a notification — the two column sets may not be synchronized.</span></span> 
    
- <span data-ttu-id="1eaad-116">Notifications de table sont envoyées uniquement pour les lignes qui font partie de l’affichage.</span><span class="sxs-lookup"><span data-stu-id="1eaad-116">Table notifications are only sent for rows that are part of the view.</span></span> <span data-ttu-id="1eaad-117">Autrement dit, si une ligne est exclue de l’affichage en raison d’une restriction ou la table est dans un état réduit, aucune notification n’est envoyée si cette ligne change.</span><span class="sxs-lookup"><span data-stu-id="1eaad-117">That is, if a row is excluded from the view due to a restriction or because the table is in a collapsed state, no notification will be sent if that row changes.</span></span> <span data-ttu-id="1eaad-118">En outre, aucun notifications ne sont envoyées à informer un client sur un changement d’état de la catégorie.</span><span class="sxs-lookup"><span data-stu-id="1eaad-118">Also, no notifications are sent to inform a client about a change in category state.</span></span>
    
<span data-ttu-id="1eaad-119">Clients Sachez que toutes les tables ne prennent en charge la notification TABLE_SORT_DONE et doivent être préparés à gérer cette condition par :</span><span class="sxs-lookup"><span data-stu-id="1eaad-119">Clients should be aware that not all tables support the TABLE_SORT_DONE notification and should be prepared to handle this condition by:</span></span>
  
1. <span data-ttu-id="1eaad-120">Forcer le tri être synchrone.</span><span class="sxs-lookup"><span data-stu-id="1eaad-120">Forcing the sort to be synchronous.</span></span>
    
2. <span data-ttu-id="1eaad-121">Recharger les lignes de la table lorsque [IMAPITable::SortTable](imapitable-sorttable.md) est retournée.</span><span class="sxs-lookup"><span data-stu-id="1eaad-121">Reloading the rows of the table when [IMAPITable::SortTable](imapitable-sorttable.md) returns.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="1eaad-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1eaad-122">See also</span></span>



[<span data-ttu-id="1eaad-123">Tables MAPI</span><span class="sxs-lookup"><span data-stu-id="1eaad-123">MAPI Tables</span></span>](mapi-tables.md)

