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
ms.openlocfilehash: ed67197e46ee159ba2175b0e86623fe1704992d2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788386"
---
# <a name="d-cell-geometry-section"></a><span data-ttu-id="c6ae7-104">D, cellule (section Geometry)</span><span class="sxs-lookup"><span data-stu-id="c6ae7-104">D Cell (Geometry Section)</span></span>

<span data-ttu-id="c6ae7-p102">Représente des informations différentes selon la ligne où elle se trouve. Le tableau ci-dessous décrit la cellule D pour chaque ligne.</span><span class="sxs-lookup"><span data-stu-id="c6ae7-p102">Represents different information in different rows. This table describes the D cell based on the row in which it's located.</span></span>
  
|<span data-ttu-id="c6ae7-107">**Row**</span><span class="sxs-lookup"><span data-stu-id="c6ae7-107">**Row**</span></span>|<span data-ttu-id="c6ae7-108">**Description**</span><span class="sxs-lookup"><span data-stu-id="c6ae7-108">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c6ae7-109">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="c6ae7-109">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="c6ae7-p103">Rapport entre l'axe majeur de l'arc et son axe mineur. Contrairement à la signification réelle de ces termes, l'axe « majeur » ne doit pas forcément être plus grand que l'axe « mineur ». Ce rapport peut donc être inférieur à 1. Si cette cellule a une valeur inférieure ou égale à 0, ou supérieure à 1000, les résultats sont imprévisibles.</span><span class="sxs-lookup"><span data-stu-id="c6ae7-p103">The ratio of an arc's major axis to its minor axis. Despite the usual meaning of these words, the "major" axis does not have to be greater than the "minor" axis, so this ratio does not have to be greater than 1. Setting this cell to a value less than or equal to 0 or greater than 1000 can lead to unpredictable results.</span></span>  <br/> |
|[<span data-ttu-id="c6ae7-113">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="c6ae7-113">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="c6ae7-114">Première épaisseur de la courbe B-spline rationnelle non uniforme (NURBS).</span><span class="sxs-lookup"><span data-stu-id="c6ae7-114">The first weight of the nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|[<span data-ttu-id="c6ae7-115">SplineStart</span><span class="sxs-lookup"><span data-stu-id="c6ae7-115">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> | <span data-ttu-id="c6ae7-116">Degré d'une spline (entier compris entre 1 et 25).</span><span class="sxs-lookup"><span data-stu-id="c6ae7-116">The degree of a spline (an integer from 1 to 25).</span></span>  <br/> |
|[<span data-ttu-id="c6ae7-117">Ellipse</span><span class="sxs-lookup"><span data-stu-id="c6ae7-117">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="c6ae7-118">*Y* -coordonnées d’un point sur une ellipse ; associée à l' *x* -coordonnée représentée par la cellule [C](c-cell-geometry-section.md) .</span><span class="sxs-lookup"><span data-stu-id="c6ae7-118">A  *y*  -coordinate of a point on an ellipse; paired with the  *x*  -coordinate represented by the [C](c-cell-geometry-section.md) cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c6ae7-119">Note</span><span class="sxs-lookup"><span data-stu-id="c6ae7-119">Remarks</span></span>

<span data-ttu-id="c6ae7-120">Pour obtenir une référence à la cellule D par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="c6ae7-120">To get a reference to the D cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c6ae7-121">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="c6ae7-121">Cell name:</span></span>  <br/> | <span data-ttu-id="c6ae7-122">Géométrie *i* . D *j* où *i* et *j* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="c6ae7-122">Geometry  *i*  .D  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="c6ae7-123">Géométrie *i* . D1 (ligne Ellipse) où *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="c6ae7-123">Geometry  *i*  .D1 (Ellipse row)            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="c6ae7-124">Pour obtenir une référence à la cellule D par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="c6ae7-124">To get a reference to the D cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c6ae7-125">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="c6ae7-125">Section index:</span></span>  <br/> |<span data-ttu-id="c6ae7-126">**visSectionFirstComponent** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="c6ae7-126">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="c6ae7-127">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="c6ae7-127">Row index:</span></span>  <br/> |<span data-ttu-id="c6ae7-128">**visRowVertex** +  *j* où *j* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="c6ae7-128">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="c6ae7-129">**visRowVertex** (Ligne ellipse)</span><span class="sxs-lookup"><span data-stu-id="c6ae7-129">**visRowVertex** (Ellipse row)</span></span>  <br/> |
| <span data-ttu-id="c6ae7-130">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="c6ae7-130">Cell index</span></span>  <br/> |<span data-ttu-id="c6ae7-131">**visAspectRatio** (Ligne EllipticalArcTo)</span><span class="sxs-lookup"><span data-stu-id="c6ae7-131">**visAspectRatio** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="c6ae7-132">**visNURBSWeightPrev** (Ligne NURBSTo)</span><span class="sxs-lookup"><span data-stu-id="c6ae7-132">**visNURBSWeightPrev** (NURBSTo row)</span></span>  <br/> |
||<span data-ttu-id="c6ae7-133">**visSplineDegree** (Ligne SplineStart)</span><span class="sxs-lookup"><span data-stu-id="c6ae7-133">**visSplineDegree** (SplineStart row)</span></span>  <br/> |
||<span data-ttu-id="c6ae7-134">**visEllipseMinorY** (Ligne ellipse)</span><span class="sxs-lookup"><span data-stu-id="c6ae7-134">**visEllipseMinorY** (Ellipse row)</span></span>  <br/> |
   

