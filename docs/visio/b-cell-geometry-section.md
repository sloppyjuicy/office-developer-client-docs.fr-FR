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
ms.openlocfilehash: ff032b5af2918ec9865360ede5c3d76e8e872e9a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346241"
---
# <a name="b-cell-geometry-section"></a><span data-ttu-id="5a321-104">B, cellule (section Geometry)</span><span class="sxs-lookup"><span data-stu-id="5a321-104">B Cell (Geometry Section)</span></span>

<span data-ttu-id="5a321-105">Représente des informations différentes selon la ligne où elle se trouve.</span><span class="sxs-lookup"><span data-stu-id="5a321-105">Represents different information in different rows.</span></span> <span data-ttu-id="5a321-106">Le tableau ci-dessous décrit la cellule B pour chaque ligne.</span><span class="sxs-lookup"><span data-stu-id="5a321-106">This table describes the B cell based on the row in which it's located.</span></span>
  
|<span data-ttu-id="5a321-107">**Ligne**</span><span class="sxs-lookup"><span data-stu-id="5a321-107">**Row**</span></span>|<span data-ttu-id="5a321-108">**Description**</span><span class="sxs-lookup"><span data-stu-id="5a321-108">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5a321-109">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="5a321-109">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="5a321-110">Coordonnée *y* du point de contrôle d'un arc.</span><span class="sxs-lookup"><span data-stu-id="5a321-110">The  *y*  -coordinate of an arc's control point.</span></span>  <br/> |
|[<span data-ttu-id="5a321-111">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="5a321-111">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="5a321-112">Dernière épaisseur de la courbe B-spline rationnelle non uniforme (NURBS).</span><span class="sxs-lookup"><span data-stu-id="5a321-112">The last weight of the nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|[<span data-ttu-id="5a321-113">SplineStart</span><span class="sxs-lookup"><span data-stu-id="5a321-113">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> | <span data-ttu-id="5a321-114">Premier nœud d’une spline</span><span class="sxs-lookup"><span data-stu-id="5a321-114">The first knot of a spline.</span></span>  <br/> |
|[<span data-ttu-id="5a321-115">InfiniteLine</span><span class="sxs-lookup"><span data-stu-id="5a321-115">InfiniteLine</span></span>](infiniteline-row-geometry-section.md) <br/> | <span data-ttu-id="5a321-116">Coordonnée *y* d'un point sur une ligne infinie; associée à la coordonnée *x* représentée par la cellule [A](a-cell-geometry-section.md) .</span><span class="sxs-lookup"><span data-stu-id="5a321-116">A  *y*  -coordinate of a point on an infinite line; paired with  *x*  -coordinate represented by the [A](a-cell-geometry-section.md) cell.</span></span>  <br/> |
|[<span data-ttu-id="5a321-117">Sélection</span><span class="sxs-lookup"><span data-stu-id="5a321-117">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="5a321-118">Coordonnée *y* d'un point sur une ellipse; associée à la coordonnée *x* représentée par la cellule [A](a-cell-geometry-section.md) .</span><span class="sxs-lookup"><span data-stu-id="5a321-118">A  *y*  -coordinate of a point on an ellipse; paired with  *x*  -coordinate represented by the [A](a-cell-geometry-section.md) cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5a321-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="5a321-119">Remarks</span></span>

<span data-ttu-id="5a321-120">Pour obtenir une référence à la cellule B par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="5a321-120">To get a reference to the B cell by name from another formula, or from a program, using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5a321-121">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="5a321-121">Cell name:</span></span>  <br/> | <span data-ttu-id="5a321-122">Géométrie *i* . B *j* où *i* et *j* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="5a321-122">Geometry  *i*  .B  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="5a321-123">Géométrie *i* . B1 (lignes InfiniteLine et ellipse)</span><span class="sxs-lookup"><span data-stu-id="5a321-123">Geometry  *i*  .B1 (InfiniteLine and Ellipse rows)</span></span>  <br/> |
   
<span data-ttu-id="5a321-124">Pour obtenir une référence à la cellule B à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="5a321-124">To get a reference to the B cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5a321-125">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="5a321-125">Section index:</span></span>  <br/> |<span data-ttu-id="5a321-126">**visSectionFirstComponent** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="5a321-126">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="5a321-127">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="5a321-127">Row index:</span></span>  <br/> |<span data-ttu-id="5a321-128">**visRowVertex** +  *j* où *j* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="5a321-128">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="5a321-129">**visRowVertex** (lignes InfiniteLine et Ellipse)</span><span class="sxs-lookup"><span data-stu-id="5a321-129">**visRowVertex** (InfiniteLine and Ellipse rows)</span></span>  <br/> |
| <span data-ttu-id="5a321-130">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="5a321-130">Cell index:</span></span>  <br/> |<span data-ttu-id="5a321-131">**visControlX** (ligne EllipticalArcTo)</span><span class="sxs-lookup"><span data-stu-id="5a321-131">**visControlX** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="5a321-132">**visControlY** (ligne EllipticalArcTo)</span><span class="sxs-lookup"><span data-stu-id="5a321-132">**visControlY** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="5a321-133">**visNURBSWeight** (ligne NURBSTo)</span><span class="sxs-lookup"><span data-stu-id="5a321-133">**visNURBSWeight** (NURBSTo row)</span></span>  <br/> |
||<span data-ttu-id="5a321-134">**visSplineKnot2** (ligne SplineStart)</span><span class="sxs-lookup"><span data-stu-id="5a321-134">**visSplineKnot2** (SplineStart row)</span></span>  <br/> |
||<span data-ttu-id="5a321-135">**visInfiniteLineY2** (ligne InfiniteLine)</span><span class="sxs-lookup"><span data-stu-id="5a321-135">**visInfiniteLineY2** (InfiniteLine row)</span></span>  <br/> |
||<span data-ttu-id="5a321-136">**visEllipseMajorY** (ligne Ellipse)</span><span class="sxs-lookup"><span data-stu-id="5a321-136">**visEllipseMajorY** (Ellipse row)</span></span>  <br/> |
   

