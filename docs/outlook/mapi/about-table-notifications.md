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
# <a name="about-table-notifications"></a><span data-ttu-id="a975e-103">À propos des notifications de table</span><span class="sxs-lookup"><span data-stu-id="a975e-103">About Table Notifications</span></span>

  
  
<span data-ttu-id="a975e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a975e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a975e-105">Les clients s'appuient souvent sur des notifications de table pour découvrir les modifications apportées aux objets au lieu de s'inscrire pour recevoir des notifications directement à partir des objets.</span><span class="sxs-lookup"><span data-stu-id="a975e-105">Clients often rely on table notifications to learn of changes to objects instead of registering to receive notifications directly from the objects.</span></span> <span data-ttu-id="a975e-106">Les modifications classiques qui provoquent l'envoi de notifications incluent l'ajout, la suppression ou la modification d'une ligne et d'une erreur critique.</span><span class="sxs-lookup"><span data-stu-id="a975e-106">Typical changes that cause notifications to be sent include the addition, deletion, or modification of a row and any critical error.</span></span> <span data-ttu-id="a975e-107">Lorsque les notifications arrivent, les clients peuvent déterminer s'il faut effectuer un autre appel pour recharger la table.</span><span class="sxs-lookup"><span data-stu-id="a975e-107">When notifications arrive, clients can determine whether to make another call to reload the table.</span></span> 
  
<span data-ttu-id="a975e-108">Étant donné que les notifications de table sont asynchrones, il existe quelques problèmes qui permettent de gérer les notifications de manière moins directe:</span><span class="sxs-lookup"><span data-stu-id="a975e-108">Because table notifications are asynchronous, there are a few issues that can make handling notifications less than straightforward:</span></span>
  
- <span data-ttu-id="a975e-109">Les données transmises dans la structure [TABLE_NOTIFICATION](table_notification.md) ne représentent pas nécessairement l'état le plus récent de la table.</span><span class="sxs-lookup"><span data-stu-id="a975e-109">The data passed in the [TABLE_NOTIFICATION](table_notification.md) structure might not represent the table's most current state.</span></span> <span data-ttu-id="a975e-110">Par exemple, un client peut modifier un message, puis décider de le supprimer.</span><span class="sxs-lookup"><span data-stu-id="a975e-110">For example, a client might make a change to a message and then decide to delete it.</span></span> <span data-ttu-id="a975e-111">Le fournisseur de banque de messages implémentant la table de contenu qui inclut le message envoie deux notifications: un événement TABLE_ROW_MODIFIED suivi d'un événement TABLE_ROW_DELETED.</span><span class="sxs-lookup"><span data-stu-id="a975e-111">The message store provider implementing the contents table that included the message sends two notifications: a TABLE_ROW_MODIFIED event followed by a TABLE_ROW_DELETED event.</span></span> <span data-ttu-id="a975e-112">En fonction de la fréquence de notification du fournisseur de banque de messages, le client peut recevoir la notification TABLE_ROW_MODIFIED après la suppression de la ligne.</span><span class="sxs-lookup"><span data-stu-id="a975e-112">Depending on how the message store provider times notifications, the client might receive the TABLE_ROW_MODIFIED notification after the deletion of the row.</span></span> 
    
- <span data-ttu-id="a975e-113">Le jeu de colonnes inclus avec une notification peut être différent de l'ensemble de colonnes actuel de la table.</span><span class="sxs-lookup"><span data-stu-id="a975e-113">The column set included with a notification might be different from the table's current column set.</span></span> <span data-ttu-id="a975e-114">MAPI exige que le jeu de colonnes de notification corresponde au jeu de colonnes qui était en vigueur lors de la génération de la notification.</span><span class="sxs-lookup"><span data-stu-id="a975e-114">MAPI requires that the notification column set match the column set that was in effect at the time that the notification was generated.</span></span> <span data-ttu-id="a975e-115">Dans la mesure où un client peut appeler [IMAPITable:: SetColumns](imapitable-setcolumns.md) pour modifier le jeu de colonnes à tout moment, y compris après une notification, les deux jeux de colonnes peuvent ne pas être synchronisés.</span><span class="sxs-lookup"><span data-stu-id="a975e-115">Because it is possible for a client to call [IMAPITable::SetColumns](imapitable-setcolumns.md) to alter the column set at any time — including after a notification — the two column sets may not be synchronized.</span></span> 
    
- <span data-ttu-id="a975e-116">Les notifications de table sont envoyées uniquement pour les lignes qui font partie de l'affichage.</span><span class="sxs-lookup"><span data-stu-id="a975e-116">Table notifications are only sent for rows that are part of the view.</span></span> <span data-ttu-id="a975e-117">Autrement dit, si une ligne est exclue de la vue en raison d'une restriction ou parce que le tableau est réduit, aucune notification n'est envoyée si cette ligne est modifiée.</span><span class="sxs-lookup"><span data-stu-id="a975e-117">That is, if a row is excluded from the view due to a restriction or because the table is in a collapsed state, no notification will be sent if that row changes.</span></span> <span data-ttu-id="a975e-118">Par ailleurs, aucune notification n'est envoyée pour informer un client de la modification de l'état de la catégorie.</span><span class="sxs-lookup"><span data-stu-id="a975e-118">Also, no notifications are sent to inform a client about a change in category state.</span></span>
    
<span data-ttu-id="a975e-119">Les clients doivent savoir que toutes les tables ne prennent pas en charge la notification TABLE_SORT_DONE et doivent être prêtes à gérer cette condition en procédant comme suit:</span><span class="sxs-lookup"><span data-stu-id="a975e-119">Clients should be aware that not all tables support the TABLE_SORT_DONE notification and should be prepared to handle this condition by:</span></span>
  
1. <span data-ttu-id="a975e-120">Forcer le tri en mode synchrone.</span><span class="sxs-lookup"><span data-stu-id="a975e-120">Forcing the sort to be synchronous.</span></span>
    
2. <span data-ttu-id="a975e-121">Rechargement des lignes de la table lorsque la méthode [IMAPITable:: SortTable](imapitable-sorttable.md) renvoie.</span><span class="sxs-lookup"><span data-stu-id="a975e-121">Reloading the rows of the table when [IMAPITable::SortTable](imapitable-sorttable.md) returns.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="a975e-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a975e-122">See also</span></span>



[<span data-ttu-id="a975e-123">Tables MAPI</span><span class="sxs-lookup"><span data-stu-id="a975e-123">MAPI Tables</span></span>](mapi-tables.md)

