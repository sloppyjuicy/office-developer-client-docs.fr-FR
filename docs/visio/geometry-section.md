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
description: Contient des lignes qui répertorient les coordonnées des sommets des traits et des arcs qui constituent la forme.
ms.openlocfilehash: 59f85c512b7038f6cfddcb657435730a2e724bd6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788708"
---
# <a name="geometry-section"></a><span data-ttu-id="9f763-103">Geometry, section</span><span class="sxs-lookup"><span data-stu-id="9f763-103">Geometry Section</span></span>

<span data-ttu-id="9f763-104">Contient des lignes qui répertorient les coordonnées des sommets des traits et des arcs qui constituent la forme.</span><span class="sxs-lookup"><span data-stu-id="9f763-104">Contains rows that list the coordinates of the vertices for the lines and arcs that make up the shape.</span></span> 
  
<span data-ttu-id="9f763-105">La géométrie d’une forme peut être exprimée en plusieurs sections **Geometry** .</span><span class="sxs-lookup"><span data-stu-id="9f763-105">The geometry of a shape can be expressed in multiple **Geometry** sections.</span></span> <span data-ttu-id="9f763-106">Plusieurs chemins d’accès peuvent être utiles lorsque plusieurs chemins d’accès sont différentes propriétés (par exemple, les chemins d’accès de [capture d’image](clippingpath-cell-foreign-image-info-section.md) ).</span><span class="sxs-lookup"><span data-stu-id="9f763-106">Multiple paths can be useful when multiple paths have different properties (e.g. [image clipping](clippingpath-cell-foreign-image-info-section.md) paths).</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="9f763-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="9f763-107">Remarks</span></span>

<span data-ttu-id="9f763-108">La section **Geometry** contient les types suivants de la ligne.</span><span class="sxs-lookup"><span data-stu-id="9f763-108">The **Geometry** section contains the following row types.</span></span> <span data-ttu-id="9f763-109">Pour plus d’informations, consultez les rubriques de la ligne.</span><span class="sxs-lookup"><span data-stu-id="9f763-109">For details, see the row topics.</span></span> 
  
|<span data-ttu-id="9f763-110">**Row**</span><span class="sxs-lookup"><span data-stu-id="9f763-110">**Row**</span></span>|<span data-ttu-id="9f763-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="9f763-111">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9f763-112">MoveTo</span><span class="sxs-lookup"><span data-stu-id="9f763-112">MoveTo</span></span>](moveto-row-geometry-section.md) <br/> |<span data-ttu-id="9f763-113">Déplace vers une coordonnée.</span><span class="sxs-lookup"><span data-stu-id="9f763-113">Move to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="9f763-114">LineTo</span><span class="sxs-lookup"><span data-stu-id="9f763-114">LineTo</span></span>](lineto-row-geometry-section.md) <br/> |<span data-ttu-id="9f763-115">Trace un trait jusqu’à une coordonnée.</span><span class="sxs-lookup"><span data-stu-id="9f763-115">Draw a line to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="9f763-116">ArcTo</span><span class="sxs-lookup"><span data-stu-id="9f763-116">ArcTo</span></span>](arcto-row-geometry-section.md) <br/> |<span data-ttu-id="9f763-117">Trace un arc de cercle jusqu’à une coordonnée.</span><span class="sxs-lookup"><span data-stu-id="9f763-117">Draw a circular arc to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="9f763-118">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="9f763-118">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> |<span data-ttu-id="9f763-119">Trace un arc elliptique jusqu’à une coordonnée.</span><span class="sxs-lookup"><span data-stu-id="9f763-119">Draw an elliptical arc to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="9f763-120">PolylineTo</span><span class="sxs-lookup"><span data-stu-id="9f763-120">PolylineTo</span></span>](polylineto-row-geometry-section.md) <br/> |<span data-ttu-id="9f763-121">Trace une polyligne ou des lignes consécutives jusqu’à une coordonnée.</span><span class="sxs-lookup"><span data-stu-id="9f763-121">Draw a polyline, or consecutive lines, to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="9f763-122">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="9f763-122">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> |<span data-ttu-id="9f763-123">Trace une non-uniform rational B-spline (NURBS) jusqu'à une coordonnée.</span><span class="sxs-lookup"><span data-stu-id="9f763-123">Draw a non-uniform rational B-spline (NURBS) to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="9f763-124">SplineStart</span><span class="sxs-lookup"><span data-stu-id="9f763-124">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> |<span data-ttu-id="9f763-125">Débute une spline.</span><span class="sxs-lookup"><span data-stu-id="9f763-125">Start a spline.</span></span>  <br/> |
|[<span data-ttu-id="9f763-126">SplineKnot</span><span class="sxs-lookup"><span data-stu-id="9f763-126">SplineKnot</span></span>](splineknot-row-geometry-section.md) <br/> |<span data-ttu-id="9f763-127">Trace un segment de spline jusqu’à une coordonnée de nœud.</span><span class="sxs-lookup"><span data-stu-id="9f763-127">Draw a spline segment to a knot coordinate.</span></span>  <br/> |
|[<span data-ttu-id="9f763-128">InfiniteLine</span><span class="sxs-lookup"><span data-stu-id="9f763-128">InfiniteLine</span></span>](infiniteline-row-geometry-section.md) <br/> |<span data-ttu-id="9f763-129">Trace une ligne infinie d’une coordonnée à une autre.</span><span class="sxs-lookup"><span data-stu-id="9f763-129">Draw an infinite line from one coordinate to another.</span></span>  <br/> |
|[<span data-ttu-id="9f763-130">Ellipse</span><span class="sxs-lookup"><span data-stu-id="9f763-130">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> |<span data-ttu-id="9f763-131">Trace une ellipse à partir de la coordonnée du centre et d’un grand/petit axe.</span><span class="sxs-lookup"><span data-stu-id="9f763-131">Draw an ellipse from a center coordinate and a major/minor axis.</span></span>  <br/> |
|[<span data-ttu-id="9f763-132">RelCubBezTo</span><span class="sxs-lookup"><span data-stu-id="9f763-132">RelCubBezTo</span></span>](relcubbezto-row-geometry-section.md) <br/> |<span data-ttu-id="9f763-133">Trace une courbe de Bézier cube par rapport à la largeur et la hauteur de la forme.</span><span class="sxs-lookup"><span data-stu-id="9f763-133">Draw a cubic Bezier curve relative to the width and height of the shape.</span></span>  <br/> |
|[<span data-ttu-id="9f763-134">RelEllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="9f763-134">RelEllipticalArcTo</span></span>](relellipticalarcto-row-geometry-section.md) <br/> |<span data-ttu-id="9f763-135">Trace un arc elliptique jusqu'à une coordonnée par rapport à la hauteur et la largeur de la forme.</span><span class="sxs-lookup"><span data-stu-id="9f763-135">Draw an elliptical arc to a coordinate relative to the height and width of the shape.</span></span>  <br/> |
|[<span data-ttu-id="9f763-136">RelLineTo</span><span class="sxs-lookup"><span data-stu-id="9f763-136">RelLineTo</span></span>](rellineto-row-geometry-section.md) <br/> |<span data-ttu-id="9f763-137">Trace un trait jusqu'à une coordonnée relative de la hauteur et la largeur d’une forme.</span><span class="sxs-lookup"><span data-stu-id="9f763-137">Draw a line to a coordinate relative the height and width of a shape.</span></span>  <br/> |
|[<span data-ttu-id="9f763-138">RelMoveTo</span><span class="sxs-lookup"><span data-stu-id="9f763-138">RelMoveTo</span></span>](relmoveto-row-geometry-section.md) <br/> |<span data-ttu-id="9f763-139">Déplacer vers une coordonnée par rapport à la largeur et la hauteur de la forme.</span><span class="sxs-lookup"><span data-stu-id="9f763-139">Move to a coordinate relative to the width and height of the shape.</span></span>  <br/> |
|[<span data-ttu-id="9f763-140">RelQuadBezTo</span><span class="sxs-lookup"><span data-stu-id="9f763-140">RelQuadBezTo</span></span>](relquadbezto-row-geometry-section.md) <br/> |<span data-ttu-id="9f763-141">Dessine une courbe de Bézier quadratique par rapport à la largeur et la hauteur de la forme.</span><span class="sxs-lookup"><span data-stu-id="9f763-141">Draws a quadratic Bezier curve relative to the width and height of the shape.</span></span>  <br/> |
   
<span data-ttu-id="9f763-142">Pour modifier un type de ligne dans cette section, avec le bouton droit de la ligne, puis cliquez sur **Modifier le Type de ligne** dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="9f763-142">To change a row type in this section, right-click the row, and then click **Change Row Type** on the shortcut menu.</span></span> 
  

