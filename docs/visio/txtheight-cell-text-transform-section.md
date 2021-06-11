---
title: TxtHeight, cellule (section Text Transform)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1025
localization_priority: Normal
ms.assetid: cfa3ecc6-61a8-506c-ba1d-b5e1f757d44f
description: 'Détermine la hauteur du bloc de texte. La formule par défaut est la suivante :'
ms.openlocfilehash: 8ad17cdf1deca6c4aa81f3388d7c112b4e179e2f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409306"
---
# <a name="txtheight-cell-text-transform-section"></a><span data-ttu-id="1c157-104">TxtHeight, cellule (section Text Transform)</span><span class="sxs-lookup"><span data-stu-id="1c157-104">TxtHeight Cell (Text Transform Section)</span></span>

<span data-ttu-id="1c157-p102">Détermine la hauteur du bloc de texte. La formule par défaut est la suivante :</span><span class="sxs-lookup"><span data-stu-id="1c157-p102">Determines the height of the text block. The default formula is:</span></span>
  
<span data-ttu-id="1c157-107">= Hauteur \* 1</span><span class="sxs-lookup"><span data-stu-id="1c157-107">= Height \* 1</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1c157-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="1c157-108">Remarks</span></span>

<span data-ttu-id="1c157-109">Pour obtenir une référence à la cellule TxtHeight par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="1c157-109">To get a reference to the TxtHeight cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1c157-110">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="1c157-110">Cell name:</span></span>  <br/> | <span data-ttu-id="1c157-111">TxtHeight</span><span class="sxs-lookup"><span data-stu-id="1c157-111">TxtHeight</span></span>  <br/> |
   
<span data-ttu-id="1c157-112">Pour obtenir une référence à la cellule TxtHeight par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="1c157-112">To get a reference to the TxtHeight cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1c157-113">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="1c157-113">Section index:</span></span>  <br/> |<span data-ttu-id="1c157-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="1c157-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="1c157-115">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="1c157-115">Row index:</span></span>  <br/> |<span data-ttu-id="1c157-116">**visRowTextXForm**</span><span class="sxs-lookup"><span data-stu-id="1c157-116">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="1c157-117">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="1c157-117">Cell index:</span></span>  <br/> |<span data-ttu-id="1c157-118">**visXFormHeight**</span><span class="sxs-lookup"><span data-stu-id="1c157-118">**visXFormHeight**</span></span> <br/> |
   

