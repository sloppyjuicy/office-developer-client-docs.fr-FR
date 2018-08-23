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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: be41a9916b6b231d5715cf18fe2b0d804434f2ea
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594480"
---
# <a name="bookmark"></a><span data-ttu-id="01573-103">BOOKMARK</span><span class="sxs-lookup"><span data-stu-id="01573-103">BOOKMARK</span></span>

  
  
<span data-ttu-id="01573-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="01573-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="01573-105">Définit les données de signets pour mémoriser une position dans un tableau.</span><span class="sxs-lookup"><span data-stu-id="01573-105">Defines bookmarks data for remembering a position in a table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="01573-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="01573-106">Header file:</span></span>  <br/> |<span data-ttu-id="01573-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="01573-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="01573-108">Méthodes associées :</span><span class="sxs-lookup"><span data-stu-id="01573-108">Related methods:</span></span>  <br/> |<span data-ttu-id="01573-109">[IMAPITable::CreateBookmark](imapitable-createbookmark.md) [IMAPITable::FreeBookmark](imapitable-freebookmark.md)</span><span class="sxs-lookup"><span data-stu-id="01573-109">[IMAPITable::CreateBookmark](imapitable-createbookmark.md)[IMAPITable::FreeBookmark](imapitable-freebookmark.md)</span></span> <br/> |
   
```cpp
typedef ULONG_PTR BOOKMARK;
```

## <a name="remarks"></a><span data-ttu-id="01573-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="01573-110">Remarks</span></span>

<span data-ttu-id="01573-111">MAPI définit trois signets, répertoriés comme suit :</span><span class="sxs-lookup"><span data-stu-id="01573-111">MAPI defines three bookmarks, listed as follows:</span></span>
  
<span data-ttu-id="01573-112">BOOKMARK_BEGINNING</span><span class="sxs-lookup"><span data-stu-id="01573-112">BOOKMARK_BEGINNING</span></span> 
  
> <span data-ttu-id="01573-113">Mémorise la position de départ de la table.</span><span class="sxs-lookup"><span data-stu-id="01573-113">Remembers the starting position of the table.</span></span> 
    
<span data-ttu-id="01573-114">BOOKMARK_CURRENT</span><span class="sxs-lookup"><span data-stu-id="01573-114">BOOKMARK_CURRENT</span></span> 
  
> <span data-ttu-id="01573-115">Mémorise la position actuelle de la table.</span><span class="sxs-lookup"><span data-stu-id="01573-115">Remembers the current position of the table.</span></span>
    
<span data-ttu-id="01573-116">BOOKMARK_END</span><span class="sxs-lookup"><span data-stu-id="01573-116">BOOKMARK_END</span></span> 
  
> <span data-ttu-id="01573-117">Mémorise la position de fin de la table.</span><span class="sxs-lookup"><span data-stu-id="01573-117">Remembers the ending position of the table.</span></span>
    
<span data-ttu-id="01573-118">Clients peuvent créer d’autres signets mémorisation des autres positions de tableau.</span><span class="sxs-lookup"><span data-stu-id="01573-118">Clients can create other bookmarks for remembering other table positions.</span></span> <span data-ttu-id="01573-119">Les signets ne sont valides que si la table est ouverte.</span><span class="sxs-lookup"><span data-stu-id="01573-119">Bookmarks are valid only when the table is open.</span></span> <span data-ttu-id="01573-120">Clients doivent libérer tous les signets qu’ils ont créés avant la fermeture de la table associée.</span><span class="sxs-lookup"><span data-stu-id="01573-120">Clients must free any bookmarks that they have created before closing the associated table.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="01573-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="01573-121">See also</span></span>



[<span data-ttu-id="01573-122">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="01573-122">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md)
  
[<span data-ttu-id="01573-123">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="01573-123">IMAPITable::FindRow</span></span>](imapitable-findrow.md)
  
[<span data-ttu-id="01573-124">IMAPITable::FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="01573-124">IMAPITable::FreeBookmark</span></span>](imapitable-freebookmark.md)
  
[<span data-ttu-id="01573-125">IMAPITable::SeekRow</span><span class="sxs-lookup"><span data-stu-id="01573-125">IMAPITable::SeekRow</span></span>](imapitable-seekrow.md)


[<span data-ttu-id="01573-126">Types de données MAPI</span><span class="sxs-lookup"><span data-stu-id="01573-126">MAPI Data Types</span></span>](mapi-data-types.md)

