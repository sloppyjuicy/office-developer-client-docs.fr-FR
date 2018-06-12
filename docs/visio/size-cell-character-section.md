---
title: Size, cellule (section Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251252
localization_priority: Normal
ms.assetid: a61b50fe-eacb-b3d4-0e4e-ab3e7c972ee9
description: Détermine la taille de la police figurant dans le bloc de texte d'une forme.
ms.openlocfilehash: f3077441844b859cf224eccc8180d0d56cce851f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789743"
---
# <a name="size-cell-character-section"></a><span data-ttu-id="74c17-103">Size, cellule (section Character)</span><span class="sxs-lookup"><span data-stu-id="74c17-103">Size Cell (Character Section)</span></span>

<span data-ttu-id="74c17-104">Détermine la taille de la police figurant dans le bloc de texte d'une forme.</span><span class="sxs-lookup"><span data-stu-id="74c17-104">Determines the size of the text in the shape's text block.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="74c17-105">Note</span><span class="sxs-lookup"><span data-stu-id="74c17-105">Remarks</span></span>

<span data-ttu-id="74c17-p101">La taille de la police est indépendante de l'échelle du dessin. Si le dessin est mis à l'échelle, la taille de la police ne change pas.</span><span class="sxs-lookup"><span data-stu-id="74c17-p101">The text's size is independent of the scale of the drawing. If the drawing is scaled, the text size remains the same.</span></span>
  
<span data-ttu-id="74c17-108">Pour obtenir une référence à la cellule Size par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="74c17-108">To get a reference to the Size cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="74c17-109">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="74c17-109">Cell name:</span></span>  <br/> | <span data-ttu-id="74c17-110">Char.Size [ *i* ] où *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="74c17-110">Char.Size[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="74c17-111">Pour obtenir une référence à la cellule Size par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="74c17-111">To get a reference to the Size cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="74c17-112">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="74c17-112">Section index:</span></span>  <br/> |<span data-ttu-id="74c17-113">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="74c17-113">**visSectionCharacter**</span></span> <br/> |
| <span data-ttu-id="74c17-114">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="74c17-114">Row index:</span></span>  <br/> |<span data-ttu-id="74c17-115">**visRowCharacter** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="74c17-115">**visRowCharacter** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="74c17-116">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="74c17-116">Cell index:</span></span>  <br/> |<span data-ttu-id="74c17-117">**visCharacterSize**</span><span class="sxs-lookup"><span data-stu-id="74c17-117">**visCharacterSize**</span></span> <br/> |
   

