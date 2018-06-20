---
title: RelQuadBezTo, ligne (Section Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ae57707-5a50-43f0-8c78-516790b5034e
description: Contient x - et y - coordonnées du point de terminaison d’une courbe de Bézier par rapport à la largeur de la forme et la hauteur et le x - et y-coordonnées du point de contrôle de la largeur et la hauteur de la forme relative courbe.
ms.openlocfilehash: 99796e85a857fd320598cb48993fc29bdfa4964d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789477"
---
# <a name="relquadbezto-row-geometry-section"></a><span data-ttu-id="b0463-103">RelQuadBezTo, ligne (Section Geometry)</span><span class="sxs-lookup"><span data-stu-id="b0463-103">RelQuadBezTo Row (Geometry Section)</span></span>

<span data-ttu-id="b0463-104">Contient *x* - et *y* - coordonnées du point de terminaison d’une courbe de Bézier par rapport à la largeur de la forme et la hauteur et le *x* - et *y* -coordonnées du point de contrôle de la largeur et la hauteur de la forme relative courbe.</span><span class="sxs-lookup"><span data-stu-id="b0463-104">Contains the  *x*  - and  *y*  -coordinates of the endpoint of a quadratic Bézier curve relative to the shape's width and height and the  *x*  - and  *y*  -coordinates of the control point of the curve relative shape's width and height.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="b0463-105">Une ligne **RelQuadBezTo** peut uniquement être conservée dans les formats de fichier .vsdx, .vsdm, .vstx, .vstm, .vssx et .vssm.</span><span class="sxs-lookup"><span data-stu-id="b0463-105">A **RelQuadBezTo** row can only be persisted in the .vsdx, .vsdm, .vstx, .vstm, .vssx, and .vssm file formats.</span></span> <span data-ttu-id="b0463-106">Lorsqu’un fichier est enregistré dans les formats de Visio 2003 à 2010, la ligne **RelQuadBezTo** est convertie en une ligne [NURBSTo](nurbsto-row-geometry-section.md) .</span><span class="sxs-lookup"><span data-stu-id="b0463-106">When a file is saved to the Visio 2003-2010 formats, the **RelQuadBezTo** row is converted to a [NURBSTo](nurbsto-row-geometry-section.md) row.</span></span> 
  
<span data-ttu-id="b0463-107">Une ligne **RelQuadBezTo** contient les cellules suivantes.</span><span class="sxs-lookup"><span data-stu-id="b0463-107">A **RelQuadBezTo** row contains the following cells.</span></span> 
  
|<span data-ttu-id="b0463-108">**Cell**</span><span class="sxs-lookup"><span data-stu-id="b0463-108">**Cell**</span></span>|<span data-ttu-id="b0463-109">**Description**</span><span class="sxs-lookup"><span data-stu-id="b0463-109">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b0463-110">X</span><span class="sxs-lookup"><span data-stu-id="b0463-110">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="b0463-111">*X* -coordonnées du sommet de fin d’une courbe de Bézier par rapport à la largeur de la forme.</span><span class="sxs-lookup"><span data-stu-id="b0463-111">The  *x*  -coordinate of the ending vertex of a quadratic Bézier curve relative to the width of the shape.</span></span>  <br/> |
|[<span data-ttu-id="b0463-112">Y</span><span class="sxs-lookup"><span data-stu-id="b0463-112">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="b0463-113">La valeur *y* -coordonnées du sommet de fin d’une courbe de Bézier par rapport à la hauteur de la forme.</span><span class="sxs-lookup"><span data-stu-id="b0463-113">The  *y*  -coordinate of the ending vertex of a quadratic Bézier curve relative to the height of the shape.</span></span>  <br/> |
|[<span data-ttu-id="b0463-114">A</span><span class="sxs-lookup"><span data-stu-id="b0463-114">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="b0463-115">*X* -coordonnées du point de contrôle de la courbe par rapport à la largeur de la forme ; un point sur l’arc. Le point de contrôle se trouve mieux sur à mi-chemin entre le début et fin sommets de l’arc.</span><span class="sxs-lookup"><span data-stu-id="b0463-115">The  *x*  -coordinate of the curve's control point relative to the shape's width; a point on the arc. The control point is best located about halfway between the beginning and ending vertices of the arc.</span></span>  <br/> |
|[<span data-ttu-id="b0463-116">B</span><span class="sxs-lookup"><span data-stu-id="b0463-116">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="b0463-117">La valeur *y* -coordonnées du point de contrôle d’une courbe par rapport à la hauteur de la forme.</span><span class="sxs-lookup"><span data-stu-id="b0463-117">The  *y*  -coordinate of a curve's control point relative to the shape's height.</span></span>  <br/> |
   

