---
title: LockMoveX, cellule (section Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm640
localization_priority: Normal
ms.assetid: 48ceeeed-66ae-a81f-2aee-f0010102dfb7
description: Verrouille la position horizontale de la forme afin d'empêcher son déplacement horizontal.
ms.openlocfilehash: af0cee32370a540cd8d7aaf960cc0cbc27cc8f97
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348264"
---
# <a name="lockmovex-cell-protection-section"></a><span data-ttu-id="40b00-103">LockMoveX, cellule (section Protection)</span><span class="sxs-lookup"><span data-stu-id="40b00-103">LockMoveX Cell (Protection Section)</span></span>

<span data-ttu-id="40b00-104">Verrouille la position horizontale de la forme afin d'empêcher son déplacement horizontal.</span><span class="sxs-lookup"><span data-stu-id="40b00-104">Locks the horizontal position of the shape so it cannot be moved horizontally.</span></span>
  
|<span data-ttu-id="40b00-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="40b00-105">**Value**</span></span>|<span data-ttu-id="40b00-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="40b00-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="40b00-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="40b00-107">TRUE</span></span>  <br/> | <span data-ttu-id="40b00-108">La position horizontale est verrouillée.</span><span class="sxs-lookup"><span data-stu-id="40b00-108">Horizontal position is locked.</span></span>  <br/> |
| <span data-ttu-id="40b00-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="40b00-109">FALSE</span></span>  <br/> | <span data-ttu-id="40b00-110">La position horizontale n'est pas verrouillée.</span><span class="sxs-lookup"><span data-stu-id="40b00-110">Horizontal position is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="40b00-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="40b00-111">Remarks</span></span>

<span data-ttu-id="40b00-112">Pour obtenir une référence à la cellule LockMoveX par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="40b00-112">To get a reference to the LockMoveX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="40b00-113">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="40b00-113">Cell name:</span></span>  <br/> | <span data-ttu-id="40b00-114">LockMoveX</span><span class="sxs-lookup"><span data-stu-id="40b00-114">LockMoveX</span></span>  <br/> |
   
<span data-ttu-id="40b00-115">Pour obtenir une référence à la cellule LockMoveX à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="40b00-115">To get a reference to the LockMoveX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="40b00-116">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="40b00-116">Section index:</span></span>  <br/> |<span data-ttu-id="40b00-117">**Définis**</span><span class="sxs-lookup"><span data-stu-id="40b00-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="40b00-118">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="40b00-118">Row index:</span></span>  <br/> |<span data-ttu-id="40b00-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="40b00-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="40b00-120">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="40b00-120">Cell index:</span></span>  <br/> |<span data-ttu-id="40b00-121">**visLockMoveX**</span><span class="sxs-lookup"><span data-stu-id="40b00-121">**visLockMoveX**</span></span> <br/> |
   

