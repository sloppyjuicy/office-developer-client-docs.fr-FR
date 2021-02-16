---
title: RelLineTo Row (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a900e174-d26a-4314-ae4f-d89e186350ce
description: Contient les coordonnées x et y du sommet de fin d’un segment de trait droit par rapport à la largeur et à la hauteur d’une forme.
ms.openlocfilehash: 2e85033b4a2e16c2df09b1a09655fcd4b97dd03d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437160"
---
# <a name="rellineto-row-geometry-section"></a><span data-ttu-id="7cc06-103">RelLineTo Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="7cc06-103">RelLineTo Row (Geometry Section)</span></span>

<span data-ttu-id="7cc06-104">Contient  *les coordonnées x*  et  *y*  du sommet de fin d’un segment de trait droit par rapport à la largeur et à la hauteur d’une forme.</span><span class="sxs-lookup"><span data-stu-id="7cc06-104">Contains  *x*  -and  *y*  -coordinates of the ending vertex of a straight line segment relative to a shape's width and height.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="7cc06-105">Une **ligne RelLineTo** ne peut être persistante que dans les formats de fichier .vsdx, .vsdm, .vstx, .vstm, .vssx et .vssm.</span><span class="sxs-lookup"><span data-stu-id="7cc06-105">A **RelLineTo** row can only be persisted in the .vsdx, .vsdm, .vstx, .vstm, .vssx, and .vssm file formats.</span></span> <span data-ttu-id="7cc06-106">Lorsqu’un fichier est enregistré dans les formats Visio 2003-2010, la ligne **RelLineTo** est convertie en ligne [LineTo.](lineto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="7cc06-106">When a file is saved to the Visio 2003-2010 formats, the **RelLineTo** row is converted to a [LineTo](lineto-row-geometry-section.md) row.</span></span> 
  
<span data-ttu-id="7cc06-107">Une **ligne RelLineTo** contient les cellules suivantes.</span><span class="sxs-lookup"><span data-stu-id="7cc06-107">A **RelLineTo** row contains the following cells.</span></span> 
  
|<span data-ttu-id="7cc06-108">**Cell**</span><span class="sxs-lookup"><span data-stu-id="7cc06-108">**Cell**</span></span>|<span data-ttu-id="7cc06-109">**Description**</span><span class="sxs-lookup"><span data-stu-id="7cc06-109">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7cc06-110">X</span><span class="sxs-lookup"><span data-stu-id="7cc06-110">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="7cc06-111">Coordonnée  *x*  du sommet de fin d’un segment de trait droit par rapport à la largeur de la forme.</span><span class="sxs-lookup"><span data-stu-id="7cc06-111">The  *x*  -coordinate of the ending vertex of a straight line segment relative to the shape's width.</span></span>  <br/> |
|[<span data-ttu-id="7cc06-112">Y</span><span class="sxs-lookup"><span data-stu-id="7cc06-112">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="7cc06-113">Coordonnée  *y*  du sommet de fin d’un segment de trait droit par rapport à la hauteur de la forme.</span><span class="sxs-lookup"><span data-stu-id="7cc06-113">The  *y*  -coordinate of the ending vertex of a straight line segment relative to the shape's height.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7cc06-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="7cc06-114">Remarks</span></span>

<span data-ttu-id="7cc06-115">Les valeurs de **la ligne RelLineTo** sont équivalentes aux valeurs d’une ligne [LineTo](lineto-row-geometry-section.md) multipliées par la largeur et la hauteur de la forme.</span><span class="sxs-lookup"><span data-stu-id="7cc06-115">Values in the **RelLineTo** row are equivalent to values in a [LineTo](lineto-row-geometry-section.md) row that are multiplied by the width and height of the shape.</span></span> <span data-ttu-id="7cc06-116">Par exemple : une ligne **RelLineTo** où la valeur de la cellule **X** est « 0 » et la valeur de la cellule **Y** est « 0,5 » peut être remplacée par une ligne **LineTo** où la valeur de la cellule **X** est la formule « Width 0 » et la cellule ***Y*** la formule « Height 0.5 ».</span><span class="sxs-lookup"><span data-stu-id="7cc06-116">For example: a **RelLineTo** row where the value of the **X** cell is "0" and the value of the **Y** cell is "0.5" can be replaced with **LineTo** row where the value of the **X** cell is the formula "Width *0" and the **Y** cell is the formula "Height* 0.5."</span></span> 
  

