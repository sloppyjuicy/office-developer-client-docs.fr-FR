---
title: ShapeFixedCode, cellule (section Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm880
localization_priority: Normal
ms.assetid: a1736a5c-421c-2bdb-b164-76a8cd06cc3d
description: Indique le comportement du positionnement d'une forme positionnable.
ms.openlocfilehash: eae44a0579129fbe8da1c0cc8c37318beb024563
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325731"
---
# <a name="shapefixedcode-cell-shape-layout-section"></a><span data-ttu-id="77b10-103">ShapeFixedCode, cellule (section Shape Layout)</span><span class="sxs-lookup"><span data-stu-id="77b10-103">ShapeFixedCode Cell (Shape Layout Section)</span></span>

<span data-ttu-id="77b10-104">Indique le comportement du positionnement d'une forme positionnable.</span><span class="sxs-lookup"><span data-stu-id="77b10-104">Specifies placement behavior for a placeable shape.</span></span>
  
|<span data-ttu-id="77b10-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="77b10-105">**Value**</span></span>|<span data-ttu-id="77b10-106">**Mode de sélection**</span><span class="sxs-lookup"><span data-stu-id="77b10-106">**Selection mode**</span></span>|<span data-ttu-id="77b10-107">**Constante d'automation**</span><span class="sxs-lookup"><span data-stu-id="77b10-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="77b10-108">&amp;H1</span><span class="sxs-lookup"><span data-stu-id="77b10-108">&amp;H1</span></span>  <br/> |<span data-ttu-id="77b10-109">Ne pas déplacer cette forme lorsque les formes sont disposées à l'aide de la boîte de dialogue **configurer la disposition** .</span><span class="sxs-lookup"><span data-stu-id="77b10-109">Don't move this shape when shapes are laid out by using the **Configure Layout** dialog box.</span></span>  <br/> |<span data-ttu-id="77b10-110">**visSLOFixedPlacement**</span><span class="sxs-lookup"><span data-stu-id="77b10-110">**visSLOFixedPlacement**</span></span> <br/> |
|<span data-ttu-id="77b10-111">&amp;H2</span><span class="sxs-lookup"><span data-stu-id="77b10-111">&amp;H2</span></span>  <br/> |<span data-ttu-id="77b10-112">Ne pas déplacer cette forme et ne pas permettre aux formes qui tracent d'être positionnées sur cette forme.</span><span class="sxs-lookup"><span data-stu-id="77b10-112">Don't move this shape and do not allow shapes that plow to be placed on top of it.</span></span>  <br/> |<span data-ttu-id="77b10-113">**visSLOFixedPlow**</span><span class="sxs-lookup"><span data-stu-id="77b10-113">**visSLOFixedPlow**</span></span> <br/> |
|<span data-ttu-id="77b10-114">&amp;H4</span><span class="sxs-lookup"><span data-stu-id="77b10-114">&amp;H4</span></span>  <br/> |<span data-ttu-id="77b10-115">Ne pas déplacer cette forme et permettre aux formes qui tracent d'être positionnées sur cette forme.</span><span class="sxs-lookup"><span data-stu-id="77b10-115">Don't move this shape and allow shapes that plow to be placed on top of it.</span></span>  <br/> |<span data-ttu-id="77b10-116">**visSLOFixedPermeablePlow**</span><span class="sxs-lookup"><span data-stu-id="77b10-116">**visSLOFixedPermeablePlow**</span></span> <br/> |
|<span data-ttu-id="77b10-117">&amp;H20 (32)</span><span class="sxs-lookup"><span data-stu-id="77b10-117">&amp;H20 (32)</span></span>  <br/> |<span data-ttu-id="77b10-118">Ne pas tenir compte des emplacements des points de connexion en cas de positionnement.</span><span class="sxs-lookup"><span data-stu-id="77b10-118">Ignore connection point locations when being routed to.</span></span>  <br/> |<span data-ttu-id="77b10-119">**visSLOFixedConnPtsIgnore**</span><span class="sxs-lookup"><span data-stu-id="77b10-119">**visSLOFixedConnPtsIgnore**</span></span> <br/> |
|<span data-ttu-id="77b10-120">&amp;H40 (64)</span><span class="sxs-lookup"><span data-stu-id="77b10-120">&amp;H40 (64)</span></span>  <br/> |<span data-ttu-id="77b10-121">Autoriser uniquement le positionnement sur les côtés ayant des points de connexion.</span><span class="sxs-lookup"><span data-stu-id="77b10-121">Only allow routing to sides with connection points.</span></span>  <br/> |<span data-ttu-id="77b10-122">**visSLOFixedConnPtsOnly**</span><span class="sxs-lookup"><span data-stu-id="77b10-122">**visSLOFixedConnPtsOnly**</span></span> <br/> |
|<span data-ttu-id="77b10-123">&amp;H80 (128)</span><span class="sxs-lookup"><span data-stu-id="77b10-123">&amp;H80 (128)</span></span>  <br/> |<span data-ttu-id="77b10-124">Ne pas coller au périmètre de cette forme.</span><span class="sxs-lookup"><span data-stu-id="77b10-124">Don't glue to the perimeter of this shape.</span></span> <span data-ttu-id="77b10-125">Coller plutôt au rectangle de sélection de la forme.</span><span class="sxs-lookup"><span data-stu-id="77b10-125">Glue to the shape's alignment box instead.</span></span>  <br/> |<span data-ttu-id="77b10-126">**visSLOFixedNoFoldToShape**</span><span class="sxs-lookup"><span data-stu-id="77b10-126">**visSLOFixedNoFoldToShape**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="77b10-127">Remarques</span><span class="sxs-lookup"><span data-stu-id="77b10-127">Remarks</span></span>

<span data-ttu-id="77b10-128">Vous pouvez également définir la valeur de cette cellule sous l'onglet **placement** de la boîte de dialogue **comportement** (sélectionnez une forme, sous l'onglet [développeur](run-in-developer-mode-display-the-developer-tab.md) , dans le groupe création de la **forme** , cliquez sur **comportement**, puis sur l'onglet **placement** . ).</span><span class="sxs-lookup"><span data-stu-id="77b10-128">You can also set the value of this cell on the **Placement** tab in the **Behavior** dialog box (with a shape selected, on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, in the **Shape Design** group, click **Behavior**, and then click the **Placement** tab).</span></span> 
  
<span data-ttu-id="77b10-129">Vous pouvez définir n’importe quelle combinaison de ces valeurs pour cette cellule.</span><span class="sxs-lookup"><span data-stu-id="77b10-129">You can set any combination of these values for this cell.</span></span> <span data-ttu-id="77b10-130">Par exemple, vous pouvez entrer la valeur 3 (&amp;H3), ce qui élimine le mouvement lorsque vous disposez des formes à l'aide de la boîte de dialogue **configurer la disposition** (sous l'onglet **création** , dans le groupe **disposition** , cliquez sur **nouvelle disposition de page**, puis cliquez sur \*\* Autres options de disposition\*\* ) et lorsque d'autres formes positionnables sont placées sur la forme ou près de celle-ci.</span><span class="sxs-lookup"><span data-stu-id="77b10-130">For example, you can enter the value 3 (&amp;H3), which eliminates movement when you lay out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options** ) and when other placeable shapes are placed on or near the shape.</span></span> 
  
<span data-ttu-id="77b10-131">Dans les versions antérieures à Visio 2000, vous pouviez définir ce comportement en faisant appel à la cellule ObjInteract de la section Miscellaneous.</span><span class="sxs-lookup"><span data-stu-id="77b10-131">In versions earlier than Visio 2000, you set this behavior using the ObjInteract cell in the Miscellaneous section.</span></span> 
  
<span data-ttu-id="77b10-132">Pour obtenir une référence à la cellule ShapeFixedCode par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="77b10-132">To get a reference to the ShapeFixedCode cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="77b10-133">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="77b10-133">Cell name:</span></span>  <br/> |<span data-ttu-id="77b10-134">ShapeFixedCode</span><span class="sxs-lookup"><span data-stu-id="77b10-134">ShapeFixedCode</span></span>  <br/> |
   
<span data-ttu-id="77b10-135">Pour obtenir une référence à la cellule ShapeFixedCode à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="77b10-135">To get a reference to the ShapeFixedCode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="77b10-136">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="77b10-136">Section index:</span></span>  <br/> |<span data-ttu-id="77b10-137">**Définis**</span><span class="sxs-lookup"><span data-stu-id="77b10-137">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="77b10-138">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="77b10-138">Row index:</span></span>  <br/> |<span data-ttu-id="77b10-139">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="77b10-139">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="77b10-140">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="77b10-140">Cell index:</span></span>  <br/> |<span data-ttu-id="77b10-141">**visSLOFixedCode**</span><span class="sxs-lookup"><span data-stu-id="77b10-141">**visSLOFixedCode**</span></span> <br/> |
   

