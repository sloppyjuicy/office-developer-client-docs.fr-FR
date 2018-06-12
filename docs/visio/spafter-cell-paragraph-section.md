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
ms.openlocfilehash: 93db93e58124b5f176fb57f843580eff6a3d4d3e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789819"
---
# <a name="spafter-cell-paragraph-section"></a><span data-ttu-id="ed95a-103">SpAfter, cellule (section Paragraph)</span><span class="sxs-lookup"><span data-stu-id="ed95a-103">SpAfter Cell (Paragraph Section)</span></span>

<span data-ttu-id="ed95a-104">Détermine l'espace inséré après chaque paragraphe dans le bloc de texte de la forme, en plus de l'espace issu de la cellule SpLine et, s'il s'agit du dernier paragraphe d'un bloc, de l'espace défini dans la cellule BottomMargin.</span><span class="sxs-lookup"><span data-stu-id="ed95a-104">Determines the amount of space inserted after each paragraph in the shape's text block, in addition to any space from the SpLine cell and, if it is the last paragraph in a text block, the BottomMargin cell.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ed95a-105">Note</span><span class="sxs-lookup"><span data-stu-id="ed95a-105">Remarks</span></span>

<span data-ttu-id="ed95a-p101">Cette valeur est indépendante de l'échelle du dessin. Si le dessin est mis à l'échelle, le paramètre de l'espace après ne change pas.</span><span class="sxs-lookup"><span data-stu-id="ed95a-p101">This value is independent of the scale of the drawing. If the drawing is scaled, the Space After setting remains the same.</span></span>
  
<span data-ttu-id="ed95a-108">Pour obtenir une référence à la cellule SpAfter par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="ed95a-108">To get a reference to the SpAfter cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ed95a-109">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="ed95a-109">Cell name:</span></span>  <br/> | <span data-ttu-id="ed95a-110">Para.SpAfter [ *i* ] où *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="ed95a-110">Para.SpAfter[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="ed95a-111">Pour obtenir une référence à la cellule SpAfter par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="ed95a-111">To get a reference to the SpAfter cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ed95a-112">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="ed95a-112">Section index:</span></span>  <br/> |<span data-ttu-id="ed95a-113">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="ed95a-113">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="ed95a-114">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="ed95a-114">Row index:</span></span>  <br/> |<span data-ttu-id="ed95a-115">**visRowParagraph** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="ed95a-115">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="ed95a-116">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="ed95a-116">Cell index:</span></span>  <br/> |<span data-ttu-id="ed95a-117">**visSpaceAfter**</span><span class="sxs-lookup"><span data-stu-id="ed95a-117">**visSpaceAfter**</span></span> <br/> |
   

