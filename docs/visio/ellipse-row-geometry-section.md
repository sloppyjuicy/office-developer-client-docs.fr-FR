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
description: Contient les coordonnées x - et y-coordonnées du centre et de deux points sur l’ellipse.
ms.openlocfilehash: 0a2acb0efa20f67d04581f827edbfc4fb4a2d6b0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788546"
---
# <a name="ellipse-row-geometry-section"></a><span data-ttu-id="ca45e-103">Ellipse, ligne (section Geometry)</span><span class="sxs-lookup"><span data-stu-id="ca45e-103">Ellipse Row (Geometry Section)</span></span>

<span data-ttu-id="ca45e-104">Contient les coordonnées *x* - et *y* -coordonnées du centre et de deux points sur l’ellipse.</span><span class="sxs-lookup"><span data-stu-id="ca45e-104">Contains the  *x*  - and  *y*  -coordinates of the ellipse's center point and two points on the ellipse.</span></span> 
  
<span data-ttu-id="ca45e-105">Une ligne Ellipse contient les cellules suivantes.</span><span class="sxs-lookup"><span data-stu-id="ca45e-105">An Ellipse row contains the following cells.</span></span>
  
|<span data-ttu-id="ca45e-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="ca45e-106">**Cell**</span></span>|<span data-ttu-id="ca45e-107">**Description**</span><span class="sxs-lookup"><span data-stu-id="ca45e-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ca45e-108">X</span><span class="sxs-lookup"><span data-stu-id="ca45e-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="ca45e-109">*X* -coordonnées du point central.</span><span class="sxs-lookup"><span data-stu-id="ca45e-109">The  *x*  -coordinate of the center point.</span></span>  <br/> |
|[<span data-ttu-id="ca45e-110">Y</span><span class="sxs-lookup"><span data-stu-id="ca45e-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="ca45e-111">La valeur *y* -coordonnées du point central.</span><span class="sxs-lookup"><span data-stu-id="ca45e-111">The  *y*  -coordinate of the center point.</span></span>  <br/> |
|[<span data-ttu-id="ca45e-112">A</span><span class="sxs-lookup"><span data-stu-id="ca45e-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="ca45e-113">Coordonnée x d’un point sur l’ellipse ; associée à *y* -coordonnée représentée par la cellule B.</span><span class="sxs-lookup"><span data-stu-id="ca45e-113">The x-coordinate of one point on the ellipse; paired with  *y*  -coordinate represented by the B cell.</span></span>  <br/> |
|[<span data-ttu-id="ca45e-114">B</span><span class="sxs-lookup"><span data-stu-id="ca45e-114">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="ca45e-115">La valeur *y* -coordonnées d’un point sur l’ellipse ; associée à la coordonnée x représentée par la cellule A.</span><span class="sxs-lookup"><span data-stu-id="ca45e-115">The  *y*  -coordinate of one point on the ellipse; paired with x-coordinate represented by the A cell.</span></span>  <br/> |
|[<span data-ttu-id="ca45e-116">C</span><span class="sxs-lookup"><span data-stu-id="ca45e-116">C</span></span>](c-cell-geometry-section.md) <br/> |<span data-ttu-id="ca45e-117">*X* -coordonnées d’un autre point sur l’ellipse ; associée à *y* -coordonnée représentée par la cellule D.</span><span class="sxs-lookup"><span data-stu-id="ca45e-117">The  *x*  -coordinate of another point on the ellipse; paired with  *y*  -coordinate represented by the D cell.</span></span>  <br/> |
|[<span data-ttu-id="ca45e-118">D</span><span class="sxs-lookup"><span data-stu-id="ca45e-118">D</span></span>](d-cell-geometry-section.md) <br/> |<span data-ttu-id="ca45e-119">La valeur *y* -coordonnées d’un autre point sur l’ellipse ; associée à *y* -coordonnée représentée par la cellule C.</span><span class="sxs-lookup"><span data-stu-id="ca45e-119">The  *y*  -coordinate of another point on the ellipse; paired with  *y*  -coordinate represented by the C cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ca45e-120">Notes</span><span class="sxs-lookup"><span data-stu-id="ca45e-120">Remarks</span></span>

<span data-ttu-id="ca45e-121">Une section Geometry contenant une ligne Ellipse ou InfiniteLine ne doit pas contenir d'autres lignes.</span><span class="sxs-lookup"><span data-stu-id="ca45e-121">A geometry section that contains an Ellipse or an InfiniteLine row should not contain any other rows.</span></span>
  

