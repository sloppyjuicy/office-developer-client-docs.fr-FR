---
title: FBadSortOrderSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBadSortOrderSet
api_type:
- COM
ms.assetid: b7f80e0a-8ddd-4b24-ab63-2078a8152058
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 0e200ea20c55cfd5729ce4c1f590de2d61ca73bc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783287"
---
# <a name="fbadsortorderset"></a><span data-ttu-id="ba1be-103">FBadSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="ba1be-103">FBadSortOrderSet</span></span>

  
  
<span data-ttu-id="ba1be-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ba1be-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ba1be-105">Valide un ordre de tri défini par vérifier son allocation de mémoire.</span><span class="sxs-lookup"><span data-stu-id="ba1be-105">Validates a sort order set by verifying its memory allocation.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ba1be-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="ba1be-106">Header file:</span></span>  <br/> |<span data-ttu-id="ba1be-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="ba1be-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="ba1be-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="ba1be-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="ba1be-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="ba1be-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="ba1be-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="ba1be-110">Called by:</span></span>  <br/> |<span data-ttu-id="ba1be-111">Fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="ba1be-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadSortOrderSet(
  LPSSortOrderSet lpsos
);
```

## <a name="parameters"></a><span data-ttu-id="ba1be-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ba1be-112">Parameters</span></span>

 <span data-ttu-id="ba1be-113">_lpsos_</span><span class="sxs-lookup"><span data-stu-id="ba1be-113">_lpsos_</span></span>
  
> <span data-ttu-id="ba1be-114">[in] Pointeur vers une structure [SSortOrderSet](ssortorderset.md) qui identifie l’ordre de tri défini à valider.</span><span class="sxs-lookup"><span data-stu-id="ba1be-114">[in] Pointer to an [SSortOrderSet](ssortorderset.md) structure identifying the sort order set to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ba1be-115">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="ba1be-115">Return value</span></span>

<span data-ttu-id="ba1be-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="ba1be-116">TRUE</span></span> 
  
> <span data-ttu-id="ba1be-117">L’ensemble d’ordre de tri spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="ba1be-117">The specified sort order set is invalid.</span></span> 
    
<span data-ttu-id="ba1be-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="ba1be-118">FALSE</span></span> 
  
> <span data-ttu-id="ba1be-119">L’ensemble d’ordre de tri spécifié est valide.</span><span class="sxs-lookup"><span data-stu-id="ba1be-119">The specified sort order set is valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ba1be-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="ba1be-120">Remarks</span></span>

<span data-ttu-id="ba1be-121">La fonction **FBadSortOrderSet** peut être utilisée pour préparer un appel à une méthode de tri telles que la méthode [IMAPITable::SortTable](imapitable-sorttable.md) .</span><span class="sxs-lookup"><span data-stu-id="ba1be-121">The **FBadSortOrderSet** function can be used to prepare for a call to a sort method such as the [IMAPITable::SortTable](imapitable-sorttable.md) method.</span></span> 
  

