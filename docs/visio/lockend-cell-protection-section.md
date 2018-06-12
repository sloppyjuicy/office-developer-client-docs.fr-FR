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
ms.openlocfilehash: d29f07e5b4b77ed2fb8b104769a2fdca55abcc8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789000"
---
# <a name="lockend-cell-protection-section"></a><span data-ttu-id="11ca6-103">LockEnd, cellule (section Protection)</span><span class="sxs-lookup"><span data-stu-id="11ca6-103">LockEnd Cell (Protection Section)</span></span>

<span data-ttu-id="11ca6-104">Verrouille le point de fin (EndX, EndY) d'une forme 1D à un emplacement donné.</span><span class="sxs-lookup"><span data-stu-id="11ca6-104">Locks the endpoint (EndX, EndY) of a 1-D shape to a specific location.</span></span>
  
|<span data-ttu-id="11ca6-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="11ca6-105">**Value**</span></span>|<span data-ttu-id="11ca6-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="11ca6-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="11ca6-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="11ca6-107">TRUE</span></span>  <br/> | <span data-ttu-id="11ca6-108">Le point de fin est verrouillé.</span><span class="sxs-lookup"><span data-stu-id="11ca6-108">Endpoint is locked.</span></span>  <br/> |
| <span data-ttu-id="11ca6-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="11ca6-109">FALSE</span></span>  <br/> | <span data-ttu-id="11ca6-110">Le point de fin n'est pas verrouillé.</span><span class="sxs-lookup"><span data-stu-id="11ca6-110">Endpoint is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="11ca6-111">Note</span><span class="sxs-lookup"><span data-stu-id="11ca6-111">Remarks</span></span>

<span data-ttu-id="11ca6-112">Pour obtenir une référence à la cellule LockEnd par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="11ca6-112">To get a reference to the LockEnd cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="11ca6-113">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="11ca6-113">Cell name:</span></span>  <br/> | <span data-ttu-id="11ca6-114">LockEnd</span><span class="sxs-lookup"><span data-stu-id="11ca6-114">LockEnd</span></span>  <br/> |
   
<span data-ttu-id="11ca6-115">Pour obtenir une référence à la cellule LockEnd par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="11ca6-115">To get a reference to the LockEnd cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="11ca6-116">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="11ca6-116">Section index:</span></span>  <br/> |<span data-ttu-id="11ca6-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="11ca6-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="11ca6-118">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="11ca6-118">Row index:</span></span>  <br/> |<span data-ttu-id="11ca6-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="11ca6-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="11ca6-120">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="11ca6-120">Cell index:</span></span>  <br/> |<span data-ttu-id="11ca6-121">**visLockEnd**</span><span class="sxs-lookup"><span data-stu-id="11ca6-121">**visLockEnd**</span></span> <br/> |
   

