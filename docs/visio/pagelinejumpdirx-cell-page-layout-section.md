---
title: PageLineJumpDirX, cellule (section Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251656
localization_priority: Normal
ms.assetid: 77892ec7-4c6a-78a5-5af4-5b6be7709e77
description: Détermine la direction des déviations de trait pour les connecteurs dynamiques horizontaux de la page de dessin n'ayant pas de direction de déviation locale.
ms.openlocfilehash: 4e1213990877e1260cc8cecd5a55beda4592a844
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283736"
---
# <a name="pagelinejumpdirx-cell-page-layout-section"></a><span data-ttu-id="2866e-103">PageLineJumpDirX, cellule (section Page Layout)</span><span class="sxs-lookup"><span data-stu-id="2866e-103">PageLineJumpDirX Cell (Page Layout Section)</span></span>

<span data-ttu-id="2866e-104">Détermine la direction des déviations de trait pour les connecteurs dynamiques horizontaux de la page de dessin n'ayant pas de direction de déviation locale.</span><span class="sxs-lookup"><span data-stu-id="2866e-104">Determines the direction of line jumps on horizontal dynamic connectors on the drawing page for which you haven't applied a local jump direction.</span></span>
  
|<span data-ttu-id="2866e-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="2866e-105">**Value**</span></span>|<span data-ttu-id="2866e-106">**Direction de la déviation de trait**</span><span class="sxs-lookup"><span data-stu-id="2866e-106">**Line jump direction**</span></span>|<span data-ttu-id="2866e-107">**Constante d'automation**</span><span class="sxs-lookup"><span data-stu-id="2866e-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="2866e-108">0</span><span class="sxs-lookup"><span data-stu-id="2866e-108">0</span></span>  <br/> | <span data-ttu-id="2866e-109">Par défaut ; à gauche ou paramètres de la page pour les formes</span><span class="sxs-lookup"><span data-stu-id="2866e-109">Default; left or the page's setting for shapes</span></span>  <br/> |<span data-ttu-id="2866e-110">**visLOJumpDirXDefault**</span><span class="sxs-lookup"><span data-stu-id="2866e-110">**visLOJumpDirXDefault**</span></span> <br/> |
| <span data-ttu-id="2866e-111">0,1</span><span class="sxs-lookup"><span data-stu-id="2866e-111">1</span></span>  <br/> | <span data-ttu-id="2866e-112">Up</span><span class="sxs-lookup"><span data-stu-id="2866e-112">Up</span></span>  <br/> |<span data-ttu-id="2866e-113">**visLOJumpDirXUp**</span><span class="sxs-lookup"><span data-stu-id="2866e-113">**visLOJumpDirXUp**</span></span> <br/> |
| <span data-ttu-id="2866e-114">n°2</span><span class="sxs-lookup"><span data-stu-id="2866e-114">2</span></span>  <br/> | <span data-ttu-id="2866e-115">Down</span><span class="sxs-lookup"><span data-stu-id="2866e-115">Down</span></span>  <br/> |<span data-ttu-id="2866e-116">**visLOJumpDirXDown**</span><span class="sxs-lookup"><span data-stu-id="2866e-116">**visLOJumpDirXDown**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2866e-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="2866e-117">Remarks</span></span>

<span data-ttu-id="2866e-118">Pour obtenir une référence à la cellule PageLineJumpDirX par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="2866e-118">To get a reference to the PageLineJumpDirX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2866e-119">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="2866e-119">Cell name:</span></span>  <br/> | <span data-ttu-id="2866e-120">PageLineJumpDirX</span><span class="sxs-lookup"><span data-stu-id="2866e-120">PageLineJumpDirX</span></span>  <br/> |
   
<span data-ttu-id="2866e-121">Pour obtenir une référence à la cellule PageLineJumpDirX à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="2866e-121">To get a reference to the PageLineJumpDirX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2866e-122">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="2866e-122">Section index:</span></span>  <br/> |<span data-ttu-id="2866e-123">**Définis**</span><span class="sxs-lookup"><span data-stu-id="2866e-123">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="2866e-124">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="2866e-124">Row index:</span></span>  <br/> |<span data-ttu-id="2866e-125">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="2866e-125">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="2866e-126">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="2866e-126">Cell index:</span></span>  <br/> |<span data-ttu-id="2866e-127">**visPLOJumpDirX**</span><span class="sxs-lookup"><span data-stu-id="2866e-127">**visPLOJumpDirX**</span></span> <br/> |
   

