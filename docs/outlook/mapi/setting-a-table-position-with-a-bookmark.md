---
title: Définition d’une position de table avec un signet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 56ab37f9-5aa6-4e9d-9dc8-b3d95aa19f35
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: f43e3a7e3376cb437620204a29aed9fb732d3427
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564093"
---
# <a name="setting-a-table-position-with-a-bookmark"></a><span data-ttu-id="c8722-103">Définition d’une position de table avec un signet</span><span class="sxs-lookup"><span data-stu-id="c8722-103">Setting a Table Position with a Bookmark</span></span>

  
  
<span data-ttu-id="c8722-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c8722-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c8722-105">Un signet est une ressource qui indique un emplacement particulier dans une table.</span><span class="sxs-lookup"><span data-stu-id="c8722-105">A bookmark is a resource that indicates a particular location in a table.</span></span> <span data-ttu-id="c8722-106">Définition d’un signet rend possible revenir à une position à une date ultérieure, une fonctionnalité qui peut améliorer sensiblement les performances des opérations de table.</span><span class="sxs-lookup"><span data-stu-id="c8722-106">Setting a bookmark makes it possible to return to a position at a later time, a feature that can significantly improve the performance of table operations.</span></span> <span data-ttu-id="c8722-107">MAPI définit trois signets standards :</span><span class="sxs-lookup"><span data-stu-id="c8722-107">MAPI defines three standard bookmarks:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c8722-108">BOOKMARK_CURRENT</span><span class="sxs-lookup"><span data-stu-id="c8722-108">BOOKMARK_CURRENT</span></span>  <br/> |<span data-ttu-id="c8722-109">Points à la ligne active dans un tableau.</span><span class="sxs-lookup"><span data-stu-id="c8722-109">Points to the current row in a table.</span></span>  <br/> |
|<span data-ttu-id="c8722-110">BOOKMARK_BEGINNING</span><span class="sxs-lookup"><span data-stu-id="c8722-110">BOOKMARK_BEGINNING</span></span>  <br/> |<span data-ttu-id="c8722-111">Points à la première ligne dans un tableau.</span><span class="sxs-lookup"><span data-stu-id="c8722-111">Points to the first row in a table.</span></span>  <br/> |
|<span data-ttu-id="c8722-112">BOOKMARK_END</span><span class="sxs-lookup"><span data-stu-id="c8722-112">BOOKMARK_END</span></span>  <br/> |<span data-ttu-id="c8722-113">Points à la dernière ligne dans une table.</span><span class="sxs-lookup"><span data-stu-id="c8722-113">Points to the last row in a table.</span></span>  <br/> |
   
<span data-ttu-id="c8722-114">L’implémentation de la table est nécessaires pour prendre en charge les signets standards et peut également prendre en charge d’autres personnes.</span><span class="sxs-lookup"><span data-stu-id="c8722-114">Table implementers are required to support these standard bookmarks and can also support others.</span></span> <span data-ttu-id="c8722-115">Toutefois, étant donné que les signets sont des ressources et les ressources sont limitées, les utilisateurs de signet doivent libérer les dès que possible.</span><span class="sxs-lookup"><span data-stu-id="c8722-115">However, because bookmarks are resources and resources are limited, bookmark users should free them as soon as possible.</span></span> 
  
 <span data-ttu-id="c8722-116">**Pour définir un signet à la position actuelle de la table**</span><span class="sxs-lookup"><span data-stu-id="c8722-116">**To set a bookmark at the current table position**</span></span>
  
- <span data-ttu-id="c8722-117">Appelez [IMAPITable::CreateBookmark](imapitable-createbookmark.md).</span><span class="sxs-lookup"><span data-stu-id="c8722-117">Call [IMAPITable::CreateBookmark](imapitable-createbookmark.md).</span></span> <span data-ttu-id="c8722-118">Il peut arriver que sera mémoire disponible insuffisante pour allouer le nouveau signet, entraînant **CreateBookmark** renvoyer la valeur d’erreur MAPI_E_UNABLE_TO_COMPLETE.</span><span class="sxs-lookup"><span data-stu-id="c8722-118">Occasionally there will be insufficient memory available to allocate the new bookmark, causing **CreateBookmark** to return the MAPI_E_UNABLE_TO_COMPLETE error value.</span></span> 
    
 <span data-ttu-id="c8722-119">**Pour libérer un signet**</span><span class="sxs-lookup"><span data-stu-id="c8722-119">**To free a bookmark**</span></span>
  
- <span data-ttu-id="c8722-120">Appelez [IMAPITable::FreeBookmark](imapitable-freebookmark.md).</span><span class="sxs-lookup"><span data-stu-id="c8722-120">Call [IMAPITable::FreeBookmark](imapitable-freebookmark.md).</span></span>
    
 <span data-ttu-id="c8722-121">**Pour déplacer le curseur vers une position marquée par un signet**</span><span class="sxs-lookup"><span data-stu-id="c8722-121">**To move the cursor to a bookmarked position**</span></span>
  
- <span data-ttu-id="c8722-122">Appelez [IMAPITable::SeekRow](imapitable-seekrow.md).</span><span class="sxs-lookup"><span data-stu-id="c8722-122">Call [IMAPITable::SeekRow](imapitable-seekrow.md).</span></span> <span data-ttu-id="c8722-123">**SeekRow** établit une nouvelle valeur pour la position BOOKMARK_CURRENT.</span><span class="sxs-lookup"><span data-stu-id="c8722-123">**SeekRow** establishes a new value for the BOOKMARK_CURRENT position.</span></span> <span data-ttu-id="c8722-124">**SeekRow** peut être utilisé, par exemple, pour positionner un lignes de tableau 10 à partir de la position actuelle ou recommencer au début.</span><span class="sxs-lookup"><span data-stu-id="c8722-124">**SeekRow** can be used, for example, to position a table ten rows from the current position or to start over at the beginning.</span></span> <span data-ttu-id="c8722-125">Clients ou fournisseurs de services peuvent rechercher en cours, à partir de, ou fin d’une table ou toute autre position qui est associée à un signet prédéfini.</span><span class="sxs-lookup"><span data-stu-id="c8722-125">Clients or service providers can seek to the current, beginning, or end of a table, or any other position that is associated with a predefined bookmark.</span></span> <span data-ttu-id="c8722-126">Ils peuvent déplacer dans un sens avancer ou reculer et le limite l’opération à un nombre spécifié de lignes.</span><span class="sxs-lookup"><span data-stu-id="c8722-126">They can move in either a forward or backward direction and limit the operation to a specified number of rows.</span></span> <span data-ttu-id="c8722-127">En règle générale, les appelants doivent seek pas plus de 50 lignes avec **SeekRow**; [IMAPI::SeekRowApprox](imapitable-seekrowapprox.md) doit être utilisé avec le plus grand nombre de lignes.</span><span class="sxs-lookup"><span data-stu-id="c8722-127">As a rule, callers should seek through no more than 50 rows with **SeekRow**; [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) should be used with larger numbers of rows.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="c8722-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c8722-128">See also</span></span>



[<span data-ttu-id="c8722-129">Tables MAPI</span><span class="sxs-lookup"><span data-stu-id="c8722-129">MAPI Tables</span></span>](mapi-tables.md)

