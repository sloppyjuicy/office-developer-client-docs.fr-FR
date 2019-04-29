---
title: LineJumpCode, cellule (section Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm540
localization_priority: Normal
ms.assetid: 56f9043d-a632-65df-c710-45867cce1627
description: Détermine les connecteurs auxquels appliquer des déviations
ms.openlocfilehash: 7b5b8c8f1de160a4dc766d30a5f518c5653c270b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416250"
---
# <a name="linejumpcode-cell-page-layout-section"></a><span data-ttu-id="edb00-103">LineJumpCode, cellule (section Page Layout)</span><span class="sxs-lookup"><span data-stu-id="edb00-103">LineJumpCode Cell (Page Layout Section)</span></span>

<span data-ttu-id="edb00-104">Détermine les connecteurs auxquels appliquer des déviations</span><span class="sxs-lookup"><span data-stu-id="edb00-104">Determines the connectors to which you want to add jumps.</span></span>
  
|<span data-ttu-id="edb00-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="edb00-105">**Value**</span></span>|<span data-ttu-id="edb00-106">**Connecteurs auxquels appliquer des déviations**</span><span class="sxs-lookup"><span data-stu-id="edb00-106">**Connectors to which you want to add jumps**</span></span>|<span data-ttu-id="edb00-107">**Constante d'automation**</span><span class="sxs-lookup"><span data-stu-id="edb00-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="edb00-108">0</span><span class="sxs-lookup"><span data-stu-id="edb00-108">0</span></span>  <br/> |<span data-ttu-id="edb00-109">Aucun</span><span class="sxs-lookup"><span data-stu-id="edb00-109">None</span></span>  <br/> |<span data-ttu-id="edb00-110">**visPLOJumpNone**</span><span class="sxs-lookup"><span data-stu-id="edb00-110">**visPLOJumpNone**</span></span> <br/> |
|<span data-ttu-id="edb00-111">0,1</span><span class="sxs-lookup"><span data-stu-id="edb00-111">1</span></span>  <br/> |<span data-ttu-id="edb00-112">Lignes horizontales</span><span class="sxs-lookup"><span data-stu-id="edb00-112">Horizontal lines</span></span>  <br/> |<span data-ttu-id="edb00-113">**visPLOJumpHorizontal**</span><span class="sxs-lookup"><span data-stu-id="edb00-113">**visPLOJumpHorizontal**</span></span> <br/> |
|<span data-ttu-id="edb00-114">n°2</span><span class="sxs-lookup"><span data-stu-id="edb00-114">2</span></span>  <br/> |<span data-ttu-id="edb00-115">Traits verticaux</span><span class="sxs-lookup"><span data-stu-id="edb00-115">Vertical lines</span></span>  <br/> |<span data-ttu-id="edb00-116">**visPLOJumpVertical**</span><span class="sxs-lookup"><span data-stu-id="edb00-116">**visPLOJumpVertical**</span></span> <br/> |
|<span data-ttu-id="edb00-117">3</span><span class="sxs-lookup"><span data-stu-id="edb00-117">3</span></span>  <br/> |<span data-ttu-id="edb00-118">Dernier trait repositionné</span><span class="sxs-lookup"><span data-stu-id="edb00-118">Last routed line</span></span>  <br/> |<span data-ttu-id="edb00-119">**visPLOJumpLastRouted**</span><span class="sxs-lookup"><span data-stu-id="edb00-119">**visPLOJumpLastRouted**</span></span> <br/> |
|<span data-ttu-id="edb00-120">4</span><span class="sxs-lookup"><span data-stu-id="edb00-120">4</span></span>  <br/> |<span data-ttu-id="edb00-121">Dernière ligne affichée (forme du haut dans l'ordre de *plan* )</span><span class="sxs-lookup"><span data-stu-id="edb00-121">Last displayed line (top shape in the  *z*  -order)</span></span>  <br/> |<span data-ttu-id="edb00-122">**visPLOJumpDisplayOrder**</span><span class="sxs-lookup"><span data-stu-id="edb00-122">**visPLOJumpDisplayOrder**</span></span> <br/> |
|<span data-ttu-id="edb00-123">disque</span><span class="sxs-lookup"><span data-stu-id="edb00-123">5</span></span>  <br/> |<span data-ttu-id="edb00-124">Première ligne affichée (forme en bas de l'ordre de *plan* )</span><span class="sxs-lookup"><span data-stu-id="edb00-124">First displayed line (shape at the bottom of the  *z*  -order)</span></span>  <br/> |<span data-ttu-id="edb00-125">**visPLOJumpReverseDisplayOrder**</span><span class="sxs-lookup"><span data-stu-id="edb00-125">**visPLOJumpReverseDisplayOrder**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="edb00-126">Remarques</span><span class="sxs-lookup"><span data-stu-id="edb00-126">Remarks</span></span>

<span data-ttu-id="edb00-127">Vous pouvez également définir la valeur de cette cellule dans l’onglet **Disposition et positionnement** dans la boîte de dialogue **Mise en page** (sous l’onglet **Création**, cliquez sur la flèche **Mise en page**, puis cliquez sur **Disposition et positionnement**).</span><span class="sxs-lookup"><span data-stu-id="edb00-127">You can also set the value of this cell on the **Layout and Routing** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then click **Layout and Routing**).</span></span>
  
<span data-ttu-id="edb00-128">Pour obtenir une référence à la cellule LineJumpCode par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="edb00-128">To get a reference to the LineJumpCode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="edb00-129">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="edb00-129">Cell name:</span></span>  <br/> |<span data-ttu-id="edb00-130">LineJumpCode</span><span class="sxs-lookup"><span data-stu-id="edb00-130">LineJumpCode</span></span>  <br/> |
   
<span data-ttu-id="edb00-131">Pour obtenir une référence à la cellule LineJumpCode à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="edb00-131">To get a reference to the LineJumpCode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="edb00-132">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="edb00-132">Section index:</span></span>  <br/> |<span data-ttu-id="edb00-133">**Définis**</span><span class="sxs-lookup"><span data-stu-id="edb00-133">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="edb00-134">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="edb00-134">Row index:</span></span>  <br/> |<span data-ttu-id="edb00-135">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="edb00-135">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="edb00-136">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="edb00-136">Cell index:</span></span>  <br/> |<span data-ttu-id="edb00-137">**visPLOJumpCode**</span><span class="sxs-lookup"><span data-stu-id="edb00-137">**visPLOJumpCode**</span></span> <br/> |
   

