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
ms.openlocfilehash: 2a942ef3d874b8d1ce2ef85f423c93bc0db33230
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405162"
---
# <a name="indleft-cell-paragraph-section"></a><span data-ttu-id="5808a-105">IndLeft, cellule (section Paragraph)</span><span class="sxs-lookup"><span data-stu-id="5808a-105">IndLeft Cell (Paragraph Section)</span></span>

<span data-ttu-id="5808a-p102">Représente la distance entre chaque ligne du paragraphe et la marge gauche du bloc de texte. Cette valeur est indépendante de l'échelle de dessin : elle ne change pas si le dessin est mis à l'échelle.</span><span class="sxs-lookup"><span data-stu-id="5808a-p102">Represents the distance all lines of text in a paragraph are indented from the left margin of the text block. This value is independent of the scale of the drawing. If the drawing is scaled, the left indent remains the same.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5808a-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="5808a-109">Remarks</span></span>

<span data-ttu-id="5808a-110">Pour obtenir une référence à la cellule IndLeft par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="5808a-110">To get a reference to the IndLeft cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5808a-111">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="5808a-111">Cell name:</span></span>  <br/> | <span data-ttu-id="5808a-112">Para.IndLeft[  *i*  ] où  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="5808a-112">Para.IndLeft[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="5808a-113">Pour obtenir une référence à la cellule IndLeft à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="5808a-113">To get a reference to the IndLeft cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5808a-114">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="5808a-114">Section index:</span></span>  <br/> |<span data-ttu-id="5808a-115">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="5808a-115">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="5808a-116">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="5808a-116">Row index:</span></span>  <br/> |<span data-ttu-id="5808a-117">**visRowParagraph**  +   *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="5808a-117">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="5808a-118">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="5808a-118">Cell index:</span></span>  <br/> |<span data-ttu-id="5808a-119">**visIndentLeft**</span><span class="sxs-lookup"><span data-stu-id="5808a-119">**visIndentLeft**</span></span> <br/> |
   

