---
title: XGridDensity, cellule (section Ruler &amp; Grid)
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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436040"
---
# <a name="xgriddensity-cell-ruler-amp-grid-section"></a><span data-ttu-id="7cc4e-103">XGridDensity, cellule (section Ruler &amp; Grid)</span><span class="sxs-lookup"><span data-stu-id="7cc4e-103">XGridDensity Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="7cc4e-104">Indique le type de grille horizontale à utiliser.</span><span class="sxs-lookup"><span data-stu-id="7cc4e-104">Specifies the type of horizontal grid to use.</span></span>
  
|<span data-ttu-id="7cc4e-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="7cc4e-105">**Value**</span></span>|<span data-ttu-id="7cc4e-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="7cc4e-106">**Description**</span></span>|<span data-ttu-id="7cc4e-107">**Constante d'automation**</span><span class="sxs-lookup"><span data-stu-id="7cc4e-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7cc4e-108">0</span><span class="sxs-lookup"><span data-stu-id="7cc4e-108">0</span></span>  <br/> |<span data-ttu-id="7cc4e-109">Fixed</span><span class="sxs-lookup"><span data-stu-id="7cc4e-109">Fixed</span></span>  <br/> |<span data-ttu-id="7cc4e-110">**visGridFixed**</span><span class="sxs-lookup"><span data-stu-id="7cc4e-110">**visGridFixed**</span></span> <br/> |
|<span data-ttu-id="7cc4e-111">2 </span><span class="sxs-lookup"><span data-stu-id="7cc4e-111">2</span></span>  <br/> |<span data-ttu-id="7cc4e-112">Entâyé</span><span class="sxs-lookup"><span data-stu-id="7cc4e-112">Coarse</span></span>  <br/> |<span data-ttu-id="7cc4e-113">**visGridCoarse**</span><span class="sxs-lookup"><span data-stu-id="7cc4e-113">**visGridCoarse**</span></span> <br/> |
|<span data-ttu-id="7cc4e-114">4 </span><span class="sxs-lookup"><span data-stu-id="7cc4e-114">4</span></span>  <br/> |<span data-ttu-id="7cc4e-115">Normal (valeur par défaut)</span><span class="sxs-lookup"><span data-stu-id="7cc4e-115">Normal (default)</span></span>  <br/> |<span data-ttu-id="7cc4e-116">**visGridNormal**</span><span class="sxs-lookup"><span data-stu-id="7cc4e-116">**visGridNormal**</span></span> <br/> |
|<span data-ttu-id="7cc4e-117">8 </span><span class="sxs-lookup"><span data-stu-id="7cc4e-117">8</span></span>  <br/> |<span data-ttu-id="7cc4e-118">Fine</span><span class="sxs-lookup"><span data-stu-id="7cc4e-118">Fine</span></span>  <br/> |<span data-ttu-id="7cc4e-119">**visGridFine**</span><span class="sxs-lookup"><span data-stu-id="7cc4e-119">**visGridFine**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7cc4e-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="7cc4e-120">Remarks</span></span>

<span data-ttu-id="7cc4e-121">Cette cellule correspond à l’option  espacement grille horizontal dans  la boîte de dialogue Grille de règle (sous l’onglet Affichage, cliquez sur **Afficher** la flèche). **&amp;**</span><span class="sxs-lookup"><span data-stu-id="7cc4e-121">This cell corresponds to the horizontal **Grid spacing** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="7cc4e-122">Pour obtenir une référence à la cellule XGridDensity par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="7cc4e-122">To get a reference to the XGridDensity cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7cc4e-123">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="7cc4e-123">Cell name:</span></span>  <br/> |<span data-ttu-id="7cc4e-124">XGridDensity</span><span class="sxs-lookup"><span data-stu-id="7cc4e-124">XGridDensity</span></span>  <br/> |
   
<span data-ttu-id="7cc4e-125">Pour obtenir une référence à la cellule XGridDensity par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="7cc4e-125">To get a reference to the XGridDensity cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7cc4e-126">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="7cc4e-126">Section index:</span></span>  <br/> |<span data-ttu-id="7cc4e-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="7cc4e-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="7cc4e-128">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="7cc4e-128">Row index:</span></span>  <br/> |<span data-ttu-id="7cc4e-129">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="7cc4e-129">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="7cc4e-130">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="7cc4e-130">Cell index:</span></span>  <br/> |<span data-ttu-id="7cc4e-131">**visXGridDensity**</span><span class="sxs-lookup"><span data-stu-id="7cc4e-131">**visXGridDensity**</span></span> <br/> |
   

