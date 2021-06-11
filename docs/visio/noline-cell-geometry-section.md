---
title: NoLine, cellule (section Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm715
localization_priority: Normal
ms.assetid: f9624af2-c087-3dde-9140-339c438b3652
description: Détermine si un trait est tracé autour du contour du chemin.
ms.openlocfilehash: ad3744ae8deb4ffb4dd2282e50590439c4b218a4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433751"
---
# <a name="noline-cell-geometry-section"></a><span data-ttu-id="a151e-103">NoLine, cellule (section Geometry)</span><span class="sxs-lookup"><span data-stu-id="a151e-103">NoLine Cell (Geometry Section)</span></span>

<span data-ttu-id="a151e-104">Détermine si un trait est tracé autour du contour du chemin.</span><span class="sxs-lookup"><span data-stu-id="a151e-104">Determines whether a line is drawn around the boundary of the path.</span></span>
  
|<span data-ttu-id="a151e-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="a151e-105">**Value**</span></span>|<span data-ttu-id="a151e-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="a151e-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="a151e-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="a151e-107">TRUE</span></span>  <br/> | <span data-ttu-id="a151e-108">Aucun trait n'est tracé autour du contour du chemin correspondant à la limite d'une région qu'il est possible de remplir.</span><span class="sxs-lookup"><span data-stu-id="a151e-108">A line is not drawn around the boundary of the path that is the boundary of a filled region.</span></span>  <br/> |
| <span data-ttu-id="a151e-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="a151e-109">FALSE</span></span>  <br/> | <span data-ttu-id="a151e-110">Un trait est tracé autour du contour du chemin.</span><span class="sxs-lookup"><span data-stu-id="a151e-110">A line is drawn around the boundary of a path.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a151e-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="a151e-111">Remarks</span></span>

<span data-ttu-id="a151e-p101">Lorsque vous décidez d'utiliser le blanc comme couleur de trait, le trait existe même s'il n'est pas visible sur un arrière-plan blanc. Lorsque vous définissez la valeur de cette cellule comme TRUE, aucun trait n'est tracé.</span><span class="sxs-lookup"><span data-stu-id="a151e-p101">When you change the color of a line to white, the line still exists even though you can't see it on a white background. When you set the value of this cell to TRUE, no line is drawn.</span></span>
  
<span data-ttu-id="a151e-114">Pour obtenir une référence à la cellule NoLine par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="a151e-114">To get a reference to the NoLine cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a151e-115">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="a151e-115">Cell name:</span></span>  <br/> | <span data-ttu-id="a151e-116">Geometry  *i*  . NoLine où  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="a151e-116">Geometry  *i*  .NoLine            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="a151e-117">Pour obtenir une référence à la cellule NoLine à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="a151e-117">To get a reference to the NoLine cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a151e-118">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="a151e-118">Section index:</span></span>  <br/> |<span data-ttu-id="a151e-119">**visSectionFirstComponent**  +   *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="a151e-119">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="a151e-120">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="a151e-120">Row index:</span></span>  <br/> |<span data-ttu-id="a151e-121">**visRowComponent**</span><span class="sxs-lookup"><span data-stu-id="a151e-121">**visRowComponent**</span></span> <br/> |
| <span data-ttu-id="a151e-122">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="a151e-122">Cell index:</span></span>  <br/> |<span data-ttu-id="a151e-123">**visCompNoLine**</span><span class="sxs-lookup"><span data-stu-id="a151e-123">**visCompNoLine**</span></span> <br/> |
   

