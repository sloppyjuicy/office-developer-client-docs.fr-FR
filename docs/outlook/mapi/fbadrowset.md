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
ms.openlocfilehash: 49e6c8254cbd527635685c3f974da57ee3ac82a5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411791"
---
# <a name="fbadrowset"></a><span data-ttu-id="bde0f-103">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="bde0f-103">FBadRowSet</span></span>

  
  
<span data-ttu-id="bde0f-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bde0f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bde0f-105">Valide toutes les lignes de tableau incluses dans un ensemble de lignes de tableau.</span><span class="sxs-lookup"><span data-stu-id="bde0f-105">Validates all table rows included in a set of table rows.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bde0f-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="bde0f-106">Header file:</span></span>  <br/> |<span data-ttu-id="bde0f-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="bde0f-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="bde0f-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="bde0f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="bde0f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="bde0f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="bde0f-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="bde0f-110">Called by:</span></span>  <br/> |<span data-ttu-id="bde0f-111">Fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="bde0f-111">Service providers</span></span>  <br/> |
   
```cpp
BOOL FBadRowSet(
  LPSRowSet lpRowSet
);
```

## <a name="parameters"></a><span data-ttu-id="bde0f-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bde0f-112">Parameters</span></span>

 <span data-ttu-id="bde0f-113">_lpRowSet_</span><span class="sxs-lookup"><span data-stu-id="bde0f-113">_lpRowSet_</span></span>
  
> <span data-ttu-id="bde0f-114">[in] Pointeur vers une structure [SRowSet](srowset.md) identifiant le jeu de lignes à valider.</span><span class="sxs-lookup"><span data-stu-id="bde0f-114">[in] Pointer to an [SRowSet](srowset.md) structure identifying the row set to be validated.</span></span> <span data-ttu-id="bde0f-115">Si le pointeur est NULL, la structure n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="bde0f-115">If the pointer is NULL, the structure is invalid.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="bde0f-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="bde0f-116">Return value</span></span>

<span data-ttu-id="bde0f-117">TRUE</span><span class="sxs-lookup"><span data-stu-id="bde0f-117">TRUE</span></span> 
  
> <span data-ttu-id="bde0f-118">Une ligne du jeu de lignes spécifié n’est pas valide ou le jeu de lignes lui-même n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="bde0f-118">A row of the specified row set is invalid, or the row set itself is invalid.</span></span> 
    
<span data-ttu-id="bde0f-119">FALSE</span><span class="sxs-lookup"><span data-stu-id="bde0f-119">FALSE</span></span> 
  
> <span data-ttu-id="bde0f-120">Les lignes du jeu de lignes spécifié et du jeu de lignes lui-même sont toutes valides.</span><span class="sxs-lookup"><span data-stu-id="bde0f-120">The rows of the specified row set and the row set itself are all valid.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bde0f-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bde0f-121">See also</span></span>



[<span data-ttu-id="bde0f-122">FBadRow</span><span class="sxs-lookup"><span data-stu-id="bde0f-122">FBadRow</span></span>](fbadrow.md)

