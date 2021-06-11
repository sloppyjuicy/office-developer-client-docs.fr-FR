---
title: RelCubBezTo Row (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 77777dd4-5a2c-4048-9ea4-9bd876862963
description: Contient les coordonnées x et y du point de terminaison d’une courbe de Bézier cubique par rapport à la largeur et à la hauteur de la forme, les coordonnées x et y du point de contrôle du début de la largeur et de la hauteur de la forme relative de courbe, et les coordonnées x et y du point de contrôle de la fin de la largeur et de la hauteur de la forme relative de courbe.
ms.openlocfilehash: cb886706c4c5cbb3488a95b57dcc84e0e45ee326
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430328"
---
# <a name="relcubbezto-row-geometry-section"></a><span data-ttu-id="af1f6-103">RelCubBezTo Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="af1f6-103">RelCubBezTo Row (Geometry Section)</span></span>

<span data-ttu-id="af1f6-104">Contient les coordonnées  *x*  et  *y*  du point de terminaison d’une courbe de Bézier cubique par rapport à la largeur et à la hauteur de la forme, les coordonnées  *x*  et  *y*  du point de contrôle du début de la largeur et de la hauteur de la forme relative de courbe, et les coordonnées  *x*  et  *y*  du point de contrôle de la fin de la largeur et de la hauteur de la forme relative de courbe.</span><span class="sxs-lookup"><span data-stu-id="af1f6-104">Contains the  *x*  - and  *y*  -coordinates of the endpoint of a cubic Bézier curve relative to the shape's width and height, the  *x*  - and  *y*  -coordinates of the control point of the beginning of the curve relative shape's width and height, and the  *x*  - and  *y*  -coordinates of the control point of the ending of the curve relative shape's width and height.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="af1f6-105">Une **ligne RelCubBezTo** ne peut être persistante que dans les formats de fichier .vsdx, .vsdm, .vstx, .vstm, .vssx et .vssm.</span><span class="sxs-lookup"><span data-stu-id="af1f6-105">A **RelCubBezTo** row can only be persisted in the .vsdx, .vsdm, .vstx, .vstm, .vssx, and .vssm file formats.</span></span> <span data-ttu-id="af1f6-106">Lorsqu’un fichier est enregistré dans les formats Visio 2003-2010, la ligne **RelCubBezTo** est convertie en ligne [NURBSTo.](nurbsto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="af1f6-106">When a file is saved to the Visio 2003-2010 formats, the **RelCubBezTo** row is converted to a [NURBSTo](nurbsto-row-geometry-section.md) row.</span></span> 
  
<span data-ttu-id="af1f6-107">Une **ligne RelCubBezTo** contient les cellules suivantes.</span><span class="sxs-lookup"><span data-stu-id="af1f6-107">A **RelCubBezTo** row contains the following cells.</span></span> 
  
|<span data-ttu-id="af1f6-108">**Cell**</span><span class="sxs-lookup"><span data-stu-id="af1f6-108">**Cell**</span></span>|<span data-ttu-id="af1f6-109">**Description**</span><span class="sxs-lookup"><span data-stu-id="af1f6-109">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="af1f6-110">X</span><span class="sxs-lookup"><span data-stu-id="af1f6-110">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="af1f6-111">Coordonnée  *x*  du sommet de fin d’une courbe de Bézier cubique par rapport à la largeur de la forme.</span><span class="sxs-lookup"><span data-stu-id="af1f6-111">The  *x*  -coordinate of the ending vertex of a cubic Bézier curve relative to the width of the shape.</span></span>  <br/> |
|[<span data-ttu-id="af1f6-112">Y</span><span class="sxs-lookup"><span data-stu-id="af1f6-112">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="af1f6-113">Coordonnée  *y*  du sommet de fin d’une courbe de Bézier cubique par rapport à la hauteur de la forme.</span><span class="sxs-lookup"><span data-stu-id="af1f6-113">The  *y*  -coordinate of the ending vertex of a cubic Bézier curve relative to the height of the shape.</span></span>  <br/> |
|[<span data-ttu-id="af1f6-114">A</span><span class="sxs-lookup"><span data-stu-id="af1f6-114">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="af1f6-115">Coordonnée  *x*  du point de contrôle de début de la courbe par rapport à la largeur de la forme ; point sur l’arc. Le point de contrôle est mieux situé entre les vertex de début et de fin de l’arc.</span><span class="sxs-lookup"><span data-stu-id="af1f6-115">The  *x*  -coordinate of the curve's beginning control point relative to the shape's width; a point on the arc. The control point is best located between the beginning and ending vertices of the arc.</span></span>  <br/> |
|[<span data-ttu-id="af1f6-116">B</span><span class="sxs-lookup"><span data-stu-id="af1f6-116">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="af1f6-117">Coordonnée  *y*  du point de contrôle de début d’une courbe par rapport à la hauteur de la forme.</span><span class="sxs-lookup"><span data-stu-id="af1f6-117">The  *y*  -coordinate of a curve's beginning control point relative to the shape's height.</span></span>  <br/> |
|[<span data-ttu-id="af1f6-118">C</span><span class="sxs-lookup"><span data-stu-id="af1f6-118">C</span></span>](c-cell-geometry-section.md) <br/> |<span data-ttu-id="af1f6-119">Coordonnée  *x*  du point de contrôle de fin de la courbe par rapport à la largeur de la forme ; point sur l’arc. Le point de contrôle est mieux situé entre le point de contrôle de début et les vertex de fin de l’arc.</span><span class="sxs-lookup"><span data-stu-id="af1f6-119">The  *x*  -coordinate of the curve's ending control point relative to the shape's width; a point on the arc. The control point is best located between the beginning control point and ending vertices of the arc.</span></span>  <br/> |
|[<span data-ttu-id="af1f6-120">D</span><span class="sxs-lookup"><span data-stu-id="af1f6-120">D</span></span>](d-cell-geometry-section.md) <br/> |<span data-ttu-id="af1f6-121">Coordonnée  *y*  du point de contrôle de fin d’une courbe par rapport à la hauteur de la forme.</span><span class="sxs-lookup"><span data-stu-id="af1f6-121">The  *y*  -coordinate of a curve's ending control point relative to the shape's height.</span></span>  <br/> |
   

