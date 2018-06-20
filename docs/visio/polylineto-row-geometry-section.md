---
title: PolylineTo, ligne (section Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251757
localization_priority: Normal
ms.assetid: b78a993f-4165-438d-39cf-9461b2877f17
description: Contient des x et y-coordonnées du dernier point d’une polyligne et une formule de polyligne.
ms.openlocfilehash: 56cecb2eeaa1702461b1096fe468974f2f0b1f52
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789257"
---
# <a name="polylineto-row-geometry-section"></a><span data-ttu-id="209b6-103">PolylineTo, ligne (section Geometry)</span><span class="sxs-lookup"><span data-stu-id="209b6-103">PolylineTo Row (Geometry Section)</span></span>

<span data-ttu-id="209b6-104">Contient des *x* et *y* -coordonnées du dernier point d’une polyligne et une formule de polyligne.</span><span class="sxs-lookup"><span data-stu-id="209b6-104">Contains  *x*  - and  *y*  -coordinates of the last point of a polyline and a polyline formula.</span></span> 
  
<span data-ttu-id="209b6-105">Une ligne PolylineTo contient les cellules suivantes.</span><span class="sxs-lookup"><span data-stu-id="209b6-105">A PolylineTo row contains the following cells.</span></span>
  
|<span data-ttu-id="209b6-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="209b6-106">**Cell**</span></span>|<span data-ttu-id="209b6-107">**Description**</span><span class="sxs-lookup"><span data-stu-id="209b6-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="209b6-108">X</span><span class="sxs-lookup"><span data-stu-id="209b6-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="209b6-109">*X* -coordonnées du sommet de fin d’une polyligne.</span><span class="sxs-lookup"><span data-stu-id="209b6-109">The  *x*  -coordinate of the ending vertex of a polyline.</span></span>  <br/> |
|[<span data-ttu-id="209b6-110">Y</span><span class="sxs-lookup"><span data-stu-id="209b6-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="209b6-111">La valeur *y* -coordonnées du sommet de fin d’une polyligne.</span><span class="sxs-lookup"><span data-stu-id="209b6-111">The  *y*  -coordinate of the ending vertex of a polyline.</span></span>  <br/> |
|[<span data-ttu-id="209b6-112">A</span><span class="sxs-lookup"><span data-stu-id="209b6-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="209b6-113">Formule de la polyligne.</span><span class="sxs-lookup"><span data-stu-id="209b6-113">The polyline formula.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="209b6-114">Notes</span><span class="sxs-lookup"><span data-stu-id="209b6-114">Remarks</span></span>

<span data-ttu-id="209b6-115">Lignes représentés sous la forme d’une ligne Polyline sont équivalentes aux lignes représentés sous la forme d’une séquence de lignes LineTo, mais une ligne Polyline est plus efficace.</span><span class="sxs-lookup"><span data-stu-id="209b6-115">Lines represented as a Polyline row are equivalent to lines represented as a sequence of LineTo rows, but a Polyline row is more efficient.</span></span> <span data-ttu-id="209b6-116">Vous pouvez modifier une ligne PolylineTo en LineTo afin de pouvoir visualiser facilement la géométrie des formes.</span><span class="sxs-lookup"><span data-stu-id="209b6-116">You can change a PolylineTo row to a LineTo row so you can easily see the shape geometry.</span></span> <span data-ttu-id="209b6-117">Pour ce faire, avec le bouton droit de la ligne PolylineTo, puis cliquez sur **Développer la ligne** dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="209b6-117">To do this, right-click the PolylineTo row, and then click **Expand Row** on the shortcut menu.</span></span> 
  
<span data-ttu-id="209b6-118">Pour modifier un type de ligne à une ligne PolylineTo, avec le bouton droit de la ligne, puis cliquez sur **Modifier le Type de ligne** dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="209b6-118">To change a row type to a PolylineTo row, right-click the row, and then click **Change Row Type** on the shortcut menu.</span></span> 
  

