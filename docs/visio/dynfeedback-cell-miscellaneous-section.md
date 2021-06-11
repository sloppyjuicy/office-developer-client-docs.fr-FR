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
ms.openlocfilehash: 823b8db4dc6afe94a5fdac1f62aaa48d7e1b0d80
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404798"
---
# <a name="dynfeedback-cell-miscellaneous-section"></a><span data-ttu-id="ff9b3-105">DynFeedback, cellule (section Miscellaneous)</span><span class="sxs-lookup"><span data-stu-id="ff9b3-105">DynFeedback Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="ff9b3-p102">Modifie l'aspect que prend un connecteur lorsqu'il est glissé sur la page de dessin. Lorsque le bouton de la souris est relâché, la forme du connecteur qui en résulte n'est pas affectée par ce paramètre. Ce réglage ne s'applique pas aux connecteurs repositionnables.</span><span class="sxs-lookup"><span data-stu-id="ff9b3-p102">Changes the type of visual feedback provided to users when they drag a connector. When the mouse button is released, the resulting connector shape is not affected by this setting. This setting does not apply to routable connectors.</span></span>
  
|<span data-ttu-id="ff9b3-109">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="ff9b3-109">**Value**</span></span>|<span data-ttu-id="ff9b3-110">**Description**</span><span class="sxs-lookup"><span data-stu-id="ff9b3-110">**Description**</span></span>|<span data-ttu-id="ff9b3-111">**Constante d'automation**</span><span class="sxs-lookup"><span data-stu-id="ff9b3-111">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="ff9b3-112">0</span><span class="sxs-lookup"><span data-stu-id="ff9b3-112">0</span></span>  <br/> | <span data-ttu-id="ff9b3-113">Reste droit (aucune branche)</span><span class="sxs-lookup"><span data-stu-id="ff9b3-113">Remains straight (no legs).</span></span>  <br/> |<span data-ttu-id="ff9b3-114">**visDynFBDefault**</span><span class="sxs-lookup"><span data-stu-id="ff9b3-114">**visDynFBDefault**</span></span> <br/> |
| <span data-ttu-id="ff9b3-115">1</span><span class="sxs-lookup"><span data-stu-id="ff9b3-115">1</span></span>  <br/> | <span data-ttu-id="ff9b3-116">Affiche trois branches lors du déplacement.</span><span class="sxs-lookup"><span data-stu-id="ff9b3-116">Shows three legs when dragged.</span></span>  <br/> |<span data-ttu-id="ff9b3-117">**visDynFBUCon3Leg**</span><span class="sxs-lookup"><span data-stu-id="ff9b3-117">**visDynFBUCon3Leg**</span></span> <br/> |
| <span data-ttu-id="ff9b3-118">2</span><span class="sxs-lookup"><span data-stu-id="ff9b3-118">2</span></span>  <br/> | <span data-ttu-id="ff9b3-119">Affiche cinq branches lors du déplacement.</span><span class="sxs-lookup"><span data-stu-id="ff9b3-119">Shows five legs when dragged.</span></span>  <br/> |<span data-ttu-id="ff9b3-120">**visDynFBUCon5Leg**</span><span class="sxs-lookup"><span data-stu-id="ff9b3-120">**visDynFBUCon5Leg**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ff9b3-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="ff9b3-121">Remarks</span></span>

<span data-ttu-id="ff9b3-122">Pour obtenir une référence à la cellule DynFeedback par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="ff9b3-122">To get a reference to the DynFeedback cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ff9b3-123">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="ff9b3-123">Cell name:</span></span>  <br/> | <span data-ttu-id="ff9b3-124">DynFeedback</span><span class="sxs-lookup"><span data-stu-id="ff9b3-124">DynFeedback</span></span>  <br/> |
   
<span data-ttu-id="ff9b3-125">Pour obtenir une référence à la cellule DynFeedback à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="ff9b3-125">To get a reference to the DynFeedback cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ff9b3-126">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="ff9b3-126">Section index:</span></span>  <br/> |<span data-ttu-id="ff9b3-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ff9b3-127">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="ff9b3-128">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="ff9b3-128">Row index:</span></span>  <br/> |<span data-ttu-id="ff9b3-129">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="ff9b3-129">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="ff9b3-130">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="ff9b3-130">Cell index:</span></span>  <br/> |<span data-ttu-id="ff9b3-131">**visDynFeedback**</span><span class="sxs-lookup"><span data-stu-id="ff9b3-131">**visDynFeedback**</span></span> <br/> |
   

