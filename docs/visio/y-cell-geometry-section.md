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
description: Représente une y-coordonnées d’une forme dans le système de coordonnées local. Le tableau suivant décrit la cellule Y basée sur la ligne où elle se trouve.
ms.openlocfilehash: 461fd0ec41d34132f469c811292550d2f7e094f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790087"
---
# <a name="y-cell-geometry-section"></a><span data-ttu-id="d93f8-104">Y, cellule (section Geometry)</span><span class="sxs-lookup"><span data-stu-id="d93f8-104">Y Cell (Geometry Section)</span></span>

<span data-ttu-id="d93f8-105">Représente une *y* -coordonnées d’une forme dans le système de coordonnées local.</span><span class="sxs-lookup"><span data-stu-id="d93f8-105">Represents a  *y*  -coordinate on a shape in local coordinates.</span></span> <span data-ttu-id="d93f8-106">Le tableau suivant décrit la cellule Y basée sur la ligne où elle se trouve.</span><span class="sxs-lookup"><span data-stu-id="d93f8-106">This table describes the Y cell based on the row in which it's located.</span></span> 
  
|<span data-ttu-id="d93f8-107">**Row**</span><span class="sxs-lookup"><span data-stu-id="d93f8-107">**Row**</span></span>|<span data-ttu-id="d93f8-108">**Description**</span><span class="sxs-lookup"><span data-stu-id="d93f8-108">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d93f8-109">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="d93f8-109">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="d93f8-110">Si la ligne MoveTo est la première ligne dans la section, la cellule Y représente la valeur *y* -coordonnées du premier sommet d’un chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="d93f8-110">If the MoveTo row is the first row in the section, the Y cell represents the  *y*  -coordinate of the first vertex of a path.</span></span> <span data-ttu-id="d93f8-111">Si la ligne MoveTo apparaît entre deux lignes, la cellule Y représente la valeur *y* -coordonnées du premier sommet après la rupture du chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="d93f8-111">If the MoveTo row appears between two rows, the Y cell represents the  *y*  -coordinate of the first vertex after the break in the path.</span></span>  <br/> |
|[<span data-ttu-id="d93f8-112">LineTo</span><span class="sxs-lookup"><span data-stu-id="d93f8-112">LineTo</span></span>](lineto-row-geometry-section.md) <br/> | <span data-ttu-id="d93f8-113">La valeur *y* -coordonnées du sommet de fin d’un segment de trait droit.</span><span class="sxs-lookup"><span data-stu-id="d93f8-113">The  *y*  -coordinate of the ending vertex of a straight line segment.</span></span>  <br/> |
|[<span data-ttu-id="d93f8-114">ArcTo</span><span class="sxs-lookup"><span data-stu-id="d93f8-114">ArcTo</span></span>](arcto-row-geometry-section.md) <br/> | <span data-ttu-id="d93f8-115">La valeur *y* -coordonnées du sommet de fin d’un arc.</span><span class="sxs-lookup"><span data-stu-id="d93f8-115">The  *y*  -coordinate of the ending vertex of an arc.</span></span>  <br/> |
|[<span data-ttu-id="d93f8-116">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="d93f8-116">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="d93f8-117">La valeur *y* -coordonnées du sommet de fin d’un arc elliptique.</span><span class="sxs-lookup"><span data-stu-id="d93f8-117">The  *y*  -coordinate of the ending vertex of an elliptical arc.</span></span>  <br/> |
|[<span data-ttu-id="d93f8-118">PolylineTo</span><span class="sxs-lookup"><span data-stu-id="d93f8-118">PolylineTo</span></span>](polylineto-row-geometry-section.md) <br/> | <span data-ttu-id="d93f8-119">La valeur *y* -coordonnées du sommet de fin d’une polyligne.</span><span class="sxs-lookup"><span data-stu-id="d93f8-119">The  *y*  -coordinate of the ending vertex of a polyline.</span></span>  <br/> |
|[<span data-ttu-id="d93f8-120">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="d93f8-120">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="d93f8-121">La valeur *y* -coordonnées du dernier point de contrôle d’une courbe B-spline rationnelle (NURBS).</span><span class="sxs-lookup"><span data-stu-id="d93f8-121">The  *y*  -coordinate of the last control point of a nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|[<span data-ttu-id="d93f8-122">SplineStart</span><span class="sxs-lookup"><span data-stu-id="d93f8-122">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> | <span data-ttu-id="d93f8-123">La valeur *y* -coordonnées du deuxième point de contrôle d’une spline.</span><span class="sxs-lookup"><span data-stu-id="d93f8-123">The  *y*  -coordinate of a spline's second control point.</span></span>  <br/> |
|[<span data-ttu-id="d93f8-124">SplineKnot</span><span class="sxs-lookup"><span data-stu-id="d93f8-124">SplineKnot</span></span>](splineknot-row-geometry-section.md) <br/> | <span data-ttu-id="d93f8-125">La valeur *y* -coordonnées d’un point de contrôle.</span><span class="sxs-lookup"><span data-stu-id="d93f8-125">The  *y*  -coordinate of a control point.</span></span>  <br/> |
|[<span data-ttu-id="d93f8-126">InfiniteLine</span><span class="sxs-lookup"><span data-stu-id="d93f8-126">InfiniteLine</span></span>](infiniteline-row-geometry-section.md) <br/> | <span data-ttu-id="d93f8-127">Une coordonnée *y* d’un point sur une ligne infinie.</span><span class="sxs-lookup"><span data-stu-id="d93f8-127">A  *y-*  coordinate of a point on the infinite line.</span></span>  <br/> |
|[<span data-ttu-id="d93f8-128">Ellipse</span><span class="sxs-lookup"><span data-stu-id="d93f8-128">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="d93f8-129">La valeur *y* -coordonnée du centre de l’ellipse.</span><span class="sxs-lookup"><span data-stu-id="d93f8-129">The  *y*  -coordinate of the center of the ellipse.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d93f8-130">Remarques</span><span class="sxs-lookup"><span data-stu-id="d93f8-130">Remarks</span></span>

<span data-ttu-id="d93f8-131">Pour obtenir une référence à la cellule Y par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="d93f8-131">To get a reference to the Y cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d93f8-132">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="d93f8-132">Cell name:</span></span>  <br/> | <span data-ttu-id="d93f8-133">Géométrie *i* . Y *j* où *i* et *j* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="d93f8-133">Geometry  *i*  .Y  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="d93f8-134">Géométrie *i* . Y1 (lignes InfiniteLine et Ellipse) où *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="d93f8-134">Geometry  *i*  .Y1 (InfiniteLine and Ellipse rows)            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="d93f8-135">Pour obtenir une référence à la cellule Y par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="d93f8-135">To get a reference to the Y cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d93f8-136">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="d93f8-136">Section index:</span></span>  <br/> |<span data-ttu-id="d93f8-137">**visSectionFirstComponent** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="d93f8-137">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="d93f8-138">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="d93f8-138">Row index:</span></span>  <br/> |<span data-ttu-id="d93f8-139">**visRowVertex** +  *j* où *j* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="d93f8-139">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="d93f8-140">**visRowVertex** (Lignes InfiniteLine et Ellipse)</span><span class="sxs-lookup"><span data-stu-id="d93f8-140">**visRowVertex** (InfiniteLine and Ellipse rows)</span></span>  <br/> |
| <span data-ttu-id="d93f8-141">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="d93f8-141">Cell index:</span></span>  <br/> |<span data-ttu-id="d93f8-142">**visY** (Lignes MoveTo, LineTo, ArcTo, EllipticalArcTo, NURBSTo, Polyline, SplineStart et SplineKnot)</span><span class="sxs-lookup"><span data-stu-id="d93f8-142">**visY** (MoveTo, LineTo, ArcTo, EllipticalArcTo, NURBSTo, Polyline, SplineStart, and SplineKnot rows)</span></span>  <br/> |
||<span data-ttu-id="d93f8-143">**visInfiniteLineY1** (Ligne InfiniteLine)</span><span class="sxs-lookup"><span data-stu-id="d93f8-143">**visInfiniteLineY1** (InfiniteLine row)</span></span>  <br/> |
||<span data-ttu-id="d93f8-144">**visEllipseCenterY** (Ligne ellipse)</span><span class="sxs-lookup"><span data-stu-id="d93f8-144">**visEllipseCenterY** (Ellipse row)</span></span>  <br/> |
   

