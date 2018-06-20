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
description: Contient les coordonnées x - et y-coordonnées, la position de l’avant-dernier nœud, la position de la dernière épaisseur, la position du premier nœud, la position de la première épaisseur et la formule d’une courbe B-spline rationnelle (NURBS).
ms.openlocfilehash: d0c10e1da519ac98a582da9214033fb8aad5b53e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789177"
---
# <a name="nurbsto-row-geometry-section"></a><span data-ttu-id="f94f5-103">NURBSTo, ligne (section Geometry)</span><span class="sxs-lookup"><span data-stu-id="f94f5-103">NURBSTo Row (Geometry Section)</span></span>

<span data-ttu-id="f94f5-104">Contient les coordonnées *x* - et *y* -coordonnées, la position de l’avant-dernier nœud, la position de la dernière épaisseur, la position du premier nœud, la position de la première épaisseur et la formule d’une courbe B-spline rationnelle (NURBS).</span><span class="sxs-lookup"><span data-stu-id="f94f5-104">Contains the  *x*  - and  *y*  -coordinates, position of the second to last knot, position of the last weight, position of the first knot, position of the first weight, and the formula for a nonuniform rational B-spline (NURBS).</span></span> 
  
<span data-ttu-id="f94f5-105">Une ligne NURBSTo contient les cellules suivantes.</span><span class="sxs-lookup"><span data-stu-id="f94f5-105">A NURBSTo row contains the following cells.</span></span>
  
|<span data-ttu-id="f94f5-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="f94f5-106">**Cell**</span></span>|<span data-ttu-id="f94f5-107">**Description**</span><span class="sxs-lookup"><span data-stu-id="f94f5-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f94f5-108">X</span><span class="sxs-lookup"><span data-stu-id="f94f5-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="f94f5-109">*X* -coordonnées du dernier point de contrôle d’une courbe NURBS.</span><span class="sxs-lookup"><span data-stu-id="f94f5-109">The  *x*  -coordinate of the last control point of a NURBS.</span></span>  <br/> |
|[<span data-ttu-id="f94f5-110">Y</span><span class="sxs-lookup"><span data-stu-id="f94f5-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="f94f5-111">La valeur *y* -coordonnées du dernier point de contrôle d’une courbe NURBS.</span><span class="sxs-lookup"><span data-stu-id="f94f5-111">The  *y*  -coordinate of the last control point of a NURBS.</span></span>  <br/> |
|[<span data-ttu-id="f94f5-112">A</span><span class="sxs-lookup"><span data-stu-id="f94f5-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="f94f5-113">Avant-dernier nœud de la courbe NURBS.</span><span class="sxs-lookup"><span data-stu-id="f94f5-113">The second to the last knot of the NURBS.</span></span>  <br/> |
|[<span data-ttu-id="f94f5-114">B</span><span class="sxs-lookup"><span data-stu-id="f94f5-114">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="f94f5-115">La dernière épaisseur de la courbe NURBS.</span><span class="sxs-lookup"><span data-stu-id="f94f5-115">The last weight of the NURBS.</span></span>  <br/> |
|[<span data-ttu-id="f94f5-116">C</span><span class="sxs-lookup"><span data-stu-id="f94f5-116">C</span></span>](c-cell-geometry-section.md) <br/> |<span data-ttu-id="f94f5-117">Le premier nœud de la courbe NURBS.</span><span class="sxs-lookup"><span data-stu-id="f94f5-117">The first knot of the NURBS.</span></span>  <br/> |
|[<span data-ttu-id="f94f5-118">D</span><span class="sxs-lookup"><span data-stu-id="f94f5-118">D</span></span>](d-cell-geometry-section.md) <br/> |<span data-ttu-id="f94f5-119">La première épaisseur de la courbe NURBS.</span><span class="sxs-lookup"><span data-stu-id="f94f5-119">The first weight of the NURBS.</span></span>  <br/> |
|[<span data-ttu-id="f94f5-120">E</span><span class="sxs-lookup"><span data-stu-id="f94f5-120">E</span></span>](e-cell-geometry-section.md) <br/> |<span data-ttu-id="f94f5-121">Une formule de courbe NURBS.</span><span class="sxs-lookup"><span data-stu-id="f94f5-121">A NURBS formula.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f94f5-122">Notes</span><span class="sxs-lookup"><span data-stu-id="f94f5-122">Remarks</span></span>

<span data-ttu-id="f94f5-123">NURBS est un moyen pour représenter une courbe mathématique courantes.</span><span class="sxs-lookup"><span data-stu-id="f94f5-123">NURBS is a common way to represent a curve mathematically.</span></span> <span data-ttu-id="f94f5-124">Vous pouvez créer une courbe NURBS avec l’outil **forme libre** .</span><span class="sxs-lookup"><span data-stu-id="f94f5-124">You can create a NURBS with the **Freeform** tool.</span></span> 
  

