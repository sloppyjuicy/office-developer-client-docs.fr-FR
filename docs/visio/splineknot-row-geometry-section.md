---
title: SplineKnot, ligne (section Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm3050
localization_priority: Normal
ms.assetid: 9fbae27d-4f1b-c5f7-aacb-16f359331e83
description: Contient les coordonnées x et y pour le point de contrôle d’une spline et le nœud d’une spline.
ms.openlocfilehash: 432b714772d96e0ab0861bbfb62075258404e607
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407416"
---
# <a name="splineknot-row-geometry-section"></a><span data-ttu-id="d56d1-103">SplineKnot, ligne (section Geometry)</span><span class="sxs-lookup"><span data-stu-id="d56d1-103">SplineKnot Row (Geometry Section)</span></span>

<span data-ttu-id="d56d1-104">Contient  *les coordonnées*  x et  *y*  du point de contrôle d’une spline et du nœud d’une spline.</span><span class="sxs-lookup"><span data-stu-id="d56d1-104">Contains  *x*  - and  *y*  -coordinates for a spline's control point and a spline's knot.</span></span> 
  
<span data-ttu-id="d56d1-105">Une ligne SplineKnot contient les cellules suivantes.</span><span class="sxs-lookup"><span data-stu-id="d56d1-105">A SplineKnot row contains the following cells.</span></span>
  
|<span data-ttu-id="d56d1-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="d56d1-106">**Cell**</span></span>|<span data-ttu-id="d56d1-107">**Description**</span><span class="sxs-lookup"><span data-stu-id="d56d1-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d56d1-108">X</span><span class="sxs-lookup"><span data-stu-id="d56d1-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="d56d1-109">Coordonnée  *x*  d’un point de contrôle.</span><span class="sxs-lookup"><span data-stu-id="d56d1-109">The  *x*  -coordinate of a control point.</span></span>  <br/> |
|[<span data-ttu-id="d56d1-110">Y</span><span class="sxs-lookup"><span data-stu-id="d56d1-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="d56d1-111">Coordonnée  *y*  d’un point de contrôle.</span><span class="sxs-lookup"><span data-stu-id="d56d1-111">The  *y*  -coordinate of a control point.</span></span>  <br/> |
|[<span data-ttu-id="d56d1-112">A</span><span class="sxs-lookup"><span data-stu-id="d56d1-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="d56d1-113">Un des nœuds de la spline (autre que le dernier ou les deux premiers).</span><span class="sxs-lookup"><span data-stu-id="d56d1-113">One of the spline's knots (other than the last one or the first two).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d56d1-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="d56d1-114">Remarks</span></span>

<span data-ttu-id="d56d1-p101">Visio affiche la définition d'une spline dans la section Geometry qui contient une ligne SplineStart, suivie d'une ou de plusieurs lignes SplineKnot. La ligne SplineStart doit être précédée d'un autre type de ligne, tel que la ligne MoveTo pour indiquer le premier point de contrôle de la spline. La ligne précédente peut être une ligne LineTo, ArcTo, NURBSTo, PolylineTo ou EllipticalArcTo si la spline suit un segment de ce type.</span><span class="sxs-lookup"><span data-stu-id="d56d1-p101">Visio displays the definition of a spline in a Geometry section that contains a SplineStart row followed by one or more SplineKnot rows. The SplineStart row must be preceded by another kind of row, such as a MoveTo row, to indicate the first control point of the spline. The preceding row can be a LineTo, ArcTo, NURBSTo, PolylineTo, or EllipticalArcTo row if the spline follows a segment of that type.</span></span>
  

