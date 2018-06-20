---
title: A, cellule (section Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm51215
localization_priority: Normal
ms.assetid: 6853df0f-d22e-89ca-7d34-342b9c0bea23
description: Représente des informations différentes selon la ligne où elle se trouve. Le tableau ci-dessous décrit la cellule A pour chaque ligne.
ms.openlocfilehash: b907552c2346292a6b14baf16481b6b40cc80fc4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787986"
---
# <a name="a-cell-geometry-section"></a><span data-ttu-id="3b678-104">A, cellule (section Geometry)</span><span class="sxs-lookup"><span data-stu-id="3b678-104">A Cell (Geometry Section)</span></span>

<span data-ttu-id="3b678-p102">Représente des informations différentes selon la ligne où elle se trouve. Le tableau ci-dessous décrit la cellule A pour chaque ligne.</span><span class="sxs-lookup"><span data-stu-id="3b678-p102">Represents different information in different rows. This table describes the A cell based on the row in which it's located.</span></span>
  
|<span data-ttu-id="3b678-107">**Row**</span><span class="sxs-lookup"><span data-stu-id="3b678-107">**Row**</span></span>|<span data-ttu-id="3b678-108">**Description**</span><span class="sxs-lookup"><span data-stu-id="3b678-108">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3b678-109">ArcTo</span><span class="sxs-lookup"><span data-stu-id="3b678-109">ArcTo</span></span>](arcto-row-geometry-section.md) <br/> | <span data-ttu-id="3b678-110">Distance entre le milieu de l’arc et le milieu de sa corde.</span><span class="sxs-lookup"><span data-stu-id="3b678-110">The distance from the arc's midpoint to the midpoint of its chord.</span></span>  <br/> |
|[<span data-ttu-id="3b678-111">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="3b678-111">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="3b678-112">*X* -coordonnées du point de contrôle de l’arc, un point sur l’arc. Le point de contrôle se trouve mieux sur à mi-chemin entre le début et fin sommets de l’arc. Sinon, l’arc peut atteindre une taille extrême afin de passer par le point de contrôle, avec des résultats imprévisibles.</span><span class="sxs-lookup"><span data-stu-id="3b678-112">The  *x*  -coordinate of the arc's control point, a point on the arc. The control point is best located about halfway between the beginning and ending vertices of the arc. Otherwise, the arc may grow to an extreme size in order to pass through the control point, with unpredictable results.</span></span>  <br/> |
|[<span data-ttu-id="3b678-113">PolylineTo</span><span class="sxs-lookup"><span data-stu-id="3b678-113">PolylineTo</span></span>](polylineto-row-geometry-section.md) <br/> | <span data-ttu-id="3b678-114">Formule de la polyligne.</span><span class="sxs-lookup"><span data-stu-id="3b678-114">The polyline formula.</span></span>  <br/> |
|[<span data-ttu-id="3b678-115">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="3b678-115">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="3b678-116">Avant-dernier nœud de la courbe B-spline rationnelle non uniforme (NURBS).</span><span class="sxs-lookup"><span data-stu-id="3b678-116">The second to the last knot of the nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|[<span data-ttu-id="3b678-117">SplineStart</span><span class="sxs-lookup"><span data-stu-id="3b678-117">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> | <span data-ttu-id="3b678-118">Deuxième nœud de la spline.</span><span class="sxs-lookup"><span data-stu-id="3b678-118">The second knot of the spline.</span></span>  <br/> |
|[<span data-ttu-id="3b678-119">SplineKnot</span><span class="sxs-lookup"><span data-stu-id="3b678-119">SplineKnot</span></span>](splineknot-row-geometry-section.md) <br/> | <span data-ttu-id="3b678-120">Un des nœuds de la spline (autre que le dernier ou les deux premiers).</span><span class="sxs-lookup"><span data-stu-id="3b678-120">One of the spline's knots (other than the last one or the first two).</span></span>  <br/> |
|[<span data-ttu-id="3b678-121">InfiniteLine</span><span class="sxs-lookup"><span data-stu-id="3b678-121">InfiniteLine</span></span>](infiniteline-row-geometry-section.md) <br/> | <span data-ttu-id="3b678-122">*X* -coordonnées d’un point sur la ligne infinie ; associée à *y* -coordonnée représentée par la cellule [B](b-cell-geometry-section.md) .</span><span class="sxs-lookup"><span data-stu-id="3b678-122">An  *x*  -coordinate of a point on the infinite line; paired with  *y*  -coordinate represented by the [B](b-cell-geometry-section.md) cell.</span></span>  <br/> |
|[<span data-ttu-id="3b678-123">Ellipse</span><span class="sxs-lookup"><span data-stu-id="3b678-123">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="3b678-124">*X* -coordonnées d’un point sur l’ellipse ; associée à *y* -coordonnée représentée par la cellule [B](b-cell-geometry-section.md) .</span><span class="sxs-lookup"><span data-stu-id="3b678-124">An  *x*  -coordinate of a point on the ellipse; paired with  *y*  -coordinate represented by the [B](b-cell-geometry-section.md) cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3b678-125">Remarques</span><span class="sxs-lookup"><span data-stu-id="3b678-125">Remarks</span></span>

<span data-ttu-id="3b678-126">Pour obtenir une référence à la cellule A par un nom à partir d’une autre formule ou d’un programme, utilisez la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="3b678-126">To get a reference to the A cell by name from another formula, or from a program, using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3b678-127">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="3b678-127">Cell name:</span></span>  <br/> | <span data-ttu-id="3b678-128">Géométrie *i* . Un *j* où *i* et *j* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="3b678-128">Geometry  *i*  .A  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="3b678-129">Géométrie *i* . A1 (lignes InfiniteLine et Ellipse) où *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="3b678-129">Geometry  *i*  .A1 (InfiniteLine and Ellipse rows)            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="3b678-130">Pour obtenir une référence à la cellule A par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="3b678-130">To get a reference to the A cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3b678-131">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="3b678-131">Section index:</span></span>  <br/> |<span data-ttu-id="3b678-132">**visSectionFirstComponent** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="3b678-132">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="3b678-133">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="3b678-133">Row index:</span></span>  <br/> |<span data-ttu-id="3b678-134">**visRowVertex** +  *j* où *j* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="3b678-134">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="3b678-135">**visRowVertex** (Lignes InfiniteLine et Ellipse)</span><span class="sxs-lookup"><span data-stu-id="3b678-135">**visRowVertex** (InfiniteLine and Ellipse rows)</span></span>  <br/> |
| <span data-ttu-id="3b678-136">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="3b678-136">Cell index:</span></span>  <br/> |<span data-ttu-id="3b678-137">**visBow** (Ligne ArcTo)</span><span class="sxs-lookup"><span data-stu-id="3b678-137">**visBow** (ArcTo row)</span></span>  <br/> |
||<span data-ttu-id="3b678-138">**visControlX** (Ligne EllipticalArcTo)</span><span class="sxs-lookup"><span data-stu-id="3b678-138">**visControlX** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="3b678-139">**visControlY** (Ligne EllipticalArcTo)</span><span class="sxs-lookup"><span data-stu-id="3b678-139">**visControlY** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="3b678-140">**visPolylineData** (Ligne Polyline)</span><span class="sxs-lookup"><span data-stu-id="3b678-140">**visPolylineData** (Polyline row)</span></span>  <br/> |
||<span data-ttu-id="3b678-141">**visNURBSKnot** (Ligne NURBSTo)</span><span class="sxs-lookup"><span data-stu-id="3b678-141">**visNURBSKnot** (NURBSTo row)</span></span>  <br/> |
||<span data-ttu-id="3b678-142">**visSplineKnot** (Lignes SplineStart et SplineKnot)</span><span class="sxs-lookup"><span data-stu-id="3b678-142">**visSplineKnot** (SplineStart and SplineKnot rows)</span></span>  <br/> |
||<span data-ttu-id="3b678-143">**visInfiniteLineX2** (Ligne InfiniteLine)</span><span class="sxs-lookup"><span data-stu-id="3b678-143">**visInfiniteLineX2** (InfiniteLine row)</span></span>  <br/> |
||<span data-ttu-id="3b678-144">**visEllipseMajorX** (Ligne ellipse)</span><span class="sxs-lookup"><span data-stu-id="3b678-144">**visEllipseMajorX** (Ellipse row)</span></span>  <br/> |
   

