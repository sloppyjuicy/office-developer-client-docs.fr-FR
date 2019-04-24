---
title: Cellule XRulerDensity (section &amp; règle et grille)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1165
localization_priority: Normal
ms.assetid: c11717c5-eb0e-e4fa-5a91-c62ecc048635
description: Définit les graduations horizontales de la règle pour la page.
ms.openlocfilehash: f459e5d1d19580201f1404ac2d1ae53c824293f8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331849"
---
# <a name="xrulerdensity-cell-ruler-amp-grid-section"></a><span data-ttu-id="b0641-103">Cellule XRulerDensity (section &amp; règle et grille)</span><span class="sxs-lookup"><span data-stu-id="b0641-103">XRulerDensity Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="b0641-104">Définit les graduations horizontales de la règle pour la page.</span><span class="sxs-lookup"><span data-stu-id="b0641-104">Specifies the horizontal subdivisions on the ruler for the page.</span></span>
  
|<span data-ttu-id="b0641-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="b0641-105">**Value**</span></span>|<span data-ttu-id="b0641-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="b0641-106">**Description**</span></span>|<span data-ttu-id="b0641-107">**Constante d'automation**</span><span class="sxs-lookup"><span data-stu-id="b0641-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b0641-108">0</span><span class="sxs-lookup"><span data-stu-id="b0641-108">0</span></span>  <br/> |<span data-ttu-id="b0641-109">Fixed</span><span class="sxs-lookup"><span data-stu-id="b0641-109">Fixed</span></span>  <br/> |<span data-ttu-id="b0641-110">**visRulerFixed**</span><span class="sxs-lookup"><span data-stu-id="b0641-110">**visRulerFixed**</span></span> <br/> |
|<span data-ttu-id="b0641-111">8 (&amp;H8)</span><span class="sxs-lookup"><span data-stu-id="b0641-111">8 (&amp;H8)</span></span>  <br/> |<span data-ttu-id="b0641-112">Grossier</span><span class="sxs-lookup"><span data-stu-id="b0641-112">Coarse</span></span>  <br/> |<span data-ttu-id="b0641-113">**visRulerCoarse**</span><span class="sxs-lookup"><span data-stu-id="b0641-113">**visRulerCoarse**</span></span> <br/> |
|<span data-ttu-id="b0641-114">16 (&amp;H10)</span><span class="sxs-lookup"><span data-stu-id="b0641-114">16 (&amp;H10)</span></span>  <br/> |<span data-ttu-id="b0641-115">Normal (valeur par défaut)</span><span class="sxs-lookup"><span data-stu-id="b0641-115">Normal (Default)</span></span>  <br/> |<span data-ttu-id="b0641-116">**visRulerNormal**</span><span class="sxs-lookup"><span data-stu-id="b0641-116">**visRulerNormal**</span></span> <br/> |
|<span data-ttu-id="b0641-117">32 (&amp;H20)</span><span class="sxs-lookup"><span data-stu-id="b0641-117">32 (&amp;H20)</span></span>  <br/> |<span data-ttu-id="b0641-118">Précisément</span><span class="sxs-lookup"><span data-stu-id="b0641-118">Fine</span></span>  <br/> |<span data-ttu-id="b0641-119">**visRulerFine**</span><span class="sxs-lookup"><span data-stu-id="b0641-119">**visRulerFine**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b0641-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="b0641-120">Remarks</span></span>

<span data-ttu-id="b0641-121">Cette cellule correspond à l'option sous- **divisions** horizontales de la boîte de dialogue **grille de &amp; règle** (sous l'onglet **affichage** , cliquez sur la flèche **Afficher** ).</span><span class="sxs-lookup"><span data-stu-id="b0641-121">This cell corresponds to the horizontal **Subdivisions** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="b0641-122">Pour obtenir une référence à la cellule XRulerDensity par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="b0641-122">To get a reference to the XRulerDensity cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b0641-123">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="b0641-123">Cell name:</span></span>  <br/> |<span data-ttu-id="b0641-124">XRulerDensity</span><span class="sxs-lookup"><span data-stu-id="b0641-124">XRulerDensity</span></span>  <br/> |
   
<span data-ttu-id="b0641-125">Pour obtenir une référence à la cellule XRulerDensity par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="b0641-125">To get a reference to the XRulerDensity cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b0641-126">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="b0641-126">Section index:</span></span>  <br/> |<span data-ttu-id="b0641-127">**Définis**</span><span class="sxs-lookup"><span data-stu-id="b0641-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="b0641-128">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="b0641-128">Row index:</span></span>  <br/> |<span data-ttu-id="b0641-129">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="b0641-129">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="b0641-130">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="b0641-130">Cell index:</span></span>  <br/> |<span data-ttu-id="b0641-131">**visXRulerDensity**</span><span class="sxs-lookup"><span data-stu-id="b0641-131">**visXRulerDensity**</span></span> <br/> |
   

