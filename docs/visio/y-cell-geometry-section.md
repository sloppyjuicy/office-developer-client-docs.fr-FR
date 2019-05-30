---
title: Y, cellule (section Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251750
localization_priority: Normal
ms.assetid: a53b5787-f419-7a36-3c04-c63b3c173ac7
description: Représente la coordonnée y d’une forme en coordonnées locales. Ce tableau décrit la cellule Y suivant la ligne sur laquelle elle se trouve.
ms.openlocfilehash: 7dea96b544c84f09abe1d72304da0bacaa09432f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540489"
---
# <a name="y-cell-geometry-section"></a><span data-ttu-id="95a7e-104">Y, cellule (section Geometry)</span><span class="sxs-lookup"><span data-stu-id="95a7e-104">Y Cell (Geometry Section)</span></span>

<span data-ttu-id="95a7e-105">Représente la coordonnée *y* d’une forme en coordonnées locales.</span><span class="sxs-lookup"><span data-stu-id="95a7e-105">Represents a  *y*  -coordinate on a shape in local coordinates.</span></span> <span data-ttu-id="95a7e-106">Ce tableau décrit la cellule Y suivant la ligne sur laquelle elle se trouve.</span><span class="sxs-lookup"><span data-stu-id="95a7e-106">This table describes the Y cell based on the row in which it's located.</span></span> 
  
|<span data-ttu-id="95a7e-107">Ligne</span><span class="sxs-lookup"><span data-stu-id="95a7e-107">Row</span></span>|<span data-ttu-id="95a7e-108">Description</span><span class="sxs-lookup"><span data-stu-id="95a7e-108">Description</span></span>|
|:-----|:-----|
|[<span data-ttu-id="95a7e-109">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="95a7e-109">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="95a7e-110">Si la ligne MoveTo est la première ligne de la section, la cellule Y représente la coordonnée *y* du premier sommet d’un chemin.</span><span class="sxs-lookup"><span data-stu-id="95a7e-110">If the MoveTo row is the first row in the section, the Y cell represents the  *y*  -coordinate of the first vertex of a path.</span></span> <span data-ttu-id="95a7e-111">Si la ligne MoveTo apparaît entre deux lignes, la cellule Y représente la coordonnée *y* du premier sommet après la rupture du chemin.</span><span class="sxs-lookup"><span data-stu-id="95a7e-111">If the MoveTo row appears between two rows, the Y cell represents the  *y*  -coordinate of the first vertex after the break in the path.</span></span>  <br/> |
|[<span data-ttu-id="95a7e-112">LineTo</span><span class="sxs-lookup"><span data-stu-id="95a7e-112">LineTo</span></span>](lineto-row-geometry-section.md) <br/> | <span data-ttu-id="95a7e-113">Coordonnée *y* du sommet de fin d’un segment de trait droit.</span><span class="sxs-lookup"><span data-stu-id="95a7e-113">The  *y*  -coordinate of the ending vertex of a straight line segment.</span></span>  <br/> |
|[<span data-ttu-id="95a7e-114">ArcTo</span><span class="sxs-lookup"><span data-stu-id="95a7e-114">ArcTo</span></span>](arcto-row-geometry-section.md) <br/> | <span data-ttu-id="95a7e-115">Coordonnée *y* du sommet de fin d’un arc.</span><span class="sxs-lookup"><span data-stu-id="95a7e-115">The  *y*  -coordinate of the ending vertex of an arc.</span></span>  <br/> |
|[<span data-ttu-id="95a7e-116">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="95a7e-116">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="95a7e-117">Coordonnée *y* du sommet de fin d’un arc elliptique.</span><span class="sxs-lookup"><span data-stu-id="95a7e-117">The  *y*  -coordinate of the ending vertex of an elliptical arc.</span></span>  <br/> |
|[<span data-ttu-id="95a7e-118">PolylineTo</span><span class="sxs-lookup"><span data-stu-id="95a7e-118">PolylineTo</span></span>](polylineto-row-geometry-section.md) <br/> | <span data-ttu-id="95a7e-119">Coordonnée *y* du sommet de fin d’une polyligne.</span><span class="sxs-lookup"><span data-stu-id="95a7e-119">The  *y*  -coordinate of the ending vertex of a polyline.</span></span>  <br/> |
|[<span data-ttu-id="95a7e-120">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="95a7e-120">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="95a7e-121">Coordonnée *y* du dernier point de contrôle d’une courbe B-spline rationnelle inuniforme (NURBS).</span><span class="sxs-lookup"><span data-stu-id="95a7e-121">The  *y*  -coordinate of the last control point of a nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|[<span data-ttu-id="95a7e-122">SplineStart</span><span class="sxs-lookup"><span data-stu-id="95a7e-122">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> | <span data-ttu-id="95a7e-123">Coordonnée *y* du deuxième point de contrôle d’une spline.</span><span class="sxs-lookup"><span data-stu-id="95a7e-123">The  *y*  -coordinate of a spline's second control point.</span></span>  <br/> |
|[<span data-ttu-id="95a7e-124">SplineKnot</span><span class="sxs-lookup"><span data-stu-id="95a7e-124">SplineKnot</span></span>](splineknot-row-geometry-section.md) <br/> | <span data-ttu-id="95a7e-125">Coordonnée *y* d’un point de contrôle.</span><span class="sxs-lookup"><span data-stu-id="95a7e-125">The  *y*  -coordinate of a control point.</span></span>  <br/> |
|[<span data-ttu-id="95a7e-126">InfiniteLine</span><span class="sxs-lookup"><span data-stu-id="95a7e-126">InfiniteLine</span></span>](infiniteline-row-geometry-section.md) <br/> | <span data-ttu-id="95a7e-127">Coordonnée *y* d’un point sur la ligne infinie.</span><span class="sxs-lookup"><span data-stu-id="95a7e-127">A  *y-*  coordinate of a point on the infinite line.</span></span>  <br/> |
|[<span data-ttu-id="95a7e-128">Sélection</span><span class="sxs-lookup"><span data-stu-id="95a7e-128">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="95a7e-129">Coordonnée *y* du centre de l’ellipse.</span><span class="sxs-lookup"><span data-stu-id="95a7e-129">The  *y*  -coordinate of the center of the ellipse.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="95a7e-130">Remarques</span><span class="sxs-lookup"><span data-stu-id="95a7e-130">Remarks</span></span>

<span data-ttu-id="95a7e-131">Pour obtenir une référence à la cellule Y à l'aide d'un nom à partir d'une autre formule ou programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="95a7e-131">To get a reference to the Y cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="95a7e-132">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="95a7e-132">Cell name:</span></span>  <br/> | <span data-ttu-id="95a7e-133">Géométrie *i* . Y *j* où *i* et *j* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="95a7e-133">Geometry  *i*  .Y  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="95a7e-134">Géométrie *i* . Y1 (lignes InfiniteLine et ellipse) où *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="95a7e-134">Geometry  *i*  .Y1 (InfiniteLine and Ellipse rows)            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="95a7e-135">Pour obtenir une référence à la cellule Y à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="95a7e-135">To get a reference to the Y cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="95a7e-136">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="95a7e-136">Section index:</span></span>  <br/> |<span data-ttu-id="95a7e-137">**visSectionFirstComponent** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="95a7e-137">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="95a7e-138">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="95a7e-138">Row index:</span></span>  <br/> |<span data-ttu-id="95a7e-139">**visRowVertex** +  *j* où *j* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="95a7e-139">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="95a7e-140">**visRowVertex** (lignes InfiniteLine et Ellipse)</span><span class="sxs-lookup"><span data-stu-id="95a7e-140">**visRowVertex** (InfiniteLine and Ellipse rows)</span></span>  <br/> |
| <span data-ttu-id="95a7e-141">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="95a7e-141">Cell index:</span></span>  <br/> |<span data-ttu-id="95a7e-142">**visY** (lignes MoveTo, LineTo, ArcTo, EllipticalArcTo, NURBSTo, Polyline, SplineStart et SplineKnot)</span><span class="sxs-lookup"><span data-stu-id="95a7e-142">**visY** (MoveTo, LineTo, ArcTo, EllipticalArcTo, NURBSTo, Polyline, SplineStart, and SplineKnot rows)</span></span>  <br/> |
||<span data-ttu-id="95a7e-143">**visInfiniteLineY1** (ligne InfiniteLine)</span><span class="sxs-lookup"><span data-stu-id="95a7e-143">**visInfiniteLineY1** (InfiniteLine row)</span></span>  <br/> |
||<span data-ttu-id="95a7e-144">**visEllipseCenterY** (ligne Ellipse)</span><span class="sxs-lookup"><span data-stu-id="95a7e-144">**visEllipseCenterY** (Ellipse row)</span></span>  <br/> |
   

