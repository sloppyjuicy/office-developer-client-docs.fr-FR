---
title: EllipticalArcTo, ligne (section Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm3015
localization_priority: Normal
ms.assetid: 7ceb30a8-1d05-feff-35d8-08a198784a27
description: Contient des x et y-coordonnées d’un arc elliptique point de terminaison, x et y-coordonnées des points de contrôle sur l’arc, l’angle de la x-axe du grand axe et de rapport entre les axes principaux et secondaires de l’ellipse.
ms.openlocfilehash: 9a356429f14a20b72a8bd55689855e2954d4a807
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788548"
---
# <a name="ellipticalarcto-row-geometry-section"></a><span data-ttu-id="bf04f-103">EllipticalArcTo, ligne (section Geometry)</span><span class="sxs-lookup"><span data-stu-id="bf04f-103">EllipticalArcTo Row (Geometry Section)</span></span>

<span data-ttu-id="bf04f-104">Contient des *x* et *y* - coordonnées du point de terminaison d’un arc elliptique, *x* - et *y* -coordonnées des points de contrôle sur l’arc, l’angle de la *x* -axe du grand axe et de rapport entre l’ellipse et minor axes r.</span><span class="sxs-lookup"><span data-stu-id="bf04f-104">Contains  *x*  - and  *y*  -coordinates of an elliptical arc's endpoint,  *x*  - and  *y*  -coordinates of the control points on the arc, angle from the  *x*  -axis to the ellipse's major axis, and ratio between the ellipse's major and minor axes.</span></span> 
  
<span data-ttu-id="bf04f-105">La ligne EllipticalArcTo contient les cellules suivantes.</span><span class="sxs-lookup"><span data-stu-id="bf04f-105">An EllipticalArcTo row contains the following cells.</span></span>
  
|<span data-ttu-id="bf04f-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="bf04f-106">**Cell**</span></span>|<span data-ttu-id="bf04f-107">**Description**</span><span class="sxs-lookup"><span data-stu-id="bf04f-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bf04f-108">X</span><span class="sxs-lookup"><span data-stu-id="bf04f-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="bf04f-109">*X* -coordonnées du sommet de fin d’un arc.</span><span class="sxs-lookup"><span data-stu-id="bf04f-109">The  *x*  -coordinate of the ending vertex on an arc.</span></span>  <br/> |
|[<span data-ttu-id="bf04f-110">Y</span><span class="sxs-lookup"><span data-stu-id="bf04f-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="bf04f-111">La valeur *y* -coordonnées du sommet de fin d’un arc.</span><span class="sxs-lookup"><span data-stu-id="bf04f-111">The  *y*  -coordinate of the ending vertex on an arc.</span></span>  <br/> |
|[<span data-ttu-id="bf04f-112">A</span><span class="sxs-lookup"><span data-stu-id="bf04f-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="bf04f-113">*X* -coordonnées du point de contrôle de l’arc ; un point sur l’arc. Le point de contrôle se trouve mieux sur à mi-chemin entre le début et fin sommets de l’arc. Sinon, l’arc peut atteindre une taille extrême afin de passer par le point de contrôle, avec des résultats imprévisibles.</span><span class="sxs-lookup"><span data-stu-id="bf04f-113">The  *x*  -coordinate of the arc's control point; a point on the arc. The control point is best located about halfway between the beginning and ending vertices of the arc. Otherwise, the arc may grow to an extreme size in order to pass through the control point, with unpredictable results.</span></span>  <br/> |
|[<span data-ttu-id="bf04f-114">B</span><span class="sxs-lookup"><span data-stu-id="bf04f-114">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="bf04f-115">La valeur *y* -coordonnées du point de contrôle d’un arc.</span><span class="sxs-lookup"><span data-stu-id="bf04f-115">The  *y*  -coordinate of an arc's control point.</span></span>  <br/> |
|[<span data-ttu-id="bf04f-116">C</span><span class="sxs-lookup"><span data-stu-id="bf04f-116">C</span></span>](c-cell-geometry-section.md) <br/> |<span data-ttu-id="bf04f-117">L’angle de l’axe de principal d’un arc par rapport à *x* -axe de son parent.</span><span class="sxs-lookup"><span data-stu-id="bf04f-117">The angle of an arc's major axis relative to the  *x*  -axis of its parent.</span></span>  <br/> |
|[<span data-ttu-id="bf04f-118">D</span><span class="sxs-lookup"><span data-stu-id="bf04f-118">D</span></span>](d-cell-geometry-section.md) <br/> |<span data-ttu-id="bf04f-p101">Rapport entre l'axe majeur de l'arc et son axe mineur. Contrairement à la signification réelle de ces termes, l'axe « majeur » ne doit pas forcément être plus grand que l'axe « mineur ». Ce rapport peut donc être inférieur à 1. Si cette cellule a une valeur inférieure ou égale à 0, ou supérieure à 1000, les résultats sont imprévisibles.</span><span class="sxs-lookup"><span data-stu-id="bf04f-p101">The ratio of an arc's major axis to its minor axis. Despite the usual meaning of these words, the "major" axis does not have to be greater than the "minor" axis, so this ratio does not have to be greater than 1. Setting this cell to a value less than or equal to 0 or greater than 1000 can lead to unpredictable results.</span></span>  <br/> |
   

