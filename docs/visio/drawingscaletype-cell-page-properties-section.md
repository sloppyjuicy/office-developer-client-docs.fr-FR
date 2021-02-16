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
description: Détermine l’échelle de dessin sélectionnée dans la boîte de dialogue Mise en page (cliquez sur la flèche Mise en page sous l’onglet Accueil).
ms.openlocfilehash: d1c1c00ffe025c566646a1f8b9fe034732ad86a8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428738"
---
# <a name="drawingscaletype-cell-page-properties-section"></a><span data-ttu-id="97f05-103">DrawingScaleType, cellule (section Page Properties)</span><span class="sxs-lookup"><span data-stu-id="97f05-103">DrawingScaleType Cell (Page Properties Section)</span></span>

<span data-ttu-id="97f05-104">Détermine l’échelle de dessin sélectionnée dans la boîte de dialogue **Mise en page** (cliquez sur la flèche **Mise en page** sous l’onglet **Accueil**).</span><span class="sxs-lookup"><span data-stu-id="97f05-104">Determines the drawing scale selected in the **Page Setup** dialog box (click the **Page Setup** arrow on the **Home** tab).</span></span> 
  
|<span data-ttu-id="97f05-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="97f05-105">**Value**</span></span>|<span data-ttu-id="97f05-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="97f05-106">**Description**</span></span>|<span data-ttu-id="97f05-107">**Constante d'automation**</span><span class="sxs-lookup"><span data-stu-id="97f05-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="97f05-108">0</span><span class="sxs-lookup"><span data-stu-id="97f05-108">0</span></span>  <br/> | <span data-ttu-id="97f05-109">Pas d'échelle</span><span class="sxs-lookup"><span data-stu-id="97f05-109">No Scale</span></span>  <br/> |<span data-ttu-id="97f05-110">**visNoScale**</span><span class="sxs-lookup"><span data-stu-id="97f05-110">**visNoScale**</span></span> <br/> |
| <span data-ttu-id="97f05-111">1 </span><span class="sxs-lookup"><span data-stu-id="97f05-111">1</span></span>  <br/> | <span data-ttu-id="97f05-112">Échelle architecturale</span><span class="sxs-lookup"><span data-stu-id="97f05-112">Architectural Scale</span></span>  <br/> |<span data-ttu-id="97f05-113">**visArchitectural**</span><span class="sxs-lookup"><span data-stu-id="97f05-113">**visArchitectural**</span></span> <br/> |
| <span data-ttu-id="97f05-114">2 </span><span class="sxs-lookup"><span data-stu-id="97f05-114">2</span></span>  <br/> | <span data-ttu-id="97f05-115">Échelle Génie civil</span><span class="sxs-lookup"><span data-stu-id="97f05-115">Civil Engineering Scale</span></span>  <br/> |<span data-ttu-id="97f05-116">**visEngineering**</span><span class="sxs-lookup"><span data-stu-id="97f05-116">**visEngineering**</span></span> <br/> |
| <span data-ttu-id="97f05-117">3 </span><span class="sxs-lookup"><span data-stu-id="97f05-117">3</span></span>  <br/> | <span data-ttu-id="97f05-118">Échelle personnalisée</span><span class="sxs-lookup"><span data-stu-id="97f05-118">Custom Scale</span></span>  <br/> |<span data-ttu-id="97f05-119">**visScaleCustom**</span><span class="sxs-lookup"><span data-stu-id="97f05-119">**visScaleCustom**</span></span> <br/> |
| <span data-ttu-id="97f05-120">4 </span><span class="sxs-lookup"><span data-stu-id="97f05-120">4</span></span>  <br/> | <span data-ttu-id="97f05-121">Métrique</span><span class="sxs-lookup"><span data-stu-id="97f05-121">Metric</span></span>  <br/> |<span data-ttu-id="97f05-122">**visScaleMetric**</span><span class="sxs-lookup"><span data-stu-id="97f05-122">**visScaleMetric**</span></span> <br/> |
| <span data-ttu-id="97f05-123">5 </span><span class="sxs-lookup"><span data-stu-id="97f05-123">5</span></span>  <br/> | <span data-ttu-id="97f05-124">Échelle Génie mécanique</span><span class="sxs-lookup"><span data-stu-id="97f05-124">Mechanical Engineering Scale</span></span>  <br/> |<span data-ttu-id="97f05-125">**visScaleMechanical**</span><span class="sxs-lookup"><span data-stu-id="97f05-125">**visScaleMechanical**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="97f05-126">Remarques</span><span class="sxs-lookup"><span data-stu-id="97f05-126">Remarks</span></span>

<span data-ttu-id="97f05-127">Pour obtenir une référence à la cellule DrawingScaleType par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="97f05-127">To get a reference to the DrawingScaleType cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="97f05-128">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="97f05-128">Cell name:</span></span>  <br/> | <span data-ttu-id="97f05-129">DrawingScaleType</span><span class="sxs-lookup"><span data-stu-id="97f05-129">DrawingScaleType</span></span>  <br/> |
   
<span data-ttu-id="97f05-130">Pour obtenir une référence à la cellule DrawingScaleType à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="97f05-130">To get a reference to the DrawingScaleType cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="97f05-131">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="97f05-131">Section index:</span></span>  <br/> |<span data-ttu-id="97f05-132">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="97f05-132">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="97f05-133">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="97f05-133">Row index:</span></span>  <br/> |<span data-ttu-id="97f05-134">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="97f05-134">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="97f05-135">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="97f05-135">Cell index:</span></span>  <br/> |<span data-ttu-id="97f05-136">**visPageDrawScaleType**</span><span class="sxs-lookup"><span data-stu-id="97f05-136">**visPageDrawScaleType**</span></span> <br/> |
   

