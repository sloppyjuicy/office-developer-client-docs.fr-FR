---
title: SplineStart, ligne (section Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm3055
localization_priority: Normal
ms.assetid: 8e327e00-0844-efa4-900b-6954d3b009bb
description: Contient les coordonnées x et y pour le deuxième point de contrôle d’une spline, son deuxième nœud, son premier nœud, le dernier nœud et le degré de la spline.
ms.openlocfilehash: 2ec06619770af4e5dbcc1a763595b6e01a39052b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417475"
---
# <a name="splinestart-row-geometry-section"></a><span data-ttu-id="3b76b-103">SplineStart, ligne (section Geometry)</span><span class="sxs-lookup"><span data-stu-id="3b76b-103">SplineStart Row (Geometry Section)</span></span>

<span data-ttu-id="3b76b-104">Contient  *les coordonnées x*  et  *y*  pour le deuxième point de contrôle d’une spline, son deuxième nœud, son premier nœud, le dernier nœud et le degré de la spline.</span><span class="sxs-lookup"><span data-stu-id="3b76b-104">Contains  *x*  - and  *y*  -coordinates for a spline's second control point, its second knot, its first knot, the last knot, and the degree of the spline.</span></span> 
  
<span data-ttu-id="3b76b-105">Une ligne SplineStart contient les cellules suivantes.</span><span class="sxs-lookup"><span data-stu-id="3b76b-105">A SplineStart row contains the following cells.</span></span>
  
|<span data-ttu-id="3b76b-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="3b76b-106">**Cell**</span></span>|<span data-ttu-id="3b76b-107">**Description**</span><span class="sxs-lookup"><span data-stu-id="3b76b-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3b76b-108">X</span><span class="sxs-lookup"><span data-stu-id="3b76b-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="3b76b-109">Coordonnée  *x*  du deuxième point de contrôle d’une spline.</span><span class="sxs-lookup"><span data-stu-id="3b76b-109">The  *x*  -coordinate of a spline's second control point.</span></span>  <br/> |
|[<span data-ttu-id="3b76b-110">Y</span><span class="sxs-lookup"><span data-stu-id="3b76b-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="3b76b-111">Coordonnée  *y*  du deuxième point de contrôle d’une spline.</span><span class="sxs-lookup"><span data-stu-id="3b76b-111">The  *y*  -coordinate of a spline's second control point.</span></span>  <br/> |
|[<span data-ttu-id="3b76b-112">A</span><span class="sxs-lookup"><span data-stu-id="3b76b-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="3b76b-113">Deuxième nœud de la spline.</span><span class="sxs-lookup"><span data-stu-id="3b76b-113">The second knot of the spline.</span></span>  <br/> |
|[<span data-ttu-id="3b76b-114">B</span><span class="sxs-lookup"><span data-stu-id="3b76b-114">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="3b76b-115">Premier nœud d'une spline.</span><span class="sxs-lookup"><span data-stu-id="3b76b-115">The first knot of a spline.</span></span>  <br/> |
|[<span data-ttu-id="3b76b-116">C</span><span class="sxs-lookup"><span data-stu-id="3b76b-116">C</span></span>](c-cell-geometry-section.md) <br/> |<span data-ttu-id="3b76b-117">Dernier nœud d'une spline.</span><span class="sxs-lookup"><span data-stu-id="3b76b-117">The last knot of a spline.</span></span>  <br/> |
|[<span data-ttu-id="3b76b-118">D</span><span class="sxs-lookup"><span data-stu-id="3b76b-118">D</span></span>](d-cell-geometry-section.md) <br/> |<span data-ttu-id="3b76b-119">Degré d'une spline (entier compris entre 1 et 25).</span><span class="sxs-lookup"><span data-stu-id="3b76b-119">The degree of a spline (an integer from 1 to 25).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3b76b-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="3b76b-120">Remarks</span></span>

<span data-ttu-id="3b76b-p101">Visio affiche la définition d'une spline dans la section Geometry qui contient une ligne SplineStart, suivie d'une ou de plusieurs lignes SplineKnot. La ligne SplineStart doit être précédée d'un autre type de ligne, tel que la ligne MoveTo pour indiquer le premier point de contrôle de la spline. La ligne précédente peut être une ligne LineTo, ArcTo, NURBSTo, PolylineTo ou EllipticalArcTo si la spline suit un segment de ce type.</span><span class="sxs-lookup"><span data-stu-id="3b76b-p101">Visio displays the definition of a spline in a Geometry section that contains a SplineStart row followed by one or more SplineKnot rows. The SplineStart row must be preceded by another kind of row, such as a MoveTo row, to indicate the first control point of the spline. The preceding row can be a LineTo, ArcTo, NURBSTo, PolylineTo, or EllipticalArcTo row if the spline follows a segment of that type.</span></span>
  

