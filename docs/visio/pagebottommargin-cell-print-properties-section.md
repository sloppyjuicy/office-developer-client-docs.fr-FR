---
title: PageBottomMargin, cellule (section Print Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60060
localization_priority: Normal
ms.assetid: 7a97e97c-278d-2e1e-6c4f-f5f32e2cdeb0
description: Indique la marge au bas de la page d'impression.
ms.openlocfilehash: fb67cf87f5e50719d24b0f354acc93209eed8811
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789198"
---
# <a name="pagebottommargin-cell-print-properties-section"></a><span data-ttu-id="7f5c8-103">PageBottomMargin, cellule (section Print Properties)</span><span class="sxs-lookup"><span data-stu-id="7f5c8-103">PageBottomMargin Cell (Print Properties Section)</span></span>

<span data-ttu-id="7f5c8-104">Indique la marge au bas de la page d'impression.</span><span class="sxs-lookup"><span data-stu-id="7f5c8-104">Specifies the margin at the bottom of the printed page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7f5c8-105">Note</span><span class="sxs-lookup"><span data-stu-id="7f5c8-105">Remarks</span></span>

<span data-ttu-id="7f5c8-p101">Cette valeur représente des unités physiques et n'est pas affectée par les unités d'échelle ou de dessin. Par exemple, si cette cellule a une valeur de 13 mm, la marge est de 13 mm, même si les unités de page sont des cm. Si les unités ne sont pas explicitement mentionnées, cette valeur s'exprime par défaut en unités de page.</span><span class="sxs-lookup"><span data-stu-id="7f5c8-p101">This value represents physical units and is unaffected by scale or drawing units. For example, if this cell has a value of 0.5 in., this margin is 0.5 inch even if page units are feet. If units are not explicitly stated, this value defaults to page units.</span></span> 
  
<span data-ttu-id="7f5c8-109">Pour obtenir une référence à la cellule PageBottomMargin par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="7f5c8-109">To get a reference to the PageBottomMargin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7f5c8-110">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="7f5c8-110">Cell name:</span></span>  <br/> | <span data-ttu-id="7f5c8-111">PageBottomMargin</span><span class="sxs-lookup"><span data-stu-id="7f5c8-111">PageBottomMargin</span></span>  <br/> |
   
<span data-ttu-id="7f5c8-112">Pour obtenir une référence à la cellule PageBottomMargin par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="7f5c8-112">To get a reference to the PageBottomMargin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7f5c8-113">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="7f5c8-113">Section index:</span></span>  <br/> |<span data-ttu-id="7f5c8-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="7f5c8-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="7f5c8-115">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="7f5c8-115">Row index:</span></span>  <br/> |<span data-ttu-id="7f5c8-116">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="7f5c8-116">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="7f5c8-117">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="7f5c8-117">Cell index:</span></span>  <br/> |<span data-ttu-id="7f5c8-118">**visPrintPropertiesBottomMargin**</span><span class="sxs-lookup"><span data-stu-id="7f5c8-118">**visPrintPropertiesBottomMargin**</span></span> <br/> |
   

