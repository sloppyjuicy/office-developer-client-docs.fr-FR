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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404714"
---
# <a name="nurbsto-row-geometry-section"></a><span data-ttu-id="e1021-103">NURBSTo, ligne (section Geometry)</span><span class="sxs-lookup"><span data-stu-id="e1021-103">NURBSTo Row (Geometry Section)</span></span>

<span data-ttu-id="e1021-104">Contient les coordonnées *x* et *y* , la position de l'avant-dernier nœud, la position de la dernière épaisseur, la position du premier nœud, la position de la première épaisseur et la formule pour une courbe B-spline rationnelle inuniforme (NURBS).</span><span class="sxs-lookup"><span data-stu-id="e1021-104">Contains the  *x*  - and  *y*  -coordinates, position of the second to last knot, position of the last weight, position of the first knot, position of the first weight, and the formula for a nonuniform rational B-spline (NURBS).</span></span> 
  
<span data-ttu-id="e1021-105">Une ligne NURBSTo contient les cellules suivantes.</span><span class="sxs-lookup"><span data-stu-id="e1021-105">A NURBSTo row contains the following cells.</span></span>
  
|<span data-ttu-id="e1021-106">**Cellule**</span><span class="sxs-lookup"><span data-stu-id="e1021-106">**Cell**</span></span>|<span data-ttu-id="e1021-107">**Description**</span><span class="sxs-lookup"><span data-stu-id="e1021-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e1021-108">X</span><span class="sxs-lookup"><span data-stu-id="e1021-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="e1021-109">Coordonnée *x* du dernier point de contrôle d'une courbe NURBS.</span><span class="sxs-lookup"><span data-stu-id="e1021-109">The  *x*  -coordinate of the last control point of a NURBS.</span></span>  <br/> |
|[<span data-ttu-id="e1021-110">Y</span><span class="sxs-lookup"><span data-stu-id="e1021-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="e1021-111">Coordonnée *y* du dernier point de contrôle d'une courbe NURBS.</span><span class="sxs-lookup"><span data-stu-id="e1021-111">The  *y*  -coordinate of the last control point of a NURBS.</span></span>  <br/> |
|[<span data-ttu-id="e1021-112">A</span><span class="sxs-lookup"><span data-stu-id="e1021-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="e1021-113">Avant-dernier nœud de la courbe NURBS.</span><span class="sxs-lookup"><span data-stu-id="e1021-113">The second to the last knot of the NURBS.</span></span>  <br/> |
|[<span data-ttu-id="e1021-114">Point</span><span class="sxs-lookup"><span data-stu-id="e1021-114">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="e1021-115">La dernière épaisseur de la courbe NURBS.</span><span class="sxs-lookup"><span data-stu-id="e1021-115">The last weight of the NURBS.</span></span>  <br/> |
|[<span data-ttu-id="e1021-116">C</span><span class="sxs-lookup"><span data-stu-id="e1021-116">C</span></span>](c-cell-geometry-section.md) <br/> |<span data-ttu-id="e1021-117">Le premier nœud de la courbe NURBS.</span><span class="sxs-lookup"><span data-stu-id="e1021-117">The first knot of the NURBS.</span></span>  <br/> |
|[<span data-ttu-id="e1021-118">D</span><span class="sxs-lookup"><span data-stu-id="e1021-118">D</span></span>](d-cell-geometry-section.md) <br/> |<span data-ttu-id="e1021-119">La première épaisseur de la courbe NURBS.</span><span class="sxs-lookup"><span data-stu-id="e1021-119">The first weight of the NURBS.</span></span>  <br/> |
|[<span data-ttu-id="e1021-120">E</span><span class="sxs-lookup"><span data-stu-id="e1021-120">E</span></span>](e-cell-geometry-section.md) <br/> |<span data-ttu-id="e1021-121">Une formule de courbe NURBS.</span><span class="sxs-lookup"><span data-stu-id="e1021-121">A NURBS formula.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e1021-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="e1021-122">Remarks</span></span>

<span data-ttu-id="e1021-p101">La courbe NURBS est la méthode habituelle de représentation mathématique d'une courbe. Vous pouvez créer une courbe NURBS à l'aide de l'outil **Dessin à main levée**.</span><span class="sxs-lookup"><span data-stu-id="e1021-p101">NURBS is a common way to represent a curve mathematically. You can create a NURBS with the **Freeform** tool.</span></span> 
  

