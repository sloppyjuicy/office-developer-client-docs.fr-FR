---
title: ConLineJumpDirY, cellule (section Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251654
localization_priority: Normal
ms.assetid: 93f82ae0-3442-fac1-9906-b84afef85f5c
description: Détermine la direction de la déviation de trait dans le cas d'un connecteur dynamique vertical d'une forme.
ms.openlocfilehash: 2d0c0964b52c9afbccc9cb507024825434702b6d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788315"
---
# <a name="conlinejumpdiry-cell-shape-layout-section"></a><span data-ttu-id="e7611-103">ConLineJumpDirY, cellule (section Shape Layout)</span><span class="sxs-lookup"><span data-stu-id="e7611-103">ConLineJumpDirY Cell (Shape Layout Section)</span></span>

<span data-ttu-id="e7611-104">Détermine la direction de la déviation de trait dans le cas d'un connecteur dynamique vertical d'une forme.</span><span class="sxs-lookup"><span data-stu-id="e7611-104">Determines the line jump direction for line jumps occurring on a vertical dynamic connector for a shape.</span></span>
  
|<span data-ttu-id="e7611-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="e7611-105">**Value**</span></span>|<span data-ttu-id="e7611-106">**Direction de déviation de trait**</span><span class="sxs-lookup"><span data-stu-id="e7611-106">**Line Jump Direction**</span></span>|<span data-ttu-id="e7611-107">**Constante d’Automation**</span><span class="sxs-lookup"><span data-stu-id="e7611-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="e7611-108">0</span><span class="sxs-lookup"><span data-stu-id="e7611-108">0</span></span>  <br/> | <span data-ttu-id="e7611-109">Valeur par défaut de la page</span><span class="sxs-lookup"><span data-stu-id="e7611-109">Page default</span></span>  <br/> |<span data-ttu-id="e7611-110">**visLOJumpDirYDefault**</span><span class="sxs-lookup"><span data-stu-id="e7611-110">**visLOJumpDirYDefault**</span></span> <br/> |
| <span data-ttu-id="e7611-111">1</span><span class="sxs-lookup"><span data-stu-id="e7611-111">1</span></span>  <br/> | <span data-ttu-id="e7611-112">Gauche</span><span class="sxs-lookup"><span data-stu-id="e7611-112">Left</span></span>  <br/> |<span data-ttu-id="e7611-113">**visLOJumpDirYLeft**</span><span class="sxs-lookup"><span data-stu-id="e7611-113">**visLOJumpDirYLeft**</span></span> <br/> |
| <span data-ttu-id="e7611-114">2</span><span class="sxs-lookup"><span data-stu-id="e7611-114">2</span></span>  <br/> | <span data-ttu-id="e7611-115">Droite</span><span class="sxs-lookup"><span data-stu-id="e7611-115">Right</span></span>  <br/> |<span data-ttu-id="e7611-116">**visLOJumpDirYRight**</span><span class="sxs-lookup"><span data-stu-id="e7611-116">**visLOJumpDirYRight**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e7611-117">Note</span><span class="sxs-lookup"><span data-stu-id="e7611-117">Remarks</span></span>

<span data-ttu-id="e7611-118">Pour définir la valeur par défaut direction verticale de connecteur de *toutes les* déviations sur une page, utilisez la cellule PageLineJumpDirY de la section Page Layout.</span><span class="sxs-lookup"><span data-stu-id="e7611-118">To set the default vertical direction for  *all*  connector jumps on a page, use the PageLineJumpDirY cell in the Page Layout section.</span></span> 
  
<span data-ttu-id="e7611-119">Pour obtenir une référence à la cellule ConLineJumpDirY par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="e7611-119">To get a reference to the ConLineJumpDirY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e7611-120">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="e7611-120">Cell name:</span></span>  <br/> | <span data-ttu-id="e7611-121">ConLineJumpDirY</span><span class="sxs-lookup"><span data-stu-id="e7611-121">ConLineJumpDirY</span></span>  <br/> |
   
<span data-ttu-id="e7611-122">Pour obtenir une référence à la cellule ConLineJumpDirY par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="e7611-122">To get a reference to the ConLineJumpDirY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e7611-123">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="e7611-123">Section index:</span></span>  <br/> |<span data-ttu-id="e7611-124">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e7611-124">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="e7611-125">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="e7611-125">Row index:</span></span>  <br/> |<span data-ttu-id="e7611-126">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="e7611-126">**visRowShapeLayout**</span></span> <br/> |
| <span data-ttu-id="e7611-127">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="e7611-127">Cell index:</span></span>  <br/> |<span data-ttu-id="e7611-128">**visSLOJumpDirY**</span><span class="sxs-lookup"><span data-stu-id="e7611-128">**visSLOJumpDirY**</span></span> <br/> |
   

