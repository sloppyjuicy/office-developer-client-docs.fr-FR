---
title: PlaceFlip, cellule (section Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253251
localization_priority: Normal
ms.assetid: df014b98-cfd5-b6d3-4b8a-b0acb3b94412
description: Détermine les formes positionnables comment retourner ou faire pivoter une page lorsque vous utilisez la boîte de dialogue Configurer la disposition (sous l’onglet Création, dans le groupe mise en page, cliquez sur Re-mise en Page, puis cliquez sur autres Options de mise en page).
ms.openlocfilehash: fb16849c7a496a4277133c68453d94d6fd2e67f8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789237"
---
# <a name="placeflip-cell-page-layout-section"></a><span data-ttu-id="6408e-103">PlaceFlip, cellule (section Page Layout)</span><span class="sxs-lookup"><span data-stu-id="6408e-103">PlaceFlip Cell (Page Layout Section)</span></span>

<span data-ttu-id="6408e-104">Détermine les formes positionnables comment retourner ou faire pivoter une page lorsque vous utilisez la boîte de dialogue **Configurer la disposition** (sous l’onglet **Création** , dans le groupe **mise en page** , cliquez sur **Re-mise en Page**, puis cliquez sur **Autres Options de mise en page**).</span><span class="sxs-lookup"><span data-stu-id="6408e-104">Determines how placeable shapes flip and/or rotate on a page when you use the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**).</span></span>
  
|<span data-ttu-id="6408e-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="6408e-105">**Value**</span></span>|<span data-ttu-id="6408e-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="6408e-106">**Description**</span></span>|<span data-ttu-id="6408e-107">**Constante d’Automation**</span><span class="sxs-lookup"><span data-stu-id="6408e-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6408e-108">&amp;H0</span><span class="sxs-lookup"><span data-stu-id="6408e-108">&amp;H0</span></span>  <br/> |<span data-ttu-id="6408e-p101">Par défaut. Pas de retournement.</span><span class="sxs-lookup"><span data-stu-id="6408e-p101">Default. Do not flip.</span></span>  <br/> |<span data-ttu-id="6408e-111">**visLOFlipDefault**</span><span class="sxs-lookup"><span data-stu-id="6408e-111">**visLOFlipDefault**</span></span> <br/> |
|<span data-ttu-id="6408e-112">&amp;H1</span><span class="sxs-lookup"><span data-stu-id="6408e-112">&amp;H1</span></span>  <br/> |<span data-ttu-id="6408e-113">Retournement horizontal.</span><span class="sxs-lookup"><span data-stu-id="6408e-113">Flip horizontal.</span></span>  <br/> |<span data-ttu-id="6408e-114">**visLOFlipX**</span><span class="sxs-lookup"><span data-stu-id="6408e-114">**visLOFlipX**</span></span> <br/> |
|<span data-ttu-id="6408e-115">&amp;H2</span><span class="sxs-lookup"><span data-stu-id="6408e-115">&amp;H2</span></span>  <br/> |<span data-ttu-id="6408e-116">Retournement vertical.</span><span class="sxs-lookup"><span data-stu-id="6408e-116">Flip vertical.</span></span>  <br/> |<span data-ttu-id="6408e-117">**visLOFlipY**</span><span class="sxs-lookup"><span data-stu-id="6408e-117">**visLOFlipY**</span></span> <br/> |
|<span data-ttu-id="6408e-118">&amp;H4</span><span class="sxs-lookup"><span data-stu-id="6408e-118">&amp;H4</span></span>  <br/> |<span data-ttu-id="6408e-119">Retournement par incréments de 90 degrés.</span><span class="sxs-lookup"><span data-stu-id="6408e-119">Flip in 90 degree increments.</span></span>  <br/> |<span data-ttu-id="6408e-120">**visLOFlipRotate**</span><span class="sxs-lookup"><span data-stu-id="6408e-120">**visLOFlipRotate**</span></span> <br/> |
|<span data-ttu-id="6408e-121">&amp;H8</span><span class="sxs-lookup"><span data-stu-id="6408e-121">&amp;H8</span></span>  <br/> |<span data-ttu-id="6408e-122">Pas de retournement.</span><span class="sxs-lookup"><span data-stu-id="6408e-122">Do not flip.</span></span>  <br/> |<span data-ttu-id="6408e-123">**visLOFlipNone**</span><span class="sxs-lookup"><span data-stu-id="6408e-123">**visLOFlipNone**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6408e-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="6408e-124">Remarks</span></span>

<span data-ttu-id="6408e-p102">La valeur de la cellule PlaceFlip facilite l'orientation d'une forme positionnable vers la forme positionnable suivante à laquelle elle est liée. Elle est généralement utilisée pour la mise en page de dessins qui utilisent le collage statique.</span><span class="sxs-lookup"><span data-stu-id="6408e-p102">The value in the PlaceFlip cell helps orient a placeable shape toward the next placeable shape it is connected to. It is typically used when laying out drawings that use static glue.</span></span>
  
<span data-ttu-id="6408e-127">Pour définir ce comportement pour une forme donnée, utilisez la cellule ShapePlaceFlip de la section Shape Layout.</span><span class="sxs-lookup"><span data-stu-id="6408e-127">To set this behavior for a particular shape, use the ShapePlaceFlip cell in the Shape Layout section.</span></span>
  
<span data-ttu-id="6408e-128">Pour obtenir une référence à la cellule PlaceFlip par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="6408e-128">To get a reference to the PlaceFlip cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6408e-129">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="6408e-129">Cell name:</span></span>  <br/> |<span data-ttu-id="6408e-130">PlaceFlip</span><span class="sxs-lookup"><span data-stu-id="6408e-130">PlaceFlip</span></span>  <br/> |
   
<span data-ttu-id="6408e-131">Pour obtenir une référence à la cellule PlaceFlip par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="6408e-131">To get a reference to the PlaceFlip cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6408e-132">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="6408e-132">Section index:</span></span>  <br/> |<span data-ttu-id="6408e-133">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="6408e-133">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="6408e-134">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="6408e-134">Row index:</span></span>  <br/> |<span data-ttu-id="6408e-135">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="6408e-135">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="6408e-136">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="6408e-136">Cell index:</span></span>  <br/> |<span data-ttu-id="6408e-137">**visPLOPlaceFlip**</span><span class="sxs-lookup"><span data-stu-id="6408e-137">**visPLOPlaceFlip**</span></span> <br/> |
   

