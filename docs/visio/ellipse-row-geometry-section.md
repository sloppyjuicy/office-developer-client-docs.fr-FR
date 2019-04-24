---
title: Ellipse, ligne (section Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm3010
localization_priority: Normal
ms.assetid: 183fb303-4acb-a486-7b97-f11f7ae3978f
description: Contient les coordonnées x et y du centre de l'ellipse et de deux points sur l'ellipse.
ms.openlocfilehash: 5121ba0c7bf97eaeaaf8a438dd40eccddada4362
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345681"
---
# <a name="ellipse-row-geometry-section"></a><span data-ttu-id="2e500-103">Ellipse Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="2e500-103">Ellipse Row (Geometry Section)</span></span>

<span data-ttu-id="2e500-104">Contient les coordonnées *x* et *y* du centre de l'ellipse et de deux points sur l'ellipse.</span><span class="sxs-lookup"><span data-stu-id="2e500-104">Contains the  *x*  - and  *y*  -coordinates of the ellipse's center point and two points on the ellipse.</span></span> 
  
<span data-ttu-id="2e500-105">Une ligne Ellipse contient les cellules suivantes.</span><span class="sxs-lookup"><span data-stu-id="2e500-105">An Ellipse row contains the following cells.</span></span>
  
|<span data-ttu-id="2e500-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="2e500-106">**Cell**</span></span>|<span data-ttu-id="2e500-107">**Description**</span><span class="sxs-lookup"><span data-stu-id="2e500-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2e500-108">X</span><span class="sxs-lookup"><span data-stu-id="2e500-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="2e500-109">Coordonnée *x* du point central.</span><span class="sxs-lookup"><span data-stu-id="2e500-109">The  *x*  -coordinate of the center point.</span></span>  <br/> |
|[<span data-ttu-id="2e500-110">Y</span><span class="sxs-lookup"><span data-stu-id="2e500-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="2e500-111">Coordonnée *y* du point central.</span><span class="sxs-lookup"><span data-stu-id="2e500-111">The  *y*  -coordinate of the center point.</span></span>  <br/> |
|[<span data-ttu-id="2e500-112">A</span><span class="sxs-lookup"><span data-stu-id="2e500-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="2e500-113">Coordonnée x d'un point sur l'ellipse; associée à la coordonnée *y* représentée par la cellule B.</span><span class="sxs-lookup"><span data-stu-id="2e500-113">The x-coordinate of one point on the ellipse; paired with  *y*  -coordinate represented by the B cell.</span></span>  <br/> |
|[<span data-ttu-id="2e500-114">Point</span><span class="sxs-lookup"><span data-stu-id="2e500-114">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="2e500-115">Coordonnée *y* d'un point sur l'ellipse; associée à la coordonnée x représentée par la cellule A.</span><span class="sxs-lookup"><span data-stu-id="2e500-115">The  *y*  -coordinate of one point on the ellipse; paired with x-coordinate represented by the A cell.</span></span>  <br/> |
|[<span data-ttu-id="2e500-116">C</span><span class="sxs-lookup"><span data-stu-id="2e500-116">C</span></span>](c-cell-geometry-section.md) <br/> |<span data-ttu-id="2e500-117">Coordonnée *x* d'un autre point sur l'ellipse; associée à la coordonnée *y* représentée par la cellule D.</span><span class="sxs-lookup"><span data-stu-id="2e500-117">The  *x*  -coordinate of another point on the ellipse; paired with  *y*  -coordinate represented by the D cell.</span></span>  <br/> |
|[<span data-ttu-id="2e500-118">D</span><span class="sxs-lookup"><span data-stu-id="2e500-118">D</span></span>](d-cell-geometry-section.md) <br/> |<span data-ttu-id="2e500-119">Coordonnée *y* d'un autre point sur l'ellipse; associée à la coordonnée *y* représentée par la cellule C.</span><span class="sxs-lookup"><span data-stu-id="2e500-119">The  *y*  -coordinate of another point on the ellipse; paired with  *y*  -coordinate represented by the C cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2e500-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="2e500-120">Remarks</span></span>

<span data-ttu-id="2e500-121">Une section Geometry contenant une ligne Ellipse ou InfiniteLine ne doit pas contenir d'autres lignes.</span><span class="sxs-lookup"><span data-stu-id="2e500-121">A geometry section that contains an Ellipse or an InfiniteLine row should not contain any other rows.</span></span>
  

