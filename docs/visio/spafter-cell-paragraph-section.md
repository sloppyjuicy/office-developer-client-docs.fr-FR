---
title: SpAfter, cellule (section Paragraph)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm960
localization_priority: Normal
ms.assetid: 2dd56ae5-300e-ba09-a73a-83c2b6c2a0ef
description: Détermine l'espace inséré après chaque paragraphe dans le bloc de texte de la forme, en plus de l'espace issu de la cellule SpLine et, s'il s'agit du dernier paragraphe d'un bloc, de l'espace défini dans la cellule BottomMargin.
ms.openlocfilehash: 2b8fe7e2b0df09561d0db4367f917c8f4b71335d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439834"
---
# <a name="spafter-cell-paragraph-section"></a><span data-ttu-id="7f50c-103">SpAfter, cellule (section Paragraph)</span><span class="sxs-lookup"><span data-stu-id="7f50c-103">SpAfter Cell (Paragraph Section)</span></span>

<span data-ttu-id="7f50c-104">Détermine l'espace inséré après chaque paragraphe dans le bloc de texte de la forme, en plus de l'espace issu de la cellule SpLine et, s'il s'agit du dernier paragraphe d'un bloc, de l'espace défini dans la cellule BottomMargin.</span><span class="sxs-lookup"><span data-stu-id="7f50c-104">Determines the amount of space inserted after each paragraph in the shape's text block, in addition to any space from the SpLine cell and, if it is the last paragraph in a text block, the BottomMargin cell.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7f50c-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="7f50c-105">Remarks</span></span>

<span data-ttu-id="7f50c-p101">Cette valeur est indépendante de l'échelle du dessin. Si le dessin est mis à l'échelle, le paramètre de l'espace après ne change pas.</span><span class="sxs-lookup"><span data-stu-id="7f50c-p101">This value is independent of the scale of the drawing. If the drawing is scaled, the Space After setting remains the same.</span></span>
  
<span data-ttu-id="7f50c-108">Pour obtenir une référence à la cellule SpAfter par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="7f50c-108">To get a reference to the SpAfter cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7f50c-109">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="7f50c-109">Cell name:</span></span>  <br/> | <span data-ttu-id="7f50c-110">Para.SpAfter[  *i*  ] où  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="7f50c-110">Para.SpAfter[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="7f50c-111">Pour obtenir une référence à la cellule SpAfter par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="7f50c-111">To get a reference to the SpAfter cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7f50c-112">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="7f50c-112">Section index:</span></span>  <br/> |<span data-ttu-id="7f50c-113">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="7f50c-113">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="7f50c-114">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="7f50c-114">Row index:</span></span>  <br/> |<span data-ttu-id="7f50c-115">**visRowParagraph**  +   *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="7f50c-115">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="7f50c-116">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="7f50c-116">Cell index:</span></span>  <br/> |<span data-ttu-id="7f50c-117">**visSpaceAfter**</span><span class="sxs-lookup"><span data-stu-id="7f50c-117">**visSpaceAfter**</span></span> <br/> |
   

