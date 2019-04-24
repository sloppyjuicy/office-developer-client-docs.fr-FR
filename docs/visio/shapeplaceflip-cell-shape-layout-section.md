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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332668"
---
# <a name="shapeplaceflip-cell-shape-layout-section"></a><span data-ttu-id="333bf-103">ShapePlaceFlip, cellule (section Shape Layout)</span><span class="sxs-lookup"><span data-stu-id="333bf-103">ShapePlaceFlip Cell (Shape Layout Section)</span></span>

<span data-ttu-id="333bf-104">Détermine la façon dont une forme positionnable est retournée et/ou pivote sur la page lorsque vous disposez des formes à l’aide de la boîte de dialogue **Configurer la disposition** (dans le groupe **Disposition** de l’onglet **Création**, cliquez sur **Nouvelle disposition de page**, puis cliquez sur **Autres options de disposition**).</span><span class="sxs-lookup"><span data-stu-id="333bf-104">Determines how a placeable shape flips, rotates, or both on the page when you are laying out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**).</span></span>
  
|<span data-ttu-id="333bf-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="333bf-105">**Value**</span></span>|<span data-ttu-id="333bf-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="333bf-106">**Description**</span></span>|<span data-ttu-id="333bf-107">**Constante d'automation**</span><span class="sxs-lookup"><span data-stu-id="333bf-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="333bf-108">0</span><span class="sxs-lookup"><span data-stu-id="333bf-108">0</span></span>  <br/> |<span data-ttu-id="333bf-109">Utiliser la valeur page par défaut.</span><span class="sxs-lookup"><span data-stu-id="333bf-109">Use page default.</span></span>  <br/> |<span data-ttu-id="333bf-110">**visLOFlipDefault**</span><span class="sxs-lookup"><span data-stu-id="333bf-110">**visLOFlipDefault**</span></span> <br/> |
|<span data-ttu-id="333bf-111">0,1</span><span class="sxs-lookup"><span data-stu-id="333bf-111">1</span></span>  <br/> |<span data-ttu-id="333bf-112">Retournement horizontal.</span><span class="sxs-lookup"><span data-stu-id="333bf-112">Flip horizontal.</span></span>  <br/> |<span data-ttu-id="333bf-113">**visLOFlipX**</span><span class="sxs-lookup"><span data-stu-id="333bf-113">**visLOFlipX**</span></span> <br/> |
|<span data-ttu-id="333bf-114">n°2</span><span class="sxs-lookup"><span data-stu-id="333bf-114">2</span></span>  <br/> |<span data-ttu-id="333bf-115">Retournement vertical.</span><span class="sxs-lookup"><span data-stu-id="333bf-115">Flip vertical.</span></span>  <br/> |<span data-ttu-id="333bf-116">**visLOFlipY**</span><span class="sxs-lookup"><span data-stu-id="333bf-116">**visLOFlipY**</span></span> <br/> |
|<span data-ttu-id="333bf-117">4</span><span class="sxs-lookup"><span data-stu-id="333bf-117">4</span></span>  <br/> |<span data-ttu-id="333bf-118">Retourner par incréments de 90 degrés entre 0 et 270.</span><span class="sxs-lookup"><span data-stu-id="333bf-118">Flip in 90 degree increments between 0 and 270.</span></span>  <br/> |<span data-ttu-id="333bf-119">**visLOFlipRotate**</span><span class="sxs-lookup"><span data-stu-id="333bf-119">**visLOFlipRotate**</span></span> <br/> |
|<span data-ttu-id="333bf-120">8bits</span><span class="sxs-lookup"><span data-stu-id="333bf-120">8</span></span>  <br/> |<span data-ttu-id="333bf-121">Ne pas retourner.</span><span class="sxs-lookup"><span data-stu-id="333bf-121">Do not flip.</span></span>  <br/> |<span data-ttu-id="333bf-122">**visLOFlipNone**</span><span class="sxs-lookup"><span data-stu-id="333bf-122">**visLOFlipNone**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="333bf-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="333bf-123">Remarks</span></span>

<span data-ttu-id="333bf-124">La valeur de la cellule ShapePlaceFlip facilite l'orientation d'une forme positionnable vers la forme positionnable suivante à laquelle elle est liée.</span><span class="sxs-lookup"><span data-stu-id="333bf-124">The value in the ShapePlaceFlip cell helps orient a placeable shape toward the next placeable shape it is connected to.</span></span>
  
<span data-ttu-id="333bf-125">Pour définir ce comportement pour *toutes* les formes de la page de dessin, utilisez la cellule PlaceFlip de la section Page Layout.</span><span class="sxs-lookup"><span data-stu-id="333bf-125">To set this behavior for  *all*  the shapes on the drawing page, use the PlaceFlip cell in the Page Layout section.</span></span> 
  
<span data-ttu-id="333bf-126">Pour obtenir une référence à la cellule ShapePlaceFlip par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="333bf-126">To get a reference to the ShapePlaceFlip cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="333bf-127">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="333bf-127">Cell name:</span></span>  <br/> |<span data-ttu-id="333bf-128">ShapePlaceFlip</span><span class="sxs-lookup"><span data-stu-id="333bf-128">ShapePlaceFlip</span></span>  <br/> |
   
<span data-ttu-id="333bf-129">Pour obtenir une référence à la cellule ShapePlaceFlip à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="333bf-129">To get a reference to the ShapePlaceFlip cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="333bf-130">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="333bf-130">Section index:</span></span>  <br/> |<span data-ttu-id="333bf-131">**Définis**</span><span class="sxs-lookup"><span data-stu-id="333bf-131">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="333bf-132">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="333bf-132">Row index:</span></span>  <br/> |<span data-ttu-id="333bf-133">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="333bf-133">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="333bf-134">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="333bf-134">Cell index:</span></span>  <br/> |<span data-ttu-id="333bf-135">**visSLOPlaceFlip**</span><span class="sxs-lookup"><span data-stu-id="333bf-135">**visSLOPlaceFlip**</span></span> <br/> |
   

