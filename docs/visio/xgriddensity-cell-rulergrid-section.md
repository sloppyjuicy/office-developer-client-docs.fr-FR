---
title: Cellule XGridDensity (règle &amp; Section grille)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1150
localization_priority: Normal
ms.assetid: db7b353f-4379-8865-1c35-36b89cf93257
description: Indique le type de grille horizontale à utiliser.
ms.openlocfilehash: 107cde8e8b0d630a4dc4b43127412de2f6b0115d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790063"
---
# <a name="xgriddensity-cell-ruler-amp-grid-section"></a><span data-ttu-id="575fb-103">Cellule XGridDensity (règle &amp; Section grille)</span><span class="sxs-lookup"><span data-stu-id="575fb-103">XGridDensity Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="575fb-104">Indique le type de grille horizontale à utiliser.</span><span class="sxs-lookup"><span data-stu-id="575fb-104">Specifies the type of horizontal grid to use.</span></span>
  
|<span data-ttu-id="575fb-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="575fb-105">**Value**</span></span>|<span data-ttu-id="575fb-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="575fb-106">**Description**</span></span>|<span data-ttu-id="575fb-107">**Constante d’Automation**</span><span class="sxs-lookup"><span data-stu-id="575fb-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="575fb-108">0</span><span class="sxs-lookup"><span data-stu-id="575fb-108">0</span></span>  <br/> |<span data-ttu-id="575fb-109">Fixe</span><span class="sxs-lookup"><span data-stu-id="575fb-109">Fixed</span></span>  <br/> |<span data-ttu-id="575fb-110">**visGridFixed**</span><span class="sxs-lookup"><span data-stu-id="575fb-110">**visGridFixed**</span></span> <br/> |
|<span data-ttu-id="575fb-111">2</span><span class="sxs-lookup"><span data-stu-id="575fb-111">2</span></span>  <br/> |<span data-ttu-id="575fb-112">Épais</span><span class="sxs-lookup"><span data-stu-id="575fb-112">Coarse</span></span>  <br/> |<span data-ttu-id="575fb-113">**visGridCoarse**</span><span class="sxs-lookup"><span data-stu-id="575fb-113">**visGridCoarse**</span></span> <br/> |
|<span data-ttu-id="575fb-114">4</span><span class="sxs-lookup"><span data-stu-id="575fb-114">4</span></span>  <br/> |<span data-ttu-id="575fb-115">Normal (valeur par défaut)</span><span class="sxs-lookup"><span data-stu-id="575fb-115">Normal (default)</span></span>  <br/> |<span data-ttu-id="575fb-116">**visGridNormal**</span><span class="sxs-lookup"><span data-stu-id="575fb-116">**visGridNormal**</span></span> <br/> |
|<span data-ttu-id="575fb-117">8</span><span class="sxs-lookup"><span data-stu-id="575fb-117">8</span></span>  <br/> |<span data-ttu-id="575fb-118">Fin</span><span class="sxs-lookup"><span data-stu-id="575fb-118">Fine</span></span>  <br/> |<span data-ttu-id="575fb-119">**visGridFine**</span><span class="sxs-lookup"><span data-stu-id="575fb-119">**visGridFine**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="575fb-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="575fb-120">Remarks</span></span>

<span data-ttu-id="575fb-121">Cette cellule correspond à l' **espacement** horizontal d’option dans le **règle &amp; grille** boîte de dialogue (sous l’onglet **affichage** , cliquez sur la flèche **Afficher** ).</span><span class="sxs-lookup"><span data-stu-id="575fb-121">This cell corresponds to the horizontal **Grid spacing** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="575fb-122">Pour obtenir une référence à la cellule XGridDensity par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="575fb-122">To get a reference to the XGridDensity cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="575fb-123">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="575fb-123">Cell name:</span></span>  <br/> |<span data-ttu-id="575fb-124">XGridDensity</span><span class="sxs-lookup"><span data-stu-id="575fb-124">XGridDensity</span></span>  <br/> |
   
<span data-ttu-id="575fb-125">Pour obtenir une référence à la cellule XGridDensity par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="575fb-125">To get a reference to the XGridDensity cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="575fb-126">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="575fb-126">Section index:</span></span>  <br/> |<span data-ttu-id="575fb-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="575fb-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="575fb-128">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="575fb-128">Row index:</span></span>  <br/> |<span data-ttu-id="575fb-129">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="575fb-129">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="575fb-130">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="575fb-130">Cell index:</span></span>  <br/> |<span data-ttu-id="575fb-131">**visXGridDensity**</span><span class="sxs-lookup"><span data-stu-id="575fb-131">**visXGridDensity**</span></span> <br/> |
   

