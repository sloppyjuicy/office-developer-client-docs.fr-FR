---
title: NURBSTo, ligne (section Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251758
localization_priority: Normal
ms.assetid: 7e47acfe-5ec0-3689-eb89-0168f596a739
description: Contient les coordonnées x et y, la position de l'avant-dernier nœud, la position de la dernière épaisseur, la position du premier nœud, la position de la première épaisseur et la formule pour une courbe B-spline rationnelle inuniforme (NURBS).
ms.openlocfilehash: a5fc83f9581277580d076c2a850bfe937602aef0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361018"
---
# <a name="nurbsto-row-geometry-section"></a><span data-ttu-id="e4cac-103">NURBSTo, ligne (section Geometry)</span><span class="sxs-lookup"><span data-stu-id="e4cac-103">NURBSTo Row (Geometry Section)</span></span>

<span data-ttu-id="e4cac-104">Contient les coordonnées *x* et *y* , la position de l'avant-dernier nœud, la position de la dernière épaisseur, la position du premier nœud, la position de la première épaisseur et la formule pour une courbe B-spline rationnelle inuniforme (NURBS).</span><span class="sxs-lookup"><span data-stu-id="e4cac-104">Contains the  *x*  - and  *y*  -coordinates, position of the second to last knot, position of the last weight, position of the first knot, position of the first weight, and the formula for a nonuniform rational B-spline (NURBS).</span></span> 
  
<span data-ttu-id="e4cac-105">Une ligne NURBSTo contient les cellules suivantes.</span><span class="sxs-lookup"><span data-stu-id="e4cac-105">A NURBSTo row contains the following cells.</span></span>
  
|<span data-ttu-id="e4cac-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="e4cac-106">**Cell**</span></span>|<span data-ttu-id="e4cac-107">**Description**</span><span class="sxs-lookup"><span data-stu-id="e4cac-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e4cac-108">X</span><span class="sxs-lookup"><span data-stu-id="e4cac-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="e4cac-109">Coordonnée *x* du dernier point de contrôle d'une courbe NURBS.</span><span class="sxs-lookup"><span data-stu-id="e4cac-109">The  *x*  -coordinate of the last control point of a NURBS.</span></span>  <br/> |
|[<span data-ttu-id="e4cac-110">Y</span><span class="sxs-lookup"><span data-stu-id="e4cac-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="e4cac-111">Coordonnée *y* du dernier point de contrôle d'une courbe NURBS.</span><span class="sxs-lookup"><span data-stu-id="e4cac-111">The  *y*  -coordinate of the last control point of a NURBS.</span></span>  <br/> |
|[<span data-ttu-id="e4cac-112">A</span><span class="sxs-lookup"><span data-stu-id="e4cac-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="e4cac-113">Avant-dernier nœud de la courbe NURBS.</span><span class="sxs-lookup"><span data-stu-id="e4cac-113">The second to the last knot of the NURBS.</span></span>  <br/> |
|[<span data-ttu-id="e4cac-114">Point</span><span class="sxs-lookup"><span data-stu-id="e4cac-114">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="e4cac-115">La dernière épaisseur de la courbe NURBS.</span><span class="sxs-lookup"><span data-stu-id="e4cac-115">The last weight of the NURBS.</span></span>  <br/> |
|[<span data-ttu-id="e4cac-116">C</span><span class="sxs-lookup"><span data-stu-id="e4cac-116">C</span></span>](c-cell-geometry-section.md) <br/> |<span data-ttu-id="e4cac-117">Le premier nœud de la courbe NURBS.</span><span class="sxs-lookup"><span data-stu-id="e4cac-117">The first knot of the NURBS.</span></span>  <br/> |
|[<span data-ttu-id="e4cac-118">D</span><span class="sxs-lookup"><span data-stu-id="e4cac-118">D</span></span>](d-cell-geometry-section.md) <br/> |<span data-ttu-id="e4cac-119">La première épaisseur de la courbe NURBS.</span><span class="sxs-lookup"><span data-stu-id="e4cac-119">The first weight of the NURBS.</span></span>  <br/> |
|[<span data-ttu-id="e4cac-120">E</span><span class="sxs-lookup"><span data-stu-id="e4cac-120">E</span></span>](e-cell-geometry-section.md) <br/> |<span data-ttu-id="e4cac-121">Une formule de courbe NURBS.</span><span class="sxs-lookup"><span data-stu-id="e4cac-121">A NURBS formula.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e4cac-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="e4cac-122">Remarks</span></span>

<span data-ttu-id="e4cac-p101">La courbe NURBS est la méthode habituelle de représentation mathématique d'une courbe. Vous pouvez créer une courbe NURBS à l'aide de l'outil **Dessin à main levée**.</span><span class="sxs-lookup"><span data-stu-id="e4cac-p101">NURBS is a common way to represent a curve mathematically. You can create a NURBS with the **Freeform** tool.</span></span> 
  

