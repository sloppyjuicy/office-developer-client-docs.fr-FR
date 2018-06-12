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
ms.openlocfilehash: f7f9c99eb4978e9b32968d3076b0341efe42faa6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788988"
---
# <a name="lockcalcwh-cell-protection-section"></a><span data-ttu-id="dc894-103">LockCalcWH, cellule (section Protection)</span><span class="sxs-lookup"><span data-stu-id="dc894-103">LockCalcWH Cell (Protection Section)</span></span>

<span data-ttu-id="dc894-104">Verrouille un rectangle de sélection de la forme de sorte qu'elle ne puisse pas être recalculée lorsqu'un sommet est modifié ou que le type d'une ligne est changé dans la section Geometry.</span><span class="sxs-lookup"><span data-stu-id="dc894-104">Locks a shape's selection rectangle so it cannot be recalculated when a vertex is edited or a row type is changed in the Geometry section.</span></span>
  
|<span data-ttu-id="dc894-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="dc894-105">**Value**</span></span>|<span data-ttu-id="dc894-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="dc894-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="dc894-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="dc894-107">TRUE</span></span>  <br/> | <span data-ttu-id="dc894-108">La largeur et la hauteur ne peuvent pas être recalculées.</span><span class="sxs-lookup"><span data-stu-id="dc894-108">Width and height cannot be recalculated.</span></span>  <br/> |
| <span data-ttu-id="dc894-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="dc894-109">FALSE</span></span>  <br/> | <span data-ttu-id="dc894-110">La largeur et la hauteur peuvent être recalculées.</span><span class="sxs-lookup"><span data-stu-id="dc894-110">Width and height can be recalculated.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dc894-111">Note</span><span class="sxs-lookup"><span data-stu-id="dc894-111">Remarks</span></span>

<span data-ttu-id="dc894-112">Pour obtenir une référence à la cellule LockCalcWH par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="dc894-112">To get a reference to the LockCalcWH cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="dc894-113">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="dc894-113">Cell name:</span></span>  <br/> | <span data-ttu-id="dc894-114">LockCalcWH</span><span class="sxs-lookup"><span data-stu-id="dc894-114">LockCalcWH</span></span>  <br/> |
   
<span data-ttu-id="dc894-115">Pour obtenir une référence à la cellule LockCalcWH par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="dc894-115">To get a reference to the LockCalcWH cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="dc894-116">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="dc894-116">Section index:</span></span>  <br/> |<span data-ttu-id="dc894-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="dc894-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="dc894-118">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="dc894-118">Row index:</span></span>  <br/> |<span data-ttu-id="dc894-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="dc894-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="dc894-120">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="dc894-120">Cell index:</span></span>  <br/> |<span data-ttu-id="dc894-121">**visLockCalcWH**</span><span class="sxs-lookup"><span data-stu-id="dc894-121">**visLockCalcWH**</span></span> <br/> |
   

