---
title: DrawingScaleType, cellule (section Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm270
localization_priority: Normal
ms.assetid: 5d4f1cf8-bc1f-07b8-1da5-7253808e337e
description: Détermine l’échelle de dessin sélectionnée dans la boîte de dialogue Mise en Page (cliquez sur la flèche mise en Page sous l’onglet Accueil).
ms.openlocfilehash: b93bd95a30fe5a8a5de15a8e5ea104279cf1bcda
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788531"
---
# <a name="drawingscaletype-cell-page-properties-section"></a><span data-ttu-id="752e4-103">DrawingScaleType, cellule (section Page Properties)</span><span class="sxs-lookup"><span data-stu-id="752e4-103">DrawingScaleType Cell (Page Properties Section)</span></span>

<span data-ttu-id="752e4-104">Détermine l’échelle de dessin sélectionnée dans la boîte de dialogue **Mise en Page** (cliquez sur la flèche **Mise en Page** sous l’onglet **accueil** ).</span><span class="sxs-lookup"><span data-stu-id="752e4-104">Determines the drawing scale selected in the **Page Setup** dialog box (click the **Page Setup** arrow on the **Home** tab).</span></span> 
  
|<span data-ttu-id="752e4-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="752e4-105">**Value**</span></span>|<span data-ttu-id="752e4-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="752e4-106">**Description**</span></span>|<span data-ttu-id="752e4-107">**Constante d’Automation**</span><span class="sxs-lookup"><span data-stu-id="752e4-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="752e4-108">0</span><span class="sxs-lookup"><span data-stu-id="752e4-108">0</span></span>  <br/> | <span data-ttu-id="752e4-109">Pas d'échelle</span><span class="sxs-lookup"><span data-stu-id="752e4-109">No Scale</span></span>  <br/> |<span data-ttu-id="752e4-110">**visNoScale**</span><span class="sxs-lookup"><span data-stu-id="752e4-110">**visNoScale**</span></span> <br/> |
| <span data-ttu-id="752e4-111">1</span><span class="sxs-lookup"><span data-stu-id="752e4-111">1</span></span>  <br/> | <span data-ttu-id="752e4-112">Échelle architecturale</span><span class="sxs-lookup"><span data-stu-id="752e4-112">Architectural Scale</span></span>  <br/> |<span data-ttu-id="752e4-113">**visArchitectural**</span><span class="sxs-lookup"><span data-stu-id="752e4-113">**visArchitectural**</span></span> <br/> |
| <span data-ttu-id="752e4-114">2</span><span class="sxs-lookup"><span data-stu-id="752e4-114">2</span></span>  <br/> | <span data-ttu-id="752e4-115">Échelle Génie civil</span><span class="sxs-lookup"><span data-stu-id="752e4-115">Civil Engineering Scale</span></span>  <br/> |<span data-ttu-id="752e4-116">**visEngineering**</span><span class="sxs-lookup"><span data-stu-id="752e4-116">**visEngineering**</span></span> <br/> |
| <span data-ttu-id="752e4-117">3</span><span class="sxs-lookup"><span data-stu-id="752e4-117">3</span></span>  <br/> | <span data-ttu-id="752e4-118">Échelle personnalisée</span><span class="sxs-lookup"><span data-stu-id="752e4-118">Custom Scale</span></span>  <br/> |<span data-ttu-id="752e4-119">**visScaleCustom**</span><span class="sxs-lookup"><span data-stu-id="752e4-119">**visScaleCustom**</span></span> <br/> |
| <span data-ttu-id="752e4-120">4</span><span class="sxs-lookup"><span data-stu-id="752e4-120">4</span></span>  <br/> | <span data-ttu-id="752e4-121">Métrique</span><span class="sxs-lookup"><span data-stu-id="752e4-121">Metric</span></span>  <br/> |<span data-ttu-id="752e4-122">**visScaleMetric**</span><span class="sxs-lookup"><span data-stu-id="752e4-122">**visScaleMetric**</span></span> <br/> |
| <span data-ttu-id="752e4-123">5</span><span class="sxs-lookup"><span data-stu-id="752e4-123">5</span></span>  <br/> | <span data-ttu-id="752e4-124">Échelle Génie mécanique</span><span class="sxs-lookup"><span data-stu-id="752e4-124">Mechanical Engineering Scale</span></span>  <br/> |<span data-ttu-id="752e4-125">**visScaleMechanical**</span><span class="sxs-lookup"><span data-stu-id="752e4-125">**visScaleMechanical**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="752e4-126">Remarques</span><span class="sxs-lookup"><span data-stu-id="752e4-126">Remarks</span></span>

<span data-ttu-id="752e4-127">Pour obtenir une référence à la cellule DrawingScaleType par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="752e4-127">To get a reference to the DrawingScaleType cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="752e4-128">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="752e4-128">Cell name:</span></span>  <br/> | <span data-ttu-id="752e4-129">DrawingScaleType</span><span class="sxs-lookup"><span data-stu-id="752e4-129">DrawingScaleType</span></span>  <br/> |
   
<span data-ttu-id="752e4-130">Pour obtenir une référence à la cellule DrawingScaleType par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="752e4-130">To get a reference to the DrawingScaleType cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="752e4-131">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="752e4-131">Section index:</span></span>  <br/> |<span data-ttu-id="752e4-132">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="752e4-132">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="752e4-133">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="752e4-133">Row index:</span></span>  <br/> |<span data-ttu-id="752e4-134">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="752e4-134">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="752e4-135">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="752e4-135">Cell index:</span></span>  <br/> |<span data-ttu-id="752e4-136">**visPageDrawScaleType**</span><span class="sxs-lookup"><span data-stu-id="752e4-136">**visPageDrawScaleType**</span></span> <br/> |
   

