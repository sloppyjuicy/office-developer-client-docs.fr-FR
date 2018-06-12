---
title: HideText, cellule (section Miscellaneous)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251323
localization_priority: Normal
ms.assetid: 3d23647a-e567-da71-50df-336a0f2f4071
description: Masque le texte d'une forme. Vous pouvez visualiser le texte, modifier ses propriétés et lui appliquer des styles dans le bloc de texte, mais les modifications n'apparaîtront pas tant que vous ne rétablirez pas la cellule sur FALSE (0).
ms.openlocfilehash: e2d220e9d7874382f2aaeade5488bd4809f3a9dd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788782"
---
# <a name="hidetext-cell-miscellaneous-section"></a><span data-ttu-id="27c54-104">HideText, cellule (section Miscellaneous)</span><span class="sxs-lookup"><span data-stu-id="27c54-104">HideText Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="27c54-p102">Masque le texte d'une forme. Vous pouvez visualiser le texte, modifier ses propriétés et lui appliquer des styles dans le bloc de texte, mais les modifications n'apparaîtront pas tant que vous ne rétablirez pas la cellule sur FALSE (0).</span><span class="sxs-lookup"><span data-stu-id="27c54-p102">Hides the text for a shape. You can view text, edit properties, and apply styles to the text in the text block, although the changes will not appear until you reset HideText to FALSE (0).</span></span>
  
|<span data-ttu-id="27c54-107">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="27c54-107">**Value**</span></span>|<span data-ttu-id="27c54-108">**Description**</span><span class="sxs-lookup"><span data-stu-id="27c54-108">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="27c54-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="27c54-109">TRUE</span></span>  <br/> | <span data-ttu-id="27c54-110">Le texte est masqué et ne s'imprime pas.</span><span class="sxs-lookup"><span data-stu-id="27c54-110">Text is hidden and does not print.</span></span>  <br/> |
| <span data-ttu-id="27c54-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="27c54-111">FALSE</span></span>  <br/> | <span data-ttu-id="27c54-112">Le texte n'est pas masqué.</span><span class="sxs-lookup"><span data-stu-id="27c54-112">Text is not hidden.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="27c54-113">Note</span><span class="sxs-lookup"><span data-stu-id="27c54-113">Remarks</span></span>

<span data-ttu-id="27c54-114">Pour obtenir une référence à la cellule HideText par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="27c54-114">To get a reference to the HideText cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="27c54-115">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="27c54-115">Cell name:</span></span>  <br/> | <span data-ttu-id="27c54-116">HideText</span><span class="sxs-lookup"><span data-stu-id="27c54-116">HideText</span></span>  <br/> |
   
<span data-ttu-id="27c54-117">Pour obtenir une référence à la cellule HideText par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="27c54-117">To get a reference to the HideText cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="27c54-118">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="27c54-118">Section index:</span></span>  <br/> |<span data-ttu-id="27c54-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="27c54-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="27c54-120">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="27c54-120">Row index:</span></span>  <br/> |<span data-ttu-id="27c54-121">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="27c54-121">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="27c54-122">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="27c54-122">Cell index:</span></span>  <br/> |<span data-ttu-id="27c54-123">**visHideText**</span><span class="sxs-lookup"><span data-stu-id="27c54-123">**visHideText**</span></span> <br/> |
   

