---
title: Width, cellule (section Shape Transform)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251194
localization_priority: Normal
ms.assetid: 992ae9d8-ea15-0f5c-ccd6-e4c536099692
description: "Contient la largeur de la forme sélectionnée, exprimée en unités de dessin. La formule par défaut permettant de déterminer la largeur d'une forme 1D est la suivante :"
ms.openlocfilehash: c99f4669f3b27390a5b8e9062d6085a5a9db54e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415193"
---
# <a name="width-cell-shape-transform-section"></a><span data-ttu-id="9cbb7-104">Width, cellule (section Shape Transform)</span><span class="sxs-lookup"><span data-stu-id="9cbb7-104">Width Cell (Shape Transform Section)</span></span>

<span data-ttu-id="9cbb7-p102">Contient la largeur de la forme sélectionnée, exprimée en unités de dessin. La formule par défaut permettant de déterminer la largeur d'une forme 1D est la suivante :</span><span class="sxs-lookup"><span data-stu-id="9cbb7-p102">Contains the width of the selected shape in drawing units. The default formula for determining the width of a 1-D shape is:</span></span>
  
<span data-ttu-id="9cbb7-107">= SQRT((EndX - BeginX) ^ 2 + (EndY - BeginY) ^ 2)</span><span class="sxs-lookup"><span data-stu-id="9cbb7-107">= SQRT((EndX - BeginX) ^ 2 + (EndY - BeginY) ^ 2)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9cbb7-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="9cbb7-108">Remarks</span></span>

<span data-ttu-id="9cbb7-109">Pour obtenir une référence à la cellule Width par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="9cbb7-109">To get a reference to the Width cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9cbb7-110">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="9cbb7-110">Cell name:</span></span>  <br/> | <span data-ttu-id="9cbb7-111">Largeur</span><span class="sxs-lookup"><span data-stu-id="9cbb7-111">Width</span></span>  <br/> |
   
<span data-ttu-id="9cbb7-112">Pour obtenir une référence à la cellule Width par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="9cbb7-112">To get a reference to the Width cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9cbb7-113">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="9cbb7-113">Section index:</span></span>  <br/> |<span data-ttu-id="9cbb7-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="9cbb7-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="9cbb7-115">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="9cbb7-115">Row index:</span></span>  <br/> |<span data-ttu-id="9cbb7-116">**visRowXFormOut**</span><span class="sxs-lookup"><span data-stu-id="9cbb7-116">**visRowXFormOut**</span></span> <br/> |
| <span data-ttu-id="9cbb7-117">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="9cbb7-117">Cell index:</span></span>  <br/> |<span data-ttu-id="9cbb7-118">**visXFormWidth**</span><span class="sxs-lookup"><span data-stu-id="9cbb7-118">**visXFormWidth**</span></span> <br/> |
   

