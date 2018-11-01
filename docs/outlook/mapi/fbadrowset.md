---
title: FBadRowSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBadRowSet
api_type:
- COM
ms.assetid: 3890dd50-e6ca-4859-bada-f6752ab61d41
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: e86e9fbf4901b5944775886f38db1ba12c4b122d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590959"
---
# <a name="fbadrowset"></a><span data-ttu-id="de71a-103">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="de71a-103">FBadRowSet</span></span>

  
  
<span data-ttu-id="de71a-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="de71a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="de71a-105">Valide toutes les lignes de tableau inclus dans un ensemble de lignes du tableau.</span><span class="sxs-lookup"><span data-stu-id="de71a-105">Validates all table rows included in a set of table rows.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="de71a-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="de71a-106">Header file:</span></span>  <br/> |<span data-ttu-id="de71a-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="de71a-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="de71a-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="de71a-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="de71a-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="de71a-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="de71a-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="de71a-110">Called by:</span></span>  <br/> |<span data-ttu-id="de71a-111">Fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="de71a-111">Service providers</span></span>  <br/> |
   
```cpp
BOOL FBadRowSet(
  LPSRowSet lpRowSet
);
```

## <a name="parameters"></a><span data-ttu-id="de71a-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="de71a-112">Parameters</span></span>

 <span data-ttu-id="de71a-113">_lpRowSet_</span><span class="sxs-lookup"><span data-stu-id="de71a-113">_lpRowSet_</span></span>
  
> <span data-ttu-id="de71a-114">[in] Pointeur vers une structure [SRowSet](srowset.md) qui identifie la ligne la valeur à valider.</span><span class="sxs-lookup"><span data-stu-id="de71a-114">[in] Pointer to an [SRowSet](srowset.md) structure identifying the row set to be validated.</span></span> <span data-ttu-id="de71a-115">Si le pointeur est NULL, la structure n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="de71a-115">If the pointer is NULL, the structure is invalid.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="de71a-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="de71a-116">Return value</span></span>

<span data-ttu-id="de71a-117">TRUE</span><span class="sxs-lookup"><span data-stu-id="de71a-117">TRUE</span></span> 
  
> <span data-ttu-id="de71a-118">Une ligne de l’ensemble de la ligne spécifiée n’est pas valide ou la ligne lui-même la valeur n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="de71a-118">A row of the specified row set is invalid, or the row set itself is invalid.</span></span> 
    
<span data-ttu-id="de71a-119">FALSE</span><span class="sxs-lookup"><span data-stu-id="de71a-119">FALSE</span></span> 
  
> <span data-ttu-id="de71a-120">Les lignes de l’ensemble de la ligne spécifiée et la ligne se sont valides.</span><span class="sxs-lookup"><span data-stu-id="de71a-120">The rows of the specified row set and the row set itself are all valid.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="de71a-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="de71a-121">See also</span></span>



[<span data-ttu-id="de71a-122">FBadRow</span><span class="sxs-lookup"><span data-stu-id="de71a-122">FBadRow</span></span>](fbadrow.md)

