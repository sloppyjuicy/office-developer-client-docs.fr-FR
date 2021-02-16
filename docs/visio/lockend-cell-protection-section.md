---
title: LockEnd, cellule (section Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm620
localization_priority: Normal
ms.assetid: e9742142-4d34-1ba9-480e-d1ecff4fc7cd
description: Verrouille le point de fin (EndX, EndY) d'une forme 1D à un emplacement donné.
ms.openlocfilehash: d9fe0372c44fe3b029a4d06056c8d3871c3f91e8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425581"
---
# <a name="lockend-cell-protection-section"></a><span data-ttu-id="a4279-103">LockEnd, cellule (section Protection)</span><span class="sxs-lookup"><span data-stu-id="a4279-103">LockEnd Cell (Protection Section)</span></span>

<span data-ttu-id="a4279-104">Verrouille le point de fin (EndX, EndY) d'une forme 1D à un emplacement donné.</span><span class="sxs-lookup"><span data-stu-id="a4279-104">Locks the endpoint (EndX, EndY) of a 1-D shape to a specific location.</span></span>
  
|<span data-ttu-id="a4279-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="a4279-105">**Value**</span></span>|<span data-ttu-id="a4279-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="a4279-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="a4279-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="a4279-107">TRUE</span></span>  <br/> | <span data-ttu-id="a4279-108">Le point de fin est verrouillé.</span><span class="sxs-lookup"><span data-stu-id="a4279-108">Endpoint is locked.</span></span>  <br/> |
| <span data-ttu-id="a4279-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="a4279-109">FALSE</span></span>  <br/> | <span data-ttu-id="a4279-110">Le point de fin n'est pas verrouillé.</span><span class="sxs-lookup"><span data-stu-id="a4279-110">Endpoint is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a4279-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="a4279-111">Remarks</span></span>

<span data-ttu-id="a4279-112">Pour obtenir une référence à la cellule LockEnd par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="a4279-112">To get a reference to the LockEnd cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a4279-113">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="a4279-113">Cell name:</span></span>  <br/> | <span data-ttu-id="a4279-114">LockEnd</span><span class="sxs-lookup"><span data-stu-id="a4279-114">LockEnd</span></span>  <br/> |
   
<span data-ttu-id="a4279-115">Pour obtenir une référence à la cellule LockEnd à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="a4279-115">To get a reference to the LockEnd cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a4279-116">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="a4279-116">Section index:</span></span>  <br/> |<span data-ttu-id="a4279-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a4279-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="a4279-118">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="a4279-118">Row index:</span></span>  <br/> |<span data-ttu-id="a4279-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="a4279-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="a4279-120">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="a4279-120">Cell index:</span></span>  <br/> |<span data-ttu-id="a4279-121">**visLockEnd**</span><span class="sxs-lookup"><span data-stu-id="a4279-121">**visLockEnd**</span></span> <br/> |
   

