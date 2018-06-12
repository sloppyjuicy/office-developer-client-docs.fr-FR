---
title: IndLeft, cellule (section Paragraph)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251255
localization_priority: Normal
ms.assetid: 31a7d0d4-4666-ddef-c5eb-4d13803e6a2f
description: "Représente la distance entre chaque ligne du paragraphe et la marge gauche du bloc de texte. Cette valeur est indépendante de l'échelle de dessin : elle ne change pas si le dessin est mis à l'échelle."
ms.openlocfilehash: 2ccccfdeacc73539c612790613c7eca85de55b34
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788824"
---
# <a name="indleft-cell-paragraph-section"></a><span data-ttu-id="10399-105">IndLeft, cellule (section Paragraph)</span><span class="sxs-lookup"><span data-stu-id="10399-105">IndLeft Cell (Paragraph Section)</span></span>

<span data-ttu-id="10399-p102">Représente la distance entre chaque ligne du paragraphe et la marge gauche du bloc de texte. Cette valeur est indépendante de l'échelle de dessin : elle ne change pas si le dessin est mis à l'échelle.</span><span class="sxs-lookup"><span data-stu-id="10399-p102">Represents the distance all lines of text in a paragraph are indented from the left margin of the text block. This value is independent of the scale of the drawing. If the drawing is scaled, the left indent remains the same.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="10399-109">Note</span><span class="sxs-lookup"><span data-stu-id="10399-109">Remarks</span></span>

<span data-ttu-id="10399-110">Pour obtenir une référence à la cellule IndLeft par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="10399-110">To get a reference to the IndLeft cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="10399-111">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="10399-111">Cell name:</span></span>  <br/> | <span data-ttu-id="10399-112">Para.IndLeft [ *i* ] où *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="10399-112">Para.IndLeft[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="10399-113">Pour obtenir une référence à la cellule IndLeft par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="10399-113">To get a reference to the IndLeft cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="10399-114">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="10399-114">Section index:</span></span>  <br/> |<span data-ttu-id="10399-115">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="10399-115">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="10399-116">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="10399-116">Row index:</span></span>  <br/> |<span data-ttu-id="10399-117">**visRowParagraph** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="10399-117">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="10399-118">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="10399-118">Cell index:</span></span>  <br/> |<span data-ttu-id="10399-119">**visIndentLeft**</span><span class="sxs-lookup"><span data-stu-id="10399-119">**visIndentLeft**</span></span> <br/> |
   

