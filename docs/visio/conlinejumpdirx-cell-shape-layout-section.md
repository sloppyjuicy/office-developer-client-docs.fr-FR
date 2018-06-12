---
title: ConLineJumpDirX, cellule (section Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm185
localization_priority: Normal
ms.assetid: f0671835-8d48-907a-eca6-43953658f800
description: Détermine la direction de la déviation du trait dans le cas d'un connecteur dynamique horizontal d'une forme.
ms.openlocfilehash: 396830d0da22c15f036f95808b3a94c33e9dc5bb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788327"
---
# <a name="conlinejumpdirx-cell-shape-layout-section"></a><span data-ttu-id="e6eb4-103">ConLineJumpDirX, cellule (section Shape Layout)</span><span class="sxs-lookup"><span data-stu-id="e6eb4-103">ConLineJumpDirX Cell (Shape Layout Section)</span></span>

<span data-ttu-id="e6eb4-104">Détermine la direction de la déviation du trait dans le cas d'un connecteur dynamique horizontal d'une forme.</span><span class="sxs-lookup"><span data-stu-id="e6eb4-104">Determines the line jump direction for line jumps occurring on a horizontal dynamic connector for a shape.</span></span>
  
|<span data-ttu-id="e6eb4-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="e6eb4-105">**Value**</span></span>|<span data-ttu-id="e6eb4-106">**Direction de déviation de trait**</span><span class="sxs-lookup"><span data-stu-id="e6eb4-106">**Line jump direction**</span></span>|<span data-ttu-id="e6eb4-107">**Constante d’Automation**</span><span class="sxs-lookup"><span data-stu-id="e6eb4-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="e6eb4-108">0</span><span class="sxs-lookup"><span data-stu-id="e6eb4-108">0</span></span>  <br/> | <span data-ttu-id="e6eb4-109">Valeur par défaut de la page</span><span class="sxs-lookup"><span data-stu-id="e6eb4-109">Page default</span></span>  <br/> |<span data-ttu-id="e6eb4-110">**visLOJumpDirXDefault**</span><span class="sxs-lookup"><span data-stu-id="e6eb4-110">**visLOJumpDirXDefault**</span></span> <br/> |
| <span data-ttu-id="e6eb4-111">1</span><span class="sxs-lookup"><span data-stu-id="e6eb4-111">1</span></span>  <br/> | <span data-ttu-id="e6eb4-112">Haut</span><span class="sxs-lookup"><span data-stu-id="e6eb4-112">Up</span></span>  <br/> |<span data-ttu-id="e6eb4-113">**visLOJumpDirXUp**</span><span class="sxs-lookup"><span data-stu-id="e6eb4-113">**visLOJumpDirXUp**</span></span> <br/> |
| <span data-ttu-id="e6eb4-114">2</span><span class="sxs-lookup"><span data-stu-id="e6eb4-114">2</span></span>  <br/> | <span data-ttu-id="e6eb4-115">Bas</span><span class="sxs-lookup"><span data-stu-id="e6eb4-115">Down</span></span>  <br/> |<span data-ttu-id="e6eb4-116">**visLOJumpDirXDown**</span><span class="sxs-lookup"><span data-stu-id="e6eb4-116">**visLOJumpDirXDown**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e6eb4-117">Note</span><span class="sxs-lookup"><span data-stu-id="e6eb4-117">Remarks</span></span>

<span data-ttu-id="e6eb4-118">Pour définir la valeur par défaut direction horizontale de connecteur de *toutes les* déviations sur une page, utilisez la cellule PageLineJumpDirX de la section Page Layout.</span><span class="sxs-lookup"><span data-stu-id="e6eb4-118">To set the default horizontal direction for  *all*  connector jumps on a page, use the PageLineJumpDirX cell in the Page Layout section.</span></span> 
  
<span data-ttu-id="e6eb4-119">Pour obtenir une référence à la cellule ConLineJumpDirX par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="e6eb4-119">To get a reference to the ConLineJumpDirX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e6eb4-120">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="e6eb4-120">Cell name:</span></span>  <br/> | <span data-ttu-id="e6eb4-121">ConLineJumpDirX</span><span class="sxs-lookup"><span data-stu-id="e6eb4-121">ConLineJumpDirX</span></span>  <br/> |
   
<span data-ttu-id="e6eb4-122">Pour obtenir une référence à la cellule ConLineJumpDirX par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="e6eb4-122">To get a reference to the ConLineJumpDirX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e6eb4-123">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="e6eb4-123">Section index:</span></span>  <br/> |<span data-ttu-id="e6eb4-124">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e6eb4-124">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="e6eb4-125">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="e6eb4-125">Row index:</span></span>  <br/> |<span data-ttu-id="e6eb4-126">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="e6eb4-126">**visRowShapeLayout**</span></span> <br/> |
| <span data-ttu-id="e6eb4-127">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="e6eb4-127">Cell index:</span></span>  <br/> |<span data-ttu-id="e6eb4-128">**visSLOJumpDirX**</span><span class="sxs-lookup"><span data-stu-id="e6eb4-128">**visSLOJumpDirX**</span></span> <br/> |
   

