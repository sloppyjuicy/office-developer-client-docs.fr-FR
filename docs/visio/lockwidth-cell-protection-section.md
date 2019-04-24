---
title: LockWidth, cellule (section Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm675
localization_priority: Normal
ms.assetid: fef022ea-38ab-2b66-60c8-b94a6b0bdfbf
description: Verrouille la largeur d'une forme afin qu'elle demeure intacte lorsque la forme est dimensionnée.
ms.openlocfilehash: 84c89b5f264c00d6fe5f95cb27eae74b91b88dc3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314832"
---
# <a name="lockwidth-cell-protection-section"></a><span data-ttu-id="5ef0d-103">LockWidth, cellule (section Protection)</span><span class="sxs-lookup"><span data-stu-id="5ef0d-103">LockWidth Cell (Protection Section)</span></span>

<span data-ttu-id="5ef0d-104">Verrouille la largeur d'une forme afin qu'elle demeure intacte lorsque la forme est dimensionnée.</span><span class="sxs-lookup"><span data-stu-id="5ef0d-104">Locks the width of the shape so that its width remains unchanged when the shape is sized.</span></span>
  
|<span data-ttu-id="5ef0d-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="5ef0d-105">**Value**</span></span>|<span data-ttu-id="5ef0d-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="5ef0d-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="5ef0d-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="5ef0d-107">TRUE</span></span>  <br/> | <span data-ttu-id="5ef0d-108">La largeur est verrouillée.</span><span class="sxs-lookup"><span data-stu-id="5ef0d-108">Width is locked.</span></span>  <br/> |
| <span data-ttu-id="5ef0d-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="5ef0d-109">FALSE</span></span>  <br/> | <span data-ttu-id="5ef0d-110">La largeur n'est pas verrouillée.</span><span class="sxs-lookup"><span data-stu-id="5ef0d-110">Width is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5ef0d-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="5ef0d-111">Remarks</span></span>

<span data-ttu-id="5ef0d-112">Pour obtenir une référence à la cellule LockWidth par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="5ef0d-112">To get a reference to the LockWidth cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5ef0d-113">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="5ef0d-113">Cell name:</span></span>  <br/> | <span data-ttu-id="5ef0d-114">LockWidth</span><span class="sxs-lookup"><span data-stu-id="5ef0d-114">LockWidth</span></span>  <br/> |
   
<span data-ttu-id="5ef0d-115">Pour obtenir une référence à la cellule LockWidth à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="5ef0d-115">To get a reference to the LockWidth cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5ef0d-116">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="5ef0d-116">Section index:</span></span>  <br/> |<span data-ttu-id="5ef0d-117">**Définis**</span><span class="sxs-lookup"><span data-stu-id="5ef0d-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="5ef0d-118">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="5ef0d-118">Row index:</span></span>  <br/> |<span data-ttu-id="5ef0d-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="5ef0d-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="5ef0d-120">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="5ef0d-120">Cell index:</span></span>  <br/> |<span data-ttu-id="5ef0d-121">**visLockWidth**</span><span class="sxs-lookup"><span data-stu-id="5ef0d-121">**visLockWidth**</span></span> <br/> |
   

