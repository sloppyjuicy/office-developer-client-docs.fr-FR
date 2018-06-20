---
title: Cellule YRulerDensity (règle &amp; Section grille)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1215
localization_priority: Normal
ms.assetid: aebcd321-9d1c-e04e-7c85-3ec1ed851561
description: Définit les graduations verticales de la règle pour la page.
ms.openlocfilehash: 4b5dcba7a5cb1a588f742b1c2ea6b430cb2af12c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790091"
---
# <a name="yrulerdensity-cell-ruler-amp-grid-section"></a><span data-ttu-id="f4ae4-103">Cellule YRulerDensity (règle &amp; Section grille)</span><span class="sxs-lookup"><span data-stu-id="f4ae4-103">YRulerDensity Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="f4ae4-104">Définit les graduations verticales de la règle pour la page.</span><span class="sxs-lookup"><span data-stu-id="f4ae4-104">Specifies the vertical subdivisions on the ruler for the page.</span></span>
  
|<span data-ttu-id="f4ae4-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="f4ae4-105">**Value**</span></span>|<span data-ttu-id="f4ae4-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="f4ae4-106">**Description**</span></span>|<span data-ttu-id="f4ae4-107">**Constante d’Automation**</span><span class="sxs-lookup"><span data-stu-id="f4ae4-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f4ae4-108">0</span><span class="sxs-lookup"><span data-stu-id="f4ae4-108">0</span></span>  <br/> |<span data-ttu-id="f4ae4-109">Fixe</span><span class="sxs-lookup"><span data-stu-id="f4ae4-109">Fixed</span></span>  <br/> |<span data-ttu-id="f4ae4-110">**visRulerFixed**</span><span class="sxs-lookup"><span data-stu-id="f4ae4-110">**visRulerFixed**</span></span> <br/> |
|<span data-ttu-id="f4ae4-111">8 (&amp;H8)</span><span class="sxs-lookup"><span data-stu-id="f4ae4-111">8 (&amp;H8)</span></span>  <br/> |<span data-ttu-id="f4ae4-112">Épais</span><span class="sxs-lookup"><span data-stu-id="f4ae4-112">Coarse</span></span>  <br/> |<span data-ttu-id="f4ae4-113">**visRulerCoarse**</span><span class="sxs-lookup"><span data-stu-id="f4ae4-113">**visRulerCoarse**</span></span> <br/> |
|<span data-ttu-id="f4ae4-114">16 (&amp;H10)</span><span class="sxs-lookup"><span data-stu-id="f4ae4-114">16 (&amp;H10)</span></span>  <br/> |<span data-ttu-id="f4ae4-115">Normal (valeur par défaut)</span><span class="sxs-lookup"><span data-stu-id="f4ae4-115">Normal (Default)</span></span>  <br/> |<span data-ttu-id="f4ae4-116">**visRulerNormal**</span><span class="sxs-lookup"><span data-stu-id="f4ae4-116">**visRulerNormal**</span></span> <br/> |
|<span data-ttu-id="f4ae4-117">32 (&amp;H20)</span><span class="sxs-lookup"><span data-stu-id="f4ae4-117">32 (&amp;H20)</span></span>  <br/> |<span data-ttu-id="f4ae4-118">Fin</span><span class="sxs-lookup"><span data-stu-id="f4ae4-118">Fine</span></span>  <br/> |<span data-ttu-id="f4ae4-119">**visRulerFine**</span><span class="sxs-lookup"><span data-stu-id="f4ae4-119">**visRulerFine**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f4ae4-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="f4ae4-120">Remarks</span></span>

<span data-ttu-id="f4ae4-121">Cette cellule correspond à l’option **graduations** verticale de la **règle &amp; grille** boîte de dialogue (sous l’onglet **affichage** , cliquez sur la flèche **Afficher** ).</span><span class="sxs-lookup"><span data-stu-id="f4ae4-121">This cell corresponds to the vertical **Subdivisions** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="f4ae4-122">Pour obtenir une référence à la cellule YRulerDensity par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="f4ae4-122">To get a reference to the YRulerDensity cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f4ae4-123">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="f4ae4-123">Cell name:</span></span>  <br/> |<span data-ttu-id="f4ae4-124">YRulerDensity</span><span class="sxs-lookup"><span data-stu-id="f4ae4-124">YRulerDensity</span></span>  <br/> |
   
<span data-ttu-id="f4ae4-125">Pour obtenir une référence à la cellule YRulerDensity par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="f4ae4-125">To get a reference to the YRulerDensity cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f4ae4-126">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="f4ae4-126">Section index:</span></span>  <br/> |<span data-ttu-id="f4ae4-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f4ae4-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="f4ae4-128">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="f4ae4-128">Row index:</span></span>  <br/> |<span data-ttu-id="f4ae4-129">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="f4ae4-129">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="f4ae4-130">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="f4ae4-130">Cell index:</span></span>  <br/> |<span data-ttu-id="f4ae4-131">**visYRulerDensity**</span><span class="sxs-lookup"><span data-stu-id="f4ae4-131">**visYRulerDensity**</span></span> <br/> |
   

