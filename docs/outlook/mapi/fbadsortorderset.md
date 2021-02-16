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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 31840923e24cddd0dc3dfa9cc67b610d0dcd7e47
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428458"
---
# <a name="fbadsortorderset"></a><span data-ttu-id="20893-103">FBadSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="20893-103">FBadSortOrderSet</span></span>

  
  
<span data-ttu-id="20893-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="20893-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="20893-105">Valide un ordre de tri en vérifiant son allocation de mémoire.</span><span class="sxs-lookup"><span data-stu-id="20893-105">Validates a sort order set by verifying its memory allocation.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="20893-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="20893-106">Header file:</span></span>  <br/> |<span data-ttu-id="20893-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="20893-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="20893-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="20893-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="20893-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="20893-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="20893-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="20893-110">Called by:</span></span>  <br/> |<span data-ttu-id="20893-111">Fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="20893-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadSortOrderSet(
  LPSSortOrderSet lpsos
);
```

## <a name="parameters"></a><span data-ttu-id="20893-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="20893-112">Parameters</span></span>

 <span data-ttu-id="20893-113">_lpsos_</span><span class="sxs-lookup"><span data-stu-id="20893-113">_lpsos_</span></span>
  
> <span data-ttu-id="20893-114">[in] Pointeur vers une structure [SSortOrderSet](ssortorderset.md) identifiant l’ordre de tri à valider.</span><span class="sxs-lookup"><span data-stu-id="20893-114">[in] Pointer to an [SSortOrderSet](ssortorderset.md) structure identifying the sort order set to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="20893-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="20893-115">Return value</span></span>

<span data-ttu-id="20893-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="20893-116">TRUE</span></span> 
  
> <span data-ttu-id="20893-117">Le jeu d’ordre de tri spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="20893-117">The specified sort order set is invalid.</span></span> 
    
<span data-ttu-id="20893-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="20893-118">FALSE</span></span> 
  
> <span data-ttu-id="20893-119">Le jeu d’ordre de tri spécifié est valide.</span><span class="sxs-lookup"><span data-stu-id="20893-119">The specified sort order set is valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="20893-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="20893-120">Remarks</span></span>

<span data-ttu-id="20893-121">La **fonction FBadSortOrderSet** peut être utilisée pour préparer un appel à une méthode de tri telle que la méthode [IMAPITable::SortTable.](imapitable-sorttable.md)</span><span class="sxs-lookup"><span data-stu-id="20893-121">The **FBadSortOrderSet** function can be used to prepare for a call to a sort method such as the [IMAPITable::SortTable](imapitable-sorttable.md) method.</span></span> 
  

