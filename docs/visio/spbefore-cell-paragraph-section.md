---
title: SpBefore, cellule (section Paragraph)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm965
localization_priority: Normal
ms.assetid: a7d5b0a1-3657-8211-f0e0-eaed588fa0bc
description: Détermine l'espace inséré avant chaque paragraphe dans le bloc de texte de la forme, en plus de l'espace issu de la cellule SpLine et, s'il s'agit du premier paragraphe d'un bloc, de l'espace défini dans la cellule TopMargin.
ms.openlocfilehash: 9890910a11990bb5be7fe3ee4af95e578c8d9799
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425756"
---
# <a name="spbefore-cell-paragraph-section"></a><span data-ttu-id="e5ff4-103">SpBefore, cellule (section Paragraph)</span><span class="sxs-lookup"><span data-stu-id="e5ff4-103">SpBefore Cell (Paragraph Section)</span></span>

<span data-ttu-id="e5ff4-104">Détermine l'espace inséré avant chaque paragraphe dans le bloc de texte de la forme, en plus de l'espace issu de la cellule SpLine et, s'il s'agit du premier paragraphe d'un bloc, de l'espace défini dans la cellule TopMargin.</span><span class="sxs-lookup"><span data-stu-id="e5ff4-104">Determines the amount of space inserted before each paragraph in the shape's text block, in addition to any space from the SpLine cell if it is the first paragraph in a text block, the TopMargin cell.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e5ff4-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="e5ff4-105">Remarks</span></span>

<span data-ttu-id="e5ff4-p101">Cette valeur est indépendante de l'échelle du dessin. Si le dessin est mis à l'échelle, le paramètre de l'espace avant ne change pas.</span><span class="sxs-lookup"><span data-stu-id="e5ff4-p101">This value is independent of the scale of the drawing. If the drawing is scaled, the Space Before setting remains the same.</span></span>
  
<span data-ttu-id="e5ff4-108">Pour obtenir une référence à la cellule SpBefore par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="e5ff4-108">To get a reference to the SpBefore cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e5ff4-109">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="e5ff4-109">Cell name:</span></span>  <br/> | <span data-ttu-id="e5ff4-110">Para. SpBefore [ *i* ] où *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="e5ff4-110">Para.SpBefore[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="e5ff4-111">Pour obtenir une référence à la cellule SpBefore par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="e5ff4-111">To get a reference to the SpBefore cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e5ff4-112">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="e5ff4-112">Section index:</span></span>  <br/> |<span data-ttu-id="e5ff4-113">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="e5ff4-113">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="e5ff4-114">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="e5ff4-114">Row index:</span></span>  <br/> |<span data-ttu-id="e5ff4-115">**visRowParagraph** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="e5ff4-115">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="e5ff4-116">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="e5ff4-116">Cell index:</span></span>  <br/> |<span data-ttu-id="e5ff4-117">**visSpaceBefore**</span><span class="sxs-lookup"><span data-stu-id="e5ff4-117">**visSpaceBefore**</span></span> <br/> |
   

