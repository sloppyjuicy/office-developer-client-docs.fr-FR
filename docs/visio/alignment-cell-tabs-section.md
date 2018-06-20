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
ms.openlocfilehash: a2178c63d0005ee8b2f0c8ebcfbc25854a5b1567
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788008"
---
# <a name="alignment-cell-tabs-section"></a><span data-ttu-id="9fe94-103">Alignment, cellule (section Tabs)</span><span class="sxs-lookup"><span data-stu-id="9fe94-103">Alignment Cell (Tabs Section)</span></span>

<span data-ttu-id="9fe94-104">Détermine l'alignement des tabulations.</span><span class="sxs-lookup"><span data-stu-id="9fe94-104">Specifies the tab alignment.</span></span>
  
|<span data-ttu-id="9fe94-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="9fe94-105">**Value**</span></span>|<span data-ttu-id="9fe94-106">**Alignment**</span><span class="sxs-lookup"><span data-stu-id="9fe94-106">**Alignment**</span></span>|<span data-ttu-id="9fe94-107">**Constante d’Automation**</span><span class="sxs-lookup"><span data-stu-id="9fe94-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="9fe94-108">0</span><span class="sxs-lookup"><span data-stu-id="9fe94-108">0</span></span>  <br/> | <span data-ttu-id="9fe94-109">À gauche</span><span class="sxs-lookup"><span data-stu-id="9fe94-109">Left</span></span>  <br/> |<span data-ttu-id="9fe94-110">**visTabStopLeft**</span><span class="sxs-lookup"><span data-stu-id="9fe94-110">**visTabStopLeft**</span></span> <br/> |
| <span data-ttu-id="9fe94-111">1</span><span class="sxs-lookup"><span data-stu-id="9fe94-111">1</span></span>  <br/> | <span data-ttu-id="9fe94-112">Au centre</span><span class="sxs-lookup"><span data-stu-id="9fe94-112">Center</span></span>  <br/> |<span data-ttu-id="9fe94-113">**visTabStopCenter**</span><span class="sxs-lookup"><span data-stu-id="9fe94-113">**visTabStopCenter**</span></span> <br/> |
| <span data-ttu-id="9fe94-114">2</span><span class="sxs-lookup"><span data-stu-id="9fe94-114">2</span></span>  <br/> | <span data-ttu-id="9fe94-115">Droite</span><span class="sxs-lookup"><span data-stu-id="9fe94-115">Right</span></span>  <br/> |<span data-ttu-id="9fe94-116">**visTabStopRight**</span><span class="sxs-lookup"><span data-stu-id="9fe94-116">**visTabStopRight**</span></span> <br/> |
| <span data-ttu-id="9fe94-117">3</span><span class="sxs-lookup"><span data-stu-id="9fe94-117">3</span></span>  <br/> | <span data-ttu-id="9fe94-118">Décimal</span><span class="sxs-lookup"><span data-stu-id="9fe94-118">Decimal</span></span>  <br/> |<span data-ttu-id="9fe94-119">**visTabStopDecimal**</span><span class="sxs-lookup"><span data-stu-id="9fe94-119">**visTabStopDecimal**</span></span> <br/> |
| <span data-ttu-id="9fe94-120">4</span><span class="sxs-lookup"><span data-stu-id="9fe94-120">4</span></span>  <br/> | <span data-ttu-id="9fe94-121">Virgule</span><span class="sxs-lookup"><span data-stu-id="9fe94-121">Comma</span></span>  <br/> |<span data-ttu-id="9fe94-122">**visTabStopComma**</span><span class="sxs-lookup"><span data-stu-id="9fe94-122">**visTabStopComma**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9fe94-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="9fe94-123">Remarks</span></span>

<span data-ttu-id="9fe94-124">Pour obtenir une référence à la cellule Alignment par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="9fe94-124">To get a reference to the Alignment cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9fe94-125">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="9fe94-125">Cell name:</span></span>  <br/> | <span data-ttu-id="9fe94-126">Onglets.</span><span class="sxs-lookup"><span data-stu-id="9fe94-126">Tabs.</span></span>  <span data-ttu-id="9fe94-127">*ij* où *i et j =* < 1 >, 2, 3</span><span class="sxs-lookup"><span data-stu-id="9fe94-127">*ij*            where  *i and j =*  <1>, 2, 3</span></span>  <br/> |
   
<span data-ttu-id="9fe94-128">Pour obtenir une référence à la cellule Alignment par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="9fe94-128">To get a reference to the Alignment cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9fe94-129">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="9fe94-129">Section index:</span></span>  <br/> |<span data-ttu-id="9fe94-130">**visSectionTab**</span><span class="sxs-lookup"><span data-stu-id="9fe94-130">**visSectionTab**</span></span> <br/> |
| <span data-ttu-id="9fe94-131">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="9fe94-131">Row index:</span></span>  <br/> |<span data-ttu-id="9fe94-132">**visRowTab +** *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="9fe94-132">**visRowTab +** *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="9fe94-133">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="9fe94-133">Cell index:</span></span>  <br/> | <span data-ttu-id="9fe94-134">(*j* \* 3) **+ visTabAlign**</span><span class="sxs-lookup"><span data-stu-id="9fe94-134">(*j*  \*3) **+ visTabAlign**</span></span> <br/> |
   

