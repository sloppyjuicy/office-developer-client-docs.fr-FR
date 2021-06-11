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
ms.openlocfilehash: 7009658c7a6844a5c6071f502c05114a4accd7b7
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541301"
---
# <a name="a-cell-geometry-section"></a><span data-ttu-id="71ef2-104">A, cellule (section Geometry)</span><span class="sxs-lookup"><span data-stu-id="71ef2-104">A Cell (Geometry Section)</span></span>

<span data-ttu-id="71ef2-p102">Représente des informations différentes selon la ligne où elle se trouve. Le tableau ci-dessous décrit la cellule A pour chaque ligne.</span><span class="sxs-lookup"><span data-stu-id="71ef2-p102">Represents different information in different rows. This table describes the A cell based on the row in which it's located.</span></span>
  
|<span data-ttu-id="71ef2-107">Ligne</span><span class="sxs-lookup"><span data-stu-id="71ef2-107">Row</span></span>|<span data-ttu-id="71ef2-108">Description</span><span class="sxs-lookup"><span data-stu-id="71ef2-108">Description</span></span>|
|:-----|:-----|
|[<span data-ttu-id="71ef2-109">ArcTo</span><span class="sxs-lookup"><span data-stu-id="71ef2-109">ArcTo</span></span>](arcto-row-geometry-section.md) <br/> | <span data-ttu-id="71ef2-110">Distance entre le milieu de l’arc et le milieu de sa corde.</span><span class="sxs-lookup"><span data-stu-id="71ef2-110">The distance from the arc's midpoint to the midpoint of its chord.</span></span>  <br/> |
|[<span data-ttu-id="71ef2-111">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="71ef2-111">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="71ef2-112">Coordonnée  *x*  du point de contrôle de l’arc, un point sur l’arc. Le point de contrôle est mieux situé à mi-chemin entre les vertex de début et de fin de l’arc. Dans le cas contraire, l’arc peut atteindre une taille extrême afin de passer par le point de contrôle, avec des résultats imprévisibles.</span><span class="sxs-lookup"><span data-stu-id="71ef2-112">The  *x*  -coordinate of the arc's control point, a point on the arc. The control point is best located about halfway between the beginning and ending vertices of the arc. Otherwise, the arc may grow to an extreme size in order to pass through the control point, with unpredictable results.</span></span>  <br/> |
|[<span data-ttu-id="71ef2-113">PolylineTo</span><span class="sxs-lookup"><span data-stu-id="71ef2-113">PolylineTo</span></span>](polylineto-row-geometry-section.md) <br/> | <span data-ttu-id="71ef2-114">Formule de la polyligne</span><span class="sxs-lookup"><span data-stu-id="71ef2-114">The polyline formula.</span></span>  <br/> |
|[<span data-ttu-id="71ef2-115">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="71ef2-115">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="71ef2-116">Avant-dernier nœud de la courbe B-spline rationnelle non uniforme (NURBS).</span><span class="sxs-lookup"><span data-stu-id="71ef2-116">The second to the last knot of the nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|[<span data-ttu-id="71ef2-117">SplineStart</span><span class="sxs-lookup"><span data-stu-id="71ef2-117">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> | <span data-ttu-id="71ef2-118">Deuxième nœud de la spline</span><span class="sxs-lookup"><span data-stu-id="71ef2-118">The second knot of the spline.</span></span>  <br/> |
|[<span data-ttu-id="71ef2-119">SplineKnot</span><span class="sxs-lookup"><span data-stu-id="71ef2-119">SplineKnot</span></span>](splineknot-row-geometry-section.md) <br/> | <span data-ttu-id="71ef2-120">Un des nœuds de la spline (autre que le dernier ou les deux premiers)</span><span class="sxs-lookup"><span data-stu-id="71ef2-120">One of the spline's knots (other than the last one or the first two).</span></span>  <br/> |
|[<span data-ttu-id="71ef2-121">InfiniteLine</span><span class="sxs-lookup"><span data-stu-id="71ef2-121">InfiniteLine</span></span>](infiniteline-row-geometry-section.md) <br/> | <span data-ttu-id="71ef2-122">Coordonnée *x* d’un point sur la ligne infinie ; associé à *la coordonnée y* représentée par la cellule [B.](b-cell-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="71ef2-122">An  *x*  -coordinate of a point on the infinite line; paired with  *y*  -coordinate represented by the [B](b-cell-geometry-section.md) cell.</span></span>  <br/> |
|[<span data-ttu-id="71ef2-123">Ellipse</span><span class="sxs-lookup"><span data-stu-id="71ef2-123">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="71ef2-124">Coordonnée *x* d’un point sur l’ellipse ; associé à *la coordonnée y* représentée par la cellule [B.](b-cell-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="71ef2-124">An  *x*  -coordinate of a point on the ellipse; paired with  *y*  -coordinate represented by the [B](b-cell-geometry-section.md) cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="71ef2-125">Remarques</span><span class="sxs-lookup"><span data-stu-id="71ef2-125">Remarks</span></span>

<span data-ttu-id="71ef2-126">Pour obtenir une référence à la cellule A par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="71ef2-126">To get a reference to the A cell by name from another formula, or from a program, using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="71ef2-127">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="71ef2-127">Cell name:</span></span>  <br/> | <span data-ttu-id="71ef2-128">Geometry  *i*  . A  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="71ef2-128">Geometry  *i*  .A  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="71ef2-129">Geometry  *i*  . A1 (lignes InfiniteLine et Ellipse) où  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="71ef2-129">Geometry  *i*  .A1 (InfiniteLine and Ellipse rows)            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="71ef2-130">Pour obtenir une référence à la cellule A à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="71ef2-130">To get a reference to the A cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="71ef2-131">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="71ef2-131">Section index:</span></span>  <br/> |<span data-ttu-id="71ef2-132">**visSectionFirstComponent**  +   *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="71ef2-132">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="71ef2-133">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="71ef2-133">Row index:</span></span>  <br/> |<span data-ttu-id="71ef2-134">**visRowVertex**  +   *j* où *j* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="71ef2-134">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="71ef2-135">**visRowVertex** (lignes InfiniteLine et Ellipse)</span><span class="sxs-lookup"><span data-stu-id="71ef2-135">**visRowVertex** (InfiniteLine and Ellipse rows)</span></span>  <br/> |
| <span data-ttu-id="71ef2-136">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="71ef2-136">Cell index:</span></span>  <br/> |<span data-ttu-id="71ef2-137">**visBow** (ligne ArcTo)</span><span class="sxs-lookup"><span data-stu-id="71ef2-137">**visBow** (ArcTo row)</span></span>  <br/> |
||<span data-ttu-id="71ef2-138">**visControlX** (ligne EllipticalArcTo)</span><span class="sxs-lookup"><span data-stu-id="71ef2-138">**visControlX** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="71ef2-139">**visControlY** (ligne EllipticalArcTo)</span><span class="sxs-lookup"><span data-stu-id="71ef2-139">**visControlY** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="71ef2-140">**visPolylineData** (ligne Polyline)</span><span class="sxs-lookup"><span data-stu-id="71ef2-140">**visPolylineData** (Polyline row)</span></span>  <br/> |
||<span data-ttu-id="71ef2-141">**visNURBSKnot** (ligne NURBSTo)</span><span class="sxs-lookup"><span data-stu-id="71ef2-141">**visNURBSKnot** (NURBSTo row)</span></span>  <br/> |
||<span data-ttu-id="71ef2-142">**visSplineKnot** (lignes SplineStart et SplineKnot)</span><span class="sxs-lookup"><span data-stu-id="71ef2-142">**visSplineKnot** (SplineStart and SplineKnot rows)</span></span>  <br/> |
||<span data-ttu-id="71ef2-143">**visInfiniteLineX2** (ligne InfiniteLine)</span><span class="sxs-lookup"><span data-stu-id="71ef2-143">**visInfiniteLineX2** (InfiniteLine row)</span></span>  <br/> |
||<span data-ttu-id="71ef2-144">**visEllipseMajorX** (ligne Ellipse)</span><span class="sxs-lookup"><span data-stu-id="71ef2-144">**visEllipseMajorX** (Ellipse row)</span></span>  <br/> |
   

