---
title: TheText, cellule (section Events)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1005
localization_priority: Normal
ms.assetid: 2d63768e-afdb-4b3f-de49-f9ba69ae5391
description: Cellule d'événement qui est calculée lorsque la composition du texte ou le texte d'une forme change.
ms.openlocfilehash: 6aa5e14f339d0030d8421eaae62b0e481be91fc7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326676"
---
# <a name="thetext-cell-events-section"></a><span data-ttu-id="59d30-103">TheText, cellule (section Events)</span><span class="sxs-lookup"><span data-stu-id="59d30-103">TheText Cell (Events Section)</span></span>

<span data-ttu-id="59d30-104">Cellule d'événement qui est calculée lorsque la composition du texte ou le texte d'une forme change.</span><span class="sxs-lookup"><span data-stu-id="59d30-104">An event cell that is evaluated when a shape's text or text composition changes.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="59d30-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="59d30-105">Remarks</span></span>

<span data-ttu-id="59d30-p101">Les cellules d'événement sont évaluées lorsque l'événement se produit et non lors de la saisie de la formule. La cellule TheText permet de déclencher des recalculs, pour recalculer par exemple la largeur et la hauteur du texte avec les fonctions TEXTWIDTH( ) et TEXTHEIGHT( ).</span><span class="sxs-lookup"><span data-stu-id="59d30-p101">Event cells are evaluated only when the event occurs, not upon formula entry. You can use the TheText cell to trigger recalculations, for example, to recalculate the text width and height with the TEXTWIDTH( ) and TEXTHEIGHT( ) functions.</span></span>
  
<span data-ttu-id="59d30-108">Pour obtenir une référence à la cellule TheText par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="59d30-108">To get a reference to the TheText cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="59d30-109">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="59d30-109">Cell name:</span></span>  <br/> | <span data-ttu-id="59d30-110">TheText</span><span class="sxs-lookup"><span data-stu-id="59d30-110">TheText</span></span>  <br/> |
   
<span data-ttu-id="59d30-111">Pour obtenir une référence à la cellule TheText par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="59d30-111">To get a reference to the TheText cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="59d30-112">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="59d30-112">Section index:</span></span>  <br/> |<span data-ttu-id="59d30-113">**Définis**</span><span class="sxs-lookup"><span data-stu-id="59d30-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="59d30-114">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="59d30-114">Row index:</span></span>  <br/> |<span data-ttu-id="59d30-115">**visRowEvent**</span><span class="sxs-lookup"><span data-stu-id="59d30-115">**visRowEvent**</span></span> <br/> |
| <span data-ttu-id="59d30-116">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="59d30-116">Cell index:</span></span>  <br/> |<span data-ttu-id="59d30-117">**visEvtCellTheText**</span><span class="sxs-lookup"><span data-stu-id="59d30-117">**visEvtCellTheText**</span></span> <br/> |
   

