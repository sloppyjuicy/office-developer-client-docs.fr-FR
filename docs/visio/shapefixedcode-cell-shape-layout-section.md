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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431742"
---
# <a name="shapefixedcode-cell-shape-layout-section"></a><span data-ttu-id="240ca-103">ShapeFixedCode, cellule (section Shape Layout)</span><span class="sxs-lookup"><span data-stu-id="240ca-103">ShapeFixedCode Cell (Shape Layout Section)</span></span>

<span data-ttu-id="240ca-104">Indique le comportement du positionnement d'une forme positionnable.</span><span class="sxs-lookup"><span data-stu-id="240ca-104">Specifies placement behavior for a placeable shape.</span></span>
  
|<span data-ttu-id="240ca-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="240ca-105">**Value**</span></span>|<span data-ttu-id="240ca-106">**Mode de sélection**</span><span class="sxs-lookup"><span data-stu-id="240ca-106">**Selection mode**</span></span>|<span data-ttu-id="240ca-107">**Constante d'automation**</span><span class="sxs-lookup"><span data-stu-id="240ca-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="240ca-108">&amp;H1</span><span class="sxs-lookup"><span data-stu-id="240ca-108">&amp;H1</span></span>  <br/> |<span data-ttu-id="240ca-109">Ne déplacez pas cette forme lorsque les formes sont disposés à l’aide de la **boîte** de dialogue Configurer la disposition.</span><span class="sxs-lookup"><span data-stu-id="240ca-109">Don't move this shape when shapes are laid out by using the **Configure Layout** dialog box.</span></span>  <br/> |<span data-ttu-id="240ca-110">**visSLOFixedPlacement**</span><span class="sxs-lookup"><span data-stu-id="240ca-110">**visSLOFixedPlacement**</span></span> <br/> |
|<span data-ttu-id="240ca-111">&amp;H2</span><span class="sxs-lookup"><span data-stu-id="240ca-111">&amp;H2</span></span>  <br/> |<span data-ttu-id="240ca-112">Ne pas déplacer cette forme et ne pas permettre aux formes qui tracent d'être positionnées sur cette forme.</span><span class="sxs-lookup"><span data-stu-id="240ca-112">Don't move this shape and do not allow shapes that plow to be placed on top of it.</span></span>  <br/> |<span data-ttu-id="240ca-113">**visSLOFixedPlow**</span><span class="sxs-lookup"><span data-stu-id="240ca-113">**visSLOFixedPlow**</span></span> <br/> |
|<span data-ttu-id="240ca-114">&amp;H4</span><span class="sxs-lookup"><span data-stu-id="240ca-114">&amp;H4</span></span>  <br/> |<span data-ttu-id="240ca-115">Ne pas déplacer cette forme et permettre aux formes qui tracent d'être positionnées sur cette forme.</span><span class="sxs-lookup"><span data-stu-id="240ca-115">Don't move this shape and allow shapes that plow to be placed on top of it.</span></span>  <br/> |<span data-ttu-id="240ca-116">**visSLOFixedPermeablePlow**</span><span class="sxs-lookup"><span data-stu-id="240ca-116">**visSLOFixedPermeablePlow**</span></span> <br/> |
|<span data-ttu-id="240ca-117">&amp;H20 (32)</span><span class="sxs-lookup"><span data-stu-id="240ca-117">&amp;H20 (32)</span></span>  <br/> |<span data-ttu-id="240ca-118">Ne pas tenir compte des emplacements des points de connexion en cas de positionnement.</span><span class="sxs-lookup"><span data-stu-id="240ca-118">Ignore connection point locations when being routed to.</span></span>  <br/> |<span data-ttu-id="240ca-119">**visSLOFixedConnPtsIgnore**</span><span class="sxs-lookup"><span data-stu-id="240ca-119">**visSLOFixedConnPtsIgnore**</span></span> <br/> |
|<span data-ttu-id="240ca-120">&amp;H40 (64)</span><span class="sxs-lookup"><span data-stu-id="240ca-120">&amp;H40 (64)</span></span>  <br/> |<span data-ttu-id="240ca-121">Autoriser uniquement le positionnement sur les côtés ayant des points de connexion.</span><span class="sxs-lookup"><span data-stu-id="240ca-121">Only allow routing to sides with connection points.</span></span>  <br/> |<span data-ttu-id="240ca-122">**visSLOFixedConnPtsOnly**</span><span class="sxs-lookup"><span data-stu-id="240ca-122">**visSLOFixedConnPtsOnly**</span></span> <br/> |
|<span data-ttu-id="240ca-123">&amp;H80 (128)</span><span class="sxs-lookup"><span data-stu-id="240ca-123">&amp;H80 (128)</span></span>  <br/> |<span data-ttu-id="240ca-124">Ne pas coller au périmètre de cette forme.</span><span class="sxs-lookup"><span data-stu-id="240ca-124">Don't glue to the perimeter of this shape.</span></span> <span data-ttu-id="240ca-125">Coller plutôt au rectangle de sélection de la forme.</span><span class="sxs-lookup"><span data-stu-id="240ca-125">Glue to the shape's alignment box instead.</span></span>  <br/> |<span data-ttu-id="240ca-126">**visSLOFixedNoFoldToShape**</span><span class="sxs-lookup"><span data-stu-id="240ca-126">**visSLOFixedNoFoldToShape**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="240ca-127">Remarques</span><span class="sxs-lookup"><span data-stu-id="240ca-127">Remarks</span></span>

<span data-ttu-id="240ca-128">Vous pouvez également définir la valeur de cette  cellule sous l’onglet **Placement** dans la boîte  de dialogue Comportement (avec une forme sélectionnée, sous l’onglet Développeur, dans le groupe Création de formes, cliquez sur **Comportement,** puis cliquez sur l’onglet **Placement).** [](run-in-developer-mode-display-the-developer-tab.md)</span><span class="sxs-lookup"><span data-stu-id="240ca-128">You can also set the value of this cell on the **Placement** tab in the **Behavior** dialog box (with a shape selected, on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, in the **Shape Design** group, click **Behavior**, and then click the **Placement** tab).</span></span> 
  
<span data-ttu-id="240ca-129">Vous pouvez définir n’importe quelle combinaison de ces valeurs pour cette cellule.</span><span class="sxs-lookup"><span data-stu-id="240ca-129">You can set any combination of these values for this cell.</span></span> <span data-ttu-id="240ca-130">Par exemple, vous pouvez entrer la valeur 3 ( H3), ce qui élimine le mouvement lorsque vous placez des formes à l’aide de la boîte de dialogue Configurer la disposition (sous l’onglet Création, dans le groupe Disposition, cliquez sur Nouvelle disposition page, puis cliquez sur Autres options de disposition) et lorsque d’autres formes &amp; positionnables     sont placées sur ou près de la forme. </span><span class="sxs-lookup"><span data-stu-id="240ca-130">For example, you can enter the value 3 (&amp;H3), which eliminates movement when you lay out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options** ) and when other placeable shapes are placed on or near the shape.</span></span> 
  
<span data-ttu-id="240ca-131">Dans les versions antérieures à Visio 2000, vous pouviez définir ce comportement en faisant appel à la cellule ObjInteract de la section Miscellaneous.</span><span class="sxs-lookup"><span data-stu-id="240ca-131">In versions earlier than Visio 2000, you set this behavior using the ObjInteract cell in the Miscellaneous section.</span></span> 
  
<span data-ttu-id="240ca-132">Pour obtenir une référence à la cellule ShapeFixedCode par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="240ca-132">To get a reference to the ShapeFixedCode cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="240ca-133">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="240ca-133">Cell name:</span></span>  <br/> |<span data-ttu-id="240ca-134">ShapeFixedCode</span><span class="sxs-lookup"><span data-stu-id="240ca-134">ShapeFixedCode</span></span>  <br/> |
   
<span data-ttu-id="240ca-135">Pour obtenir une référence à la cellule ShapeFixedCode à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="240ca-135">To get a reference to the ShapeFixedCode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="240ca-136">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="240ca-136">Section index:</span></span>  <br/> |<span data-ttu-id="240ca-137">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="240ca-137">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="240ca-138">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="240ca-138">Row index:</span></span>  <br/> |<span data-ttu-id="240ca-139">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="240ca-139">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="240ca-140">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="240ca-140">Cell index:</span></span>  <br/> |<span data-ttu-id="240ca-141">**visSLOFixedCode**</span><span class="sxs-lookup"><span data-stu-id="240ca-141">**visSLOFixedCode**</span></span> <br/> |
   

