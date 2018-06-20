---
title: Cellule XRulerDensity (règle &amp; Section grille)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1165
localization_priority: Normal
ms.assetid: c11717c5-eb0e-e4fa-5a91-c62ecc048635
description: Définit les graduations horizontales de la règle pour la page.
ms.openlocfilehash: 633b2e54ca77216fd20ead00f047283c54f8164d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790059"
---
# <a name="xrulerdensity-cell-ruler-amp-grid-section"></a><span data-ttu-id="e3fd3-103">Cellule XRulerDensity (règle &amp; Section grille)</span><span class="sxs-lookup"><span data-stu-id="e3fd3-103">XRulerDensity Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="e3fd3-104">Définit les graduations horizontales de la règle pour la page.</span><span class="sxs-lookup"><span data-stu-id="e3fd3-104">Specifies the horizontal subdivisions on the ruler for the page.</span></span>
  
|<span data-ttu-id="e3fd3-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="e3fd3-105">**Value**</span></span>|<span data-ttu-id="e3fd3-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="e3fd3-106">**Description**</span></span>|<span data-ttu-id="e3fd3-107">**Constante d’Automation**</span><span class="sxs-lookup"><span data-stu-id="e3fd3-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e3fd3-108">0</span><span class="sxs-lookup"><span data-stu-id="e3fd3-108">0</span></span>  <br/> |<span data-ttu-id="e3fd3-109">Fixe</span><span class="sxs-lookup"><span data-stu-id="e3fd3-109">Fixed</span></span>  <br/> |<span data-ttu-id="e3fd3-110">**visRulerFixed**</span><span class="sxs-lookup"><span data-stu-id="e3fd3-110">**visRulerFixed**</span></span> <br/> |
|<span data-ttu-id="e3fd3-111">8 (&amp;H8)</span><span class="sxs-lookup"><span data-stu-id="e3fd3-111">8 (&amp;H8)</span></span>  <br/> |<span data-ttu-id="e3fd3-112">Épais</span><span class="sxs-lookup"><span data-stu-id="e3fd3-112">Coarse</span></span>  <br/> |<span data-ttu-id="e3fd3-113">**visRulerCoarse**</span><span class="sxs-lookup"><span data-stu-id="e3fd3-113">**visRulerCoarse**</span></span> <br/> |
|<span data-ttu-id="e3fd3-114">16 (&amp;H10)</span><span class="sxs-lookup"><span data-stu-id="e3fd3-114">16 (&amp;H10)</span></span>  <br/> |<span data-ttu-id="e3fd3-115">Normal (valeur par défaut)</span><span class="sxs-lookup"><span data-stu-id="e3fd3-115">Normal (Default)</span></span>  <br/> |<span data-ttu-id="e3fd3-116">**visRulerNormal**</span><span class="sxs-lookup"><span data-stu-id="e3fd3-116">**visRulerNormal**</span></span> <br/> |
|<span data-ttu-id="e3fd3-117">32 (&amp;H20)</span><span class="sxs-lookup"><span data-stu-id="e3fd3-117">32 (&amp;H20)</span></span>  <br/> |<span data-ttu-id="e3fd3-118">Fin</span><span class="sxs-lookup"><span data-stu-id="e3fd3-118">Fine</span></span>  <br/> |<span data-ttu-id="e3fd3-119">**visRulerFine**</span><span class="sxs-lookup"><span data-stu-id="e3fd3-119">**visRulerFine**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e3fd3-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="e3fd3-120">Remarks</span></span>

<span data-ttu-id="e3fd3-121">Cette cellule correspond à l’option **graduations** horizontale de la **règle &amp; grille** boîte de dialogue (sous l’onglet **affichage** , cliquez sur la flèche **Afficher** ).</span><span class="sxs-lookup"><span data-stu-id="e3fd3-121">This cell corresponds to the horizontal **Subdivisions** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="e3fd3-122">Pour obtenir une référence à la cellule XRulerDensity par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="e3fd3-122">To get a reference to the XRulerDensity cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e3fd3-123">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="e3fd3-123">Cell name:</span></span>  <br/> |<span data-ttu-id="e3fd3-124">XRulerDensity</span><span class="sxs-lookup"><span data-stu-id="e3fd3-124">XRulerDensity</span></span>  <br/> |
   
<span data-ttu-id="e3fd3-125">Pour obtenir une référence à la cellule XRulerDensity par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="e3fd3-125">To get a reference to the XRulerDensity cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e3fd3-126">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="e3fd3-126">Section index:</span></span>  <br/> |<span data-ttu-id="e3fd3-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e3fd3-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="e3fd3-128">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="e3fd3-128">Row index:</span></span>  <br/> |<span data-ttu-id="e3fd3-129">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="e3fd3-129">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="e3fd3-130">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="e3fd3-130">Cell index:</span></span>  <br/> |<span data-ttu-id="e3fd3-131">**visXRulerDensity**</span><span class="sxs-lookup"><span data-stu-id="e3fd3-131">**visXRulerDensity**</span></span> <br/> |
   

