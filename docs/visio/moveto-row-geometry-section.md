---
title: MoveTo, ligne (section Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm3030
localization_priority: Normal
ms.assetid: c5b20257-676c-279d-f730-1b6fbbe98305
description: Contient les coordonnées x - et y - les coordonnées du premier sommet d’une forme ou représente le x - et y-coordonnées du premier sommet après une rupture de chemin d’accès.
ms.openlocfilehash: cee62701074269350ae52c6fa7f7aee5cb612f49
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789155"
---
# <a name="moveto-row-geometry-section"></a><span data-ttu-id="197cf-103">MoveTo, ligne (section Geometry)</span><span class="sxs-lookup"><span data-stu-id="197cf-103">MoveTo Row (Geometry Section)</span></span>

<span data-ttu-id="197cf-104">Contient les coordonnées *x* - et *y* - les coordonnées du premier sommet d’une forme ou représente le *x* - et *y* -coordonnées du premier sommet après une rupture de chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="197cf-104">Contains the  *x*  - and  *y*  -coordinates of the first vertex of a shape, or represents the  *x*  - and  *y*  -coordinates of the first vertex after a break in a path.</span></span> 
  
<span data-ttu-id="197cf-105">Une ligne **MoveTo** contient les cellules suivantes.</span><span class="sxs-lookup"><span data-stu-id="197cf-105">A **MoveTo** row contains the following cells.</span></span> 
  
|<span data-ttu-id="197cf-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="197cf-106">**Cell**</span></span>|<span data-ttu-id="197cf-107">**Description**</span><span class="sxs-lookup"><span data-stu-id="197cf-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="197cf-108">X</span><span class="sxs-lookup"><span data-stu-id="197cf-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="197cf-109">Si la ligne **MoveTo** est la première ligne dans la section, la cellule X représente la *x* -coordonnées du premier sommet d’une forme.</span><span class="sxs-lookup"><span data-stu-id="197cf-109">If the **MoveTo** row is the first row in the section, the X cell represents the  *x*  -coordinate of the first vertex of a shape.</span></span> <span data-ttu-id="197cf-110">Si la ligne **MoveTo** apparaît entre deux lignes, la cellule X représente la *x* -coordonnées du premier sommet après la rupture du chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="197cf-110">If the **MoveTo** row appears between two rows, the X cell represents the  *x*  -coordinate of the first vertex after the break in the path.</span></span>  <br/> |
|[<span data-ttu-id="197cf-111">Y</span><span class="sxs-lookup"><span data-stu-id="197cf-111">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="197cf-112">Si la ligne **MoveTo** est la première ligne dans la section, la cellule Y représente la valeur *y* -coordonnées du premier sommet d’une forme.</span><span class="sxs-lookup"><span data-stu-id="197cf-112">If the **MoveTo** row is the first row in the section, the Y cell represents the  *y*  -coordinate of the first vertex of a shape.</span></span> <span data-ttu-id="197cf-113">Si la ligne **MoveTo** apparaît entre deux lignes, la cellule Y représente la valeur *y* -coordonnées du premier sommet après la rupture du chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="197cf-113">If the **MoveTo** row appears between two rows, the Y cell represents the  *y*  -coordinate of the first vertex after the break in the path.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="197cf-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="197cf-114">Remarks</span></span>

<span data-ttu-id="197cf-115">La ligne **MoveTo** contient les coordonnées *x* - et *y* -coordonnées du premier sommet de la forme si la ligne **MoveTo** est la première ligne dans la section.</span><span class="sxs-lookup"><span data-stu-id="197cf-115">The **MoveTo** row contains the  *x*  - and  *y*  -coordinates of the first vertex for the shape if the **MoveTo** row is the first row in the section.</span></span> <span data-ttu-id="197cf-116">Généralement, il s’agit du premier sommet placé lors de la forme a été dessinée, et il ne correspond pas nécessairement au point de début d’une forme 1D.</span><span class="sxs-lookup"><span data-stu-id="197cf-116">Usually this is the first vertex placed when the shape was drawn, and it does not necessarily correspond to the begin point of a 1-D shape.</span></span> 
  
<span data-ttu-id="197cf-117">Une section geometry doit commencer par un **RelMoveTo** ou une ligne **MoveTo** , mais vous pouvez également utiliser les lignes **MoveTo** et **RelMoveTo** pour représenter un espace dans le traçage du chemin d’accès d’une forme.</span><span class="sxs-lookup"><span data-stu-id="197cf-117">A geometry section must begin with either a **RelMoveTo** or a **MoveTo** row, but you can also use the **MoveTo** and **RelMoveTo** rows to represent a gap in the stroking of a shape's path.</span></span> <span data-ttu-id="197cf-118">Toutefois, lorsque le chemin d’accès est utilisée pour définir la limite d’une zone remplie, cet intervalle est interprétée comme un segment de trait droit.</span><span class="sxs-lookup"><span data-stu-id="197cf-118">However, when the path is used to define the boundary of a filled region, this gap is interpreted as a straight line segment.</span></span> <span data-ttu-id="197cf-119">Pour insérer un espace, insérer une ligne entre deux lignes et changez le type de ligne **MoveTo**.</span><span class="sxs-lookup"><span data-stu-id="197cf-119">To insert such a gap, insert a row between two rows and change the row type to **MoveTo**.</span></span> <span data-ttu-id="197cf-120">Si la ligne **MoveTo** est entre deux lignes, elle contient les coordonnées *x* - et *y* -coordonnées du premier sommet de la ligne après la rupture de chemin d’accès de la forme.</span><span class="sxs-lookup"><span data-stu-id="197cf-120">If the **MoveTo** row is between two rows, it contains the  *x*  - and  *y*  -coordinates of the first vertex of the line after the break in the shape's path.</span></span> 
  

