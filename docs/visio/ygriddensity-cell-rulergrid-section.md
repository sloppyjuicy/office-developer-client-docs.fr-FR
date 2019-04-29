---
title: Cellule YGridDensity (section &amp; règle et grille)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251363
localization_priority: Normal
ms.assetid: 3ea2b3c7-0c69-a9f2-379f-8daa0c665810
description: Indique le type de grille verticale à utiliser.
ms.openlocfilehash: 793fa40316edd591c8b4873d8919507c2393b5d8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429809"
---
# <a name="ygriddensity-cell-ruler-amp-grid-section"></a><span data-ttu-id="2f4b6-103">Cellule YGridDensity (section &amp; règle et grille)</span><span class="sxs-lookup"><span data-stu-id="2f4b6-103">YGridDensity Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="2f4b6-104">Indique le type de grille verticale à utiliser.</span><span class="sxs-lookup"><span data-stu-id="2f4b6-104">Specifies the type of vertical grid to use.</span></span>
  
|<span data-ttu-id="2f4b6-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="2f4b6-105">**Value**</span></span>|<span data-ttu-id="2f4b6-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="2f4b6-106">**Description**</span></span>|<span data-ttu-id="2f4b6-107">**Constante d'automation**</span><span class="sxs-lookup"><span data-stu-id="2f4b6-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2f4b6-108">0</span><span class="sxs-lookup"><span data-stu-id="2f4b6-108">0</span></span>  <br/> |<span data-ttu-id="2f4b6-109">Fixed</span><span class="sxs-lookup"><span data-stu-id="2f4b6-109">Fixed</span></span>  <br/> |<span data-ttu-id="2f4b6-110">**visGridFixed**</span><span class="sxs-lookup"><span data-stu-id="2f4b6-110">**visGridFixed**</span></span> <br/> |
|<span data-ttu-id="2f4b6-111">n°2</span><span class="sxs-lookup"><span data-stu-id="2f4b6-111">2</span></span>  <br/> |<span data-ttu-id="2f4b6-112">Grossier</span><span class="sxs-lookup"><span data-stu-id="2f4b6-112">Coarse</span></span>  <br/> |<span data-ttu-id="2f4b6-113">**visGridCoarse**</span><span class="sxs-lookup"><span data-stu-id="2f4b6-113">**visGridCoarse**</span></span> <br/> |
|<span data-ttu-id="2f4b6-114">4</span><span class="sxs-lookup"><span data-stu-id="2f4b6-114">4</span></span>  <br/> |<span data-ttu-id="2f4b6-115">Normal (valeur par défaut)</span><span class="sxs-lookup"><span data-stu-id="2f4b6-115">Normal (default)</span></span>  <br/> |<span data-ttu-id="2f4b6-116">**visGridNormal**</span><span class="sxs-lookup"><span data-stu-id="2f4b6-116">**visGridNormal**</span></span> <br/> |
|<span data-ttu-id="2f4b6-117">8bits</span><span class="sxs-lookup"><span data-stu-id="2f4b6-117">8</span></span>  <br/> |<span data-ttu-id="2f4b6-118">Précisément</span><span class="sxs-lookup"><span data-stu-id="2f4b6-118">Fine</span></span>  <br/> |<span data-ttu-id="2f4b6-119">**visGridFine**</span><span class="sxs-lookup"><span data-stu-id="2f4b6-119">**visGridFine**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2f4b6-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="2f4b6-120">Remarks</span></span>

<span data-ttu-id="2f4b6-121">Cette cellule correspond à l'option espacement de la **grille** verticale dans la boîte de dialogue **grille de &amp; règle** (sous l'onglet **affichage** , cliquez sur la flèche **Afficher** ).</span><span class="sxs-lookup"><span data-stu-id="2f4b6-121">This cell corresponds to the vertical **Grid spacing** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="2f4b6-122">Pour obtenir une référence à la cellule XGridDensity par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="2f4b6-122">To get a reference to the YGridDensity cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2f4b6-123">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="2f4b6-123">Cell name:</span></span>  <br/> |<span data-ttu-id="2f4b6-124">YGridDensity</span><span class="sxs-lookup"><span data-stu-id="2f4b6-124">YGridDensity</span></span>  <br/> |
   
<span data-ttu-id="2f4b6-125">Pour obtenir une référence à la cellule XGridDensity par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="2f4b6-125">To get a reference to the YGridDensity cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2f4b6-126">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="2f4b6-126">Section index:</span></span>  <br/> |<span data-ttu-id="2f4b6-127">**Définis**</span><span class="sxs-lookup"><span data-stu-id="2f4b6-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="2f4b6-128">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="2f4b6-128">Row index:</span></span>  <br/> |<span data-ttu-id="2f4b6-129">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="2f4b6-129">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="2f4b6-130">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="2f4b6-130">Cell index:</span></span>  <br/> |<span data-ttu-id="2f4b6-131">**visYGridDensity**</span><span class="sxs-lookup"><span data-stu-id="2f4b6-131">**visYGridDensity**</span></span> <br/> |
   

