---
title: LineAdjustTo, cellule (section Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm525
localization_priority: Normal
ms.assetid: 81cd9670-8a6f-824b-528c-e9b88c86f525
description: Indique les connecteurs dynamiques qui se superposent.
ms.openlocfilehash: 13540f9dc5e6e6861d3f3679bcf49204d553397a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788947"
---
# <a name="lineadjustto-cell-page-layout-section"></a><span data-ttu-id="51b78-103">LineAdjustTo, cellule (section Page Layout)</span><span class="sxs-lookup"><span data-stu-id="51b78-103">LineAdjustTo Cell (Page Layout Section)</span></span>

<span data-ttu-id="51b78-104">Indique les connecteurs dynamiques qui se superposent.</span><span class="sxs-lookup"><span data-stu-id="51b78-104">Determines which dynamic connectors line up on top of one another.</span></span>
  
|<span data-ttu-id="51b78-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="51b78-105">**Value**</span></span>|<span data-ttu-id="51b78-106">**Ajustement**</span><span class="sxs-lookup"><span data-stu-id="51b78-106">**Adjustment**</span></span>|<span data-ttu-id="51b78-107">**Constante d’Automation**</span><span class="sxs-lookup"><span data-stu-id="51b78-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="51b78-108">0</span><span class="sxs-lookup"><span data-stu-id="51b78-108">0</span></span>  <br/> |<span data-ttu-id="51b78-109">Style de positionnement par défaut</span><span class="sxs-lookup"><span data-stu-id="51b78-109">Routing style default</span></span>  <br/> |<span data-ttu-id="51b78-110">**visPLOLineAdjustToDefault**</span><span class="sxs-lookup"><span data-stu-id="51b78-110">**visPLOLineAdjustToDefault**</span></span> <br/> |
|<span data-ttu-id="51b78-111">1</span><span class="sxs-lookup"><span data-stu-id="51b78-111">1</span></span>  <br/> |<span data-ttu-id="51b78-112">Traits proches les uns des autres</span><span class="sxs-lookup"><span data-stu-id="51b78-112">Lines that are close to each other</span></span>  <br/> |<span data-ttu-id="51b78-113">**visPLOLineAdjustToAll**</span><span class="sxs-lookup"><span data-stu-id="51b78-113">**visPLOLineAdjustToAll**</span></span> <br/> |
|<span data-ttu-id="51b78-114">2</span><span class="sxs-lookup"><span data-stu-id="51b78-114">2</span></span>  <br/> |<span data-ttu-id="51b78-115">Aucun trait</span><span class="sxs-lookup"><span data-stu-id="51b78-115">No lines</span></span>  <br/> |<span data-ttu-id="51b78-116">**visPLOLineAdjustToNone**</span><span class="sxs-lookup"><span data-stu-id="51b78-116">**visPLOLineAdjustToNone**</span></span> <br/> |
|<span data-ttu-id="51b78-117">3</span><span class="sxs-lookup"><span data-stu-id="51b78-117">3</span></span>  <br/> |<span data-ttu-id="51b78-118">Traits connexes</span><span class="sxs-lookup"><span data-stu-id="51b78-118">Related lines</span></span>  <br/> |<span data-ttu-id="51b78-119">**visPLOLineAdjustToRelated**</span><span class="sxs-lookup"><span data-stu-id="51b78-119">**visPLOLineAdjustToRelated**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="51b78-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="51b78-120">Remarks</span></span>

<span data-ttu-id="51b78-121">Vous pouvez également définir la valeur de cette cellule sous l’onglet **disposition et positionnement** dans la boîte de dialogue **Mise en Page** (sous l’onglet **Création** , cliquez sur la flèche **Mise en Page** , puis cliquez sur **disposition et positionnement**).</span><span class="sxs-lookup"><span data-stu-id="51b78-121">You can also set the value of this cell on the **Layout and Routing** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then click **Layout and Routing**).</span></span>
  
<span data-ttu-id="51b78-122">Pour obtenir une référence à la cellule LineAdjustTo par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="51b78-122">To get a reference to the LineAdjustTo cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="51b78-123">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="51b78-123">Cell name:</span></span>  <br/> |<span data-ttu-id="51b78-124">LineAdjustTo</span><span class="sxs-lookup"><span data-stu-id="51b78-124">LineAdjustTo</span></span>  <br/> |
   
<span data-ttu-id="51b78-125">Pour obtenir une référence à la cellule LineAdjustTo par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="51b78-125">To get a reference to the LineAdjustTo cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="51b78-126">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="51b78-126">Section index:</span></span>  <br/> |<span data-ttu-id="51b78-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="51b78-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="51b78-128">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="51b78-128">Row index:</span></span>  <br/> |<span data-ttu-id="51b78-129">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="51b78-129">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="51b78-130">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="51b78-130">Cell index:</span></span>  <br/> |<span data-ttu-id="51b78-131">**visPLOLineAdjustTo**</span><span class="sxs-lookup"><span data-stu-id="51b78-131">**visPLOLineAdjustTo**</span></span> <br/> |
   

