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
ms.openlocfilehash: 22b9366b750a85a76498b83880aac2b9b974e1ac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342748"
---
# <a name="conlinejumpdirx-cell-shape-layout-section"></a><span data-ttu-id="30d0b-103">ConLineJumpDirX, cellule (section Shape Layout)</span><span class="sxs-lookup"><span data-stu-id="30d0b-103">ConLineJumpDirX Cell (Shape Layout Section)</span></span>

<span data-ttu-id="30d0b-104">Détermine la direction de la déviation du trait dans le cas d'un connecteur dynamique horizontal d'une forme.</span><span class="sxs-lookup"><span data-stu-id="30d0b-104">Determines the line jump direction for line jumps occurring on a horizontal dynamic connector for a shape.</span></span>
  
|<span data-ttu-id="30d0b-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="30d0b-105">**Value**</span></span>|<span data-ttu-id="30d0b-106">**Direction de la déviation de trait**</span><span class="sxs-lookup"><span data-stu-id="30d0b-106">**Line jump direction**</span></span>|<span data-ttu-id="30d0b-107">**Constante d'automation**</span><span class="sxs-lookup"><span data-stu-id="30d0b-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="30d0b-108">0</span><span class="sxs-lookup"><span data-stu-id="30d0b-108">0</span></span>  <br/> | <span data-ttu-id="30d0b-109">Valeur par défaut de la page</span><span class="sxs-lookup"><span data-stu-id="30d0b-109">Page default</span></span>  <br/> |<span data-ttu-id="30d0b-110">**visLOJumpDirXDefault**</span><span class="sxs-lookup"><span data-stu-id="30d0b-110">**visLOJumpDirXDefault**</span></span> <br/> |
| <span data-ttu-id="30d0b-111">0,1</span><span class="sxs-lookup"><span data-stu-id="30d0b-111">1</span></span>  <br/> | <span data-ttu-id="30d0b-112">Up</span><span class="sxs-lookup"><span data-stu-id="30d0b-112">Up</span></span>  <br/> |<span data-ttu-id="30d0b-113">**visLOJumpDirXUp**</span><span class="sxs-lookup"><span data-stu-id="30d0b-113">**visLOJumpDirXUp**</span></span> <br/> |
| <span data-ttu-id="30d0b-114">n°2</span><span class="sxs-lookup"><span data-stu-id="30d0b-114">2</span></span>  <br/> | <span data-ttu-id="30d0b-115">Down</span><span class="sxs-lookup"><span data-stu-id="30d0b-115">Down</span></span>  <br/> |<span data-ttu-id="30d0b-116">**visLOJumpDirXDown**</span><span class="sxs-lookup"><span data-stu-id="30d0b-116">**visLOJumpDirXDown**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="30d0b-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="30d0b-117">Remarks</span></span>

<span data-ttu-id="30d0b-118">Pour définir la direction horizontale par défaut de *toutes les* déviations de connecteur d'une page, utilisez la cellule PageLineJumpDirX de la section Page Layout.</span><span class="sxs-lookup"><span data-stu-id="30d0b-118">To set the default horizontal direction for  *all*  connector jumps on a page, use the PageLineJumpDirX cell in the Page Layout section.</span></span> 
  
<span data-ttu-id="30d0b-119">Pour obtenir une référence à la cellule ConLineJumpDirX par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="30d0b-119">To get a reference to the ConLineJumpDirX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="30d0b-120">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="30d0b-120">Cell name:</span></span>  <br/> | <span data-ttu-id="30d0b-121">ConLineJumpDirX</span><span class="sxs-lookup"><span data-stu-id="30d0b-121">ConLineJumpDirX</span></span>  <br/> |
   
<span data-ttu-id="30d0b-122">Pour obtenir une référence à la cellule ConLineJumpDirX à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="30d0b-122">To get a reference to the ConLineJumpDirX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="30d0b-123">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="30d0b-123">Section index:</span></span>  <br/> |<span data-ttu-id="30d0b-124">**Définis**</span><span class="sxs-lookup"><span data-stu-id="30d0b-124">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="30d0b-125">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="30d0b-125">Row index:</span></span>  <br/> |<span data-ttu-id="30d0b-126">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="30d0b-126">**visRowShapeLayout**</span></span> <br/> |
| <span data-ttu-id="30d0b-127">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="30d0b-127">Cell index:</span></span>  <br/> |<span data-ttu-id="30d0b-128">**visSLOJumpDirX**</span><span class="sxs-lookup"><span data-stu-id="30d0b-128">**visSLOJumpDirX**</span></span> <br/> |
   

