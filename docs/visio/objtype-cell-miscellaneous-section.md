---
title: ObjType, cellule (section Miscellaneous)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm745
localization_priority: Normal
ms.assetid: 3afee07b-e91a-a91c-fba2-0e3251dd6385
description: Détermine si les objets sont positionnables ou repositionnables dans les diagrammes lorsque vous utilisez la boîte de dialogue Configurer la disposition pour disposer des formes.
ms.openlocfilehash: 23887e1d265e9e5ac1dfa9750bab65e8428b1c76
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789195"
---
# <a name="objtype-cell-miscellaneous-section"></a><span data-ttu-id="4115a-103">ObjType, cellule (section Miscellaneous)</span><span class="sxs-lookup"><span data-stu-id="4115a-103">ObjType Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="4115a-104">Détermine si les objets sont positionnables ou repositionnables dans les diagrammes lorsque vous utilisez la boîte de dialogue **Configurer la disposition** pour disposer des formes.</span><span class="sxs-lookup"><span data-stu-id="4115a-104">Determines whether objects are placeable or routable in diagrams when you use the **Configure Layout** dialog box to lay out shapes.</span></span> 
  
|<span data-ttu-id="4115a-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="4115a-105">**Value**</span></span>|<span data-ttu-id="4115a-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="4115a-106">**Description**</span></span>|<span data-ttu-id="4115a-107">**Constante d’Automation**</span><span class="sxs-lookup"><span data-stu-id="4115a-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4115a-108">&amp;H0</span><span class="sxs-lookup"><span data-stu-id="4115a-108">&amp;H0</span></span>  <br/> |<span data-ttu-id="4115a-p101">Par défaut. L'application décide en fonction du contexte de dessin.</span><span class="sxs-lookup"><span data-stu-id="4115a-p101">Default. The application decides based on the drawing context.</span></span>  <br/> |<span data-ttu-id="4115a-111">**visLOFlagsVisDecides**</span><span class="sxs-lookup"><span data-stu-id="4115a-111">**visLOFlagsVisDecides**</span></span> <br/> |
|<span data-ttu-id="4115a-112">&amp;H1</span><span class="sxs-lookup"><span data-stu-id="4115a-112">&amp;H1</span></span>  <br/> |<span data-ttu-id="4115a-113">La forme est positionnable.</span><span class="sxs-lookup"><span data-stu-id="4115a-113">Shape is placeable.</span></span>  <br/> |<span data-ttu-id="4115a-114">**visLOFlagsPlacable**</span><span class="sxs-lookup"><span data-stu-id="4115a-114">**visLOFlagsPlacable**</span></span> <br/> |
|<span data-ttu-id="4115a-115">&amp;H2</span><span class="sxs-lookup"><span data-stu-id="4115a-115">&amp;H2</span></span>  <br/> |<span data-ttu-id="4115a-p102">La forme est repositionnable. Il doit s'agir d'une forme à une dimension (1D).</span><span class="sxs-lookup"><span data-stu-id="4115a-p102">Shape is routable. Must be a one-dimensional (1-D) shape.</span></span>  <br/> |<span data-ttu-id="4115a-118">**visLOFlagsRoutable**</span><span class="sxs-lookup"><span data-stu-id="4115a-118">**visLOFlagsRoutable**</span></span> <br/> |
|<span data-ttu-id="4115a-119">&amp;H4</span><span class="sxs-lookup"><span data-stu-id="4115a-119">&amp;H4</span></span>  <br/> |<span data-ttu-id="4115a-120">La forme n'est ni positionnable ni repositionnable.</span><span class="sxs-lookup"><span data-stu-id="4115a-120">Shape is not placeable, not routable.</span></span>  <br/> |<span data-ttu-id="4115a-121">**visLOFlagsDont**</span><span class="sxs-lookup"><span data-stu-id="4115a-121">**visLOFlagsDont**</span></span> <br/> |
|<span data-ttu-id="4115a-122">&amp;H8</span><span class="sxs-lookup"><span data-stu-id="4115a-122">&amp;H8</span></span>  <br/> |<span data-ttu-id="4115a-123">Le groupe contient des formes positionnables ou repositionnables.</span><span class="sxs-lookup"><span data-stu-id="4115a-123">Group contains placeable/routable shapes.</span></span>  <br/> |<span data-ttu-id="4115a-124">**visLOFlagsPNRGroup**</span><span class="sxs-lookup"><span data-stu-id="4115a-124">**visLOFlagsPNRGroup**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4115a-125">Remarques</span><span class="sxs-lookup"><span data-stu-id="4115a-125">Remarks</span></span>

<span data-ttu-id="4115a-126">Par défaut, la cellule ObjType est définie sur aucune formule d’une forme, prend la valeur 0, ce qui signifie que l’application détermine si la forme peut être positionnable en fonction de son contexte.</span><span class="sxs-lookup"><span data-stu-id="4115a-126">By default, the ObjType cell is set to No Formula for a shape, which evaluates to 0, meaning that the application determines whether the shape can be placeable depending on its context.</span></span> <span data-ttu-id="4115a-127">Par exemple, si vous dessinez un rectangle, la valeur de la cellule ObjType associée est 0.</span><span class="sxs-lookup"><span data-stu-id="4115a-127">For example, if you draw a simple rectangle, the value of its ObjType cell is 0.</span></span> <span data-ttu-id="4115a-128">Si vous utilisez ensuite l’outil **connecteur** pour relier le rectangle à une autre forme, Visio rétablit la valeur de la cellule ObjType du rectangle 1 (positionnable).</span><span class="sxs-lookup"><span data-stu-id="4115a-128">If you then use the **Connector** tool to connect the rectangle to another shape, Visio resets the value of the rectangle's ObjType cell to 1 (placeable).</span></span> 
  
<span data-ttu-id="4115a-129">La valeur de la cellule ObjType peut être une combinaison de valeurs.</span><span class="sxs-lookup"><span data-stu-id="4115a-129">The value of the ObjType cell can be a combination of values.</span></span> <span data-ttu-id="4115a-130">Si le bit non positionnable est défini (&amp;H4), toutefois, il est prioritaire sur les autres valeurs, à l’exception de la valeur de groupe (&amp;H8).</span><span class="sxs-lookup"><span data-stu-id="4115a-130">If the non-placeable bit is set (&amp;H4), however, it takes precedence over other values except the group value (&amp;H8).</span></span>
  
<span data-ttu-id="4115a-131">Pour obtenir une référence à la cellule ObjType par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="4115a-131">To get a reference to the ObjType cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4115a-132">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="4115a-132">Cell name:</span></span>  <br/> |<span data-ttu-id="4115a-133">Type de l’objet</span><span class="sxs-lookup"><span data-stu-id="4115a-133">ObjType</span></span>  <br/> |
   
<span data-ttu-id="4115a-134">Pour obtenir une référence à la cellule ObjType par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="4115a-134">To get a reference to the ObjType cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4115a-135">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="4115a-135">Section index:</span></span>  <br/> |<span data-ttu-id="4115a-136">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="4115a-136">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="4115a-137">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="4115a-137">Row index:</span></span>  <br/> |<span data-ttu-id="4115a-138">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="4115a-138">**visRowMisc**</span></span> <br/> |
|<span data-ttu-id="4115a-139">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="4115a-139">Cell index:</span></span>  <br/> |<span data-ttu-id="4115a-140">**visLOFlags**</span><span class="sxs-lookup"><span data-stu-id="4115a-140">**visLOFlags**</span></span> <br/> |
   

