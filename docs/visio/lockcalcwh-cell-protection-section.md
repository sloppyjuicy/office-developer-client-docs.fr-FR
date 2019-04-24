---
title: LockCalcWH, cellule (section Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm605
localization_priority: Normal
ms.assetid: 6eb51e5a-03d8-3daa-b4e1-6107d540aed9
description: Verrouille un rectangle de sélection de la forme de sorte qu'elle ne puisse pas être recalculée lorsqu'un sommet est modifié ou que le type d'une ligne est changé dans la section Geometry.
ms.openlocfilehash: 2b1d907f480a22a56f5847035da8d1cbde5fdcc5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359632"
---
# <a name="lockcalcwh-cell-protection-section"></a><span data-ttu-id="2656f-103">LockCalcWH, cellule (section Protection)</span><span class="sxs-lookup"><span data-stu-id="2656f-103">LockCalcWH Cell (Protection Section)</span></span>

<span data-ttu-id="2656f-104">Verrouille un rectangle de sélection de la forme de sorte qu'elle ne puisse pas être recalculée lorsqu'un sommet est modifié ou que le type d'une ligne est changé dans la section Geometry.</span><span class="sxs-lookup"><span data-stu-id="2656f-104">Locks a shape's selection rectangle so it cannot be recalculated when a vertex is edited or a row type is changed in the Geometry section.</span></span>
  
|<span data-ttu-id="2656f-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="2656f-105">**Value**</span></span>|<span data-ttu-id="2656f-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="2656f-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="2656f-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="2656f-107">TRUE</span></span>  <br/> | <span data-ttu-id="2656f-108">La largeur et la hauteur ne peuvent pas être recalculées.</span><span class="sxs-lookup"><span data-stu-id="2656f-108">Width and height cannot be recalculated.</span></span>  <br/> |
| <span data-ttu-id="2656f-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="2656f-109">FALSE</span></span>  <br/> | <span data-ttu-id="2656f-110">La largeur et la hauteur peuvent être recalculées.</span><span class="sxs-lookup"><span data-stu-id="2656f-110">Width and height can be recalculated.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2656f-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="2656f-111">Remarks</span></span>

<span data-ttu-id="2656f-112">Pour obtenir une référence à la cellule LockCalcWH par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="2656f-112">To get a reference to the LockCalcWH cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2656f-113">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="2656f-113">Cell name:</span></span>  <br/> | <span data-ttu-id="2656f-114">LockCalcWH</span><span class="sxs-lookup"><span data-stu-id="2656f-114">LockCalcWH</span></span>  <br/> |
   
<span data-ttu-id="2656f-115">Pour obtenir une référence à la cellule LockCalcWH à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="2656f-115">To get a reference to the LockCalcWH cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2656f-116">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="2656f-116">Section index:</span></span>  <br/> |<span data-ttu-id="2656f-117">**Définis**</span><span class="sxs-lookup"><span data-stu-id="2656f-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="2656f-118">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="2656f-118">Row index:</span></span>  <br/> |<span data-ttu-id="2656f-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="2656f-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="2656f-120">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="2656f-120">Cell index:</span></span>  <br/> |<span data-ttu-id="2656f-121">**visLockCalcWH**</span><span class="sxs-lookup"><span data-stu-id="2656f-121">**visLockCalcWH**</span></span> <br/> |
   

