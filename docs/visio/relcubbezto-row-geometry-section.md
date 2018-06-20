---
title: RelCubBezTo, ligne (Section Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 77777dd4-5a2c-4048-9ea4-9bd876862963
description: Contient le x et y - coordonnées du point de terminaison d’une courbe de Bézier cube par rapport à la largeur de la forme et height, x - et y - coordonnées du point de contrôle du début de la largeur de la courbe relative d’une forme et la hauteur et x - et y-coordonnées de le contro l point de fin de la largeur et la hauteur de la forme relative courbe.
ms.openlocfilehash: 918701c19e36753dcbf1a210dda2234d1e540d6d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789429"
---
# <a name="relcubbezto-row-geometry-section"></a><span data-ttu-id="90609-103">RelCubBezTo, ligne (Section Geometry)</span><span class="sxs-lookup"><span data-stu-id="90609-103">RelCubBezTo Row (Geometry Section)</span></span>

<span data-ttu-id="90609-104">Contient *x* - et *y* - coordonnées du point de terminaison d’une courbe de Bézier cube par rapport à la largeur de la forme et height, *x* - et *y* -coordonnées du point de contrôle du début de la largeur et la hauteur de la forme relative courbe et le *x* et *y* -coordonnées du point de contrôle de la fin de la largeur et la hauteur de la forme relative courbe.</span><span class="sxs-lookup"><span data-stu-id="90609-104">Contains the  *x*  - and  *y*  -coordinates of the endpoint of a cubic Bézier curve relative to the shape's width and height, the  *x*  - and  *y*  -coordinates of the control point of the beginning of the curve relative shape's width and height, and the  *x*  - and  *y*  -coordinates of the control point of the ending of the curve relative shape's width and height.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="90609-105">Une ligne **RelCubBezTo** peut uniquement être conservée dans les formats de fichier .vsdx, .vsdm, .vstx, .vstm, .vssx et .vssm.</span><span class="sxs-lookup"><span data-stu-id="90609-105">A **RelCubBezTo** row can only be persisted in the .vsdx, .vsdm, .vstx, .vstm, .vssx, and .vssm file formats.</span></span> <span data-ttu-id="90609-106">Lorsqu’un fichier est enregistré dans les formats de Visio 2003 à 2010, la ligne **RelCubBezTo** est convertie en une ligne [NURBSTo](nurbsto-row-geometry-section.md) .</span><span class="sxs-lookup"><span data-stu-id="90609-106">When a file is saved to the Visio 2003-2010 formats, the **RelCubBezTo** row is converted to a [NURBSTo](nurbsto-row-geometry-section.md) row.</span></span> 
  
<span data-ttu-id="90609-107">Une ligne **RelCubBezTo** contient les cellules suivantes.</span><span class="sxs-lookup"><span data-stu-id="90609-107">A **RelCubBezTo** row contains the following cells.</span></span> 
  
|<span data-ttu-id="90609-108">**Cell**</span><span class="sxs-lookup"><span data-stu-id="90609-108">**Cell**</span></span>|<span data-ttu-id="90609-109">**Description**</span><span class="sxs-lookup"><span data-stu-id="90609-109">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="90609-110">X</span><span class="sxs-lookup"><span data-stu-id="90609-110">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="90609-111">*X* -coordonnées du sommet de fin d’une courbe de Bézier cube par rapport à la largeur de la forme.</span><span class="sxs-lookup"><span data-stu-id="90609-111">The  *x*  -coordinate of the ending vertex of a cubic Bézier curve relative to the width of the shape.</span></span>  <br/> |
|[<span data-ttu-id="90609-112">Y</span><span class="sxs-lookup"><span data-stu-id="90609-112">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="90609-113">La valeur *y* -coordonnées du sommet de fin d’une courbe de Bézier cube par rapport à la hauteur de la forme.</span><span class="sxs-lookup"><span data-stu-id="90609-113">The  *y*  -coordinate of the ending vertex of a cubic Bézier curve relative to the height of the shape.</span></span>  <br/> |
|[<span data-ttu-id="90609-114">A</span><span class="sxs-lookup"><span data-stu-id="90609-114">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="90609-115">*X* -coordonnée de la courbe d’ouverture du point de contrôle par rapport à la largeur de la forme ; un point sur l’arc. Le point de contrôle est mieux situé entre le début et de fin des sommets de l’arc.</span><span class="sxs-lookup"><span data-stu-id="90609-115">The  *x*  -coordinate of the curve's beginning control point relative to the shape's width; a point on the arc. The control point is best located between the beginning and ending vertices of the arc.</span></span>  <br/> |
|[<span data-ttu-id="90609-116">B</span><span class="sxs-lookup"><span data-stu-id="90609-116">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="90609-117">La valeur *y* -coordonnées d’une courbe de début de point de contrôle par rapport à la hauteur de la forme.</span><span class="sxs-lookup"><span data-stu-id="90609-117">The  *y*  -coordinate of a curve's beginning control point relative to the shape's height.</span></span>  <br/> |
|[<span data-ttu-id="90609-118">C</span><span class="sxs-lookup"><span data-stu-id="90609-118">C</span></span>](c-cell-geometry-section.md) <br/> |<span data-ttu-id="90609-119">*X* -coordonnée de la courbe de fin du point de contrôle par rapport à la largeur de la forme ; un point sur l’arc. Le point de contrôle est mieux situé entre les début contrôle point et se terminant sommets de l’arc.</span><span class="sxs-lookup"><span data-stu-id="90609-119">The  *x*  -coordinate of the curve's ending control point relative to the shape's width; a point on the arc. The control point is best located between the beginning control point and ending vertices of the arc.</span></span>  <br/> |
|[<span data-ttu-id="90609-120">D</span><span class="sxs-lookup"><span data-stu-id="90609-120">D</span></span>](d-cell-geometry-section.md) <br/> |<span data-ttu-id="90609-121">La valeur *y* -point de contrôle par rapport à la hauteur de la forme de fin de la coordonnée d’une courbe.</span><span class="sxs-lookup"><span data-stu-id="90609-121">The  *y*  -coordinate of a curve's ending control point relative to the shape's height.</span></span>  <br/> |
   

