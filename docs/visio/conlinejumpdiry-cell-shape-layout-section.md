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
ms.openlocfilehash: f86c77da62042d1bc2c0274564efa9fdb0887971
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404770"
---
# <a name="conlinejumpdiry-cell-shape-layout-section"></a><span data-ttu-id="958df-103">ConLineJumpDirY, cellule (section Shape Layout)</span><span class="sxs-lookup"><span data-stu-id="958df-103">ConLineJumpDirY Cell (Shape Layout Section)</span></span>

<span data-ttu-id="958df-104">Détermine la direction de la déviation de trait dans le cas d'un connecteur dynamique vertical d'une forme.</span><span class="sxs-lookup"><span data-stu-id="958df-104">Determines the line jump direction for line jumps occurring on a vertical dynamic connector for a shape.</span></span>
  
|<span data-ttu-id="958df-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="958df-105">**Value**</span></span>|<span data-ttu-id="958df-106">**Direction de la déviation**</span><span class="sxs-lookup"><span data-stu-id="958df-106">**Line Jump Direction**</span></span>|<span data-ttu-id="958df-107">**Constante d'automation**</span><span class="sxs-lookup"><span data-stu-id="958df-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="958df-108">0</span><span class="sxs-lookup"><span data-stu-id="958df-108">0</span></span>  <br/> | <span data-ttu-id="958df-109">Valeur par défaut de la page</span><span class="sxs-lookup"><span data-stu-id="958df-109">Page default</span></span>  <br/> |<span data-ttu-id="958df-110">**visLOJumpDirYDefault**</span><span class="sxs-lookup"><span data-stu-id="958df-110">**visLOJumpDirYDefault**</span></span> <br/> |
| <span data-ttu-id="958df-111">0,1</span><span class="sxs-lookup"><span data-stu-id="958df-111">1</span></span>  <br/> | <span data-ttu-id="958df-112">À gauche</span><span class="sxs-lookup"><span data-stu-id="958df-112">Left</span></span>  <br/> |<span data-ttu-id="958df-113">**visLOJumpDirYLeft**</span><span class="sxs-lookup"><span data-stu-id="958df-113">**visLOJumpDirYLeft**</span></span> <br/> |
| <span data-ttu-id="958df-114">n°2</span><span class="sxs-lookup"><span data-stu-id="958df-114">2</span></span>  <br/> | <span data-ttu-id="958df-115">À droite</span><span class="sxs-lookup"><span data-stu-id="958df-115">Right</span></span>  <br/> |<span data-ttu-id="958df-116">**visLOJumpDirYRight**</span><span class="sxs-lookup"><span data-stu-id="958df-116">**visLOJumpDirYRight**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="958df-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="958df-117">Remarks</span></span>

<span data-ttu-id="958df-118">Pour définir la direction verticale par défaut de *toutes les* déviations de connecteur d'une page, utilisez la cellule PageLineJumpDirY de la section Page Layout.</span><span class="sxs-lookup"><span data-stu-id="958df-118">To set the default vertical direction for  *all*  connector jumps on a page, use the PageLineJumpDirY cell in the Page Layout section.</span></span> 
  
<span data-ttu-id="958df-119">Pour obtenir une référence à la cellule ConLineJumpDirY par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="958df-119">To get a reference to the ConLineJumpDirY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="958df-120">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="958df-120">Cell name:</span></span>  <br/> | <span data-ttu-id="958df-121">ConLineJumpDirY</span><span class="sxs-lookup"><span data-stu-id="958df-121">ConLineJumpDirY</span></span>  <br/> |
   
<span data-ttu-id="958df-122">Pour obtenir une référence à la cellule ConLineJumpDirY à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="958df-122">To get a reference to the ConLineJumpDirY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="958df-123">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="958df-123">Section index:</span></span>  <br/> |<span data-ttu-id="958df-124">**Définis**</span><span class="sxs-lookup"><span data-stu-id="958df-124">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="958df-125">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="958df-125">Row index:</span></span>  <br/> |<span data-ttu-id="958df-126">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="958df-126">**visRowShapeLayout**</span></span> <br/> |
| <span data-ttu-id="958df-127">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="958df-127">Cell index:</span></span>  <br/> |<span data-ttu-id="958df-128">**visSLOJumpDirY**</span><span class="sxs-lookup"><span data-stu-id="958df-128">**visSLOJumpDirY**</span></span> <br/> |
   

