---
title: DynFeedback, cellule (section Miscellaneous)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251317
localization_priority: Normal
ms.assetid: 44017319-7146-3431-e476-fbb1a40341ca
description: Modifie l'aspect que prend un connecteur lorsqu'il est glissé sur la page de dessin. Lorsque le bouton de la souris est relâché, la forme du connecteur qui en résulte n'est pas affectée par ce paramètre. Ce réglage ne s'applique pas aux connecteurs repositionnables.
ms.openlocfilehash: 858d98c8ee55eb49f58bbe98491ddc8752e75504
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788544"
---
# <a name="dynfeedback-cell-miscellaneous-section"></a><span data-ttu-id="024d7-105">DynFeedback, cellule (section Miscellaneous)</span><span class="sxs-lookup"><span data-stu-id="024d7-105">DynFeedback Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="024d7-p102">Modifie l'aspect que prend un connecteur lorsqu'il est glissé sur la page de dessin. Lorsque le bouton de la souris est relâché, la forme du connecteur qui en résulte n'est pas affectée par ce paramètre. Ce réglage ne s'applique pas aux connecteurs repositionnables.</span><span class="sxs-lookup"><span data-stu-id="024d7-p102">Changes the type of visual feedback provided to users when they drag a connector. When the mouse button is released, the resulting connector shape is not affected by this setting. This setting does not apply to routable connectors.</span></span>
  
|<span data-ttu-id="024d7-109">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="024d7-109">**Value**</span></span>|<span data-ttu-id="024d7-110">**Description**</span><span class="sxs-lookup"><span data-stu-id="024d7-110">**Description**</span></span>|<span data-ttu-id="024d7-111">**Constante d’Automation**</span><span class="sxs-lookup"><span data-stu-id="024d7-111">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="024d7-112">0</span><span class="sxs-lookup"><span data-stu-id="024d7-112">0</span></span>  <br/> | <span data-ttu-id="024d7-113">Reste droit (aucune branche)</span><span class="sxs-lookup"><span data-stu-id="024d7-113">Remains straight (no legs).</span></span>  <br/> |<span data-ttu-id="024d7-114">**visDynFBDefault**</span><span class="sxs-lookup"><span data-stu-id="024d7-114">**visDynFBDefault**</span></span> <br/> |
| <span data-ttu-id="024d7-115">1</span><span class="sxs-lookup"><span data-stu-id="024d7-115">1</span></span>  <br/> | <span data-ttu-id="024d7-116">Affiche trois branches lors du déplacement.</span><span class="sxs-lookup"><span data-stu-id="024d7-116">Shows three legs when dragged.</span></span>  <br/> |<span data-ttu-id="024d7-117">**visDynFBUCon3Leg**</span><span class="sxs-lookup"><span data-stu-id="024d7-117">**visDynFBUCon3Leg**</span></span> <br/> |
| <span data-ttu-id="024d7-118">2</span><span class="sxs-lookup"><span data-stu-id="024d7-118">2</span></span>  <br/> | <span data-ttu-id="024d7-119">Affiche cinq branches lors du déplacement.</span><span class="sxs-lookup"><span data-stu-id="024d7-119">Shows five legs when dragged.</span></span>  <br/> |<span data-ttu-id="024d7-120">**visDynFBUCon5Leg**</span><span class="sxs-lookup"><span data-stu-id="024d7-120">**visDynFBUCon5Leg**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="024d7-121">Note</span><span class="sxs-lookup"><span data-stu-id="024d7-121">Remarks</span></span>

<span data-ttu-id="024d7-122">Pour obtenir une référence à la cellule DynFeedback par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="024d7-122">To get a reference to the DynFeedback cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="024d7-123">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="024d7-123">Cell name:</span></span>  <br/> | <span data-ttu-id="024d7-124">DynFeedback</span><span class="sxs-lookup"><span data-stu-id="024d7-124">DynFeedback</span></span>  <br/> |
   
<span data-ttu-id="024d7-125">Pour obtenir une référence à la cellule DynFeedback par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="024d7-125">To get a reference to the DynFeedback cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="024d7-126">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="024d7-126">Section index:</span></span>  <br/> |<span data-ttu-id="024d7-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="024d7-127">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="024d7-128">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="024d7-128">Row index:</span></span>  <br/> |<span data-ttu-id="024d7-129">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="024d7-129">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="024d7-130">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="024d7-130">Cell index:</span></span>  <br/> |<span data-ttu-id="024d7-131">**visDynFeedback**</span><span class="sxs-lookup"><span data-stu-id="024d7-131">**visDynFeedback**</span></span> <br/> |
   

