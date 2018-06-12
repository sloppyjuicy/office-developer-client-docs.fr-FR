---
title: PageLeftMargin, cellule (section Print Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60061
localization_priority: Normal
ms.assetid: 7ecdfc37-c9d4-2fde-ed3e-be81657c24e2
description: Indique la marge de gauche de la page d'impression.
ms.openlocfilehash: 5fd2c8cd5b18a4baedd355627005b7c5c2df3252
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789199"
---
# <a name="pageleftmargin-cell-print-properties-section"></a><span data-ttu-id="19ffe-103">PageLeftMargin, cellule (section Print Properties)</span><span class="sxs-lookup"><span data-stu-id="19ffe-103">PageLeftMargin Cell (Print Properties Section)</span></span>

<span data-ttu-id="19ffe-104">Indique la marge de gauche de la page d'impression.</span><span class="sxs-lookup"><span data-stu-id="19ffe-104">Specifies the margin on the left of the printed page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="19ffe-105">Note</span><span class="sxs-lookup"><span data-stu-id="19ffe-105">Remarks</span></span>

<span data-ttu-id="19ffe-p101">Cette valeur représente des unités physiques et n'est pas affectée par les unités d'échelle ou de dessin. Par exemple, si cette cellule a une valeur de 6,35 mm, la marge est de 6,35 mm, même si les unités de page sont des cm. Si les unités ne sont pas explicitement mentionnées, cette valeur s'exprime par défaut en unités de page.</span><span class="sxs-lookup"><span data-stu-id="19ffe-p101">This value represents physical units and is unaffected by scale or drawing units. For example, if this cell has a value of 0.25 in., this margin is 0.25 inch even if page units are feet. If units are not explicitly stated, this value defaults to page units.</span></span> 
  
<span data-ttu-id="19ffe-109">Pour obtenir une référence à la cellule PageLeftMargin par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="19ffe-109">To get a reference to the PageLeftMargin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="19ffe-110">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="19ffe-110">Cell name:</span></span>  <br/> | <span data-ttu-id="19ffe-111">PageLeftMargin</span><span class="sxs-lookup"><span data-stu-id="19ffe-111">PageLeftMargin</span></span>  <br/> |
   
<span data-ttu-id="19ffe-112">Pour obtenir une référence à la cellule PageLeftMargin par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="19ffe-112">To get a reference to the PageLeftMargin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="19ffe-113">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="19ffe-113">Section index:</span></span>  <br/> |<span data-ttu-id="19ffe-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="19ffe-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="19ffe-115">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="19ffe-115">Row index:</span></span>  <br/> |<span data-ttu-id="19ffe-116">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="19ffe-116">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="19ffe-117">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="19ffe-117">Cell index:</span></span>  <br/> |<span data-ttu-id="19ffe-118">**visPrintPropertiesLeftMargin**</span><span class="sxs-lookup"><span data-stu-id="19ffe-118">**visPrintPropertiesLeftMargin**</span></span> <br/> |
   

