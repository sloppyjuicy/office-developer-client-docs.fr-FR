---
title: LockMoveY, cellule (section Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm645
localization_priority: Normal
ms.assetid: 4ed8cab4-112a-e96a-f4e3-02490a6f87fa
description: Verrouille la position verticale de la forme afin d'empêcher son déplacement vertical.
ms.openlocfilehash: 24f6f477860ea3634cfdcfd92199f2de65e543db
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789005"
---
# <a name="lockmovey-cell-protection-section"></a><span data-ttu-id="c800f-103">LockMoveY, cellule (section Protection)</span><span class="sxs-lookup"><span data-stu-id="c800f-103">LockMoveY Cell (Protection Section)</span></span>

<span data-ttu-id="c800f-104">Verrouille la position verticale de la forme afin d'empêcher son déplacement vertical.</span><span class="sxs-lookup"><span data-stu-id="c800f-104">Locks the vertical position of the shape so it cannot be moved vertically.</span></span>
  
|<span data-ttu-id="c800f-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="c800f-105">**Value**</span></span>|<span data-ttu-id="c800f-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="c800f-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="c800f-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="c800f-107">TRUE</span></span>  <br/> | <span data-ttu-id="c800f-108">La position verticale est verrouillée.</span><span class="sxs-lookup"><span data-stu-id="c800f-108">Vertical position is locked.</span></span>  <br/> |
| <span data-ttu-id="c800f-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="c800f-109">FALSE</span></span>  <br/> | <span data-ttu-id="c800f-110">La position verticale n'est pas verrouillée.</span><span class="sxs-lookup"><span data-stu-id="c800f-110">Vertical position is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c800f-111">Note</span><span class="sxs-lookup"><span data-stu-id="c800f-111">Remarks</span></span>

<span data-ttu-id="c800f-112">Pour obtenir une référence à la cellule LockMoveY par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="c800f-112">To get a reference to the LockMoveY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c800f-113">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="c800f-113">Cell name:</span></span>  <br/> | <span data-ttu-id="c800f-114">LockMoveY</span><span class="sxs-lookup"><span data-stu-id="c800f-114">LockMoveY</span></span>  <br/> |
   
<span data-ttu-id="c800f-115">Pour obtenir une référence à la cellule LockMoveY par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="c800f-115">To get a reference to the LockMoveY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c800f-116">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="c800f-116">Section index:</span></span>  <br/> |<span data-ttu-id="c800f-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c800f-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c800f-118">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="c800f-118">Row index:</span></span>  <br/> |<span data-ttu-id="c800f-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="c800f-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="c800f-120">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="c800f-120">Cell index:</span></span>  <br/> |<span data-ttu-id="c800f-121">**visLockMoveY**</span><span class="sxs-lookup"><span data-stu-id="c800f-121">**visLockMoveY**</span></span> <br/> |
   

