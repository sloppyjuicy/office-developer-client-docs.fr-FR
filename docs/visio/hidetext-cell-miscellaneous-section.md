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
ms.openlocfilehash: 3e1be814984ed15247c451f5cd86d0f7a6dba71a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425483"
---
# <a name="hidetext-cell-miscellaneous-section"></a><span data-ttu-id="065a5-104">HideText, cellule (section Miscellaneous)</span><span class="sxs-lookup"><span data-stu-id="065a5-104">HideText Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="065a5-p102">Masque le texte d'une forme. Vous pouvez visualiser le texte, modifier ses propriétés et lui appliquer des styles dans le bloc de texte, mais les modifications n'apparaîtront pas tant que vous ne rétablirez pas la cellule sur FALSE (0).</span><span class="sxs-lookup"><span data-stu-id="065a5-p102">Hides the text for a shape. You can view text, edit properties, and apply styles to the text in the text block, although the changes will not appear until you reset HideText to FALSE (0).</span></span>
  
|<span data-ttu-id="065a5-107">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="065a5-107">**Value**</span></span>|<span data-ttu-id="065a5-108">**Description**</span><span class="sxs-lookup"><span data-stu-id="065a5-108">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="065a5-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="065a5-109">TRUE</span></span>  <br/> | <span data-ttu-id="065a5-110">Le texte est masqué et ne s'imprime pas.</span><span class="sxs-lookup"><span data-stu-id="065a5-110">Text is hidden and does not print.</span></span>  <br/> |
| <span data-ttu-id="065a5-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="065a5-111">FALSE</span></span>  <br/> | <span data-ttu-id="065a5-112">Le texte n'est pas masqué.</span><span class="sxs-lookup"><span data-stu-id="065a5-112">Text is not hidden.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="065a5-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="065a5-113">Remarks</span></span>

<span data-ttu-id="065a5-114">Pour obtenir une référence à la cellule HideText par un nom à partir d’une autre formule ou d’un programme en faisant appel à la **propriété CellsU,** utilisez :</span><span class="sxs-lookup"><span data-stu-id="065a5-114">To get a reference to the HideText cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="065a5-115">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="065a5-115">Cell name:</span></span>  <br/> | <span data-ttu-id="065a5-116">HideText</span><span class="sxs-lookup"><span data-stu-id="065a5-116">HideText</span></span>  <br/> |
   
<span data-ttu-id="065a5-117">Pour obtenir une référence à la cellule HideText à l’aide d’un index à partir d’un programme, utilisez la **propriété CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="065a5-117">To get a reference to the HideText cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="065a5-118">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="065a5-118">Section index:</span></span>  <br/> |<span data-ttu-id="065a5-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="065a5-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="065a5-120">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="065a5-120">Row index:</span></span>  <br/> |<span data-ttu-id="065a5-121">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="065a5-121">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="065a5-122">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="065a5-122">Cell index:</span></span>  <br/> |<span data-ttu-id="065a5-123">**visHideText**</span><span class="sxs-lookup"><span data-stu-id="065a5-123">**visHideText**</span></span> <br/> |
   

