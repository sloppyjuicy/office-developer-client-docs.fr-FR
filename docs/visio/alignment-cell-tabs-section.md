---
title: Alignment, cellule (section Tabs)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm35
localization_priority: Normal
ms.assetid: 84234177-a2df-6acc-2761-230bc5d12627
description: Détermine l'alignement des tabulations.
ms.openlocfilehash: 461357c9c838fb4c0e5b0159bf027dd6adce26f9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425539"
---
# <a name="alignment-cell-tabs-section"></a><span data-ttu-id="3dac0-103">Alignment, cellule (section Tabs)</span><span class="sxs-lookup"><span data-stu-id="3dac0-103">Alignment Cell (Tabs Section)</span></span>

<span data-ttu-id="3dac0-104">Détermine l'alignement des tabulations.</span><span class="sxs-lookup"><span data-stu-id="3dac0-104">Specifies the tab alignment.</span></span>
  
|<span data-ttu-id="3dac0-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="3dac0-105">**Value**</span></span>|<span data-ttu-id="3dac0-106">**Alignment**</span><span class="sxs-lookup"><span data-stu-id="3dac0-106">**Alignment**</span></span>|<span data-ttu-id="3dac0-107">**Constante d'automation**</span><span class="sxs-lookup"><span data-stu-id="3dac0-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="3dac0-108">0</span><span class="sxs-lookup"><span data-stu-id="3dac0-108">0</span></span>  <br/> | <span data-ttu-id="3dac0-109">Gauche</span><span class="sxs-lookup"><span data-stu-id="3dac0-109">Left</span></span>  <br/> |<span data-ttu-id="3dac0-110">**visTabStopLeft**</span><span class="sxs-lookup"><span data-stu-id="3dac0-110">**visTabStopLeft**</span></span> <br/> |
| <span data-ttu-id="3dac0-111">1 </span><span class="sxs-lookup"><span data-stu-id="3dac0-111">1</span></span>  <br/> | <span data-ttu-id="3dac0-112">Centre</span><span class="sxs-lookup"><span data-stu-id="3dac0-112">Center</span></span>  <br/> |<span data-ttu-id="3dac0-113">**visTabStopCenter**</span><span class="sxs-lookup"><span data-stu-id="3dac0-113">**visTabStopCenter**</span></span> <br/> |
| <span data-ttu-id="3dac0-114">2 </span><span class="sxs-lookup"><span data-stu-id="3dac0-114">2</span></span>  <br/> | <span data-ttu-id="3dac0-115">À droite</span><span class="sxs-lookup"><span data-stu-id="3dac0-115">Right</span></span>  <br/> |<span data-ttu-id="3dac0-116">**visTabStopRight**</span><span class="sxs-lookup"><span data-stu-id="3dac0-116">**visTabStopRight**</span></span> <br/> |
| <span data-ttu-id="3dac0-117">3 </span><span class="sxs-lookup"><span data-stu-id="3dac0-117">3</span></span>  <br/> | <span data-ttu-id="3dac0-118">Décimal</span><span class="sxs-lookup"><span data-stu-id="3dac0-118">Decimal</span></span>  <br/> |<span data-ttu-id="3dac0-119">**visTabStopDecimal**</span><span class="sxs-lookup"><span data-stu-id="3dac0-119">**visTabStopDecimal**</span></span> <br/> |
| <span data-ttu-id="3dac0-120">4 </span><span class="sxs-lookup"><span data-stu-id="3dac0-120">4</span></span>  <br/> | <span data-ttu-id="3dac0-121">Virgule</span><span class="sxs-lookup"><span data-stu-id="3dac0-121">Comma</span></span>  <br/> |<span data-ttu-id="3dac0-122">**visTabStopComma**</span><span class="sxs-lookup"><span data-stu-id="3dac0-122">**visTabStopComma**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3dac0-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="3dac0-123">Remarks</span></span>

<span data-ttu-id="3dac0-124">Pour obtenir une référence à la cellule Alignment par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="3dac0-124">To get a reference to the Alignment cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3dac0-125">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="3dac0-125">Cell name:</span></span>  <br/> | <span data-ttu-id="3dac0-126">Onglets.</span><span class="sxs-lookup"><span data-stu-id="3dac0-126">Tabs.</span></span>  <span data-ttu-id="3dac0-127">*ij*            où  *i et j =*  <1>, 2, 3</span><span class="sxs-lookup"><span data-stu-id="3dac0-127">*ij*            where  *i and j =*  <1>, 2, 3</span></span>  <br/> |
   
<span data-ttu-id="3dac0-128">Pour obtenir une référence à la cellule Alignment à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="3dac0-128">To get a reference to the Alignment cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3dac0-129">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="3dac0-129">Section index:</span></span>  <br/> |<span data-ttu-id="3dac0-130">**visSectionTab**</span><span class="sxs-lookup"><span data-stu-id="3dac0-130">**visSectionTab**</span></span> <br/> |
| <span data-ttu-id="3dac0-131">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="3dac0-131">Row index:</span></span>  <br/> |<span data-ttu-id="3dac0-132">**visRowTab +** *i*            où  *i*  = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="3dac0-132">**visRowTab +** *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="3dac0-133">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="3dac0-133">Cell index:</span></span>  <br/> | <span data-ttu-id="3dac0-134">(*j*  \*3) **+ visTabAlign**</span><span class="sxs-lookup"><span data-stu-id="3dac0-134">(*j*  \*3) **+ visTabAlign**</span></span> <br/> |
   

