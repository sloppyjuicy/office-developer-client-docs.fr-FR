---
title: Cellule XGridDensity (section &amp; règle et grille)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1150
localization_priority: Normal
ms.assetid: db7b353f-4379-8865-1c35-36b89cf93257
description: Indique le type de grille horizontale à utiliser.
ms.openlocfilehash: 5ebd172e56a66bfb39bd9bfa20967bb6b52c5aa2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328985"
---
# <a name="xgriddensity-cell-ruler-amp-grid-section"></a><span data-ttu-id="b263a-103">Cellule XGridDensity (section &amp; règle et grille)</span><span class="sxs-lookup"><span data-stu-id="b263a-103">XGridDensity Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="b263a-104">Indique le type de grille horizontale à utiliser.</span><span class="sxs-lookup"><span data-stu-id="b263a-104">Specifies the type of horizontal grid to use.</span></span>
  
|<span data-ttu-id="b263a-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="b263a-105">**Value**</span></span>|<span data-ttu-id="b263a-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="b263a-106">**Description**</span></span>|<span data-ttu-id="b263a-107">**Constante d'automation**</span><span class="sxs-lookup"><span data-stu-id="b263a-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b263a-108">0</span><span class="sxs-lookup"><span data-stu-id="b263a-108">0</span></span>  <br/> |<span data-ttu-id="b263a-109">Fixed</span><span class="sxs-lookup"><span data-stu-id="b263a-109">Fixed</span></span>  <br/> |<span data-ttu-id="b263a-110">**visGridFixed**</span><span class="sxs-lookup"><span data-stu-id="b263a-110">**visGridFixed**</span></span> <br/> |
|<span data-ttu-id="b263a-111">n°2</span><span class="sxs-lookup"><span data-stu-id="b263a-111">2</span></span>  <br/> |<span data-ttu-id="b263a-112">Grossier</span><span class="sxs-lookup"><span data-stu-id="b263a-112">Coarse</span></span>  <br/> |<span data-ttu-id="b263a-113">**visGridCoarse**</span><span class="sxs-lookup"><span data-stu-id="b263a-113">**visGridCoarse**</span></span> <br/> |
|<span data-ttu-id="b263a-114">4</span><span class="sxs-lookup"><span data-stu-id="b263a-114">4</span></span>  <br/> |<span data-ttu-id="b263a-115">Normal (valeur par défaut)</span><span class="sxs-lookup"><span data-stu-id="b263a-115">Normal (default)</span></span>  <br/> |<span data-ttu-id="b263a-116">**visGridNormal**</span><span class="sxs-lookup"><span data-stu-id="b263a-116">**visGridNormal**</span></span> <br/> |
|<span data-ttu-id="b263a-117">8bits</span><span class="sxs-lookup"><span data-stu-id="b263a-117">8</span></span>  <br/> |<span data-ttu-id="b263a-118">Précisément</span><span class="sxs-lookup"><span data-stu-id="b263a-118">Fine</span></span>  <br/> |<span data-ttu-id="b263a-119">**visGridFine**</span><span class="sxs-lookup"><span data-stu-id="b263a-119">**visGridFine**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b263a-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="b263a-120">Remarks</span></span>

<span data-ttu-id="b263a-121">Cette cellule correspond à l'option espacement horizontal de la **grille** dans la boîte de dialogue **règle de &amp; règle** (sous l'onglet **affichage** , cliquez sur la flèche **Afficher** ).</span><span class="sxs-lookup"><span data-stu-id="b263a-121">This cell corresponds to the horizontal **Grid spacing** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="b263a-122">Pour obtenir une référence à la cellule XGridDensity par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="b263a-122">To get a reference to the XGridDensity cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b263a-123">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="b263a-123">Cell name:</span></span>  <br/> |<span data-ttu-id="b263a-124">XGridDensity</span><span class="sxs-lookup"><span data-stu-id="b263a-124">XGridDensity</span></span>  <br/> |
   
<span data-ttu-id="b263a-125">Pour obtenir une référence à la cellule XGridDensity par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="b263a-125">To get a reference to the XGridDensity cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b263a-126">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="b263a-126">Section index:</span></span>  <br/> |<span data-ttu-id="b263a-127">**Définis**</span><span class="sxs-lookup"><span data-stu-id="b263a-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="b263a-128">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="b263a-128">Row index:</span></span>  <br/> |<span data-ttu-id="b263a-129">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="b263a-129">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="b263a-130">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="b263a-130">Cell index:</span></span>  <br/> |<span data-ttu-id="b263a-131">**visXGridDensity**</span><span class="sxs-lookup"><span data-stu-id="b263a-131">**visXGridDensity**</span></span> <br/> |
   

