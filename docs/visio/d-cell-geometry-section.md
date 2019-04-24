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
ms.openlocfilehash: 1da6ac19e6a50ea87f07bf3e3c9f96378b512ba8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346514"
---
# <a name="d-cell-geometry-section"></a><span data-ttu-id="7872b-104">D, cellule (section Geometry)</span><span class="sxs-lookup"><span data-stu-id="7872b-104">D Cell (Geometry Section)</span></span>

<span data-ttu-id="7872b-105">Représente des informations différentes selon la ligne où elle se trouve.</span><span class="sxs-lookup"><span data-stu-id="7872b-105">Represents different information in different rows.</span></span> <span data-ttu-id="7872b-106">Le tableau ci-dessous décrit la cellule D pour chaque ligne.</span><span class="sxs-lookup"><span data-stu-id="7872b-106">This table describes the D cell based on the row in which it's located.</span></span>
  
|<span data-ttu-id="7872b-107">**Ligne**</span><span class="sxs-lookup"><span data-stu-id="7872b-107">**Row**</span></span>|<span data-ttu-id="7872b-108">**Description**</span><span class="sxs-lookup"><span data-stu-id="7872b-108">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7872b-109">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="7872b-109">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="7872b-p103">Rapport entre l’axe majeur de l’arc et son axe mineur. Contrairement à la signification réelle de ces termes, l’axe « majeur » ne doit pas forcément être plus grand que l’axe « mineur ». Ce rapport peut donc être inférieur à 1. Si cette cellule a une valeur inférieure ou égale à 0, ou supérieure à 1000, les résultats sont imprévisibles.</span><span class="sxs-lookup"><span data-stu-id="7872b-p103">The ratio of an arc's major axis to its minor axis. Despite the usual meaning of these words, the "major" axis does not have to be greater than the "minor" axis, so this ratio does not have to be greater than 1. Setting this cell to a value less than or equal to 0 or greater than 1000 can lead to unpredictable results.</span></span>  <br/> |
|[<span data-ttu-id="7872b-113">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="7872b-113">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="7872b-114">Première épaisseur de la courbe B-spline rationnelle non uniforme (NURBS).</span><span class="sxs-lookup"><span data-stu-id="7872b-114">The first weight of the nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|[<span data-ttu-id="7872b-115">SplineStart</span><span class="sxs-lookup"><span data-stu-id="7872b-115">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> | <span data-ttu-id="7872b-116">Degré d’une spline (entier entre 1 et 25)</span><span class="sxs-lookup"><span data-stu-id="7872b-116">The degree of a spline (an integer from 1 to 25).</span></span>  <br/> |
|[<span data-ttu-id="7872b-117">Sélection</span><span class="sxs-lookup"><span data-stu-id="7872b-117">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="7872b-118">Coordonnée *y* d'un point sur une ellipse; associée à la coordonnée *x* représentée par la cellule [C](c-cell-geometry-section.md) .</span><span class="sxs-lookup"><span data-stu-id="7872b-118">A  *y*  -coordinate of a point on an ellipse; paired with the  *x*  -coordinate represented by the [C](c-cell-geometry-section.md) cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7872b-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="7872b-119">Remarks</span></span>

<span data-ttu-id="7872b-120">Pour obtenir une référence à la cellule D par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="7872b-120">To get a reference to the D cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7872b-121">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="7872b-121">Cell name:</span></span>  <br/> | <span data-ttu-id="7872b-122">Géométrie *i* . D *j* où *i* et *j* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="7872b-122">Geometry  *i*  .D  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="7872b-123">Géométrie *i* . D1 (ligne ellipse) où *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="7872b-123">Geometry  *i*  .D1 (Ellipse row)            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="7872b-124">Pour obtenir une référence à la cellule D à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="7872b-124">To get a reference to the D cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7872b-125">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="7872b-125">Section index:</span></span>  <br/> |<span data-ttu-id="7872b-126">**visSectionFirstComponent** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="7872b-126">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="7872b-127">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="7872b-127">Row index:</span></span>  <br/> |<span data-ttu-id="7872b-128">**visRowVertex** +  *j* où *j* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="7872b-128">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="7872b-129">**visRowVertex** (ligne Ellipse)</span><span class="sxs-lookup"><span data-stu-id="7872b-129">**visRowVertex** (Ellipse row)</span></span>  <br/> |
| <span data-ttu-id="7872b-130">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="7872b-130">Cell index</span></span>  <br/> |<span data-ttu-id="7872b-131">**visAspectRatio** (ligne EllipticalArcTo)</span><span class="sxs-lookup"><span data-stu-id="7872b-131">**visAspectRatio** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="7872b-132">**visNURBSWeightPrev** (ligne NURBSTo)</span><span class="sxs-lookup"><span data-stu-id="7872b-132">**visNURBSWeightPrev** (NURBSTo row)</span></span>  <br/> |
||<span data-ttu-id="7872b-133">**visSplineDegree** (ligne SplineStart)</span><span class="sxs-lookup"><span data-stu-id="7872b-133">**visSplineDegree** (SplineStart row)</span></span>  <br/> |
||<span data-ttu-id="7872b-134">**visEllipseMinorY** (ligne Ellipse)</span><span class="sxs-lookup"><span data-stu-id="7872b-134">**visEllipseMinorY** (Ellipse row)</span></span>  <br/> |
   

