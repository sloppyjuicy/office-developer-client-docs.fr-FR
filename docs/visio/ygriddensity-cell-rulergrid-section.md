---
title: YGridDensity, cellule (section Ruler &amp; Grid)
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
# <a name="ygriddensity-cell-ruler-amp-grid-section"></a><span data-ttu-id="b09f5-103">YGridDensity, cellule (section Ruler &amp; Grid)</span><span class="sxs-lookup"><span data-stu-id="b09f5-103">YGridDensity Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="b09f5-104">Indique le type de grille verticale à utiliser.</span><span class="sxs-lookup"><span data-stu-id="b09f5-104">Specifies the type of vertical grid to use.</span></span>
  
|<span data-ttu-id="b09f5-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="b09f5-105">**Value**</span></span>|<span data-ttu-id="b09f5-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="b09f5-106">**Description**</span></span>|<span data-ttu-id="b09f5-107">**Constante d'automation**</span><span class="sxs-lookup"><span data-stu-id="b09f5-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b09f5-108">0</span><span class="sxs-lookup"><span data-stu-id="b09f5-108">0</span></span>  <br/> |<span data-ttu-id="b09f5-109">Fixed</span><span class="sxs-lookup"><span data-stu-id="b09f5-109">Fixed</span></span>  <br/> |<span data-ttu-id="b09f5-110">**visGridFixed**</span><span class="sxs-lookup"><span data-stu-id="b09f5-110">**visGridFixed**</span></span> <br/> |
|<span data-ttu-id="b09f5-111">2 </span><span class="sxs-lookup"><span data-stu-id="b09f5-111">2</span></span>  <br/> |<span data-ttu-id="b09f5-112">Entâyé</span><span class="sxs-lookup"><span data-stu-id="b09f5-112">Coarse</span></span>  <br/> |<span data-ttu-id="b09f5-113">**visGridCoarse**</span><span class="sxs-lookup"><span data-stu-id="b09f5-113">**visGridCoarse**</span></span> <br/> |
|<span data-ttu-id="b09f5-114">4 </span><span class="sxs-lookup"><span data-stu-id="b09f5-114">4</span></span>  <br/> |<span data-ttu-id="b09f5-115">Normal (valeur par défaut)</span><span class="sxs-lookup"><span data-stu-id="b09f5-115">Normal (default)</span></span>  <br/> |<span data-ttu-id="b09f5-116">**visGridNormal**</span><span class="sxs-lookup"><span data-stu-id="b09f5-116">**visGridNormal**</span></span> <br/> |
|<span data-ttu-id="b09f5-117">8 </span><span class="sxs-lookup"><span data-stu-id="b09f5-117">8</span></span>  <br/> |<span data-ttu-id="b09f5-118">Fine</span><span class="sxs-lookup"><span data-stu-id="b09f5-118">Fine</span></span>  <br/> |<span data-ttu-id="b09f5-119">**visGridFine**</span><span class="sxs-lookup"><span data-stu-id="b09f5-119">**visGridFine**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b09f5-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="b09f5-120">Remarks</span></span>

<span data-ttu-id="b09f5-121">Cette cellule correspond à l’option  d’espacement de la  grille verticale dans la boîte de dialogue Grille de règle (sous l’onglet Affichage, cliquez sur **Afficher** la flèche). **&amp;**</span><span class="sxs-lookup"><span data-stu-id="b09f5-121">This cell corresponds to the vertical **Grid spacing** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="b09f5-122">Pour obtenir une référence à la cellule XGridDensity par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="b09f5-122">To get a reference to the YGridDensity cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b09f5-123">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="b09f5-123">Cell name:</span></span>  <br/> |<span data-ttu-id="b09f5-124">YGridDensity</span><span class="sxs-lookup"><span data-stu-id="b09f5-124">YGridDensity</span></span>  <br/> |
   
<span data-ttu-id="b09f5-125">Pour obtenir une référence à la cellule XGridDensity par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="b09f5-125">To get a reference to the YGridDensity cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b09f5-126">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="b09f5-126">Section index:</span></span>  <br/> |<span data-ttu-id="b09f5-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b09f5-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="b09f5-128">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="b09f5-128">Row index:</span></span>  <br/> |<span data-ttu-id="b09f5-129">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="b09f5-129">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="b09f5-130">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="b09f5-130">Cell index:</span></span>  <br/> |<span data-ttu-id="b09f5-131">**visYGridDensity**</span><span class="sxs-lookup"><span data-stu-id="b09f5-131">**visYGridDensity**</span></span> <br/> |
   

