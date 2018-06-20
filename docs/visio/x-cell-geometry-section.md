---
title: X, cellule (section Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1135
localization_priority: Normal
ms.assetid: 2416b323-e084-18e1-c9be-a797078dfab9
description: Représente un x-coordonnées d’une forme dans le système de coordonnées local. Le tableau suivant décrit la cellule X en fonction de la ligne dans laquelle il se trouve.
ms.openlocfilehash: e5bc99d4f73d49741c4378009dfc2a883bb655ed
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790052"
---
# <a name="x-cell-geometry-section"></a><span data-ttu-id="dac60-104">X, cellule (section Geometry)</span><span class="sxs-lookup"><span data-stu-id="dac60-104">X Cell (Geometry Section)</span></span>

<span data-ttu-id="dac60-105">Représente un *x* -coordonnées d’une forme dans le système de coordonnées local.</span><span class="sxs-lookup"><span data-stu-id="dac60-105">Represents an  *x*  -coordinate on a shape in local coordinates.</span></span> <span data-ttu-id="dac60-106">Le tableau suivant décrit la cellule X en fonction de la ligne dans laquelle il se trouve.</span><span class="sxs-lookup"><span data-stu-id="dac60-106">This table describes the X cell based on the row in which it's located.</span></span> 
  
|<span data-ttu-id="dac60-107">**Row**</span><span class="sxs-lookup"><span data-stu-id="dac60-107">**Row**</span></span>|<span data-ttu-id="dac60-108">**Description**</span><span class="sxs-lookup"><span data-stu-id="dac60-108">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dac60-109">MoveTo</span><span class="sxs-lookup"><span data-stu-id="dac60-109">MoveTo</span></span>](moveto-row-geometry-section.md) <br/> | <span data-ttu-id="dac60-110">Si la ligne MoveTo est la première ligne dans la section, la cellule X représente la *x* -coordonnées du premier sommet d’un chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="dac60-110">If the MoveTo row is the first row in the section, the X cell represents the  *x*  -coordinate of the first vertex of a path.</span></span> <span data-ttu-id="dac60-111">Si la ligne MoveTo apparaît entre deux lignes, la cellule X représente la *x* -coordonnées du premier sommet après la rupture du chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="dac60-111">If the MoveTo row appears between two rows, the X cell represents the  *x*  -coordinate of the first vertex after the break in the path.</span></span>  <br/> |
|[<span data-ttu-id="dac60-112">LineTo</span><span class="sxs-lookup"><span data-stu-id="dac60-112">LineTo</span></span>](lineto-row-geometry-section.md) <br/> | <span data-ttu-id="dac60-113">*X* -coordonnées du sommet de fin d’un segment de trait droit.</span><span class="sxs-lookup"><span data-stu-id="dac60-113">The  *x*  -coordinate of the ending vertex of a straight line segment.</span></span>  <br/> |
|[<span data-ttu-id="dac60-114">ArcTo</span><span class="sxs-lookup"><span data-stu-id="dac60-114">ArcTo</span></span>](arcto-row-geometry-section.md) <br/> | <span data-ttu-id="dac60-115">*X* -coordonnées du sommet de fin d’un arc.</span><span class="sxs-lookup"><span data-stu-id="dac60-115">The  *x*  -coordinate of the ending vertex of an arc.</span></span>  <br/> |
|[<span data-ttu-id="dac60-116">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="dac60-116">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="dac60-117">*X* -coordonnées du sommet de fin d’un arc elliptique.</span><span class="sxs-lookup"><span data-stu-id="dac60-117">The  *x*  -coordinate of the ending vertex of an elliptical arc.</span></span>  <br/> |
|[<span data-ttu-id="dac60-118">PolylineTo</span><span class="sxs-lookup"><span data-stu-id="dac60-118">PolylineTo</span></span>](polylineto-row-geometry-section.md) <br/> | <span data-ttu-id="dac60-119">*X* -coordonnées du sommet de fin d’une polyligne.</span><span class="sxs-lookup"><span data-stu-id="dac60-119">The  *x*  -coordinate of the ending vertex of a polyline.</span></span>  <br/> |
|[<span data-ttu-id="dac60-120">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="dac60-120">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="dac60-121">*X* -coordonnées du dernier point de contrôle d’une courbe B-spline rationnelle (NURBS).</span><span class="sxs-lookup"><span data-stu-id="dac60-121">The  *x*  -coordinate of the last control point of a nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|[<span data-ttu-id="dac60-122">SplineStart</span><span class="sxs-lookup"><span data-stu-id="dac60-122">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> | <span data-ttu-id="dac60-123">*X* -coordonnées du deuxième point de contrôle d’une spline.</span><span class="sxs-lookup"><span data-stu-id="dac60-123">The  *x*  -coordinate of a spline's second control point.</span></span>  <br/> |
|[<span data-ttu-id="dac60-124">SplineKnot</span><span class="sxs-lookup"><span data-stu-id="dac60-124">SplineKnot</span></span>](splineknot-row-geometry-section.md) <br/> | <span data-ttu-id="dac60-125">*X* -coordonnées d’un point de contrôle.</span><span class="sxs-lookup"><span data-stu-id="dac60-125">The  *x*  -coordinate of a control point.</span></span>  <br/> |
|[<span data-ttu-id="dac60-126">InfiniteLine</span><span class="sxs-lookup"><span data-stu-id="dac60-126">InfiniteLine</span></span>](infiniteline-row-geometry-section.md) <br/> | <span data-ttu-id="dac60-127">*X* -coordonnées d’un point sur une ligne infinie.</span><span class="sxs-lookup"><span data-stu-id="dac60-127">An  *x*  -coordinate of a point on the infinite line.</span></span>  <br/> |
|[<span data-ttu-id="dac60-128">Ellipse</span><span class="sxs-lookup"><span data-stu-id="dac60-128">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="dac60-129">*X* -coordonnée du centre de l’ellipse.</span><span class="sxs-lookup"><span data-stu-id="dac60-129">The  *x*  -coordinate of the center of the ellipse.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dac60-130">Remarques</span><span class="sxs-lookup"><span data-stu-id="dac60-130">Remarks</span></span>

<span data-ttu-id="dac60-131">Pour obtenir une référence à la cellule X par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="dac60-131">To get a reference to the X cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="dac60-132">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="dac60-132">Cell name:</span></span>  <br/> | <span data-ttu-id="dac60-133">Géométrie *i* . X *j* où *i* et *j* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="dac60-133">Geometry  *i*  .X  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="dac60-134">Géométrie *i* . X1 (lignes InfiniteLine et Ellipse) où *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="dac60-134">Geometry  *i*  .X1 (InfiniteLine and Ellipse rows)            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="dac60-135">Pour obtenir une référence à la cellule X par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="dac60-135">To get a reference to the X cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="dac60-136">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="dac60-136">Section index:</span></span>  <br/> |<span data-ttu-id="dac60-137">**visSectionFirstComponent** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="dac60-137">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="dac60-138">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="dac60-138">Row index:</span></span>  <br/> |<span data-ttu-id="dac60-139">**visRowVertex** +  *j* où *j* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="dac60-139">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="dac60-140">**visRowVertex** (Lignes InfiniteLine et Ellipse)</span><span class="sxs-lookup"><span data-stu-id="dac60-140">**visRowVertex** (InfiniteLine and Ellipse rows)</span></span>  <br/> |
| <span data-ttu-id="dac60-141">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="dac60-141">Cell index:</span></span>  <br/> |<span data-ttu-id="dac60-142">**visX** (Lignes MoveTo, LineTo, ArcTo, EllipticalArcTo, NURBSTo, Polyline, SplineStart et SplineKnot)</span><span class="sxs-lookup"><span data-stu-id="dac60-142">**visX** (MoveTo, LineTo, ArcTo, EllipticalArcTo, NURBSTo, Polyline, SplineStart, and SplineKnot rows)</span></span>  <br/> |
||<span data-ttu-id="dac60-143">**visInfiniteLineX1** (Ligne InfiniteLine)</span><span class="sxs-lookup"><span data-stu-id="dac60-143">**visInfiniteLineX1** (InfiniteLine row)</span></span>  <br/> |
||<span data-ttu-id="dac60-144">**visEllipseCenterX** (Ligne ellipse)</span><span class="sxs-lookup"><span data-stu-id="dac60-144">**visEllipseCenterX** (Ellipse row)</span></span>  <br/> |
   

