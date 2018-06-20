---
title: C, cellule (section Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm140
localization_priority: Normal
ms.assetid: d51a1dd8-678a-a34d-658d-bd7a027dd379
description: Représente des informations différentes selon la ligne où elle se trouve. Le tableau ci-dessous décrit la cellule C pour chaque ligne.
ms.openlocfilehash: 1b9a813be825f2deeb5c90d596ffd9f3705bcef6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788192"
---
# <a name="c-cell-geometry-section"></a><span data-ttu-id="f2623-104">C, cellule (section Geometry)</span><span class="sxs-lookup"><span data-stu-id="f2623-104">C Cell (Geometry Section)</span></span>

<span data-ttu-id="f2623-p102">Représente des informations différentes selon la ligne où elle se trouve. Le tableau ci-dessous décrit la cellule C pour chaque ligne.</span><span class="sxs-lookup"><span data-stu-id="f2623-p102">Represents different information in different rows. This table describes the C cell based on the row in which it's located.</span></span>
  
|<span data-ttu-id="f2623-107">**Row**</span><span class="sxs-lookup"><span data-stu-id="f2623-107">**Row**</span></span>|<span data-ttu-id="f2623-108">**Description**</span><span class="sxs-lookup"><span data-stu-id="f2623-108">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f2623-109">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="f2623-109">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="f2623-110">L’angle de l’axe de principal d’un arc par rapport à *x* -axe de son parent.</span><span class="sxs-lookup"><span data-stu-id="f2623-110">The angle of an arc's major axis relative to the  *x*  -axis of its parent.</span></span>  <br/> |
|[<span data-ttu-id="f2623-111">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="f2623-111">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="f2623-112">Premier nœud de la courbe B-spline rationnelle non uniforme (NURBS).</span><span class="sxs-lookup"><span data-stu-id="f2623-112">The first knot of the nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|[<span data-ttu-id="f2623-113">SplineStart</span><span class="sxs-lookup"><span data-stu-id="f2623-113">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> | <span data-ttu-id="f2623-114">Dernier nœud d’une spline</span><span class="sxs-lookup"><span data-stu-id="f2623-114">The last knot of a spline.</span></span>  <br/> |
|[<span data-ttu-id="f2623-115">Ellipse</span><span class="sxs-lookup"><span data-stu-id="f2623-115">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="f2623-116">*X* -coordonnées d’un point sur une ellipse ; associée à la valeur *y* -coordonnée représentée par la cellule [D](d-cell-geometry-section.md) .</span><span class="sxs-lookup"><span data-stu-id="f2623-116">An  *x*  -coordinate of a point on an ellipse; paired with the  *y*  -coordinate represented by the [D](d-cell-geometry-section.md) cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f2623-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="f2623-117">Remarks</span></span>

<span data-ttu-id="f2623-118">Pour obtenir une référence à la cellule C par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="f2623-118">To get a reference to the C cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f2623-119">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="f2623-119">Cell name:</span></span>  <br/> | <span data-ttu-id="f2623-120">Géométrie *i* . C *j* où *i* et *j* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="f2623-120">Geometry  *i*  .C  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="f2623-121">Géométrie *i* . C1 (ligne Ellipse)</span><span class="sxs-lookup"><span data-stu-id="f2623-121">Geometry  *i*  .C1 (Ellipse row)</span></span>  <br/> |
   
<span data-ttu-id="f2623-122">Pour obtenir une référence à la cellule C par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="f2623-122">To get a reference to the C cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f2623-123">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="f2623-123">Section index:</span></span>  <br/> |<span data-ttu-id="f2623-124">**visSectionFirstComponent** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="f2623-124">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="f2623-125">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="f2623-125">Row index:</span></span>  <br/> |<span data-ttu-id="f2623-126">**visRowVertex** +  *j* où *j* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="f2623-126">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="f2623-127">**visRowVertex** (Ligne ellipse)</span><span class="sxs-lookup"><span data-stu-id="f2623-127">**visRowVertex** (Ellipse row)</span></span>  <br/> |
| <span data-ttu-id="f2623-128">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="f2623-128">Cell index:</span></span>  <br/> |<span data-ttu-id="f2623-129">**visEccentricityAngle** (Ligne EllipticalArcTo)</span><span class="sxs-lookup"><span data-stu-id="f2623-129">**visEccentricityAngle** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="f2623-130">**visNURBSKnotPrev** (Ligne NURBSTo)</span><span class="sxs-lookup"><span data-stu-id="f2623-130">**visNURBSKnotPrev** (NURBSTo row)</span></span>  <br/> |
||<span data-ttu-id="f2623-131">**visSplineKnot3** (Ligne SplineStart)</span><span class="sxs-lookup"><span data-stu-id="f2623-131">**visSplineKnot3** (SplineStart row)</span></span>  <br/> |
||<span data-ttu-id="f2623-132">**visEllipseMinorX** (Ligne ellipse)</span><span class="sxs-lookup"><span data-stu-id="f2623-132">**visEllipseMinorX** (Ellipse row)</span></span>  <br/> |
   

