---
title: Définition d’une position de tableau avec un signet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 56ab37f9-5aa6-4e9d-9dc8-b3d95aa19f35
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: f0b041cecca92c0ced32631c67c72fcafdab2a16
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422459"
---
# <a name="setting-a-table-position-with-a-bookmark"></a><span data-ttu-id="e2f5d-103">Définition d’une position de tableau avec un signet</span><span class="sxs-lookup"><span data-stu-id="e2f5d-103">Setting a Table Position with a Bookmark</span></span>

  
  
<span data-ttu-id="e2f5d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e2f5d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e2f5d-105">Un signet est une ressource qui indique un emplacement particulier dans une table.</span><span class="sxs-lookup"><span data-stu-id="e2f5d-105">A bookmark is a resource that indicates a particular location in a table.</span></span> <span data-ttu-id="e2f5d-106">La définition d’un signet permet de revenir à une position ultérieurement, fonctionnalité qui peut considérablement améliorer les performances des opérations de table.</span><span class="sxs-lookup"><span data-stu-id="e2f5d-106">Setting a bookmark makes it possible to return to a position at a later time, a feature that can significantly improve the performance of table operations.</span></span> <span data-ttu-id="e2f5d-107">MAPI définit trois signets standard :</span><span class="sxs-lookup"><span data-stu-id="e2f5d-107">MAPI defines three standard bookmarks:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e2f5d-108">BOOKMARK_CURRENT</span><span class="sxs-lookup"><span data-stu-id="e2f5d-108">BOOKMARK_CURRENT</span></span>  <br/> |<span data-ttu-id="e2f5d-109">Pointe vers la ligne actuelle d’un tableau.</span><span class="sxs-lookup"><span data-stu-id="e2f5d-109">Points to the current row in a table.</span></span>  <br/> |
|<span data-ttu-id="e2f5d-110">BOOKMARK_BEGINNING</span><span class="sxs-lookup"><span data-stu-id="e2f5d-110">BOOKMARK_BEGINNING</span></span>  <br/> |<span data-ttu-id="e2f5d-111">Pointe vers la première ligne d’un tableau.</span><span class="sxs-lookup"><span data-stu-id="e2f5d-111">Points to the first row in a table.</span></span>  <br/> |
|<span data-ttu-id="e2f5d-112">BOOKMARK_END</span><span class="sxs-lookup"><span data-stu-id="e2f5d-112">BOOKMARK_END</span></span>  <br/> |<span data-ttu-id="e2f5d-113">Pointe vers la dernière ligne d’un tableau.</span><span class="sxs-lookup"><span data-stu-id="e2f5d-113">Points to the last row in a table.</span></span>  <br/> |
   
<span data-ttu-id="e2f5d-114">Les implémenteurs de tableau sont requis pour prendre en charge ces signets standard et peuvent également prendre en charge d’autres.</span><span class="sxs-lookup"><span data-stu-id="e2f5d-114">Table implementers are required to support these standard bookmarks and can also support others.</span></span> <span data-ttu-id="e2f5d-115">Toutefois, étant donné que les signets sont des ressources et que les ressources sont limitées, les utilisateurs de signets doivent les libérer dès que possible.</span><span class="sxs-lookup"><span data-stu-id="e2f5d-115">However, because bookmarks are resources and resources are limited, bookmark users should free them as soon as possible.</span></span> 
  
 <span data-ttu-id="e2f5d-116">**Pour définir un signet à la position actuelle du tableau**</span><span class="sxs-lookup"><span data-stu-id="e2f5d-116">**To set a bookmark at the current table position**</span></span>
  
- <span data-ttu-id="e2f5d-117">Appelez [IMAPITable::CreateBookmark](imapitable-createbookmark.md).</span><span class="sxs-lookup"><span data-stu-id="e2f5d-117">Call [IMAPITable::CreateBookmark](imapitable-createbookmark.md).</span></span> <span data-ttu-id="e2f5d-118">Il peut arriver que la mémoire disponible soit  insuffisante pour allouer le nouveau signet, ce qui a pour effet de renvoyer la valeur MAPI_E_UNABLE_TO_COMPLETE’erreur.</span><span class="sxs-lookup"><span data-stu-id="e2f5d-118">Occasionally there will be insufficient memory available to allocate the new bookmark, causing **CreateBookmark** to return the MAPI_E_UNABLE_TO_COMPLETE error value.</span></span> 
    
 <span data-ttu-id="e2f5d-119">**Pour libérer un signet**</span><span class="sxs-lookup"><span data-stu-id="e2f5d-119">**To free a bookmark**</span></span>
  
- <span data-ttu-id="e2f5d-120">Appelez [IMAPITable::FreeBookmark](imapitable-freebookmark.md).</span><span class="sxs-lookup"><span data-stu-id="e2f5d-120">Call [IMAPITable::FreeBookmark](imapitable-freebookmark.md).</span></span>
    
 <span data-ttu-id="e2f5d-121">**Pour déplacer le curseur vers une position avec signet**</span><span class="sxs-lookup"><span data-stu-id="e2f5d-121">**To move the cursor to a bookmarked position**</span></span>
  
- <span data-ttu-id="e2f5d-122">Appelez [IMAPITable::SeekRow](imapitable-seekrow.md).</span><span class="sxs-lookup"><span data-stu-id="e2f5d-122">Call [IMAPITable::SeekRow](imapitable-seekrow.md).</span></span> <span data-ttu-id="e2f5d-123">**SeekRow** établit une nouvelle valeur pour la position BOOKMARK_CURRENT position.</span><span class="sxs-lookup"><span data-stu-id="e2f5d-123">**SeekRow** establishes a new value for the BOOKMARK_CURRENT position.</span></span> <span data-ttu-id="e2f5d-124">**SeekRow** peut être utilisé, par exemple, pour positionner un tableau à dix lignes de la position actuelle ou pour recommencer au début.</span><span class="sxs-lookup"><span data-stu-id="e2f5d-124">**SeekRow** can be used, for example, to position a table ten rows from the current position or to start over at the beginning.</span></span> <span data-ttu-id="e2f5d-125">Les clients ou les fournisseurs de services peuvent rechercher l’état actuel, le début ou la fin d’une table, ou toute autre position associée à un signet prédéféré.</span><span class="sxs-lookup"><span data-stu-id="e2f5d-125">Clients or service providers can seek to the current, beginning, or end of a table, or any other position that is associated with a predefined bookmark.</span></span> <span data-ttu-id="e2f5d-126">Ils peuvent se déplacer vers l’avant ou l’arrière et limiter l’opération à un nombre de lignes spécifié.</span><span class="sxs-lookup"><span data-stu-id="e2f5d-126">They can move in either a forward or backward direction and limit the operation to a specified number of rows.</span></span> <span data-ttu-id="e2f5d-127">En règle générale, les appelants ne doivent pas rechercher plus de 50 lignes avec **SeekRow**; [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) doit être utilisé avec un plus grand nombre de lignes.</span><span class="sxs-lookup"><span data-stu-id="e2f5d-127">As a rule, callers should seek through no more than 50 rows with **SeekRow**; [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) should be used with larger numbers of rows.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="e2f5d-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e2f5d-128">See also</span></span>



[<span data-ttu-id="e2f5d-129">MAPI Tables</span><span class="sxs-lookup"><span data-stu-id="e2f5d-129">MAPI Tables</span></span>](mapi-tables.md)

