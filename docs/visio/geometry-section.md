---
title: Geometry, section
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm2055
localization_priority: Normal
ms.assetid: 75601a1e-6b1a-27ee-a2bd-69e569315982
description: Contient les lignes qui répertorient les coordonnées des sommets des traits et des arcs qui constituent la forme.
ms.openlocfilehash: 32a815015c7d1764399215767b674668b7235832
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345114"
---
# <a name="geometry-section"></a><span data-ttu-id="a8eff-103">Geometry, section</span><span class="sxs-lookup"><span data-stu-id="a8eff-103">Geometry Section</span></span>

<span data-ttu-id="a8eff-104">Contient les lignes qui répertorient les coordonnées des sommets des traits et des arcs qui constituent la forme.</span><span class="sxs-lookup"><span data-stu-id="a8eff-104">Contains rows that list the coordinates of the vertices for the lines and arcs that make up the shape.</span></span> 
  
<span data-ttu-id="a8eff-105">La géométrie d'une forme peut être exprimée dans plusieurs \*\*\*\* sections Geometry.</span><span class="sxs-lookup"><span data-stu-id="a8eff-105">The geometry of a shape can be expressed in multiple **Geometry** sections.</span></span> <span data-ttu-id="a8eff-106">Plusieurs chemins d'accès peuvent être utiles lorsque plusieurs chemins d'accès ont des propriétés différentes (par exemple, des masques d' [image](clippingpath-cell-foreign-image-info-section.md) ).</span><span class="sxs-lookup"><span data-stu-id="a8eff-106">Multiple paths can be useful when multiple paths have different properties (e.g. [image clipping](clippingpath-cell-foreign-image-info-section.md) paths).</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a8eff-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="a8eff-107">Remarks</span></span>

<span data-ttu-id="a8eff-108">La \*\*\*\* section Geometry contient les types de ligne suivants.</span><span class="sxs-lookup"><span data-stu-id="a8eff-108">The **Geometry** section contains the following row types.</span></span> <span data-ttu-id="a8eff-109">Pour plus de détails, voir les rubriques spécifiques des lignes.</span><span class="sxs-lookup"><span data-stu-id="a8eff-109">For details, see the row topics.</span></span> 
  
|<span data-ttu-id="a8eff-110">**Ligne**</span><span class="sxs-lookup"><span data-stu-id="a8eff-110">**Row**</span></span>|<span data-ttu-id="a8eff-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="a8eff-111">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a8eff-112">MoveTo</span><span class="sxs-lookup"><span data-stu-id="a8eff-112">MoveTo</span></span>](moveto-row-geometry-section.md) <br/> |<span data-ttu-id="a8eff-113">Déplace vers une coordonnée.</span><span class="sxs-lookup"><span data-stu-id="a8eff-113">Move to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="a8eff-114">LineTo</span><span class="sxs-lookup"><span data-stu-id="a8eff-114">LineTo</span></span>](lineto-row-geometry-section.md) <br/> |<span data-ttu-id="a8eff-115">Trace un trait jusqu’à une coordonnée.</span><span class="sxs-lookup"><span data-stu-id="a8eff-115">Draw a line to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="a8eff-116">ArcTo</span><span class="sxs-lookup"><span data-stu-id="a8eff-116">ArcTo</span></span>](arcto-row-geometry-section.md) <br/> |<span data-ttu-id="a8eff-117">Trace un arc de cercle jusqu’à une coordonnée.</span><span class="sxs-lookup"><span data-stu-id="a8eff-117">Draw a circular arc to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="a8eff-118">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="a8eff-118">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> |<span data-ttu-id="a8eff-119">Trace un arc elliptique jusqu’à une coordonnée.</span><span class="sxs-lookup"><span data-stu-id="a8eff-119">Draw an elliptical arc to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="a8eff-120">PolylineTo</span><span class="sxs-lookup"><span data-stu-id="a8eff-120">PolylineTo</span></span>](polylineto-row-geometry-section.md) <br/> |<span data-ttu-id="a8eff-121">Trace une polyligne ou des lignes consécutives jusqu’à une coordonnée.</span><span class="sxs-lookup"><span data-stu-id="a8eff-121">Draw a polyline, or consecutive lines, to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="a8eff-122">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="a8eff-122">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> |<span data-ttu-id="a8eff-123">Dessine une courbe B-spline rationnelle non uniforme (NURBS) à une coordonnée.</span><span class="sxs-lookup"><span data-stu-id="a8eff-123">Draw a non-uniform rational B-spline (NURBS) to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="a8eff-124">SplineStart</span><span class="sxs-lookup"><span data-stu-id="a8eff-124">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> |<span data-ttu-id="a8eff-125">Débute une spline.</span><span class="sxs-lookup"><span data-stu-id="a8eff-125">Start a spline.</span></span>  <br/> |
|[<span data-ttu-id="a8eff-126">SplineKnot</span><span class="sxs-lookup"><span data-stu-id="a8eff-126">SplineKnot</span></span>](splineknot-row-geometry-section.md) <br/> |<span data-ttu-id="a8eff-127">Trace un segment de spline jusqu’à une coordonnée de nœud.</span><span class="sxs-lookup"><span data-stu-id="a8eff-127">Draw a spline segment to a knot coordinate.</span></span>  <br/> |
|[<span data-ttu-id="a8eff-128">InfiniteLine</span><span class="sxs-lookup"><span data-stu-id="a8eff-128">InfiniteLine</span></span>](infiniteline-row-geometry-section.md) <br/> |<span data-ttu-id="a8eff-129">Trace une ligne infinie d’une coordonnée à une autre.</span><span class="sxs-lookup"><span data-stu-id="a8eff-129">Draw an infinite line from one coordinate to another.</span></span>  <br/> |
|[<span data-ttu-id="a8eff-130">Sélection</span><span class="sxs-lookup"><span data-stu-id="a8eff-130">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> |<span data-ttu-id="a8eff-131">Trace une ellipse à partir de la coordonnée du centre et d’un grand/petit axe.</span><span class="sxs-lookup"><span data-stu-id="a8eff-131">Draw an ellipse from a center coordinate and a major/minor axis.</span></span>  <br/> |
|[<span data-ttu-id="a8eff-132">RelCubBezTo</span><span class="sxs-lookup"><span data-stu-id="a8eff-132">RelCubBezTo</span></span>](relcubbezto-row-geometry-section.md) <br/> |<span data-ttu-id="a8eff-133">Dessine une courbe de Bézier cubique par rapport à la largeur et la hauteur de la forme.</span><span class="sxs-lookup"><span data-stu-id="a8eff-133">Draw a cubic Bezier curve relative to the width and height of the shape.</span></span>  <br/> |
|[<span data-ttu-id="a8eff-134">RelEllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="a8eff-134">RelEllipticalArcTo</span></span>](relellipticalarcto-row-geometry-section.md) <br/> |<span data-ttu-id="a8eff-135">Trace un arc elliptique jusqu'à une coordonnée par rapport à la hauteur et à la largeur de la forme.</span><span class="sxs-lookup"><span data-stu-id="a8eff-135">Draw an elliptical arc to a coordinate relative to the height and width of the shape.</span></span>  <br/> |
|[<span data-ttu-id="a8eff-136">RelLineTo</span><span class="sxs-lookup"><span data-stu-id="a8eff-136">RelLineTo</span></span>](rellineto-row-geometry-section.md) <br/> |<span data-ttu-id="a8eff-137">Trace un trait jusqu'à une coordonnée relative à la hauteur et à la largeur d'une forme.</span><span class="sxs-lookup"><span data-stu-id="a8eff-137">Draw a line to a coordinate relative the height and width of a shape.</span></span>  <br/> |
|[<span data-ttu-id="a8eff-138">RelMoveTo</span><span class="sxs-lookup"><span data-stu-id="a8eff-138">RelMoveTo</span></span>](relmoveto-row-geometry-section.md) <br/> |<span data-ttu-id="a8eff-139">Accéder à une coordonnée par rapport à la largeur et la hauteur de la forme.</span><span class="sxs-lookup"><span data-stu-id="a8eff-139">Move to a coordinate relative to the width and height of the shape.</span></span>  <br/> |
|[<span data-ttu-id="a8eff-140">RelQuadBezTo</span><span class="sxs-lookup"><span data-stu-id="a8eff-140">RelQuadBezTo</span></span>](relquadbezto-row-geometry-section.md) <br/> |<span data-ttu-id="a8eff-141">Dessine une courbe de Bézier quadratique par rapport à la largeur et la hauteur de la forme.</span><span class="sxs-lookup"><span data-stu-id="a8eff-141">Draws a quadratic Bezier curve relative to the width and height of the shape.</span></span>  <br/> |
   
<span data-ttu-id="a8eff-142">Pour changer de type de ligne dans cette section, cliquez avec le bouton droit de la souris sur la ligne, puis cliquez sur **Modifier le type de ligne** dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="a8eff-142">To change a row type in this section, right-click the row, and then click **Change Row Type** on the shortcut menu.</span></span> 
  

