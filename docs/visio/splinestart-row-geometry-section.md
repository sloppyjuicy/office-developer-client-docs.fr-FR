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
description: Contient des x et y-coordonnées pour le deuxième point de contrôle d’une spline, du deuxième nœud, du premier nœud, du dernier nœud et du degré de la spline.
ms.openlocfilehash: 0944da12e6090fde41dc5927b5705e103d29f76d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789805"
---
# <a name="splinestart-row-geometry-section"></a><span data-ttu-id="e1a18-103">SplineStart, ligne (section Geometry)</span><span class="sxs-lookup"><span data-stu-id="e1a18-103">SplineStart Row (Geometry Section)</span></span>

<span data-ttu-id="e1a18-104">Contient des *x* et *y* -coordonnées pour le deuxième point de contrôle d’une spline, du deuxième nœud, du premier nœud, du dernier nœud et du degré de la spline.</span><span class="sxs-lookup"><span data-stu-id="e1a18-104">Contains  *x*  - and  *y*  -coordinates for a spline's second control point, its second knot, its first knot, the last knot, and the degree of the spline.</span></span> 
  
<span data-ttu-id="e1a18-105">Une ligne SplineStart contient les cellules suivantes.</span><span class="sxs-lookup"><span data-stu-id="e1a18-105">A SplineStart row contains the following cells.</span></span>
  
|<span data-ttu-id="e1a18-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="e1a18-106">**Cell**</span></span>|<span data-ttu-id="e1a18-107">**Description**</span><span class="sxs-lookup"><span data-stu-id="e1a18-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e1a18-108">X</span><span class="sxs-lookup"><span data-stu-id="e1a18-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="e1a18-109">*X* -coordonnées du deuxième point de contrôle d’une spline.</span><span class="sxs-lookup"><span data-stu-id="e1a18-109">The  *x*  -coordinate of a spline's second control point.</span></span>  <br/> |
|[<span data-ttu-id="e1a18-110">Y</span><span class="sxs-lookup"><span data-stu-id="e1a18-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="e1a18-111">La valeur *y* -coordonnées du deuxième point de contrôle d’une spline.</span><span class="sxs-lookup"><span data-stu-id="e1a18-111">The  *y*  -coordinate of a spline's second control point.</span></span>  <br/> |
|[<span data-ttu-id="e1a18-112">A</span><span class="sxs-lookup"><span data-stu-id="e1a18-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="e1a18-113">Deuxième nœud de la spline.</span><span class="sxs-lookup"><span data-stu-id="e1a18-113">The second knot of the spline.</span></span>  <br/> |
|[<span data-ttu-id="e1a18-114">B</span><span class="sxs-lookup"><span data-stu-id="e1a18-114">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="e1a18-115">Premier nœud d’une spline</span><span class="sxs-lookup"><span data-stu-id="e1a18-115">The first knot of a spline.</span></span>  <br/> |
|[<span data-ttu-id="e1a18-116">C</span><span class="sxs-lookup"><span data-stu-id="e1a18-116">C</span></span>](c-cell-geometry-section.md) <br/> |<span data-ttu-id="e1a18-117">Dernier nœud d’une spline</span><span class="sxs-lookup"><span data-stu-id="e1a18-117">The last knot of a spline.</span></span>  <br/> |
|[<span data-ttu-id="e1a18-118">D</span><span class="sxs-lookup"><span data-stu-id="e1a18-118">D</span></span>](d-cell-geometry-section.md) <br/> |<span data-ttu-id="e1a18-119">Degré d'une spline (entier compris entre 1 et 25).</span><span class="sxs-lookup"><span data-stu-id="e1a18-119">The degree of a spline (an integer from 1 to 25).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e1a18-120">Notes</span><span class="sxs-lookup"><span data-stu-id="e1a18-120">Remarks</span></span>

<span data-ttu-id="e1a18-p101">Visio affiche la définition d'une spline dans la section Geometry qui contient une ligne SplineStart, suivie d'une ou de plusieurs lignes SplineKnot. La ligne SplineStart doit être précédée d'un autre type de ligne, tel que la ligne MoveTo pour indiquer le premier point de contrôle de la spline. La ligne précédente peut être une ligne LineTo, ArcTo, NURBSTo, PolylineTo ou EllipticalArcTo si la spline suit un segment de ce type.</span><span class="sxs-lookup"><span data-stu-id="e1a18-p101">Visio displays the definition of a spline in a Geometry section that contains a SplineStart row followed by one or more SplineKnot rows. The SplineStart row must be preceded by another kind of row, such as a MoveTo row, to indicate the first control point of the spline. The preceding row can be a LineTo, ArcTo, NURBSTo, PolylineTo, or EllipticalArcTo row if the spline follows a segment of that type.</span></span>
  

