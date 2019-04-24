---
title: RelLineTo Row (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a900e174-d26a-4314-ae4f-d89e186350ce
description: Contient les coordonnées x et y du sommet de fin d'un segment de ligne droite en fonction de la largeur et de la hauteur d'une forme.
ms.openlocfilehash: 2e85033b4a2e16c2df09b1a09655fcd4b97dd03d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320068"
---
# <a name="rellineto-row-geometry-section"></a><span data-ttu-id="efc17-103">RelLineTo Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="efc17-103">RelLineTo Row (Geometry Section)</span></span>

<span data-ttu-id="efc17-104">Contient les coordonnées *x* et *y* du sommet de fin d'un segment de ligne droite en fonction de la largeur et de la hauteur d'une forme.</span><span class="sxs-lookup"><span data-stu-id="efc17-104">Contains  *x*  -and  *y*  -coordinates of the ending vertex of a straight line segment relative to a shape's width and height.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="efc17-105">Une ligne **RelLineTo** ne peut être conservée que dans les formats de fichier. vsdx,. VSDM,. vstx,. vstm,. vssx et. VSSM.</span><span class="sxs-lookup"><span data-stu-id="efc17-105">A **RelLineTo** row can only be persisted in the .vsdx, .vsdm, .vstx, .vstm, .vssx, and .vssm file formats.</span></span> <span data-ttu-id="efc17-106">Lorsqu'un fichier est enregistré aux formats Visio 2003-2010, la ligne **RelLineTo** est convertie en une ligne [LineTo](lineto-row-geometry-section.md) .</span><span class="sxs-lookup"><span data-stu-id="efc17-106">When a file is saved to the Visio 2003-2010 formats, the **RelLineTo** row is converted to a [LineTo](lineto-row-geometry-section.md) row.</span></span> 
  
<span data-ttu-id="efc17-107">Une ligne **RelLineTo** contient les cellules suivantes.</span><span class="sxs-lookup"><span data-stu-id="efc17-107">A **RelLineTo** row contains the following cells.</span></span> 
  
|<span data-ttu-id="efc17-108">**Cell**</span><span class="sxs-lookup"><span data-stu-id="efc17-108">**Cell**</span></span>|<span data-ttu-id="efc17-109">**Description**</span><span class="sxs-lookup"><span data-stu-id="efc17-109">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="efc17-110">X</span><span class="sxs-lookup"><span data-stu-id="efc17-110">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="efc17-111">Coordonnée *x* du sommet de fin d'un segment de trait droit par rapport à la largeur de la forme.</span><span class="sxs-lookup"><span data-stu-id="efc17-111">The  *x*  -coordinate of the ending vertex of a straight line segment relative to the shape's width.</span></span>  <br/> |
|[<span data-ttu-id="efc17-112">Y</span><span class="sxs-lookup"><span data-stu-id="efc17-112">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="efc17-113">Coordonnée *y* du sommet de fin d'un segment de trait droit par rapport à la hauteur de la forme.</span><span class="sxs-lookup"><span data-stu-id="efc17-113">The  *y*  -coordinate of the ending vertex of a straight line segment relative to the shape's height.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="efc17-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="efc17-114">Remarks</span></span>

<span data-ttu-id="efc17-115">Les valeurs de la ligne **RelLineTo** sont équivalentes aux valeurs d'une ligne [LineTo](lineto-row-geometry-section.md) qui sont multipliées par la largeur et la hauteur de la forme.</span><span class="sxs-lookup"><span data-stu-id="efc17-115">Values in the **RelLineTo** row are equivalent to values in a [LineTo](lineto-row-geometry-section.md) row that are multiplied by the width and height of the shape.</span></span> <span data-ttu-id="efc17-116">Par exemple: une ligne **RelLineTo** où la valeur de la cellule **x** est «0» et la valeur de la cellule **Y** est «0,5» peut être remplacée par la ligne **LineTo** où la valeur de la cellule **X** est la formule «Width*0» et la cellule **Y** est le formule «hauteur*0,5».</span><span class="sxs-lookup"><span data-stu-id="efc17-116">For example: a **RelLineTo** row where the value of the **X** cell is "0" and the value of the **Y** cell is "0.5" can be replaced with **LineTo** row where the value of the **X** cell is the formula "Width*0" and the **Y** cell is the formula "Height*0.5."</span></span> 
  

