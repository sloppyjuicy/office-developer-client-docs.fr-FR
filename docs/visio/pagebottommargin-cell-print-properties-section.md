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
ms.openlocfilehash: f546d89b8761c6c1b7340af69d2b48f16c180767
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334411"
---
# <a name="pagebottommargin-cell-print-properties-section"></a><span data-ttu-id="16a24-103">PageBottomMargin, cellule (section Print Properties)</span><span class="sxs-lookup"><span data-stu-id="16a24-103">PageBottomMargin Cell (Print Properties Section)</span></span>

<span data-ttu-id="16a24-104">Indique la marge au bas de la page d'impression.</span><span class="sxs-lookup"><span data-stu-id="16a24-104">Specifies the margin at the bottom of the printed page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="16a24-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="16a24-105">Remarks</span></span>

<span data-ttu-id="16a24-p101">Cette valeur représente des unités physiques et n'est pas affectée par les unités d'échelle ou de dessin. Par exemple, si cette cellule a une valeur de 13 mm, la marge est de 13 mm, même si les unités de page sont des cm. Si les unités ne sont pas explicitement mentionnées, cette valeur s'exprime par défaut en unités de page.</span><span class="sxs-lookup"><span data-stu-id="16a24-p101">This value represents physical units and is unaffected by scale or drawing units. For example, if this cell has a value of 0.5 in., this margin is 0.5 inch even if page units are feet. If units are not explicitly stated, this value defaults to page units.</span></span> 
  
<span data-ttu-id="16a24-109">Pour obtenir une référence à la cellule PageBottomMargin par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="16a24-109">To get a reference to the PageBottomMargin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="16a24-110">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="16a24-110">Cell name:</span></span>  <br/> | <span data-ttu-id="16a24-111">PageBottomMargin</span><span class="sxs-lookup"><span data-stu-id="16a24-111">PageBottomMargin</span></span>  <br/> |
   
<span data-ttu-id="16a24-112">Pour obtenir une référence à la cellule PageBottomMargin à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="16a24-112">To get a reference to the PageBottomMargin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="16a24-113">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="16a24-113">Section index:</span></span>  <br/> |<span data-ttu-id="16a24-114">**Définis**</span><span class="sxs-lookup"><span data-stu-id="16a24-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="16a24-115">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="16a24-115">Row index:</span></span>  <br/> |<span data-ttu-id="16a24-116">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="16a24-116">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="16a24-117">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="16a24-117">Cell index:</span></span>  <br/> |<span data-ttu-id="16a24-118">**visPrintPropertiesBottomMargin**</span><span class="sxs-lookup"><span data-stu-id="16a24-118">**visPrintPropertiesBottomMargin**</span></span> <br/> |
   

