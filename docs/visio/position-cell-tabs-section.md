---
title: Position, cellule (section Tabs)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251755
localization_priority: Normal
ms.assetid: 40d7e38e-b3b0-8616-ed27-1f963a841e03
description: Définit la position d'une tabulation. La position de la tabulation est indépendante de l'échelle du dessin. Si le dessin est mis à l'échelle, la position de la tabulation ne change pas.
ms.openlocfilehash: ef17b38d708103ca004594ba04ff5b8d1ada13bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307748"
---
# <a name="position-cell-tabs-section"></a><span data-ttu-id="a71fc-105">Position, cellule (section Tabs)</span><span class="sxs-lookup"><span data-stu-id="a71fc-105">Position Cell (Tabs Section)</span></span>

<span data-ttu-id="a71fc-p102">Définit la position d'une tabulation. La position de la tabulation est indépendante de l'échelle du dessin. Si le dessin est mis à l'échelle, la position de la tabulation ne change pas.</span><span class="sxs-lookup"><span data-stu-id="a71fc-p102">Specifies the position of a tab stop. The tab position is independent of the scale of the drawing. If the drawing is scaled, the tab position remains the same.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a71fc-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="a71fc-109">Remarks</span></span>

<span data-ttu-id="a71fc-110">Pour obtenir une référence à la cellule Position par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="a71fc-110">To get a reference to the Position cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a71fc-111">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="a71fc-111">Cell name:</span></span>  <br/> | <span data-ttu-id="a71fc-112">Taquet.</span><span class="sxs-lookup"><span data-stu-id="a71fc-112">Tabs.</span></span>  <span data-ttu-id="a71fc-113">*IJ* où *i* et *j* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="a71fc-113">*ij*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="a71fc-114">Pour obtenir une référence à la cellule Position à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="a71fc-114">To get a reference to the Position cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a71fc-115">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="a71fc-115">Section index:</span></span>  <br/> |<span data-ttu-id="a71fc-116">**visSectionTab**</span><span class="sxs-lookup"><span data-stu-id="a71fc-116">**visSectionTab**</span></span> <br/> |
| <span data-ttu-id="a71fc-117">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="a71fc-117">Row index:</span></span>  <br/> |<span data-ttu-id="a71fc-118">**visRowTab** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="a71fc-118">**visRowTab** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="a71fc-119">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="a71fc-119">Cell index:</span></span>  <br/> | <span data-ttu-id="a71fc-120">(*j* \* 3) + **visTabPos**</span><span class="sxs-lookup"><span data-stu-id="a71fc-120">(*j*  \*3) + **visTabPos**</span></span> <br/> |
   

