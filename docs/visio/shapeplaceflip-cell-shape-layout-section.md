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
description: Détermine la façon dont une forme positionnable est retournée et/ou pivote sur la page lorsque vous disposez des formes à l’aide de la boîte de dialogue Configurer la disposition (dans le groupe Disposition de l’onglet Création, cliquez sur Nouvelle disposition de page, puis cliquez sur Autres options de disposition).
ms.openlocfilehash: 72ef1b67dd87d842e6a4372d1eb08d614f0eb2d3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429277"
---
# <a name="shapeplaceflip-cell-shape-layout-section"></a><span data-ttu-id="108b3-103">ShapePlaceFlip, cellule (section Shape Layout)</span><span class="sxs-lookup"><span data-stu-id="108b3-103">ShapePlaceFlip Cell (Shape Layout Section)</span></span>

<span data-ttu-id="108b3-104">Détermine la façon dont une forme positionnable est retournée et/ou pivote sur la page lorsque vous disposez des formes à l’aide de la boîte de dialogue **Configurer la disposition** (dans le groupe **Disposition** de l’onglet **Création**, cliquez sur **Nouvelle disposition de page**, puis cliquez sur **Autres options de disposition**).</span><span class="sxs-lookup"><span data-stu-id="108b3-104">Determines how a placeable shape flips, rotates, or both on the page when you are laying out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**).</span></span>
  
|<span data-ttu-id="108b3-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="108b3-105">**Value**</span></span>|<span data-ttu-id="108b3-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="108b3-106">**Description**</span></span>|<span data-ttu-id="108b3-107">**Constante d'automation**</span><span class="sxs-lookup"><span data-stu-id="108b3-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="108b3-108">0</span><span class="sxs-lookup"><span data-stu-id="108b3-108">0</span></span>  <br/> |<span data-ttu-id="108b3-109">Utiliser la valeur page par défaut.</span><span class="sxs-lookup"><span data-stu-id="108b3-109">Use page default.</span></span>  <br/> |<span data-ttu-id="108b3-110">**visLOFlipDefault**</span><span class="sxs-lookup"><span data-stu-id="108b3-110">**visLOFlipDefault**</span></span> <br/> |
|<span data-ttu-id="108b3-111">1</span><span class="sxs-lookup"><span data-stu-id="108b3-111">1</span></span>  <br/> |<span data-ttu-id="108b3-112">Retournement horizontal.</span><span class="sxs-lookup"><span data-stu-id="108b3-112">Flip horizontal.</span></span>  <br/> |<span data-ttu-id="108b3-113">**visLOFlipX**</span><span class="sxs-lookup"><span data-stu-id="108b3-113">**visLOFlipX**</span></span> <br/> |
|<span data-ttu-id="108b3-114">2</span><span class="sxs-lookup"><span data-stu-id="108b3-114">2</span></span>  <br/> |<span data-ttu-id="108b3-115">Retournement vertical.</span><span class="sxs-lookup"><span data-stu-id="108b3-115">Flip vertical.</span></span>  <br/> |<span data-ttu-id="108b3-116">**visLOFlipY**</span><span class="sxs-lookup"><span data-stu-id="108b3-116">**visLOFlipY**</span></span> <br/> |
|<span data-ttu-id="108b3-117">4 </span><span class="sxs-lookup"><span data-stu-id="108b3-117">4</span></span>  <br/> |<span data-ttu-id="108b3-118">Retourner par incréments de 90 degrés entre 0 et 270.</span><span class="sxs-lookup"><span data-stu-id="108b3-118">Flip in 90 degree increments between 0 and 270.</span></span>  <br/> |<span data-ttu-id="108b3-119">**visLOFlipRotate**</span><span class="sxs-lookup"><span data-stu-id="108b3-119">**visLOFlipRotate**</span></span> <br/> |
|<span data-ttu-id="108b3-120">8 </span><span class="sxs-lookup"><span data-stu-id="108b3-120">8</span></span>  <br/> |<span data-ttu-id="108b3-121">Ne pas retourner.</span><span class="sxs-lookup"><span data-stu-id="108b3-121">Do not flip.</span></span>  <br/> |<span data-ttu-id="108b3-122">**visLOFlipNone**</span><span class="sxs-lookup"><span data-stu-id="108b3-122">**visLOFlipNone**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="108b3-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="108b3-123">Remarks</span></span>

<span data-ttu-id="108b3-124">La valeur de la cellule ShapePlaceFlip facilite l'orientation d'une forme positionnable vers la forme positionnable suivante à laquelle elle est liée.</span><span class="sxs-lookup"><span data-stu-id="108b3-124">The value in the ShapePlaceFlip cell helps orient a placeable shape toward the next placeable shape it is connected to.</span></span>
  
<span data-ttu-id="108b3-125">Pour définir ce comportement pour  *toutes les*  formes de la page de dessin, utilisez la cellule PlaceFlip dans la section Mise en page.</span><span class="sxs-lookup"><span data-stu-id="108b3-125">To set this behavior for  *all*  the shapes on the drawing page, use the PlaceFlip cell in the Page Layout section.</span></span> 
  
<span data-ttu-id="108b3-126">Pour obtenir une référence à la cellule ShapePlaceFlip par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="108b3-126">To get a reference to the ShapePlaceFlip cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="108b3-127">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="108b3-127">Cell name:</span></span>  <br/> |<span data-ttu-id="108b3-128">ShapePlaceFlip</span><span class="sxs-lookup"><span data-stu-id="108b3-128">ShapePlaceFlip</span></span>  <br/> |
   
<span data-ttu-id="108b3-129">Pour obtenir une référence à la cellule ShapePlaceFlip à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="108b3-129">To get a reference to the ShapePlaceFlip cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="108b3-130">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="108b3-130">Section index:</span></span>  <br/> |<span data-ttu-id="108b3-131">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="108b3-131">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="108b3-132">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="108b3-132">Row index:</span></span>  <br/> |<span data-ttu-id="108b3-133">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="108b3-133">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="108b3-134">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="108b3-134">Cell index:</span></span>  <br/> |<span data-ttu-id="108b3-135">**visSLOPlaceFlip**</span><span class="sxs-lookup"><span data-stu-id="108b3-135">**visSLOPlaceFlip**</span></span> <br/> |
   

