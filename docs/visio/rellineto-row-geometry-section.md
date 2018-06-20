---
title: RelLineTo, ligne (Section Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a900e174-d26a-4314-ae4f-d89e186350ce
description: Contient x - et y-coordonnées du sommet de fin d’un segment de droite par rapport à la largeur et la hauteur d’une forme.
ms.openlocfilehash: 26cb63ac6cc0708be4e5668174022af63391c129
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789433"
---
# <a name="rellineto-row-geometry-section"></a><span data-ttu-id="67f22-103">RelLineTo, ligne (Section Geometry)</span><span class="sxs-lookup"><span data-stu-id="67f22-103">RelLineTo Row (Geometry Section)</span></span>

<span data-ttu-id="67f22-104">Contient *x* - et *y* -coordonnées du sommet de fin d’un segment de droite par rapport à la largeur et la hauteur d’une forme.</span><span class="sxs-lookup"><span data-stu-id="67f22-104">Contains  *x*  -and  *y*  -coordinates of the ending vertex of a straight line segment relative to a shape's width and height.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="67f22-105">Une ligne **RelLineTo** peut uniquement être conservée dans les formats de fichier .vsdx, .vsdm, .vstx, .vstm, .vssx et .vssm.</span><span class="sxs-lookup"><span data-stu-id="67f22-105">A **RelLineTo** row can only be persisted in the .vsdx, .vsdm, .vstx, .vstm, .vssx, and .vssm file formats.</span></span> <span data-ttu-id="67f22-106">Lorsqu’un fichier est enregistré dans les formats de Visio 2003 à 2010, la ligne **RelLineTo** est convertie en une ligne [LineTo](lineto-row-geometry-section.md) .</span><span class="sxs-lookup"><span data-stu-id="67f22-106">When a file is saved to the Visio 2003-2010 formats, the **RelLineTo** row is converted to a [LineTo](lineto-row-geometry-section.md) row.</span></span> 
  
<span data-ttu-id="67f22-107">Une ligne **RelLineTo** contient les cellules suivantes.</span><span class="sxs-lookup"><span data-stu-id="67f22-107">A **RelLineTo** row contains the following cells.</span></span> 
  
|<span data-ttu-id="67f22-108">**Cell**</span><span class="sxs-lookup"><span data-stu-id="67f22-108">**Cell**</span></span>|<span data-ttu-id="67f22-109">**Description**</span><span class="sxs-lookup"><span data-stu-id="67f22-109">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="67f22-110">X</span><span class="sxs-lookup"><span data-stu-id="67f22-110">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="67f22-111">*X* -coordonnées du sommet de fin d’un segment de droite par rapport à la largeur de la forme.</span><span class="sxs-lookup"><span data-stu-id="67f22-111">The  *x*  -coordinate of the ending vertex of a straight line segment relative to the shape's width.</span></span>  <br/> |
|[<span data-ttu-id="67f22-112">Y</span><span class="sxs-lookup"><span data-stu-id="67f22-112">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="67f22-113">La valeur *y* -coordonnées du sommet de fin d’un segment de droite par rapport à la hauteur de la forme.</span><span class="sxs-lookup"><span data-stu-id="67f22-113">The  *y*  -coordinate of the ending vertex of a straight line segment relative to the shape's height.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="67f22-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="67f22-114">Remarks</span></span>

<span data-ttu-id="67f22-115">Les valeurs dans la ligne **RelLineTo** sont équivalents aux valeurs d’une ligne [LineTo](lineto-row-geometry-section.md) sont multipliées par la largeur et la hauteur de la forme.</span><span class="sxs-lookup"><span data-stu-id="67f22-115">Values in the **RelLineTo** row are equivalent to values in a [LineTo](lineto-row-geometry-section.md) row that are multiplied by the width and height of the shape.</span></span> <span data-ttu-id="67f22-116">Par exemple : une ligne **RelLineTo** où la valeur de la cellule **X** est « 0 » et la valeur de la cellule **Y** est « 0,5 » peut être remplacée par ligne **LineTo** où la valeur de la cellule **X** est la formule « largeur*0" et la cellule **Y** est le formule « hauteur*0,5. »</span><span class="sxs-lookup"><span data-stu-id="67f22-116">For example: a **RelLineTo** row where the value of the **X** cell is "0" and the value of the **Y** cell is "0.5" can be replaced with **LineTo** row where the value of the **X** cell is the formula "Width*0" and the **Y** cell is the formula "Height*0.5."</span></span> 
  

