---
title: LineCap, cellule (section Line Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251231
localization_priority: Normal
ms.assetid: 3519216b-b6cf-2e8c-e20f-adfa373c9028
description: Indique si l'extrémité du trait est arrondie, carrée ou étendue.
ms.openlocfilehash: 1bd427801e6d95ce6167fa9681da2c567307f072
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788949"
---
# <a name="linecap-cell-line-format-section"></a><span data-ttu-id="51563-103">LineCap, cellule (section Line Format)</span><span class="sxs-lookup"><span data-stu-id="51563-103">LineCap Cell (Line Format Section)</span></span>

<span data-ttu-id="51563-104">Indique si l'extrémité du trait est arrondie, carrée ou étendue.</span><span class="sxs-lookup"><span data-stu-id="51563-104">Indicates whether a line has rounded, square, or extended line caps.</span></span>
  
|<span data-ttu-id="51563-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="51563-105">**Value**</span></span>|<span data-ttu-id="51563-106">**Style de fin de ligne**</span><span class="sxs-lookup"><span data-stu-id="51563-106">**Line end style**</span></span>|
|:-----|:-----|
|<span data-ttu-id="51563-107">0</span><span class="sxs-lookup"><span data-stu-id="51563-107">0</span></span>  <br/> |<span data-ttu-id="51563-108">Arrondi</span><span class="sxs-lookup"><span data-stu-id="51563-108">Rounded</span></span>  <br/> |
|<span data-ttu-id="51563-109">1</span><span class="sxs-lookup"><span data-stu-id="51563-109">1</span></span>  <br/> |<span data-ttu-id="51563-110">Carré</span><span class="sxs-lookup"><span data-stu-id="51563-110">Square</span></span>  <br/> |
|<span data-ttu-id="51563-111">2</span><span class="sxs-lookup"><span data-stu-id="51563-111">2</span></span>  <br/> |<span data-ttu-id="51563-112">Étendu</span><span class="sxs-lookup"><span data-stu-id="51563-112">Extended</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="51563-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="51563-113">Remarks</span></span>

<span data-ttu-id="51563-114">Vous pouvez également définir la valeur de cette cellule dans la boîte de dialogue **trait** (sous l’onglet **accueil** , dans le groupe **forme** , cliquez sur **trait**, pointez sur **flèches**, puis cliquez sur **Autres flèches**).</span><span class="sxs-lookup"><span data-stu-id="51563-114">You can also set the value of this cell in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Arrows**, and then click **More Arrows**).</span></span>
  
<span data-ttu-id="51563-115">Pour obtenir une référence à la cellule LineCap par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="51563-115">To get a reference to the LineCap cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="51563-116">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="51563-116">Cell name:</span></span>  <br/> |<span data-ttu-id="51563-117">LineCap</span><span class="sxs-lookup"><span data-stu-id="51563-117">LineCap</span></span>  <br/> |
   
<span data-ttu-id="51563-118">Pour obtenir une référence à la cellule LineCap par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="51563-118">To get a reference to the LineCap cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="51563-119">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="51563-119">Section index:</span></span>  <br/> |<span data-ttu-id="51563-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="51563-120">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="51563-121">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="51563-121">Row index:</span></span>  <br/> |<span data-ttu-id="51563-122">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="51563-122">**visRowLine**</span></span> <br/> |
|<span data-ttu-id="51563-123">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="51563-123">Cell index:</span></span>  <br/> |<span data-ttu-id="51563-124">**visLineEndCap**</span><span class="sxs-lookup"><span data-stu-id="51563-124">**visLineEndCap**</span></span> <br/> |
   

