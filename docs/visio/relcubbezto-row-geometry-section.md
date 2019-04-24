---
title: RelCubBezTo Row (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 77777dd4-5a2c-4048-9ea4-9bd876862963
description: Contient les coordonnées x et y du point de fin d'une courbe de Bézier cubique par rapport à la largeur et la hauteur de la forme, les coordonnées x et y du point de contrôle du début de la largeur et de la hauteur de la forme relative de la courbe, ainsi que les coordonnées x et y du contro l point de la fin de la largeur et de la hauteur de la forme relative de courbe.
ms.openlocfilehash: cb886706c4c5cbb3488a95b57dcc84e0e45ee326
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320033"
---
# <a name="relcubbezto-row-geometry-section"></a><span data-ttu-id="c4b55-103">RelCubBezTo Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="c4b55-103">RelCubBezTo Row (Geometry Section)</span></span>

<span data-ttu-id="c4b55-104">Contient les coordonnées *x* et *y* du point de fin d'une courbe de Bézier cubique par rapport à la largeur et la hauteur de la forme, les coordonnées *x* et *y* du point de contrôle du début de la largeur et de la hauteur de la forme relative de la courbe, et les coordonnées *x* et *y* du point de contrôle de la fin de la largeur et de la hauteur de la forme relative de courbe.</span><span class="sxs-lookup"><span data-stu-id="c4b55-104">Contains the  *x*  - and  *y*  -coordinates of the endpoint of a cubic Bézier curve relative to the shape's width and height, the  *x*  - and  *y*  -coordinates of the control point of the beginning of the curve relative shape's width and height, and the  *x*  - and  *y*  -coordinates of the control point of the ending of the curve relative shape's width and height.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="c4b55-105">Une ligne **RelCubBezTo** ne peut être conservée que dans les formats de fichier. vsdx,. VSDM,. vstx,. vstm,. vssx et. VSSM.</span><span class="sxs-lookup"><span data-stu-id="c4b55-105">A **RelCubBezTo** row can only be persisted in the .vsdx, .vsdm, .vstx, .vstm, .vssx, and .vssm file formats.</span></span> <span data-ttu-id="c4b55-106">Lorsqu'un fichier est enregistré aux formats Visio 2003-2010, la ligne **RelCubBezTo** est convertie en ligne [NURBSTo](nurbsto-row-geometry-section.md) .</span><span class="sxs-lookup"><span data-stu-id="c4b55-106">When a file is saved to the Visio 2003-2010 formats, the **RelCubBezTo** row is converted to a [NURBSTo](nurbsto-row-geometry-section.md) row.</span></span> 
  
<span data-ttu-id="c4b55-107">Une ligne **RelCubBezTo** contient les cellules suivantes.</span><span class="sxs-lookup"><span data-stu-id="c4b55-107">A **RelCubBezTo** row contains the following cells.</span></span> 
  
|<span data-ttu-id="c4b55-108">**Cell**</span><span class="sxs-lookup"><span data-stu-id="c4b55-108">**Cell**</span></span>|<span data-ttu-id="c4b55-109">**Description**</span><span class="sxs-lookup"><span data-stu-id="c4b55-109">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c4b55-110">X</span><span class="sxs-lookup"><span data-stu-id="c4b55-110">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="c4b55-111">Coordonnée *x* du sommet de fin d'une courbe de Bézier cubique par rapport à la largeur de la forme.</span><span class="sxs-lookup"><span data-stu-id="c4b55-111">The  *x*  -coordinate of the ending vertex of a cubic Bézier curve relative to the width of the shape.</span></span>  <br/> |
|[<span data-ttu-id="c4b55-112">Y</span><span class="sxs-lookup"><span data-stu-id="c4b55-112">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="c4b55-113">Coordonnée *y* du sommet de fin d'une courbe de Bézier cubique par rapport à la hauteur de la forme.</span><span class="sxs-lookup"><span data-stu-id="c4b55-113">The  *y*  -coordinate of the ending vertex of a cubic Bézier curve relative to the height of the shape.</span></span>  <br/> |
|[<span data-ttu-id="c4b55-114">A</span><span class="sxs-lookup"><span data-stu-id="c4b55-114">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="c4b55-115">Coordonnée *x* du point de contrôle de début de la courbe par rapport à la largeur de la forme; point sur l'arc. Le point de contrôle est le mieux situé entre les sommets de début et de fin de l'arc.</span><span class="sxs-lookup"><span data-stu-id="c4b55-115">The  *x*  -coordinate of the curve's beginning control point relative to the shape's width; a point on the arc. The control point is best located between the beginning and ending vertices of the arc.</span></span>  <br/> |
|[<span data-ttu-id="c4b55-116">Point</span><span class="sxs-lookup"><span data-stu-id="c4b55-116">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="c4b55-117">Coordonnée *y* du point de contrôle de début d'une courbe par rapport à la hauteur de la forme.</span><span class="sxs-lookup"><span data-stu-id="c4b55-117">The  *y*  -coordinate of a curve's beginning control point relative to the shape's height.</span></span>  <br/> |
|[<span data-ttu-id="c4b55-118">C</span><span class="sxs-lookup"><span data-stu-id="c4b55-118">C</span></span>](c-cell-geometry-section.md) <br/> |<span data-ttu-id="c4b55-119">Coordonnée *x* du point de contrôle de fin de la courbe par rapport à la largeur de la forme; point sur l'arc. Le point de contrôle est le mieux situé entre le point de contrôle de début et les sommets de fin de l'arc.</span><span class="sxs-lookup"><span data-stu-id="c4b55-119">The  *x*  -coordinate of the curve's ending control point relative to the shape's width; a point on the arc. The control point is best located between the beginning control point and ending vertices of the arc.</span></span>  <br/> |
|[<span data-ttu-id="c4b55-120">D</span><span class="sxs-lookup"><span data-stu-id="c4b55-120">D</span></span>](d-cell-geometry-section.md) <br/> |<span data-ttu-id="c4b55-121">Coordonnée *y* du point de contrôle de fin d'une courbe par rapport à la hauteur de la forme.</span><span class="sxs-lookup"><span data-stu-id="c4b55-121">The  *y*  -coordinate of a curve's ending control point relative to the shape's height.</span></span>  <br/> |
   

