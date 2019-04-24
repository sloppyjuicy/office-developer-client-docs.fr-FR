---
title: IndFirst, cellule (section Paragraph)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251254
localization_priority: Normal
ms.assetid: 0f2e362a-3ace-787d-6326-b5bf707f0727
description: Représente la distance entre la première ligne de chaque paragraphe du bloc de texte et le retrait gauche du paragraphe. Cette valeur est indépendante de l'échelle de dessin. Elle ne change pas si le dessin est mis à l'échelle.
ms.openlocfilehash: aa6d9fd14a40f4fe6b269d9750f603d8faf1d550
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335356"
---
# <a name="indfirst-cell-paragraph-section"></a><span data-ttu-id="f866a-105">IndFirst, cellule (section Paragraph)</span><span class="sxs-lookup"><span data-stu-id="f866a-105">IndFirst Cell (Paragraph Section)</span></span>

<span data-ttu-id="f866a-p102">Représente la distance entre la première ligne de chaque paragraphe du bloc de texte et le retrait gauche du paragraphe. Cette valeur est indépendante de l'échelle de dessin. Elle ne change pas si le dessin est mis à l'échelle.</span><span class="sxs-lookup"><span data-stu-id="f866a-p102">Represents the distance the first line of each paragraph in the shape's text block is indented from the left indent of the paragraph. This value is independent of the scale of the drawing. If the drawing is scaled, the first line indent remains the same.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f866a-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="f866a-109">Remarks</span></span>

<span data-ttu-id="f866a-110">Pour obtenir une référence à la cellule IndFirst par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="f866a-110">To get a reference to the IndFirst cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f866a-111">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="f866a-111">Cell name:</span></span>  <br/> | <span data-ttu-id="f866a-112">Para. IndFirst [ *i* ] où *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="f866a-112">Para.IndFirst[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="f866a-113">Pour obtenir une référence à la cellule IndFirst à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="f866a-113">To get a reference to the IndFirst cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f866a-114">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="f866a-114">Section index:</span></span>  <br/> |<span data-ttu-id="f866a-115">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="f866a-115">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="f866a-116">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="f866a-116">Row index:</span></span>  <br/> |<span data-ttu-id="f866a-117">**visRowParagraph** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="f866a-117">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="f866a-118">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="f866a-118">Cell index:</span></span>  <br/> |<span data-ttu-id="f866a-119">**visIndentFirst**</span><span class="sxs-lookup"><span data-stu-id="f866a-119">**visIndentFirst**</span></span> <br/> |
   

