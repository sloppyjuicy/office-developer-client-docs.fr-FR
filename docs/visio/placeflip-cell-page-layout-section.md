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
description: Détermine la façon dont les formes positionnables sont retournées et/ou pivotent lorsque vous utilisez la commande Configurer la disposition (sous l’onglet Création, dans le groupe Disposition, cliquez sur Nouvelle disposition de page, puis cliquez sur Autres options de disposition).
ms.openlocfilehash: d1c31654782012b3536d35f3a12a923c2cc7a8f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434297"
---
# <a name="placeflip-cell-page-layout-section"></a><span data-ttu-id="2e3f5-103">PlaceFlip, cellule (section Page Layout)</span><span class="sxs-lookup"><span data-stu-id="2e3f5-103">PlaceFlip Cell (Page Layout Section)</span></span>

<span data-ttu-id="2e3f5-104">Détermine la façon dont les formes positionnables sont retournées et/ou pivotent lorsque vous utilisez la commande **Configurer la disposition** (sous l’onglet **Création**, dans le groupe **Disposition**, cliquez sur **Nouvelle disposition de page**, puis cliquez sur **Autres options de disposition**).</span><span class="sxs-lookup"><span data-stu-id="2e3f5-104">Determines how placeable shapes flip and/or rotate on a page when you use the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**).</span></span>
  
|<span data-ttu-id="2e3f5-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="2e3f5-105">**Value**</span></span>|<span data-ttu-id="2e3f5-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="2e3f5-106">**Description**</span></span>|<span data-ttu-id="2e3f5-107">**Constante d'automation**</span><span class="sxs-lookup"><span data-stu-id="2e3f5-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2e3f5-108">&amp;H0</span><span class="sxs-lookup"><span data-stu-id="2e3f5-108">&amp;H0</span></span>  <br/> |<span data-ttu-id="2e3f5-109">Valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="2e3f5-109">Default.</span></span> <span data-ttu-id="2e3f5-110">Pas de retournement.</span><span class="sxs-lookup"><span data-stu-id="2e3f5-110">Do not flip.</span></span>  <br/> |<span data-ttu-id="2e3f5-111">**visLOFlipDefault**</span><span class="sxs-lookup"><span data-stu-id="2e3f5-111">**visLOFlipDefault**</span></span> <br/> |
|<span data-ttu-id="2e3f5-112">&amp;H1</span><span class="sxs-lookup"><span data-stu-id="2e3f5-112">&amp;H1</span></span>  <br/> |<span data-ttu-id="2e3f5-113">Retournement horizontal.</span><span class="sxs-lookup"><span data-stu-id="2e3f5-113">Flip horizontal.</span></span>  <br/> |<span data-ttu-id="2e3f5-114">**visLOFlipX**</span><span class="sxs-lookup"><span data-stu-id="2e3f5-114">**visLOFlipX**</span></span> <br/> |
|<span data-ttu-id="2e3f5-115">&amp;H2</span><span class="sxs-lookup"><span data-stu-id="2e3f5-115">&amp;H2</span></span>  <br/> |<span data-ttu-id="2e3f5-116">Retournement vertical.</span><span class="sxs-lookup"><span data-stu-id="2e3f5-116">Flip vertical.</span></span>  <br/> |<span data-ttu-id="2e3f5-117">**visLOFlipY**</span><span class="sxs-lookup"><span data-stu-id="2e3f5-117">**visLOFlipY**</span></span> <br/> |
|<span data-ttu-id="2e3f5-118">&amp;H4</span><span class="sxs-lookup"><span data-stu-id="2e3f5-118">&amp;H4</span></span>  <br/> |<span data-ttu-id="2e3f5-119">Retournement par incréments de 90 degrés.</span><span class="sxs-lookup"><span data-stu-id="2e3f5-119">Flip in 90 degree increments.</span></span>  <br/> |<span data-ttu-id="2e3f5-120">**visLOFlipRotate**</span><span class="sxs-lookup"><span data-stu-id="2e3f5-120">**visLOFlipRotate**</span></span> <br/> |
|<span data-ttu-id="2e3f5-121">&amp;H8</span><span class="sxs-lookup"><span data-stu-id="2e3f5-121">&amp;H8</span></span>  <br/> |<span data-ttu-id="2e3f5-122">Pas de retournement.</span><span class="sxs-lookup"><span data-stu-id="2e3f5-122">Do not flip.</span></span>  <br/> |<span data-ttu-id="2e3f5-123">**visLOFlipNone**</span><span class="sxs-lookup"><span data-stu-id="2e3f5-123">**visLOFlipNone**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2e3f5-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="2e3f5-124">Remarks</span></span>

<span data-ttu-id="2e3f5-p102">La valeur de la cellule PlaceFlip facilite l'orientation d'une forme positionnable vers la forme positionnable suivante à laquelle elle est liée. Elle est généralement utilisée pour la mise en page de dessins qui utilisent le collage statique.</span><span class="sxs-lookup"><span data-stu-id="2e3f5-p102">The value in the PlaceFlip cell helps orient a placeable shape toward the next placeable shape it is connected to. It is typically used when laying out drawings that use static glue.</span></span>
  
<span data-ttu-id="2e3f5-127">Pour définir ce comportement pour une forme donnée, utilisez la cellule ShapePlaceFlip de la section Shape Layout.</span><span class="sxs-lookup"><span data-stu-id="2e3f5-127">To set this behavior for a particular shape, use the ShapePlaceFlip cell in the Shape Layout section.</span></span>
  
<span data-ttu-id="2e3f5-128">Pour obtenir une référence à la cellule PlaceFlip par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="2e3f5-128">To get a reference to the PlaceFlip cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2e3f5-129">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="2e3f5-129">Cell name:</span></span>  <br/> |<span data-ttu-id="2e3f5-130">PlaceFlip</span><span class="sxs-lookup"><span data-stu-id="2e3f5-130">PlaceFlip</span></span>  <br/> |
   
<span data-ttu-id="2e3f5-131">Pour obtenir une référence à la cellule PlaceFlip à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="2e3f5-131">To get a reference to the PlaceFlip cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2e3f5-132">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="2e3f5-132">Section index:</span></span>  <br/> |<span data-ttu-id="2e3f5-133">**Définis**</span><span class="sxs-lookup"><span data-stu-id="2e3f5-133">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="2e3f5-134">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="2e3f5-134">Row index:</span></span>  <br/> |<span data-ttu-id="2e3f5-135">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="2e3f5-135">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="2e3f5-136">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="2e3f5-136">Cell index:</span></span>  <br/> |<span data-ttu-id="2e3f5-137">**visPLOPlaceFlip**</span><span class="sxs-lookup"><span data-stu-id="2e3f5-137">**visPLOPlaceFlip**</span></span> <br/> |
   

