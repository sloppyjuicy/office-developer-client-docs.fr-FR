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
description: Représente une coordonnée x sur une forme, en coordonnées locales. Ce tableau décrit la cellule X suivant la ligne sur laquelle elle se trouve.
ms.openlocfilehash: 6554000a86a6bf27d343a5647161bbe416725e64
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423943"
---
# <a name="x-cell-geometry-section"></a><span data-ttu-id="11cc0-104">X, cellule (section Geometry)</span><span class="sxs-lookup"><span data-stu-id="11cc0-104">X Cell (Geometry Section)</span></span>

<span data-ttu-id="11cc0-105">Représente une coordonnée *x* sur une forme, en coordonnées locales.</span><span class="sxs-lookup"><span data-stu-id="11cc0-105">Represents an  *x*  -coordinate on a shape in local coordinates.</span></span> <span data-ttu-id="11cc0-106">Ce tableau décrit la cellule X suivant la ligne sur laquelle elle se trouve.</span><span class="sxs-lookup"><span data-stu-id="11cc0-106">This table describes the X cell based on the row in which it's located.</span></span> 
  
|<span data-ttu-id="11cc0-107">**Ligne**</span><span class="sxs-lookup"><span data-stu-id="11cc0-107">**Row**</span></span>|<span data-ttu-id="11cc0-108">**Description**</span><span class="sxs-lookup"><span data-stu-id="11cc0-108">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="11cc0-109">MoveTo</span><span class="sxs-lookup"><span data-stu-id="11cc0-109">MoveTo</span></span>](moveto-row-geometry-section.md) <br/> | <span data-ttu-id="11cc0-110">Si la ligne MoveTo est la première ligne de la section, la cellule X représente la coordonnée *x* du premier sommet d'un chemin.</span><span class="sxs-lookup"><span data-stu-id="11cc0-110">If the MoveTo row is the first row in the section, the X cell represents the  *x*  -coordinate of the first vertex of a path.</span></span> <span data-ttu-id="11cc0-111">Si la ligne MoveTo apparaît entre deux lignes, la cellule X représente la coordonnée *x* du premier sommet après la rupture du chemin.</span><span class="sxs-lookup"><span data-stu-id="11cc0-111">If the MoveTo row appears between two rows, the X cell represents the  *x*  -coordinate of the first vertex after the break in the path.</span></span>  <br/> |
|[<span data-ttu-id="11cc0-112">LineTo</span><span class="sxs-lookup"><span data-stu-id="11cc0-112">LineTo</span></span>](lineto-row-geometry-section.md) <br/> | <span data-ttu-id="11cc0-113">Coordonnée *x* du sommet de fin d'un segment de ligne droite.</span><span class="sxs-lookup"><span data-stu-id="11cc0-113">The  *x*  -coordinate of the ending vertex of a straight line segment.</span></span>  <br/> |
|[<span data-ttu-id="11cc0-114">ArcTo</span><span class="sxs-lookup"><span data-stu-id="11cc0-114">ArcTo</span></span>](arcto-row-geometry-section.md) <br/> | <span data-ttu-id="11cc0-115">Coordonnée *x* du sommet de fin d'un arc.</span><span class="sxs-lookup"><span data-stu-id="11cc0-115">The  *x*  -coordinate of the ending vertex of an arc.</span></span>  <br/> |
|[<span data-ttu-id="11cc0-116">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="11cc0-116">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="11cc0-117">Coordonnée *x* du sommet de fin d'un arc elliptique.</span><span class="sxs-lookup"><span data-stu-id="11cc0-117">The  *x*  -coordinate of the ending vertex of an elliptical arc.</span></span>  <br/> |
|[<span data-ttu-id="11cc0-118">PolylineTo</span><span class="sxs-lookup"><span data-stu-id="11cc0-118">PolylineTo</span></span>](polylineto-row-geometry-section.md) <br/> | <span data-ttu-id="11cc0-119">Coordonnée *x* du sommet de fin d'une polyligne.</span><span class="sxs-lookup"><span data-stu-id="11cc0-119">The  *x*  -coordinate of the ending vertex of a polyline.</span></span>  <br/> |
|[<span data-ttu-id="11cc0-120">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="11cc0-120">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="11cc0-121">Coordonnée *x* du dernier point de contrôle d'une courbe B-spline rationnelle inuniforme (NURBS).</span><span class="sxs-lookup"><span data-stu-id="11cc0-121">The  *x*  -coordinate of the last control point of a nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|[<span data-ttu-id="11cc0-122">SplineStart</span><span class="sxs-lookup"><span data-stu-id="11cc0-122">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> | <span data-ttu-id="11cc0-123">Coordonnée *x* du deuxième point de contrôle d'une spline.</span><span class="sxs-lookup"><span data-stu-id="11cc0-123">The  *x*  -coordinate of a spline's second control point.</span></span>  <br/> |
|[<span data-ttu-id="11cc0-124">SplineKnot</span><span class="sxs-lookup"><span data-stu-id="11cc0-124">SplineKnot</span></span>](splineknot-row-geometry-section.md) <br/> | <span data-ttu-id="11cc0-125">Coordonnée *x* d'un point de contrôle.</span><span class="sxs-lookup"><span data-stu-id="11cc0-125">The  *x*  -coordinate of a control point.</span></span>  <br/> |
|[<span data-ttu-id="11cc0-126">InfiniteLine</span><span class="sxs-lookup"><span data-stu-id="11cc0-126">InfiniteLine</span></span>](infiniteline-row-geometry-section.md) <br/> | <span data-ttu-id="11cc0-127">Coordonnée *x* d'un point sur la ligne infinie.</span><span class="sxs-lookup"><span data-stu-id="11cc0-127">An  *x*  -coordinate of a point on the infinite line.</span></span>  <br/> |
|[<span data-ttu-id="11cc0-128">Sélection</span><span class="sxs-lookup"><span data-stu-id="11cc0-128">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="11cc0-129">Coordonnée *x* du centre de l'ellipse.</span><span class="sxs-lookup"><span data-stu-id="11cc0-129">The  *x*  -coordinate of the center of the ellipse.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="11cc0-130">Remarques</span><span class="sxs-lookup"><span data-stu-id="11cc0-130">Remarks</span></span>

<span data-ttu-id="11cc0-131">Pour obtenir une référence à la cellule X à l'aide d'un nom à partir d'une autre formule ou programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="11cc0-131">To get a reference to the X cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="11cc0-132">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="11cc0-132">Cell name:</span></span>  <br/> | <span data-ttu-id="11cc0-133">Géométrie *i* . X *j* où *i* et *j* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="11cc0-133">Geometry  *i*  .X  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="11cc0-134">Géométrie *i* . X1 (lignes InfiniteLine et ellipse) où *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="11cc0-134">Geometry  *i*  .X1 (InfiniteLine and Ellipse rows)            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="11cc0-135">Pour obtenir une référence à la cellule X à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="11cc0-135">To get a reference to the X cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="11cc0-136">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="11cc0-136">Section index:</span></span>  <br/> |<span data-ttu-id="11cc0-137">**visSectionFirstComponent** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="11cc0-137">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="11cc0-138">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="11cc0-138">Row index:</span></span>  <br/> |<span data-ttu-id="11cc0-139">**visRowVertex** +  *j* où *j* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="11cc0-139">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="11cc0-140">**visRowVertex** (lignes InfiniteLine et Ellipse)</span><span class="sxs-lookup"><span data-stu-id="11cc0-140">**visRowVertex** (InfiniteLine and Ellipse rows)</span></span>  <br/> |
| <span data-ttu-id="11cc0-141">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="11cc0-141">Cell index:</span></span>  <br/> |<span data-ttu-id="11cc0-142">**visX** (lignes MoveTo, LineTo, ArcTo, EllipticalArcTo, NURBSTo, Polyline, SplineStart et SplineKnot)</span><span class="sxs-lookup"><span data-stu-id="11cc0-142">**visX** (MoveTo, LineTo, ArcTo, EllipticalArcTo, NURBSTo, Polyline, SplineStart, and SplineKnot rows)</span></span>  <br/> |
||<span data-ttu-id="11cc0-143">**visInfiniteLineX1** (ligne InfiniteLine)</span><span class="sxs-lookup"><span data-stu-id="11cc0-143">**visInfiniteLineX1** (InfiniteLine row)</span></span>  <br/> |
||<span data-ttu-id="11cc0-144">**visEllipseCenterX** (ligne Ellipse)</span><span class="sxs-lookup"><span data-stu-id="11cc0-144">**visEllipseCenterX** (Ellipse row)</span></span>  <br/> |
   

