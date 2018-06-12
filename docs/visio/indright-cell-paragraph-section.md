---
title: IndRight, cellule (section Paragraph)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251256
localization_priority: Normal
ms.assetid: f0891064-95d9-ae1b-28f3-3aef1406b636
description: "Représente la distance entre chaque ligne du paragraphe et la marge droite du bloc de texte. Cette valeur est indépendante de l'échelle de dessin : elle ne change pas si le dessin est mis à l'échelle."
ms.openlocfilehash: 83f2688e598ffb335a9fafd1eed56ea17ffd4b2f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788826"
---
# <a name="indright-cell-paragraph-section"></a><span data-ttu-id="1299f-105">IndRight, cellule (section Paragraph)</span><span class="sxs-lookup"><span data-stu-id="1299f-105">IndRight Cell (Paragraph Section)</span></span>

<span data-ttu-id="1299f-p102">Représente la distance entre chaque ligne du paragraphe et la marge droite du bloc de texte. Cette valeur est indépendante de l'échelle de dessin : elle ne change pas si le dessin est mis à l'échelle.</span><span class="sxs-lookup"><span data-stu-id="1299f-p102">Represents the distance all lines of text in a paragraph are indented from the right margin of the text block. This value is independent of the scale of the drawing. If the drawing is scaled, the right indent remains the same.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1299f-109">Note</span><span class="sxs-lookup"><span data-stu-id="1299f-109">Remarks</span></span>

<span data-ttu-id="1299f-110">Pour obtenir une référence à la cellule IndRight par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="1299f-110">To get a reference to the IndRight cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1299f-111">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="1299f-111">Cell name:</span></span>  <br/> | <span data-ttu-id="1299f-112">Para.IndRight [ *i* ] où *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="1299f-112">Para.IndRight[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="1299f-113">Pour obtenir une référence à la cellule IndRight par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="1299f-113">To get a reference to the IndRight cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1299f-114">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="1299f-114">Section index:</span></span>  <br/> |<span data-ttu-id="1299f-115">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="1299f-115">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="1299f-116">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="1299f-116">Row index:</span></span>  <br/> |<span data-ttu-id="1299f-117">**visRowParagraph** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="1299f-117">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="1299f-118">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="1299f-118">Cell index:</span></span>  <br/> |<span data-ttu-id="1299f-119">**visIndentRight**</span><span class="sxs-lookup"><span data-stu-id="1299f-119">**visIndentRight**</span></span> <br/> |
   

