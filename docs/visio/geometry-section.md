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
ms.openlocfilehash: d45f960ecc697dc6f0f5a0efa18e6cbbc6e4fff0
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542281"
---
# <a name="geometry-section"></a><span data-ttu-id="5dd05-103">Geometry, section</span><span class="sxs-lookup"><span data-stu-id="5dd05-103">Geometry Section</span></span>

<span data-ttu-id="5dd05-104">Contient les lignes qui répertorient les coordonnées des sommets des traits et des arcs qui constituent la forme.</span><span class="sxs-lookup"><span data-stu-id="5dd05-104">Contains rows that list the coordinates of the vertices for the lines and arcs that make up the shape.</span></span> 
  
<span data-ttu-id="5dd05-105">La géométrie d’une forme peut être exprimée dans plusieurs sections **Geometry.**</span><span class="sxs-lookup"><span data-stu-id="5dd05-105">The geometry of a shape can be expressed in multiple **Geometry** sections.</span></span> <span data-ttu-id="5dd05-106">Plusieurs chemins peuvent être utiles lorsque plusieurs chemins ont des propriétés différentes (par exemple, des chemins de découpage [d’image).](clippingpath-cell-foreign-image-info-section.md)</span><span class="sxs-lookup"><span data-stu-id="5dd05-106">Multiple paths can be useful when multiple paths have different properties (e.g. [image clipping](clippingpath-cell-foreign-image-info-section.md) paths).</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="5dd05-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="5dd05-107">Remarks</span></span>

<span data-ttu-id="5dd05-108">La section **Geometry** contient les types de lignes suivants.</span><span class="sxs-lookup"><span data-stu-id="5dd05-108">The **Geometry** section contains the following row types.</span></span> <span data-ttu-id="5dd05-109">Pour plus de détails, voir les rubriques spécifiques des lignes.</span><span class="sxs-lookup"><span data-stu-id="5dd05-109">For details, see the row topics.</span></span> 
  
|<span data-ttu-id="5dd05-110">Ligne</span><span class="sxs-lookup"><span data-stu-id="5dd05-110">Row</span></span>|<span data-ttu-id="5dd05-111">Description</span><span class="sxs-lookup"><span data-stu-id="5dd05-111">Description</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5dd05-112">MoveTo</span><span class="sxs-lookup"><span data-stu-id="5dd05-112">MoveTo</span></span>](moveto-row-geometry-section.md) <br/> |<span data-ttu-id="5dd05-113">Déplace vers une coordonnée.</span><span class="sxs-lookup"><span data-stu-id="5dd05-113">Move to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="5dd05-114">LineTo</span><span class="sxs-lookup"><span data-stu-id="5dd05-114">LineTo</span></span>](lineto-row-geometry-section.md) <br/> |<span data-ttu-id="5dd05-115">Trace un trait jusqu’à une coordonnée.</span><span class="sxs-lookup"><span data-stu-id="5dd05-115">Draw a line to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="5dd05-116">ArcTo</span><span class="sxs-lookup"><span data-stu-id="5dd05-116">ArcTo</span></span>](arcto-row-geometry-section.md) <br/> |<span data-ttu-id="5dd05-117">Trace un arc de cercle jusqu’à une coordonnée.</span><span class="sxs-lookup"><span data-stu-id="5dd05-117">Draw a circular arc to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="5dd05-118">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="5dd05-118">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> |<span data-ttu-id="5dd05-119">Trace un arc elliptique jusqu’à une coordonnée.</span><span class="sxs-lookup"><span data-stu-id="5dd05-119">Draw an elliptical arc to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="5dd05-120">PolylineTo</span><span class="sxs-lookup"><span data-stu-id="5dd05-120">PolylineTo</span></span>](polylineto-row-geometry-section.md) <br/> |<span data-ttu-id="5dd05-121">Trace une polyligne ou des lignes consécutives jusqu’à une coordonnée.</span><span class="sxs-lookup"><span data-stu-id="5dd05-121">Draw a polyline, or consecutive lines, to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="5dd05-122">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="5dd05-122">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> |<span data-ttu-id="5dd05-123">Dessinez une ligne B-spline rationnelle non uniforme (NURBS) vers une coordonnée.</span><span class="sxs-lookup"><span data-stu-id="5dd05-123">Draw a non-uniform rational B-spline (NURBS) to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="5dd05-124">SplineStart</span><span class="sxs-lookup"><span data-stu-id="5dd05-124">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> |<span data-ttu-id="5dd05-125">Débute une spline.</span><span class="sxs-lookup"><span data-stu-id="5dd05-125">Start a spline.</span></span>  <br/> |
|[<span data-ttu-id="5dd05-126">SplineKnot</span><span class="sxs-lookup"><span data-stu-id="5dd05-126">SplineKnot</span></span>](splineknot-row-geometry-section.md) <br/> |<span data-ttu-id="5dd05-127">Trace un segment de spline jusqu’à une coordonnée de nœud.</span><span class="sxs-lookup"><span data-stu-id="5dd05-127">Draw a spline segment to a knot coordinate.</span></span>  <br/> |
|[<span data-ttu-id="5dd05-128">InfiniteLine</span><span class="sxs-lookup"><span data-stu-id="5dd05-128">InfiniteLine</span></span>](infiniteline-row-geometry-section.md) <br/> |<span data-ttu-id="5dd05-129">Trace une ligne infinie d’une coordonnée à une autre.</span><span class="sxs-lookup"><span data-stu-id="5dd05-129">Draw an infinite line from one coordinate to another.</span></span>  <br/> |
|[<span data-ttu-id="5dd05-130">Ellipse</span><span class="sxs-lookup"><span data-stu-id="5dd05-130">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> |<span data-ttu-id="5dd05-131">Trace une ellipse à partir de la coordonnée du centre et d’un grand/petit axe.</span><span class="sxs-lookup"><span data-stu-id="5dd05-131">Draw an ellipse from a center coordinate and a major/minor axis.</span></span>  <br/> |
|[<span data-ttu-id="5dd05-132">RelCubBezTo</span><span class="sxs-lookup"><span data-stu-id="5dd05-132">RelCubBezTo</span></span>](relcubbezto-row-geometry-section.md) <br/> |<span data-ttu-id="5dd05-133">Dessinez une courbe de Bézier cubique par rapport à la largeur et à la hauteur de la forme.</span><span class="sxs-lookup"><span data-stu-id="5dd05-133">Draw a cubic Bezier curve relative to the width and height of the shape.</span></span>  <br/> |
|[<span data-ttu-id="5dd05-134">RelEllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="5dd05-134">RelEllipticalArcTo</span></span>](relellipticalarcto-row-geometry-section.md) <br/> |<span data-ttu-id="5dd05-135">Dessinez un arc elliptique à une coordonnée par rapport à la hauteur et à la largeur de la forme.</span><span class="sxs-lookup"><span data-stu-id="5dd05-135">Draw an elliptical arc to a coordinate relative to the height and width of the shape.</span></span>  <br/> |
|[<span data-ttu-id="5dd05-136">RelLineTo</span><span class="sxs-lookup"><span data-stu-id="5dd05-136">RelLineTo</span></span>](rellineto-row-geometry-section.md) <br/> |<span data-ttu-id="5dd05-137">Dessinez un trait vers une coordonnée relative à la hauteur et à la largeur d’une forme.</span><span class="sxs-lookup"><span data-stu-id="5dd05-137">Draw a line to a coordinate relative the height and width of a shape.</span></span>  <br/> |
|[<span data-ttu-id="5dd05-138">RelMoveTo</span><span class="sxs-lookup"><span data-stu-id="5dd05-138">RelMoveTo</span></span>](relmoveto-row-geometry-section.md) <br/> |<span data-ttu-id="5dd05-139">Atteindre une coordonnée par rapport à la largeur et à la hauteur de la forme.</span><span class="sxs-lookup"><span data-stu-id="5dd05-139">Move to a coordinate relative to the width and height of the shape.</span></span>  <br/> |
|[<span data-ttu-id="5dd05-140">RelQuadBezTo</span><span class="sxs-lookup"><span data-stu-id="5dd05-140">RelQuadBezTo</span></span>](relquadbezto-row-geometry-section.md) <br/> |<span data-ttu-id="5dd05-141">Dessine une courbe de Bézier quadratique par rapport à la largeur et à la hauteur de la forme.</span><span class="sxs-lookup"><span data-stu-id="5dd05-141">Draws a quadratic Bezier curve relative to the width and height of the shape.</span></span>  <br/> |
   
<span data-ttu-id="5dd05-142">Pour changer de type de ligne dans cette section, cliquez avec le bouton droit de la souris sur la ligne, puis cliquez sur **Modifier le type de ligne** dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="5dd05-142">To change a row type in this section, right-click the row, and then click **Change Row Type** on the shortcut menu.</span></span> 
  

