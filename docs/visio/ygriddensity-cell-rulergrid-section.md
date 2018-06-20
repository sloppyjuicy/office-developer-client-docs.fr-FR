---
title: Cellule XGridDensity (règle &amp; Section grille)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251363
localization_priority: Normal
ms.assetid: 3ea2b3c7-0c69-a9f2-379f-8daa0c665810
description: Indique le type de grille verticale à utiliser.
ms.openlocfilehash: 4e0d1b1dc6f3da95b9328342e0398313b6c85eb4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790093"
---
# <a name="ygriddensity-cell-ruler-amp-grid-section"></a><span data-ttu-id="2e992-103">Cellule XGridDensity (règle &amp; Section grille)</span><span class="sxs-lookup"><span data-stu-id="2e992-103">YGridDensity Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="2e992-104">Indique le type de grille verticale à utiliser.</span><span class="sxs-lookup"><span data-stu-id="2e992-104">Specifies the type of vertical grid to use.</span></span>
  
|<span data-ttu-id="2e992-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="2e992-105">**Value**</span></span>|<span data-ttu-id="2e992-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="2e992-106">**Description**</span></span>|<span data-ttu-id="2e992-107">**Constante d’Automation**</span><span class="sxs-lookup"><span data-stu-id="2e992-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2e992-108">0</span><span class="sxs-lookup"><span data-stu-id="2e992-108">0</span></span>  <br/> |<span data-ttu-id="2e992-109">Fixe</span><span class="sxs-lookup"><span data-stu-id="2e992-109">Fixed</span></span>  <br/> |<span data-ttu-id="2e992-110">**visGridFixed**</span><span class="sxs-lookup"><span data-stu-id="2e992-110">**visGridFixed**</span></span> <br/> |
|<span data-ttu-id="2e992-111">2</span><span class="sxs-lookup"><span data-stu-id="2e992-111">2</span></span>  <br/> |<span data-ttu-id="2e992-112">Épais</span><span class="sxs-lookup"><span data-stu-id="2e992-112">Coarse</span></span>  <br/> |<span data-ttu-id="2e992-113">**visGridCoarse**</span><span class="sxs-lookup"><span data-stu-id="2e992-113">**visGridCoarse**</span></span> <br/> |
|<span data-ttu-id="2e992-114">4</span><span class="sxs-lookup"><span data-stu-id="2e992-114">4</span></span>  <br/> |<span data-ttu-id="2e992-115">Normal (valeur par défaut)</span><span class="sxs-lookup"><span data-stu-id="2e992-115">Normal (default)</span></span>  <br/> |<span data-ttu-id="2e992-116">**visGridNormal**</span><span class="sxs-lookup"><span data-stu-id="2e992-116">**visGridNormal**</span></span> <br/> |
|<span data-ttu-id="2e992-117">8</span><span class="sxs-lookup"><span data-stu-id="2e992-117">8</span></span>  <br/> |<span data-ttu-id="2e992-118">Fin</span><span class="sxs-lookup"><span data-stu-id="2e992-118">Fine</span></span>  <br/> |<span data-ttu-id="2e992-119">**visGridFine**</span><span class="sxs-lookup"><span data-stu-id="2e992-119">**visGridFine**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2e992-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="2e992-120">Remarks</span></span>

<span data-ttu-id="2e992-121">Cette cellule correspond à l' **espacement** vertical d’option dans le **règle &amp; grille** boîte de dialogue (sous l’onglet **affichage** , cliquez sur la flèche **Afficher** ).</span><span class="sxs-lookup"><span data-stu-id="2e992-121">This cell corresponds to the vertical **Grid spacing** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="2e992-122">Pour obtenir une référence à la cellule XGridDensity par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="2e992-122">To get a reference to the YGridDensity cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2e992-123">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="2e992-123">Cell name:</span></span>  <br/> |<span data-ttu-id="2e992-124">XGridDensity</span><span class="sxs-lookup"><span data-stu-id="2e992-124">YGridDensity</span></span>  <br/> |
   
<span data-ttu-id="2e992-125">Pour obtenir une référence à la cellule XGridDensity par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="2e992-125">To get a reference to the YGridDensity cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2e992-126">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="2e992-126">Section index:</span></span>  <br/> |<span data-ttu-id="2e992-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="2e992-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="2e992-128">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="2e992-128">Row index:</span></span>  <br/> |<span data-ttu-id="2e992-129">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="2e992-129">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="2e992-130">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="2e992-130">Cell index:</span></span>  <br/> |<span data-ttu-id="2e992-131">**visYGridDensity**</span><span class="sxs-lookup"><span data-stu-id="2e992-131">**visYGridDensity**</span></span> <br/> |
   

