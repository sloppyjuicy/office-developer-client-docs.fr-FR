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
ms.openlocfilehash: d33a10220499020ba1a1acedf5782fdb78925c07
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789796"
---
# <a name="spbefore-cell-paragraph-section"></a><span data-ttu-id="983a7-103">SpBefore, cellule (section Paragraph)</span><span class="sxs-lookup"><span data-stu-id="983a7-103">SpBefore Cell (Paragraph Section)</span></span>

<span data-ttu-id="983a7-104">Détermine l'espace inséré avant chaque paragraphe dans le bloc de texte de la forme, en plus de l'espace issu de la cellule SpLine et, s'il s'agit du premier paragraphe d'un bloc, de l'espace défini dans la cellule TopMargin.</span><span class="sxs-lookup"><span data-stu-id="983a7-104">Determines the amount of space inserted before each paragraph in the shape's text block, in addition to any space from the SpLine cell if it is the first paragraph in a text block, the TopMargin cell.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="983a7-105">Note</span><span class="sxs-lookup"><span data-stu-id="983a7-105">Remarks</span></span>

<span data-ttu-id="983a7-p101">Cette valeur est indépendante de l'échelle du dessin. Si le dessin est mis à l'échelle, le paramètre de l'espace avant ne change pas.</span><span class="sxs-lookup"><span data-stu-id="983a7-p101">This value is independent of the scale of the drawing. If the drawing is scaled, the Space Before setting remains the same.</span></span>
  
<span data-ttu-id="983a7-108">Pour obtenir une référence à la cellule SpBefore par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="983a7-108">To get a reference to the SpBefore cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="983a7-109">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="983a7-109">Cell name:</span></span>  <br/> | <span data-ttu-id="983a7-110">Para.SpBefore [ *i* ] où *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="983a7-110">Para.SpBefore[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="983a7-111">Pour obtenir une référence à la cellule SpBefore par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="983a7-111">To get a reference to the SpBefore cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="983a7-112">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="983a7-112">Section index:</span></span>  <br/> |<span data-ttu-id="983a7-113">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="983a7-113">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="983a7-114">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="983a7-114">Row index:</span></span>  <br/> |<span data-ttu-id="983a7-115">**visRowParagraph** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="983a7-115">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="983a7-116">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="983a7-116">Cell index:</span></span>  <br/> |<span data-ttu-id="983a7-117">**visSpaceBefore**</span><span class="sxs-lookup"><span data-stu-id="983a7-117">**visSpaceBefore**</span></span> <br/> |
   

