---
title: ShapePlaceFlip, cellule (section Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253247
localization_priority: Normal
ms.assetid: 40008507-d9e4-9c0e-603f-d5e6da73a94b
description: Détermine comment fait pivoter une forme positionnable, fait pivoter, ou les deux sur la page lorsque vous disposez des formes à l’aide de la boîte de dialogue Configurer la disposition (sous l’onglet Création, dans le groupe mise en page, cliquez sur Re-mise en Page, puis cliquez sur autres Options de mise en page).
ms.openlocfilehash: 76941b9c50e6f2c68ea9abf54e81dcd18be13a70
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789648"
---
# <a name="shapeplaceflip-cell-shape-layout-section"></a><span data-ttu-id="f1b93-103">ShapePlaceFlip, cellule (section Shape Layout)</span><span class="sxs-lookup"><span data-stu-id="f1b93-103">ShapePlaceFlip Cell (Shape Layout Section)</span></span>

<span data-ttu-id="f1b93-104">Détermine comment fait pivoter une forme positionnable, fait pivoter, ou les deux sur la page lorsque vous disposez des formes à l’aide de la boîte de dialogue **Configurer la disposition** (sous l’onglet **Création** , dans le groupe **mise en page** , cliquez sur **Re-mise en Page**, puis cliquez sur **plus Options de disposition**).</span><span class="sxs-lookup"><span data-stu-id="f1b93-104">Determines how a placeable shape flips, rotates, or both on the page when you are laying out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**).</span></span>
  
|<span data-ttu-id="f1b93-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="f1b93-105">**Value**</span></span>|<span data-ttu-id="f1b93-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="f1b93-106">**Description**</span></span>|<span data-ttu-id="f1b93-107">**Constante d’Automation**</span><span class="sxs-lookup"><span data-stu-id="f1b93-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f1b93-108">0</span><span class="sxs-lookup"><span data-stu-id="f1b93-108">0</span></span>  <br/> |<span data-ttu-id="f1b93-109">Utiliser la valeur page par défaut.</span><span class="sxs-lookup"><span data-stu-id="f1b93-109">Use page default.</span></span>  <br/> |<span data-ttu-id="f1b93-110">**visLOFlipDefault**</span><span class="sxs-lookup"><span data-stu-id="f1b93-110">**visLOFlipDefault**</span></span> <br/> |
|<span data-ttu-id="f1b93-111">1</span><span class="sxs-lookup"><span data-stu-id="f1b93-111">1</span></span>  <br/> |<span data-ttu-id="f1b93-112">Retournement horizontal.</span><span class="sxs-lookup"><span data-stu-id="f1b93-112">Flip horizontal.</span></span>  <br/> |<span data-ttu-id="f1b93-113">**visLOFlipX**</span><span class="sxs-lookup"><span data-stu-id="f1b93-113">**visLOFlipX**</span></span> <br/> |
|<span data-ttu-id="f1b93-114">2</span><span class="sxs-lookup"><span data-stu-id="f1b93-114">2</span></span>  <br/> |<span data-ttu-id="f1b93-115">Retournement vertical.</span><span class="sxs-lookup"><span data-stu-id="f1b93-115">Flip vertical.</span></span>  <br/> |<span data-ttu-id="f1b93-116">**visLOFlipY**</span><span class="sxs-lookup"><span data-stu-id="f1b93-116">**visLOFlipY**</span></span> <br/> |
|<span data-ttu-id="f1b93-117">4</span><span class="sxs-lookup"><span data-stu-id="f1b93-117">4</span></span>  <br/> |<span data-ttu-id="f1b93-118">Retourner par incréments de 90 degrés entre 0 et 270.</span><span class="sxs-lookup"><span data-stu-id="f1b93-118">Flip in 90 degree increments between 0 and 270.</span></span>  <br/> |<span data-ttu-id="f1b93-119">**visLOFlipRotate**</span><span class="sxs-lookup"><span data-stu-id="f1b93-119">**visLOFlipRotate**</span></span> <br/> |
|<span data-ttu-id="f1b93-120">8</span><span class="sxs-lookup"><span data-stu-id="f1b93-120">8</span></span>  <br/> |<span data-ttu-id="f1b93-121">Ne pas retourner.</span><span class="sxs-lookup"><span data-stu-id="f1b93-121">Do not flip.</span></span>  <br/> |<span data-ttu-id="f1b93-122">**visLOFlipNone**</span><span class="sxs-lookup"><span data-stu-id="f1b93-122">**visLOFlipNone**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f1b93-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="f1b93-123">Remarks</span></span>

<span data-ttu-id="f1b93-124">La valeur de la cellule ShapePlaceFlip facilite l'orientation d'une forme positionnable vers la forme positionnable suivante à laquelle elle est liée.</span><span class="sxs-lookup"><span data-stu-id="f1b93-124">The value in the ShapePlaceFlip cell helps orient a placeable shape toward the next placeable shape it is connected to.</span></span>
  
<span data-ttu-id="f1b93-125">Pour définir ce comportement pour *toutes* les formes sur la page de dessin, utilisez la cellule PlaceFlip de la section Page Layout.</span><span class="sxs-lookup"><span data-stu-id="f1b93-125">To set this behavior for  *all*  the shapes on the drawing page, use the PlaceFlip cell in the Page Layout section.</span></span> 
  
<span data-ttu-id="f1b93-126">Pour obtenir une référence à la cellule ShapePlaceFlip par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="f1b93-126">To get a reference to the ShapePlaceFlip cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f1b93-127">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="f1b93-127">Cell name:</span></span>  <br/> |<span data-ttu-id="f1b93-128">ShapePlaceFlip</span><span class="sxs-lookup"><span data-stu-id="f1b93-128">ShapePlaceFlip</span></span>  <br/> |
   
<span data-ttu-id="f1b93-129">Pour obtenir une référence à la cellule ShapePlaceFlip par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="f1b93-129">To get a reference to the ShapePlaceFlip cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f1b93-130">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="f1b93-130">Section index:</span></span>  <br/> |<span data-ttu-id="f1b93-131">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f1b93-131">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="f1b93-132">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="f1b93-132">Row index:</span></span>  <br/> |<span data-ttu-id="f1b93-133">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="f1b93-133">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="f1b93-134">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="f1b93-134">Cell index:</span></span>  <br/> |<span data-ttu-id="f1b93-135">**visSLOPlaceFlip**</span><span class="sxs-lookup"><span data-stu-id="f1b93-135">**visSLOPlaceFlip**</span></span> <br/> |
   

