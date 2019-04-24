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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341537"
---
# <a name="alignment-cell-tabs-section"></a><span data-ttu-id="0f35f-103">Alignment, cellule (section Tabs)</span><span class="sxs-lookup"><span data-stu-id="0f35f-103">Alignment Cell (Tabs Section)</span></span>

<span data-ttu-id="0f35f-104">Détermine l'alignement des tabulations.</span><span class="sxs-lookup"><span data-stu-id="0f35f-104">Specifies the tab alignment.</span></span>
  
|<span data-ttu-id="0f35f-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="0f35f-105">**Value**</span></span>|<span data-ttu-id="0f35f-106">**Alignment**</span><span class="sxs-lookup"><span data-stu-id="0f35f-106">**Alignment**</span></span>|<span data-ttu-id="0f35f-107">**Constante d'automation**</span><span class="sxs-lookup"><span data-stu-id="0f35f-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="0f35f-108">0</span><span class="sxs-lookup"><span data-stu-id="0f35f-108">0</span></span>  <br/> | <span data-ttu-id="0f35f-109">Gauche</span><span class="sxs-lookup"><span data-stu-id="0f35f-109">Left</span></span>  <br/> |<span data-ttu-id="0f35f-110">**visTabStopLeft**</span><span class="sxs-lookup"><span data-stu-id="0f35f-110">**visTabStopLeft**</span></span> <br/> |
| <span data-ttu-id="0f35f-111">0,1</span><span class="sxs-lookup"><span data-stu-id="0f35f-111">1</span></span>  <br/> | <span data-ttu-id="0f35f-112">Centre</span><span class="sxs-lookup"><span data-stu-id="0f35f-112">Center</span></span>  <br/> |<span data-ttu-id="0f35f-113">**visTabStopCenter**</span><span class="sxs-lookup"><span data-stu-id="0f35f-113">**visTabStopCenter**</span></span> <br/> |
| <span data-ttu-id="0f35f-114">n°2</span><span class="sxs-lookup"><span data-stu-id="0f35f-114">2</span></span>  <br/> | <span data-ttu-id="0f35f-115">À droite</span><span class="sxs-lookup"><span data-stu-id="0f35f-115">Right</span></span>  <br/> |<span data-ttu-id="0f35f-116">**visTabStopRight**</span><span class="sxs-lookup"><span data-stu-id="0f35f-116">**visTabStopRight**</span></span> <br/> |
| <span data-ttu-id="0f35f-117">3</span><span class="sxs-lookup"><span data-stu-id="0f35f-117">3</span></span>  <br/> | <span data-ttu-id="0f35f-118">Décimal</span><span class="sxs-lookup"><span data-stu-id="0f35f-118">Decimal</span></span>  <br/> |<span data-ttu-id="0f35f-119">**visTabStopDecimal**</span><span class="sxs-lookup"><span data-stu-id="0f35f-119">**visTabStopDecimal**</span></span> <br/> |
| <span data-ttu-id="0f35f-120">4</span><span class="sxs-lookup"><span data-stu-id="0f35f-120">4</span></span>  <br/> | <span data-ttu-id="0f35f-121">Virgule</span><span class="sxs-lookup"><span data-stu-id="0f35f-121">Comma</span></span>  <br/> |<span data-ttu-id="0f35f-122">**visTabStopComma**</span><span class="sxs-lookup"><span data-stu-id="0f35f-122">**visTabStopComma**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0f35f-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="0f35f-123">Remarks</span></span>

<span data-ttu-id="0f35f-124">Pour obtenir une référence à la cellule Alignment par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="0f35f-124">To get a reference to the Alignment cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0f35f-125">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="0f35f-125">Cell name:</span></span>  <br/> | <span data-ttu-id="0f35f-126">Taquet.</span><span class="sxs-lookup"><span data-stu-id="0f35f-126">Tabs.</span></span>  <span data-ttu-id="0f35f-127">*IJ* où *i et j =* <1>, 2, 3</span><span class="sxs-lookup"><span data-stu-id="0f35f-127">*ij*            where  *i and j =*  <1>, 2, 3</span></span>  <br/> |
   
<span data-ttu-id="0f35f-128">Pour obtenir une référence à la cellule Alignment à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="0f35f-128">To get a reference to the Alignment cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0f35f-129">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="0f35f-129">Section index:</span></span>  <br/> |<span data-ttu-id="0f35f-130">**visSectionTab**</span><span class="sxs-lookup"><span data-stu-id="0f35f-130">**visSectionTab**</span></span> <br/> |
| <span data-ttu-id="0f35f-131">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="0f35f-131">Row index:</span></span>  <br/> |<span data-ttu-id="0f35f-132">**visRowTab +** *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="0f35f-132">**visRowTab +** *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="0f35f-133">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="0f35f-133">Cell index:</span></span>  <br/> | <span data-ttu-id="0f35f-134">(*j* \* 3) **+ visTabAlign**</span><span class="sxs-lookup"><span data-stu-id="0f35f-134">(*j*  \*3) **+ visTabAlign**</span></span> <br/> |
   

