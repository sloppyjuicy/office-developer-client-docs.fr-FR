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
ms.openlocfilehash: 0284fea02c7eb890b56b6c865a69eb36662d8ae6
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541889"
---
# <a name="c-cell-geometry-section"></a><span data-ttu-id="fc762-104">C, cellule (section Geometry)</span><span class="sxs-lookup"><span data-stu-id="fc762-104">C Cell (Geometry Section)</span></span>

<span data-ttu-id="fc762-p102">Représente des informations différentes selon la ligne où elle se trouve. Le tableau ci-dessous décrit la cellule C pour chaque ligne.</span><span class="sxs-lookup"><span data-stu-id="fc762-p102">Represents different information in different rows. This table describes the C cell based on the row in which it's located.</span></span>
  
|<span data-ttu-id="fc762-107">Ligne</span><span class="sxs-lookup"><span data-stu-id="fc762-107">Row</span></span>|<span data-ttu-id="fc762-108">Description</span><span class="sxs-lookup"><span data-stu-id="fc762-108">Description</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fc762-109">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="fc762-109">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="fc762-110">Angle de l’axe principal d’un arc par rapport à  *l’axe X*  de son parent.</span><span class="sxs-lookup"><span data-stu-id="fc762-110">The angle of an arc's major axis relative to the  *x*  -axis of its parent.</span></span>  <br/> |
|[<span data-ttu-id="fc762-111">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="fc762-111">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="fc762-112">Premier nœud de la courbe B-spline rationnelle non uniforme (NURBS).</span><span class="sxs-lookup"><span data-stu-id="fc762-112">The first knot of the nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|[<span data-ttu-id="fc762-113">SplineStart</span><span class="sxs-lookup"><span data-stu-id="fc762-113">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> | <span data-ttu-id="fc762-114">Dernier nœud d’une spline</span><span class="sxs-lookup"><span data-stu-id="fc762-114">The last knot of a spline.</span></span>  <br/> |
|[<span data-ttu-id="fc762-115">Ellipse</span><span class="sxs-lookup"><span data-stu-id="fc762-115">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="fc762-116">Coordonnée *x* d’un point sur une ellipse ; couplée à la *coordonnée y* représentée par la cellule [D.](d-cell-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="fc762-116">An  *x*  -coordinate of a point on an ellipse; paired with the  *y*  -coordinate represented by the [D](d-cell-geometry-section.md) cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fc762-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="fc762-117">Remarks</span></span>

<span data-ttu-id="fc762-118">Pour obtenir une référence à la cellule C par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="fc762-118">To get a reference to the C cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fc762-119">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="fc762-119">Cell name:</span></span>  <br/> | <span data-ttu-id="fc762-120">Geometry  *i*  . C  *j*            où  *i*  et  *j*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="fc762-120">Geometry  *i*  .C  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="fc762-121">Geometry  *i*  . C1 (ligne Ellipse)</span><span class="sxs-lookup"><span data-stu-id="fc762-121">Geometry  *i*  .C1 (Ellipse row)</span></span>  <br/> |
   
<span data-ttu-id="fc762-122">Pour obtenir une référence à la cellule C à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="fc762-122">To get a reference to the C cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fc762-123">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="fc762-123">Section index:</span></span>  <br/> |<span data-ttu-id="fc762-124">**visSectionFirstComponent**  +   *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="fc762-124">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="fc762-125">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="fc762-125">Row index:</span></span>  <br/> |<span data-ttu-id="fc762-126">**visRowVertex**  +   *j* où *j* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="fc762-126">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="fc762-127">**visRowVertex** (ligne Ellipse)</span><span class="sxs-lookup"><span data-stu-id="fc762-127">**visRowVertex** (Ellipse row)</span></span>  <br/> |
| <span data-ttu-id="fc762-128">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="fc762-128">Cell index:</span></span>  <br/> |<span data-ttu-id="fc762-129">**visEccentricityAngle** (ligne EllipticalArcTo)</span><span class="sxs-lookup"><span data-stu-id="fc762-129">**visEccentricityAngle** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="fc762-130">**visNURBSKnotPrev** (ligne NURBSTo)</span><span class="sxs-lookup"><span data-stu-id="fc762-130">**visNURBSKnotPrev** (NURBSTo row)</span></span>  <br/> |
||<span data-ttu-id="fc762-131">**visSplineKnot3** (ligne SplineStart)</span><span class="sxs-lookup"><span data-stu-id="fc762-131">**visSplineKnot3** (SplineStart row)</span></span>  <br/> |
||<span data-ttu-id="fc762-132">**visEllipseMinorX** (ligne Ellipse)</span><span class="sxs-lookup"><span data-stu-id="fc762-132">**visEllipseMinorX** (Ellipse row)</span></span>  <br/> |
   

