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
ms.openlocfilehash: e6529bf41cb8fdd40371d9a663291961626afb56
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335342"
---
# <a name="indright-cell-paragraph-section"></a><span data-ttu-id="99863-105">IndRight, cellule (section Paragraph)</span><span class="sxs-lookup"><span data-stu-id="99863-105">IndRight Cell (Paragraph Section)</span></span>

<span data-ttu-id="99863-p102">Représente la distance entre chaque ligne du paragraphe et la marge droite du bloc de texte. Cette valeur est indépendante de l'échelle de dessin : elle ne change pas si le dessin est mis à l'échelle.</span><span class="sxs-lookup"><span data-stu-id="99863-p102">Represents the distance all lines of text in a paragraph are indented from the right margin of the text block. This value is independent of the scale of the drawing. If the drawing is scaled, the right indent remains the same.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="99863-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="99863-109">Remarks</span></span>

<span data-ttu-id="99863-110">Pour obtenir une référence à la cellule IndRight par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="99863-110">To get a reference to the IndRight cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="99863-111">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="99863-111">Cell name:</span></span>  <br/> | <span data-ttu-id="99863-112">Para. IndRight [ *i* ] où *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="99863-112">Para.IndRight[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="99863-113">Pour obtenir une référence à la cellule IndRight à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="99863-113">To get a reference to the IndRight cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="99863-114">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="99863-114">Section index:</span></span>  <br/> |<span data-ttu-id="99863-115">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="99863-115">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="99863-116">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="99863-116">Row index:</span></span>  <br/> |<span data-ttu-id="99863-117">**visRowParagraph** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="99863-117">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="99863-118">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="99863-118">Cell index:</span></span>  <br/> |<span data-ttu-id="99863-119">**visIndentRight**</span><span class="sxs-lookup"><span data-stu-id="99863-119">**visIndentRight**</span></span> <br/> |
   

