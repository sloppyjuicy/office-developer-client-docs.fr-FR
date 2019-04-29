---
title: BOOKMARK
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.BOOKMARK
api_type:
- COM
ms.assetid: 678bdc52-3404-48b2-9154-64ce2a941555
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 069cb41ceac70a2eaaa08440e43745605890f071
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418133"
---
# <a name="bookmark"></a><span data-ttu-id="e3bcf-103">BOOKMARK</span><span class="sxs-lookup"><span data-stu-id="e3bcf-103">BOOKMARK</span></span>

  
  
<span data-ttu-id="e3bcf-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e3bcf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e3bcf-105">Définit les données de signets pour la mémorisation d'une position dans un tableau.</span><span class="sxs-lookup"><span data-stu-id="e3bcf-105">Defines bookmarks data for remembering a position in a table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e3bcf-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="e3bcf-106">Header file:</span></span>  <br/> |<span data-ttu-id="e3bcf-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="e3bcf-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="e3bcf-108">Méthodes connexes:</span><span class="sxs-lookup"><span data-stu-id="e3bcf-108">Related methods:</span></span>  <br/> |<span data-ttu-id="e3bcf-109">[IMAPITable:: CreateBookmark](imapitable-createbookmark.md) [IMAPITable:: FreeBookmark](imapitable-freebookmark.md)</span><span class="sxs-lookup"><span data-stu-id="e3bcf-109">[IMAPITable::CreateBookmark](imapitable-createbookmark.md)[IMAPITable::FreeBookmark](imapitable-freebookmark.md)</span></span> <br/> |
   
```cpp
typedef ULONG_PTR BOOKMARK;
```

## <a name="remarks"></a><span data-ttu-id="e3bcf-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="e3bcf-110">Remarks</span></span>

<span data-ttu-id="e3bcf-111">MAPI définit trois signets, comme suit:</span><span class="sxs-lookup"><span data-stu-id="e3bcf-111">MAPI defines three bookmarks, listed as follows:</span></span>
  
<span data-ttu-id="e3bcf-112">BOOKMARK_BEGINNING</span><span class="sxs-lookup"><span data-stu-id="e3bcf-112">BOOKMARK_BEGINNING</span></span> 
  
> <span data-ttu-id="e3bcf-113">Mémorise la position de départ de la table.</span><span class="sxs-lookup"><span data-stu-id="e3bcf-113">Remembers the starting position of the table.</span></span> 
    
<span data-ttu-id="e3bcf-114">BOOKMARK_CURRENT</span><span class="sxs-lookup"><span data-stu-id="e3bcf-114">BOOKMARK_CURRENT</span></span> 
  
> <span data-ttu-id="e3bcf-115">Mémorise la position actuelle de la table.</span><span class="sxs-lookup"><span data-stu-id="e3bcf-115">Remembers the current position of the table.</span></span>
    
<span data-ttu-id="e3bcf-116">BOOKMARK_END</span><span class="sxs-lookup"><span data-stu-id="e3bcf-116">BOOKMARK_END</span></span> 
  
> <span data-ttu-id="e3bcf-117">Mémorise la position de fin de la table.</span><span class="sxs-lookup"><span data-stu-id="e3bcf-117">Remembers the ending position of the table.</span></span>
    
<span data-ttu-id="e3bcf-118">Les clients peuvent créer d'autres signets pour mémoriser les autres positions des tables.</span><span class="sxs-lookup"><span data-stu-id="e3bcf-118">Clients can create other bookmarks for remembering other table positions.</span></span> <span data-ttu-id="e3bcf-119">Les signets ne sont valides que lorsque le tableau est ouvert.</span><span class="sxs-lookup"><span data-stu-id="e3bcf-119">Bookmarks are valid only when the table is open.</span></span> <span data-ttu-id="e3bcf-120">Les clients doivent libérer tous les signets qu'ils ont créés avant de fermer le tableau associé.</span><span class="sxs-lookup"><span data-stu-id="e3bcf-120">Clients must free any bookmarks that they have created before closing the associated table.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e3bcf-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e3bcf-121">See also</span></span>



[<span data-ttu-id="e3bcf-122">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="e3bcf-122">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md)
  
[<span data-ttu-id="e3bcf-123">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="e3bcf-123">IMAPITable::FindRow</span></span>](imapitable-findrow.md)
  
[<span data-ttu-id="e3bcf-124">IMAPITable::FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="e3bcf-124">IMAPITable::FreeBookmark</span></span>](imapitable-freebookmark.md)
  
[<span data-ttu-id="e3bcf-125">IMAPITable::SeekRow</span><span class="sxs-lookup"><span data-stu-id="e3bcf-125">IMAPITable::SeekRow</span></span>](imapitable-seekrow.md)


[<span data-ttu-id="e3bcf-126">Types de données MAPI</span><span class="sxs-lookup"><span data-stu-id="e3bcf-126">MAPI Data Types</span></span>](mapi-data-types.md)

