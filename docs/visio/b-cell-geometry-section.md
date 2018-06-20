---
title: B, cellule (section Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251751
localization_priority: Normal
ms.assetid: b0fb6a47-47d8-ab9c-854d-0b0bbfdfcc27
description: Représente des informations différentes selon la ligne où elle se trouve. Le tableau ci-dessous décrit la cellule B pour chaque ligne.
ms.openlocfilehash: 7d6f51d037be4852c6a101ad6e576a3a13488cb7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788044"
---
# <a name="b-cell-geometry-section"></a><span data-ttu-id="f9c5c-104">B, cellule (section Geometry)</span><span class="sxs-lookup"><span data-stu-id="f9c5c-104">B Cell (Geometry Section)</span></span>

<span data-ttu-id="f9c5c-p102">Représente des informations différentes selon la ligne où elle se trouve. Le tableau ci-dessous décrit la cellule B pour chaque ligne.</span><span class="sxs-lookup"><span data-stu-id="f9c5c-p102">Represents different information in different rows. This table describes the B cell based on the row in which it's located.</span></span>
  
|<span data-ttu-id="f9c5c-107">**Row**</span><span class="sxs-lookup"><span data-stu-id="f9c5c-107">**Row**</span></span>|<span data-ttu-id="f9c5c-108">**Description**</span><span class="sxs-lookup"><span data-stu-id="f9c5c-108">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f9c5c-109">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="f9c5c-109">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="f9c5c-110">La valeur *y* -coordonnées du point de contrôle d’un arc.</span><span class="sxs-lookup"><span data-stu-id="f9c5c-110">The  *y*  -coordinate of an arc's control point.</span></span>  <br/> |
|[<span data-ttu-id="f9c5c-111">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="f9c5c-111">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="f9c5c-112">Dernière épaisseur de la courbe B-spline rationnelle non uniforme (NURBS).</span><span class="sxs-lookup"><span data-stu-id="f9c5c-112">The last weight of the nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|[<span data-ttu-id="f9c5c-113">SplineStart</span><span class="sxs-lookup"><span data-stu-id="f9c5c-113">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> | <span data-ttu-id="f9c5c-114">Premier nœud d’une spline</span><span class="sxs-lookup"><span data-stu-id="f9c5c-114">The first knot of a spline.</span></span>  <br/> |
|[<span data-ttu-id="f9c5c-115">InfiniteLine</span><span class="sxs-lookup"><span data-stu-id="f9c5c-115">InfiniteLine</span></span>](infiniteline-row-geometry-section.md) <br/> | <span data-ttu-id="f9c5c-116">*Y* -coordonnées d’un point sur la ligne infinie ; associée à la *x* -coordonnée représentée par la cellule [A](a-cell-geometry-section.md) .</span><span class="sxs-lookup"><span data-stu-id="f9c5c-116">A  *y*  -coordinate of a point on an infinite line; paired with  *x*  -coordinate represented by the [A](a-cell-geometry-section.md) cell.</span></span>  <br/> |
|[<span data-ttu-id="f9c5c-117">Ellipse</span><span class="sxs-lookup"><span data-stu-id="f9c5c-117">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="f9c5c-118">*Y* -coordonnées d’un point sur une ellipse ; associée à la *x* -coordonnée représentée par la cellule [A](a-cell-geometry-section.md) .</span><span class="sxs-lookup"><span data-stu-id="f9c5c-118">A  *y*  -coordinate of a point on an ellipse; paired with  *x*  -coordinate represented by the [A](a-cell-geometry-section.md) cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f9c5c-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="f9c5c-119">Remarks</span></span>

<span data-ttu-id="f9c5c-120">Pour obtenir une référence à la cellule B par un nom à partir d’une autre formule ou d’un programme, utilisez la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="f9c5c-120">To get a reference to the B cell by name from another formula, or from a program, using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f9c5c-121">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="f9c5c-121">Cell name:</span></span>  <br/> | <span data-ttu-id="f9c5c-122">Géométrie *i* . B *j* où *i* et *j* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="f9c5c-122">Geometry  *i*  .B  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="f9c5c-123">Géométrie *i* . B1 (lignes InfiniteLine et Ellipse)</span><span class="sxs-lookup"><span data-stu-id="f9c5c-123">Geometry  *i*  .B1 (InfiniteLine and Ellipse rows)</span></span>  <br/> |
   
<span data-ttu-id="f9c5c-124">Pour obtenir une référence à la cellule B par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="f9c5c-124">To get a reference to the B cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f9c5c-125">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="f9c5c-125">Section index:</span></span>  <br/> |<span data-ttu-id="f9c5c-126">**visSectionFirstComponent** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="f9c5c-126">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="f9c5c-127">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="f9c5c-127">Row index:</span></span>  <br/> |<span data-ttu-id="f9c5c-128">**visRowVertex** +  *j* où *j* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="f9c5c-128">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="f9c5c-129">**visRowVertex** (Lignes InfiniteLine et Ellipse)</span><span class="sxs-lookup"><span data-stu-id="f9c5c-129">**visRowVertex** (InfiniteLine and Ellipse rows)</span></span>  <br/> |
| <span data-ttu-id="f9c5c-130">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="f9c5c-130">Cell index:</span></span>  <br/> |<span data-ttu-id="f9c5c-131">**visControlX** (Ligne EllipticalArcTo)</span><span class="sxs-lookup"><span data-stu-id="f9c5c-131">**visControlX** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="f9c5c-132">**visControlY** (Ligne EllipticalArcTo)</span><span class="sxs-lookup"><span data-stu-id="f9c5c-132">**visControlY** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="f9c5c-133">**visNURBSWeight** (Ligne NURBSTo)</span><span class="sxs-lookup"><span data-stu-id="f9c5c-133">**visNURBSWeight** (NURBSTo row)</span></span>  <br/> |
||<span data-ttu-id="f9c5c-134">**visSplineKnot2** (Ligne SplineStart)</span><span class="sxs-lookup"><span data-stu-id="f9c5c-134">**visSplineKnot2** (SplineStart row)</span></span>  <br/> |
||<span data-ttu-id="f9c5c-135">**visInfiniteLineY2** (Ligne InfiniteLine)</span><span class="sxs-lookup"><span data-stu-id="f9c5c-135">**visInfiniteLineY2** (InfiniteLine row)</span></span>  <br/> |
||<span data-ttu-id="f9c5c-136">**visEllipseMajorY** (Ligne ellipse)</span><span class="sxs-lookup"><span data-stu-id="f9c5c-136">**visEllipseMajorY** (Ellipse row)</span></span>  <br/> |
   

