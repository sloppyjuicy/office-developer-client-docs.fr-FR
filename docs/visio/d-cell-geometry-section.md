---
title: D, cellule (section Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251753
localization_priority: Normal
ms.assetid: 5f1fdf59-db58-561c-e187-1af72a8b87f2
description: Représente des informations différentes selon la ligne où elle se trouve. Le tableau ci-dessous décrit la cellule D pour chaque ligne.
ms.openlocfilehash: a76093f028986907b58175bc6b8c81a7056cfe07
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542498"
---
# <a name="d-cell-geometry-section"></a><span data-ttu-id="77d5c-104">D, cellule (section Geometry)</span><span class="sxs-lookup"><span data-stu-id="77d5c-104">D Cell (Geometry Section)</span></span>

<span data-ttu-id="77d5c-105">Représente des informations différentes selon la ligne où elle se trouve.</span><span class="sxs-lookup"><span data-stu-id="77d5c-105">Represents different information in different rows.</span></span> <span data-ttu-id="77d5c-106">Le tableau ci-dessous décrit la cellule D pour chaque ligne.</span><span class="sxs-lookup"><span data-stu-id="77d5c-106">This table describes the D cell based on the row in which it's located.</span></span>
  
|<span data-ttu-id="77d5c-107">Ligne</span><span class="sxs-lookup"><span data-stu-id="77d5c-107">Row</span></span>|<span data-ttu-id="77d5c-108">Description</span><span class="sxs-lookup"><span data-stu-id="77d5c-108">Description</span></span>|
|:-----|:-----|
|[<span data-ttu-id="77d5c-109">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="77d5c-109">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="77d5c-p103">Rapport entre l’axe majeur de l’arc et son axe mineur. Contrairement à la signification réelle de ces termes, l’axe « majeur » ne doit pas forcément être plus grand que l’axe « mineur ». Ce rapport peut donc être inférieur à 1. Si cette cellule a une valeur inférieure ou égale à 0, ou supérieure à 1000, les résultats sont imprévisibles.</span><span class="sxs-lookup"><span data-stu-id="77d5c-p103">The ratio of an arc's major axis to its minor axis. Despite the usual meaning of these words, the "major" axis does not have to be greater than the "minor" axis, so this ratio does not have to be greater than 1. Setting this cell to a value less than or equal to 0 or greater than 1000 can lead to unpredictable results.</span></span>  <br/> |
|[<span data-ttu-id="77d5c-113">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="77d5c-113">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="77d5c-114">Première épaisseur de la courbe B-spline rationnelle non uniforme (NURBS).</span><span class="sxs-lookup"><span data-stu-id="77d5c-114">The first weight of the nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|[<span data-ttu-id="77d5c-115">SplineStart</span><span class="sxs-lookup"><span data-stu-id="77d5c-115">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> | <span data-ttu-id="77d5c-116">Degré d’une spline (entier entre 1 et 25)</span><span class="sxs-lookup"><span data-stu-id="77d5c-116">The degree of a spline (an integer from 1 to 25).</span></span>  <br/> |
|[<span data-ttu-id="77d5c-117">Ellipse</span><span class="sxs-lookup"><span data-stu-id="77d5c-117">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="77d5c-118">Coordonnée *y* d’un point sur une ellipse ; couplée à la *coordonnée x* représentée par la cellule [C.](c-cell-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="77d5c-118">A  *y*  -coordinate of a point on an ellipse; paired with the  *x*  -coordinate represented by the [C](c-cell-geometry-section.md) cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="77d5c-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="77d5c-119">Remarks</span></span>

<span data-ttu-id="77d5c-120">Pour obtenir une référence à la cellule D par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="77d5c-120">To get a reference to the D cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="77d5c-121">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="77d5c-121">Cell name:</span></span>  <br/> | <span data-ttu-id="77d5c-122">Geometry  *i*  . D  *j*            où  *i*  et  *j*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="77d5c-122">Geometry  *i*  .D  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="77d5c-123">Geometry  *i*  . D1 (ligne Ellipse) où  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="77d5c-123">Geometry  *i*  .D1 (Ellipse row)            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="77d5c-124">Pour obtenir une référence à la cellule D à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="77d5c-124">To get a reference to the D cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="77d5c-125">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="77d5c-125">Section index:</span></span>  <br/> |<span data-ttu-id="77d5c-126">**visSectionFirstComponent**  +   *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="77d5c-126">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="77d5c-127">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="77d5c-127">Row index:</span></span>  <br/> |<span data-ttu-id="77d5c-128">**visRowVertex**  +   *j* où *j* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="77d5c-128">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="77d5c-129">**visRowVertex** (ligne Ellipse)</span><span class="sxs-lookup"><span data-stu-id="77d5c-129">**visRowVertex** (Ellipse row)</span></span>  <br/> |
| <span data-ttu-id="77d5c-130">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="77d5c-130">Cell index</span></span>  <br/> |<span data-ttu-id="77d5c-131">**visAspectRatio** (ligne EllipticalArcTo)</span><span class="sxs-lookup"><span data-stu-id="77d5c-131">**visAspectRatio** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="77d5c-132">**visNURBSWeightPrev** (ligne NURBSTo)</span><span class="sxs-lookup"><span data-stu-id="77d5c-132">**visNURBSWeightPrev** (NURBSTo row)</span></span>  <br/> |
||<span data-ttu-id="77d5c-133">**visSplineDegree** (ligne SplineStart)</span><span class="sxs-lookup"><span data-stu-id="77d5c-133">**visSplineDegree** (SplineStart row)</span></span>  <br/> |
||<span data-ttu-id="77d5c-134">**visEllipseMinorY** (ligne Ellipse)</span><span class="sxs-lookup"><span data-stu-id="77d5c-134">**visEllipseMinorY** (Ellipse row)</span></span>  <br/> |
   

