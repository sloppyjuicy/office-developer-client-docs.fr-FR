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
ms.openlocfilehash: e4fb32c0fcb488173324ea597edc2c9d13f6bfca
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359310"
---
# <a name="lineadjustto-cell-page-layout-section"></a><span data-ttu-id="30aeb-103">LineAdjustTo, cellule (section Page Layout)</span><span class="sxs-lookup"><span data-stu-id="30aeb-103">LineAdjustTo Cell (Page Layout Section)</span></span>

<span data-ttu-id="30aeb-104">Indique les connecteurs dynamiques qui se superposent.</span><span class="sxs-lookup"><span data-stu-id="30aeb-104">Determines which dynamic connectors line up on top of one another.</span></span>
  
|<span data-ttu-id="30aeb-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="30aeb-105">**Value**</span></span>|<span data-ttu-id="30aeb-106">**Ajustement**</span><span class="sxs-lookup"><span data-stu-id="30aeb-106">**Adjustment**</span></span>|<span data-ttu-id="30aeb-107">**Constante d'automation**</span><span class="sxs-lookup"><span data-stu-id="30aeb-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="30aeb-108">0</span><span class="sxs-lookup"><span data-stu-id="30aeb-108">0</span></span>  <br/> |<span data-ttu-id="30aeb-109">Style de positionnement par défaut</span><span class="sxs-lookup"><span data-stu-id="30aeb-109">Routing style default</span></span>  <br/> |<span data-ttu-id="30aeb-110">**visPLOLineAdjustToDefault**</span><span class="sxs-lookup"><span data-stu-id="30aeb-110">**visPLOLineAdjustToDefault**</span></span> <br/> |
|<span data-ttu-id="30aeb-111">0,1</span><span class="sxs-lookup"><span data-stu-id="30aeb-111">1</span></span>  <br/> |<span data-ttu-id="30aeb-112">Traits proches les uns des autres</span><span class="sxs-lookup"><span data-stu-id="30aeb-112">Lines that are close to each other</span></span>  <br/> |<span data-ttu-id="30aeb-113">**visPLOLineAdjustToAll**</span><span class="sxs-lookup"><span data-stu-id="30aeb-113">**visPLOLineAdjustToAll**</span></span> <br/> |
|<span data-ttu-id="30aeb-114">n°2</span><span class="sxs-lookup"><span data-stu-id="30aeb-114">2</span></span>  <br/> |<span data-ttu-id="30aeb-115">Aucun trait</span><span class="sxs-lookup"><span data-stu-id="30aeb-115">No lines</span></span>  <br/> |<span data-ttu-id="30aeb-116">**visPLOLineAdjustToNone**</span><span class="sxs-lookup"><span data-stu-id="30aeb-116">**visPLOLineAdjustToNone**</span></span> <br/> |
|<span data-ttu-id="30aeb-117">3</span><span class="sxs-lookup"><span data-stu-id="30aeb-117">3</span></span>  <br/> |<span data-ttu-id="30aeb-118">Traits connexes</span><span class="sxs-lookup"><span data-stu-id="30aeb-118">Related lines</span></span>  <br/> |<span data-ttu-id="30aeb-119">**visPLOLineAdjustToRelated**</span><span class="sxs-lookup"><span data-stu-id="30aeb-119">**visPLOLineAdjustToRelated**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="30aeb-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="30aeb-120">Remarks</span></span>

<span data-ttu-id="30aeb-121">Vous pouvez également définir la valeur de cette cellule dans l’onglet **Disposition et positionnement** dans la boîte de dialogue **Mise en page** (sous l’onglet **Création**, cliquez sur la flèche **Mise en page**, puis cliquez sur **Disposition et positionnement**).</span><span class="sxs-lookup"><span data-stu-id="30aeb-121">You can also set the value of this cell on the **Layout and Routing** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then click **Layout and Routing**).</span></span>
  
<span data-ttu-id="30aeb-122">Pour obtenir une référence à la cellule LineAdjustTo par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="30aeb-122">To get a reference to the LineAdjustTo cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="30aeb-123">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="30aeb-123">Cell name:</span></span>  <br/> |<span data-ttu-id="30aeb-124">LineAdjustTo</span><span class="sxs-lookup"><span data-stu-id="30aeb-124">LineAdjustTo</span></span>  <br/> |
   
<span data-ttu-id="30aeb-125">Pour obtenir une référence à la cellule LineAdjustTo à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="30aeb-125">To get a reference to the LineAdjustTo cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="30aeb-126">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="30aeb-126">Section index:</span></span>  <br/> |<span data-ttu-id="30aeb-127">**Définis**</span><span class="sxs-lookup"><span data-stu-id="30aeb-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="30aeb-128">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="30aeb-128">Row index:</span></span>  <br/> |<span data-ttu-id="30aeb-129">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="30aeb-129">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="30aeb-130">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="30aeb-130">Cell index:</span></span>  <br/> |<span data-ttu-id="30aeb-131">**visPLOLineAdjustTo**</span><span class="sxs-lookup"><span data-stu-id="30aeb-131">**visPLOLineAdjustTo**</span></span> <br/> |
   

