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
# <a name="xgriddensity-cell-ruler-amp-grid-section"></a><span data-ttu-id="8c938-103">XGridDensity, cellule (section Ruler &amp; Grid)</span><span class="sxs-lookup"><span data-stu-id="8c938-103">XGridDensity Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="8c938-104">Indique le type de grille horizontale à utiliser.</span><span class="sxs-lookup"><span data-stu-id="8c938-104">Specifies the type of horizontal grid to use.</span></span>
  
|<span data-ttu-id="8c938-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="8c938-105">**Value**</span></span>|<span data-ttu-id="8c938-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="8c938-106">**Description**</span></span>|<span data-ttu-id="8c938-107">**Constante d'automation**</span><span class="sxs-lookup"><span data-stu-id="8c938-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8c938-108">0</span><span class="sxs-lookup"><span data-stu-id="8c938-108">0</span></span>  <br/> |<span data-ttu-id="8c938-109">Fixed</span><span class="sxs-lookup"><span data-stu-id="8c938-109">Fixed</span></span>  <br/> |<span data-ttu-id="8c938-110">**visGridFixed**</span><span class="sxs-lookup"><span data-stu-id="8c938-110">**visGridFixed**</span></span> <br/> |
|<span data-ttu-id="8c938-111">2</span><span class="sxs-lookup"><span data-stu-id="8c938-111">2</span></span>  <br/> |<span data-ttu-id="8c938-112">Entâyé</span><span class="sxs-lookup"><span data-stu-id="8c938-112">Coarse</span></span>  <br/> |<span data-ttu-id="8c938-113">**visGridCoarse**</span><span class="sxs-lookup"><span data-stu-id="8c938-113">**visGridCoarse**</span></span> <br/> |
|<span data-ttu-id="8c938-114">4 </span><span class="sxs-lookup"><span data-stu-id="8c938-114">4</span></span>  <br/> |<span data-ttu-id="8c938-115">Normal (valeur par défaut)</span><span class="sxs-lookup"><span data-stu-id="8c938-115">Normal (default)</span></span>  <br/> |<span data-ttu-id="8c938-116">**visGridNormal**</span><span class="sxs-lookup"><span data-stu-id="8c938-116">**visGridNormal**</span></span> <br/> |
|<span data-ttu-id="8c938-117">8 </span><span class="sxs-lookup"><span data-stu-id="8c938-117">8</span></span>  <br/> |<span data-ttu-id="8c938-118">Fine</span><span class="sxs-lookup"><span data-stu-id="8c938-118">Fine</span></span>  <br/> |<span data-ttu-id="8c938-119">**visGridFine**</span><span class="sxs-lookup"><span data-stu-id="8c938-119">**visGridFine**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8c938-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="8c938-120">Remarks</span></span>

<span data-ttu-id="8c938-121">Cette cellule correspond à l’option  espacement grille horizontal dans  la boîte de dialogue Grille de règle (sous l’onglet Affichage, cliquez sur **Afficher** la flèche). **&amp;**</span><span class="sxs-lookup"><span data-stu-id="8c938-121">This cell corresponds to the horizontal **Grid spacing** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="8c938-122">Pour obtenir une référence à la cellule XGridDensity par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="8c938-122">To get a reference to the XGridDensity cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8c938-123">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="8c938-123">Cell name:</span></span>  <br/> |<span data-ttu-id="8c938-124">XGridDensity</span><span class="sxs-lookup"><span data-stu-id="8c938-124">XGridDensity</span></span>  <br/> |
   
<span data-ttu-id="8c938-125">Pour obtenir une référence à la cellule XGridDensity par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="8c938-125">To get a reference to the XGridDensity cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8c938-126">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="8c938-126">Section index:</span></span>  <br/> |<span data-ttu-id="8c938-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="8c938-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="8c938-128">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="8c938-128">Row index:</span></span>  <br/> |<span data-ttu-id="8c938-129">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="8c938-129">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="8c938-130">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="8c938-130">Cell index:</span></span>  <br/> |<span data-ttu-id="8c938-131">**visXGridDensity**</span><span class="sxs-lookup"><span data-stu-id="8c938-131">**visXGridDensity**</span></span> <br/> |
   

