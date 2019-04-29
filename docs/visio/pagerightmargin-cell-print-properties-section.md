---
title: PageRightMargin, cellule (section Print Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60062
localization_priority: Normal
ms.assetid: f864c759-ed94-8ab7-d664-cc04b3ed743e
description: Indique la marge de droite de la page d'impression.
ms.openlocfilehash: d30669626fe07379521d61554010ae1bd7b0e83a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33440009"
---
# <a name="pagerightmargin-cell-print-properties-section"></a><span data-ttu-id="326c8-103">PageRightMargin, cellule (section Print Properties)</span><span class="sxs-lookup"><span data-stu-id="326c8-103">PageRightMargin Cell (Print Properties Section)</span></span>

<span data-ttu-id="326c8-104">Indique la marge de droite de la page d'impression.</span><span class="sxs-lookup"><span data-stu-id="326c8-104">Specifies the margin on the right of the printed page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="326c8-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="326c8-105">Remarks</span></span>

<span data-ttu-id="326c8-p101">Cette valeur représente des unités physiques et n'est pas affectée par les unités d'échelle ou de dessin. Par exemple, si cette cellule a une valeur de 6,35 mm, la marge est de 6,35 mm, même si les unités de page sont des cm. Si les unités ne sont pas explicitement mentionnées, cette valeur s'exprime par défaut en unités de page.</span><span class="sxs-lookup"><span data-stu-id="326c8-p101">This value represents physical units and is unaffected by scale or drawing units. For example, if this cell has a value of 0.25 in., this margin is 0.25 inch even if page units are feet. If units are not explicitly stated, this value defaults to page units.</span></span> 
  
<span data-ttu-id="326c8-109">Pour obtenir une référence à la cellule PageRightMargin par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="326c8-109">To get a reference to the PageRightMargin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="326c8-110">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="326c8-110">Cell name:</span></span>  <br/> | <span data-ttu-id="326c8-111">PageRightMargin</span><span class="sxs-lookup"><span data-stu-id="326c8-111">PageRightMargin</span></span>  <br/> |
   
<span data-ttu-id="326c8-112">Pour obtenir une référence à la cellule PageRightMargin à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="326c8-112">To get a reference to the PageRightMargin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="326c8-113">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="326c8-113">Section index:</span></span>  <br/> |<span data-ttu-id="326c8-114">**Définis**</span><span class="sxs-lookup"><span data-stu-id="326c8-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="326c8-115">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="326c8-115">Row index:</span></span>  <br/> |<span data-ttu-id="326c8-116">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="326c8-116">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="326c8-117">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="326c8-117">Cell index:</span></span>  <br/> |<span data-ttu-id="326c8-118">**visPrintPropertiesRightMargin**</span><span class="sxs-lookup"><span data-stu-id="326c8-118">**visPrintPropertiesRightMargin**</span></span> <br/> |
   

