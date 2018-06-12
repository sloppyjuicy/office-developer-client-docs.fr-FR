---
title: SortKey, cellule (section Actions)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027286
localization_priority: Normal
ms.assetid: c0c4b668-f31b-336f-4434-e94a4804ff7c
description: Numéro qui détermine l’ordre des actions qui apparaissent dans un menu contextuel ou de balise d’action.
ms.openlocfilehash: 5a5db1276d1f2544b5b2b76301c30a2bedd4be63
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789808"
---
# <a name="sortkey-cell-actions-section"></a><span data-ttu-id="2eed7-103">SortKey, cellule (section Actions)</span><span class="sxs-lookup"><span data-stu-id="2eed7-103">SortKey Cell (Actions Section)</span></span>

<span data-ttu-id="2eed7-104">Numéro qui détermine l’ordre des actions qui apparaissent dans un menu contextuel ou de balise d’action.</span><span class="sxs-lookup"><span data-stu-id="2eed7-104">A number that determines the order of actions that appear on a shortcut or action tag menu.</span></span>
  
> [!NOTE]
> <span data-ttu-id="2eed7-105">Dans les versions précédentes de Microsoft Visio, les balises d’action sont appelées « balises actives ».</span><span class="sxs-lookup"><span data-stu-id="2eed7-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="2eed7-106">Notes</span><span class="sxs-lookup"><span data-stu-id="2eed7-106">Remarks</span></span>

<span data-ttu-id="2eed7-p101">Les actions d’un menu contextuel ou de balise d’action y apparaissent triées de la plus basse à la plus élevée, celles avec les numéros les plus bas figurant en haut du menu. Si deux lignes d’action ont la même valeur de cellule SortKey, le classement est déterminé par l’ordre physique des lignes. La valeur par défaut est 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="2eed7-p101">The actions on an action tag or shortcut menu appear on the menu sorted from lowest to highest, with lower numbers appearing at the top of the menu. If two action rows have the same SortKey cell value, the order is determined by physical row order. The default is 0 (zero).</span></span>
  
<span data-ttu-id="2eed7-110">Pour obtenir une référence à la cellule SortKey par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="2eed7-110">To get a reference to the SortKey cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2eed7-111">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="2eed7-111">Cell name:</span></span>  <br/> |<span data-ttu-id="2eed7-112">Actions.</span><span class="sxs-lookup"><span data-stu-id="2eed7-112">Actions.</span></span> <span data-ttu-id="2eed7-113">*nom* . Actions SortKeywhere.</span><span class="sxs-lookup"><span data-stu-id="2eed7-113">*name*  .SortKeywhere Actions.</span></span>  <span data-ttu-id="2eed7-114">*nom* est le nom de la ligne Actions</span><span class="sxs-lookup"><span data-stu-id="2eed7-114">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="2eed7-115">Pour obtenir une référence à la cellule SortKey par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="2eed7-115">To get a reference to the SortKey cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2eed7-116">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="2eed7-116">Section index:</span></span>  <br/> |<span data-ttu-id="2eed7-117">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="2eed7-117">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="2eed7-118">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="2eed7-118">Row index:</span></span>  <br/> |<span data-ttu-id="2eed7-119">**visRowAction** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="2eed7-119">**visRowAction** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="2eed7-120">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="2eed7-120">Cell index:</span></span>  <br/> |<span data-ttu-id="2eed7-121">**visActionSortKey**</span><span class="sxs-lookup"><span data-stu-id="2eed7-121">**visActionSortKey**</span></span> <br/> |
   

