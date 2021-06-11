---
title: PageTopMargin, cellule (section Print Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033785
localization_priority: Normal
ms.assetid: 2ba0fd22-65a6-6cb6-da00-08f391705544
description: Indique la marge en haut de la page d'impression.
ms.openlocfilehash: ff2bffffed39c5571386e792d2ffc8d20d6b291e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416579"
---
# <a name="pagetopmargin-cell-print-properties-section"></a><span data-ttu-id="1c497-103">PageTopMargin, cellule (section Print Properties)</span><span class="sxs-lookup"><span data-stu-id="1c497-103">PageTopMargin Cell (Print Properties Section)</span></span>

<span data-ttu-id="1c497-104">Indique la marge en haut de la page d'impression.</span><span class="sxs-lookup"><span data-stu-id="1c497-104">Specifies the margin at the top of the printer page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1c497-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="1c497-105">Remarks</span></span>

<span data-ttu-id="1c497-p101">Cette valeur représente des unités physiques et n'est pas affectée par les unités d'échelle ou de dessin. Par exemple, si cette cellule a une valeur de 6,35 mm, la marge est de 6,35 mm, même si les unités de page sont des cm. Si les unités ne sont pas explicitement mentionnées, cette valeur s'exprime par défaut en unités de page.</span><span class="sxs-lookup"><span data-stu-id="1c497-p101">This value represents physical units and is unaffected by scale or drawing units. For example, if this cell has a value of 0.25 in., this margin is 0.25 inch even if page units are feet. If units are not explicitly stated, this value defaults to page units.</span></span> 
  
<span data-ttu-id="1c497-109">Pour obtenir une référence à la cellule PageTopMargin par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="1c497-109">To get a reference to the PageTopMargin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1c497-110">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="1c497-110">Cell name:</span></span>  <br/> | <span data-ttu-id="1c497-111">PageTopMargin</span><span class="sxs-lookup"><span data-stu-id="1c497-111">PageTopMargin</span></span>  <br/> |
   
<span data-ttu-id="1c497-112">Pour obtenir une référence à la cellule PageTopMargin à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="1c497-112">To get a reference to the PageTopMargin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1c497-113">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="1c497-113">Section index:</span></span>  <br/> |<span data-ttu-id="1c497-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="1c497-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="1c497-115">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="1c497-115">Row index:</span></span>  <br/> |<span data-ttu-id="1c497-116">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="1c497-116">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="1c497-117">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="1c497-117">Cell index:</span></span>  <br/> |<span data-ttu-id="1c497-118">**visPrintPropertiesTopMargin**</span><span class="sxs-lookup"><span data-stu-id="1c497-118">**visPrintPropertiesTopMargin**</span></span> <br/> |
   

