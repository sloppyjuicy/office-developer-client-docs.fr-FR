---
title: Cellule YRulerDensity (section &amp; règle et grille)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1215
localization_priority: Normal
ms.assetid: aebcd321-9d1c-e04e-7c85-3ec1ed851561
description: Définit les graduations verticales de la règle pour la page.
ms.openlocfilehash: c92c48f6c86fc794cf6f53a87fdb99e67a73b9f5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406800"
---
# <a name="yrulerdensity-cell-ruler-amp-grid-section"></a><span data-ttu-id="4745c-103">Cellule YRulerDensity (section &amp; règle et grille)</span><span class="sxs-lookup"><span data-stu-id="4745c-103">YRulerDensity Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="4745c-104">Définit les graduations verticales de la règle pour la page.</span><span class="sxs-lookup"><span data-stu-id="4745c-104">Specifies the vertical subdivisions on the ruler for the page.</span></span>
  
|<span data-ttu-id="4745c-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="4745c-105">**Value**</span></span>|<span data-ttu-id="4745c-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="4745c-106">**Description**</span></span>|<span data-ttu-id="4745c-107">**Constante d'automation**</span><span class="sxs-lookup"><span data-stu-id="4745c-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4745c-108">0</span><span class="sxs-lookup"><span data-stu-id="4745c-108">0</span></span>  <br/> |<span data-ttu-id="4745c-109">Fixed</span><span class="sxs-lookup"><span data-stu-id="4745c-109">Fixed</span></span>  <br/> |<span data-ttu-id="4745c-110">**visRulerFixed**</span><span class="sxs-lookup"><span data-stu-id="4745c-110">**visRulerFixed**</span></span> <br/> |
|<span data-ttu-id="4745c-111">8 (&amp;H8)</span><span class="sxs-lookup"><span data-stu-id="4745c-111">8 (&amp;H8)</span></span>  <br/> |<span data-ttu-id="4745c-112">Grossier</span><span class="sxs-lookup"><span data-stu-id="4745c-112">Coarse</span></span>  <br/> |<span data-ttu-id="4745c-113">**visRulerCoarse**</span><span class="sxs-lookup"><span data-stu-id="4745c-113">**visRulerCoarse**</span></span> <br/> |
|<span data-ttu-id="4745c-114">16 (&amp;H10)</span><span class="sxs-lookup"><span data-stu-id="4745c-114">16 (&amp;H10)</span></span>  <br/> |<span data-ttu-id="4745c-115">Normal (valeur par défaut)</span><span class="sxs-lookup"><span data-stu-id="4745c-115">Normal (Default)</span></span>  <br/> |<span data-ttu-id="4745c-116">**visRulerNormal**</span><span class="sxs-lookup"><span data-stu-id="4745c-116">**visRulerNormal**</span></span> <br/> |
|<span data-ttu-id="4745c-117">32 (&amp;H20)</span><span class="sxs-lookup"><span data-stu-id="4745c-117">32 (&amp;H20)</span></span>  <br/> |<span data-ttu-id="4745c-118">Précisément</span><span class="sxs-lookup"><span data-stu-id="4745c-118">Fine</span></span>  <br/> |<span data-ttu-id="4745c-119">**visRulerFine**</span><span class="sxs-lookup"><span data-stu-id="4745c-119">**visRulerFine**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4745c-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="4745c-120">Remarks</span></span>

<span data-ttu-id="4745c-121">Cette cellule correspond à l'option sous- **divisions** verticales de la boîte de dialogue **grille de &amp; règle** (sous l'onglet **affichage** , cliquez sur la flèche **Afficher** ).</span><span class="sxs-lookup"><span data-stu-id="4745c-121">This cell corresponds to the vertical **Subdivisions** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="4745c-122">Pour obtenir une référence à la cellule YRulerDensity par un nom dans une autre formule ou dans un programme en faisant appel à la propriété**CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="4745c-122">To get a reference to the YRulerDensity cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4745c-123">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="4745c-123">Cell name:</span></span>  <br/> |<span data-ttu-id="4745c-124">YRulerDensity</span><span class="sxs-lookup"><span data-stu-id="4745c-124">YRulerDensity</span></span>  <br/> |
   
<span data-ttu-id="4745c-125">Pour obtenir une référence à la cellule YRulerDensity par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="4745c-125">To get a reference to the YRulerDensity cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4745c-126">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="4745c-126">Section index:</span></span>  <br/> |<span data-ttu-id="4745c-127">**Définis**</span><span class="sxs-lookup"><span data-stu-id="4745c-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="4745c-128">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="4745c-128">Row index:</span></span>  <br/> |<span data-ttu-id="4745c-129">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="4745c-129">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="4745c-130">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="4745c-130">Cell index:</span></span>  <br/> |<span data-ttu-id="4745c-131">**visYRulerDensity**</span><span class="sxs-lookup"><span data-stu-id="4745c-131">**visYRulerDensity**</span></span> <br/> |
   

