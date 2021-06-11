---
title: RightMargin, cellule (section Text Block Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251266
localization_priority: Normal
ms.assetid: bc8f5469-e79f-4a68-73cb-d11c938353a4
description: Définit la distance séparant le bord droit du bloc de texte du texte qui y figure. La valeur par défaut est 2,54 mm.
ms.openlocfilehash: 7a9d2406792e9e57c6acd0e4291b624633e70dcb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433520"
---
# <a name="rightmargin-cell-text-block-format-section"></a><span data-ttu-id="ee9a8-104">RightMargin, cellule (section Text Block Format)</span><span class="sxs-lookup"><span data-stu-id="ee9a8-104">RightMargin Cell (Text Block Format Section)</span></span>

<span data-ttu-id="ee9a8-p102">Définit la distance séparant le bord droit du bloc de texte du texte qui y figure. La valeur par défaut est 2,54 mm.</span><span class="sxs-lookup"><span data-stu-id="ee9a8-p102">Determines the distance between the right border of the text block and the text it contains. The default is 0.1 inch.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ee9a8-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="ee9a8-107">Remarks</span></span>

<span data-ttu-id="ee9a8-p103">Cette valeur est indépendante de l'échelle du dessin. Si le dessin est mis à l'échelle, la marge droite ne change pas.</span><span class="sxs-lookup"><span data-stu-id="ee9a8-p103">This value is independent of the scale of the drawing. If the drawing is scaled, the right margin remains the same.</span></span>
  
<span data-ttu-id="ee9a8-110">Pour obtenir une référence à la cellule RightMargin par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="ee9a8-110">To get a reference to the RightMargin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ee9a8-111">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="ee9a8-111">Cell name:</span></span>  <br/> | <span data-ttu-id="ee9a8-112">RightMargin</span><span class="sxs-lookup"><span data-stu-id="ee9a8-112">RightMargin</span></span>  <br/> |
   
<span data-ttu-id="ee9a8-113">Pour obtenir une référence à la cellule RightMargin à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="ee9a8-113">To get a reference to the RightMargin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ee9a8-114">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="ee9a8-114">Section index:</span></span>  <br/> |<span data-ttu-id="ee9a8-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ee9a8-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="ee9a8-116">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="ee9a8-116">Row index:</span></span>  <br/> |<span data-ttu-id="ee9a8-117">**visRowText**</span><span class="sxs-lookup"><span data-stu-id="ee9a8-117">**visRowText**</span></span> <br/> |
| <span data-ttu-id="ee9a8-118">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="ee9a8-118">Cell index:</span></span>  <br/> |<span data-ttu-id="ee9a8-119">**visTxtBlkRightMargin**</span><span class="sxs-lookup"><span data-stu-id="ee9a8-119">**visTxtBlkRightMargin**</span></span> <br/> |
   

