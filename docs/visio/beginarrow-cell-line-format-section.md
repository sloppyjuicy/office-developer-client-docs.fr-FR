---
title: BeginArrow, cellule (section Line Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm51105
localization_priority: Normal
ms.assetid: 0ab4044e-2d77-1fbe-ef20-5d029bc064ba
description: Indique si un trait comporte une pointe de flèche ou un autre format d'extrémité de trait à son premier sommet. Entrez un nombre compris entre 0 et 45 ou la fonction UTILISATION avec le nom d'une extrémité de trait personnalisée ou utilisez la boîte de dialogue Trait.
ms.openlocfilehash: cf5a512dabd0e6296b83fa7bfd2a2a6134143d50
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410293"
---
# <a name="beginarrow-cell-line-format-section"></a><span data-ttu-id="b2b46-104">BeginArrow, cellule (section Line Format)</span><span class="sxs-lookup"><span data-stu-id="b2b46-104">BeginArrow Cell (Line Format Section)</span></span>

<span data-ttu-id="b2b46-p102">Indique si un trait comporte une pointe de flèche ou un autre format d'extrémité de trait à son premier sommet. Entrez un nombre compris entre 0 et 45 ou la fonction UTILISATION avec le nom d'une extrémité de trait personnalisée ou utilisez la boîte de dialogue **Trait**.</span><span class="sxs-lookup"><span data-stu-id="b2b46-p102">Indicates whether a line has an arrowhead or other line end format at its first vertex. Enter a number from 0 to 45 or the USE function with the name of a custom line end, or use the **Line** dialog box.</span></span> 
  
|<span data-ttu-id="b2b46-107">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="b2b46-107">**Value**</span></span>|<span data-ttu-id="b2b46-108">**Description**</span><span class="sxs-lookup"><span data-stu-id="b2b46-108">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="b2b46-109">0</span><span class="sxs-lookup"><span data-stu-id="b2b46-109">0</span></span>  <br/> | <span data-ttu-id="b2b46-110">Pas de pointe</span><span class="sxs-lookup"><span data-stu-id="b2b46-110">No arrowhead.</span></span>  <br/> |
| <span data-ttu-id="b2b46-111">1 - 45</span><span class="sxs-lookup"><span data-stu-id="b2b46-111">1 - 45</span></span>  <br/> | <span data-ttu-id="b2b46-112">Styles de pointes de flèches assortis correspondant aux entrées indexées de la boîte de dialogue **Trait**.</span><span class="sxs-lookup"><span data-stu-id="b2b46-112">Assorted arrowhead styles that correspond to indexed entries in the **Line** dialog box.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b2b46-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="b2b46-113">Remarks</span></span>

<span data-ttu-id="b2b46-114">La taille de la pointe de flèche est définie dans la cellule BeginArrowSize.</span><span class="sxs-lookup"><span data-stu-id="b2b46-114">The size of the arrowhead is set in the BeginArrowSize cell.</span></span>
  
<span data-ttu-id="b2b46-115">Pour obtenir une référence à la cellule BeginArrow par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="b2b46-115">To get a reference to the BeginArrow cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b2b46-116">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="b2b46-116">Cell name:</span></span>  <br/> | <span data-ttu-id="b2b46-117">BeginArrow</span><span class="sxs-lookup"><span data-stu-id="b2b46-117">BeginArrow</span></span>  <br/> |
   
<span data-ttu-id="b2b46-118">Pour obtenir une référence à la cellule BeginArrow à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="b2b46-118">To get a reference to the BeginArrow cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b2b46-119">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="b2b46-119">Section index:</span></span>  <br/> |<span data-ttu-id="b2b46-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b2b46-120">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="b2b46-121">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="b2b46-121">Row index:</span></span>  <br/> |<span data-ttu-id="b2b46-122">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="b2b46-122">**visRowLine**</span></span> <br/> |
| <span data-ttu-id="b2b46-123">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="b2b46-123">Cell index:</span></span>  <br/> |<span data-ttu-id="b2b46-124">**visLineBeginArrow**</span><span class="sxs-lookup"><span data-stu-id="b2b46-124">**visLineBeginArrow**</span></span> <br/> |
   

