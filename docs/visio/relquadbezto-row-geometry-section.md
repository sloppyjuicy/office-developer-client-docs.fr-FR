---
title: RelQuadBezTo Row (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ae57707-5a50-43f0-8c78-516790b5034e
description: Contient les coordonnées x et y du point de fin d'une courbe de Bézier quadratique par rapport à la largeur et à la hauteur de la forme, ainsi que les coordonnées x et y du point de contrôle de la largeur et de la hauteur de la forme relative de la courbe.
ms.openlocfilehash: f517fa006c6630a26e9162adfbb1be2139487e63
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319928"
---
# <a name="relquadbezto-row-geometry-section"></a><span data-ttu-id="ff9e6-103">RelQuadBezTo Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="ff9e6-103">RelQuadBezTo Row (Geometry Section)</span></span>

<span data-ttu-id="ff9e6-104">Contient les coordonnées *x* et *y* du point de fin d'une courbe de Bézier quadratique par rapport à la largeur et à la hauteur de la forme, ainsi que les coordonnées *x* et *y* du point de contrôle de la largeur et de la hauteur de la forme relative de la courbe.</span><span class="sxs-lookup"><span data-stu-id="ff9e6-104">Contains the  *x*  - and  *y*  -coordinates of the endpoint of a quadratic Bézier curve relative to the shape's width and height and the  *x*  - and  *y*  -coordinates of the control point of the curve relative shape's width and height.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="ff9e6-105">Une ligne **RelQuadBezTo** ne peut être conservée que dans les formats de fichier. vsdx,. VSDM,. vstx,. vstm,. vssx et. VSSM.</span><span class="sxs-lookup"><span data-stu-id="ff9e6-105">A **RelQuadBezTo** row can only be persisted in the .vsdx, .vsdm, .vstx, .vstm, .vssx, and .vssm file formats.</span></span> <span data-ttu-id="ff9e6-106">Lorsqu'un fichier est enregistré aux formats Visio 2003-2010, la ligne **RelQuadBezTo** est convertie en ligne [NURBSTo](nurbsto-row-geometry-section.md) .</span><span class="sxs-lookup"><span data-stu-id="ff9e6-106">When a file is saved to the Visio 2003-2010 formats, the **RelQuadBezTo** row is converted to a [NURBSTo](nurbsto-row-geometry-section.md) row.</span></span> 
  
<span data-ttu-id="ff9e6-107">Une ligne **RelQuadBezTo** contient les cellules suivantes.</span><span class="sxs-lookup"><span data-stu-id="ff9e6-107">A **RelQuadBezTo** row contains the following cells.</span></span> 
  
|<span data-ttu-id="ff9e6-108">**Cell**</span><span class="sxs-lookup"><span data-stu-id="ff9e6-108">**Cell**</span></span>|<span data-ttu-id="ff9e6-109">**Description**</span><span class="sxs-lookup"><span data-stu-id="ff9e6-109">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ff9e6-110">X</span><span class="sxs-lookup"><span data-stu-id="ff9e6-110">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="ff9e6-111">Coordonnée *x* du sommet de fin d'une courbe de Bézier quadratique par rapport à la largeur de la forme.</span><span class="sxs-lookup"><span data-stu-id="ff9e6-111">The  *x*  -coordinate of the ending vertex of a quadratic Bézier curve relative to the width of the shape.</span></span>  <br/> |
|[<span data-ttu-id="ff9e6-112">Y</span><span class="sxs-lookup"><span data-stu-id="ff9e6-112">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="ff9e6-113">Coordonnée *y* du sommet de fin d'une courbe de Bézier quadratique par rapport à la hauteur de la forme.</span><span class="sxs-lookup"><span data-stu-id="ff9e6-113">The  *y*  -coordinate of the ending vertex of a quadratic Bézier curve relative to the height of the shape.</span></span>  <br/> |
|[<span data-ttu-id="ff9e6-114">A</span><span class="sxs-lookup"><span data-stu-id="ff9e6-114">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="ff9e6-115">Coordonnée *x* du point de contrôle de la courbe par rapport à la largeur de la forme; point sur l'arc. Le point de contrôle est le mieux situé à mi-chemin entre les sommets de début et de fin de l'arc.</span><span class="sxs-lookup"><span data-stu-id="ff9e6-115">The  *x*  -coordinate of the curve's control point relative to the shape's width; a point on the arc. The control point is best located about halfway between the beginning and ending vertices of the arc.</span></span>  <br/> |
|[<span data-ttu-id="ff9e6-116">Point</span><span class="sxs-lookup"><span data-stu-id="ff9e6-116">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="ff9e6-117">Coordonnée *y* du point de contrôle d'une courbe par rapport à la hauteur de la forme.</span><span class="sxs-lookup"><span data-stu-id="ff9e6-117">The  *y*  -coordinate of a curve's control point relative to the shape's height.</span></span>  <br/> |
   

