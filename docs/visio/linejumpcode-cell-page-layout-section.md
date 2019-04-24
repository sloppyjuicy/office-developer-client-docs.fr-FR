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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361116"
---
# <a name="linejumpcode-cell-page-layout-section"></a><span data-ttu-id="b4f06-103">LineJumpCode, cellule (section Page Layout)</span><span class="sxs-lookup"><span data-stu-id="b4f06-103">LineJumpCode Cell (Page Layout Section)</span></span>

<span data-ttu-id="b4f06-104">Détermine les connecteurs auxquels appliquer des déviations</span><span class="sxs-lookup"><span data-stu-id="b4f06-104">Determines the connectors to which you want to add jumps.</span></span>
  
|<span data-ttu-id="b4f06-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="b4f06-105">**Value**</span></span>|<span data-ttu-id="b4f06-106">**Connecteurs auxquels appliquer des déviations**</span><span class="sxs-lookup"><span data-stu-id="b4f06-106">**Connectors to which you want to add jumps**</span></span>|<span data-ttu-id="b4f06-107">**Constante d'automation**</span><span class="sxs-lookup"><span data-stu-id="b4f06-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b4f06-108">0</span><span class="sxs-lookup"><span data-stu-id="b4f06-108">0</span></span>  <br/> |<span data-ttu-id="b4f06-109">Aucun</span><span class="sxs-lookup"><span data-stu-id="b4f06-109">None</span></span>  <br/> |<span data-ttu-id="b4f06-110">**visPLOJumpNone**</span><span class="sxs-lookup"><span data-stu-id="b4f06-110">**visPLOJumpNone**</span></span> <br/> |
|<span data-ttu-id="b4f06-111">0,1</span><span class="sxs-lookup"><span data-stu-id="b4f06-111">1</span></span>  <br/> |<span data-ttu-id="b4f06-112">Lignes horizontales</span><span class="sxs-lookup"><span data-stu-id="b4f06-112">Horizontal lines</span></span>  <br/> |<span data-ttu-id="b4f06-113">**visPLOJumpHorizontal**</span><span class="sxs-lookup"><span data-stu-id="b4f06-113">**visPLOJumpHorizontal**</span></span> <br/> |
|<span data-ttu-id="b4f06-114">n°2</span><span class="sxs-lookup"><span data-stu-id="b4f06-114">2</span></span>  <br/> |<span data-ttu-id="b4f06-115">Traits verticaux</span><span class="sxs-lookup"><span data-stu-id="b4f06-115">Vertical lines</span></span>  <br/> |<span data-ttu-id="b4f06-116">**visPLOJumpVertical**</span><span class="sxs-lookup"><span data-stu-id="b4f06-116">**visPLOJumpVertical**</span></span> <br/> |
|<span data-ttu-id="b4f06-117">3</span><span class="sxs-lookup"><span data-stu-id="b4f06-117">3</span></span>  <br/> |<span data-ttu-id="b4f06-118">Dernier trait repositionné</span><span class="sxs-lookup"><span data-stu-id="b4f06-118">Last routed line</span></span>  <br/> |<span data-ttu-id="b4f06-119">**visPLOJumpLastRouted**</span><span class="sxs-lookup"><span data-stu-id="b4f06-119">**visPLOJumpLastRouted**</span></span> <br/> |
|<span data-ttu-id="b4f06-120">4</span><span class="sxs-lookup"><span data-stu-id="b4f06-120">4</span></span>  <br/> |<span data-ttu-id="b4f06-121">Dernière ligne affichée (forme du haut dans l'ordre de *plan* )</span><span class="sxs-lookup"><span data-stu-id="b4f06-121">Last displayed line (top shape in the  *z*  -order)</span></span>  <br/> |<span data-ttu-id="b4f06-122">**visPLOJumpDisplayOrder**</span><span class="sxs-lookup"><span data-stu-id="b4f06-122">**visPLOJumpDisplayOrder**</span></span> <br/> |
|<span data-ttu-id="b4f06-123">disque</span><span class="sxs-lookup"><span data-stu-id="b4f06-123">5</span></span>  <br/> |<span data-ttu-id="b4f06-124">Première ligne affichée (forme en bas de l'ordre de *plan* )</span><span class="sxs-lookup"><span data-stu-id="b4f06-124">First displayed line (shape at the bottom of the  *z*  -order)</span></span>  <br/> |<span data-ttu-id="b4f06-125">**visPLOJumpReverseDisplayOrder**</span><span class="sxs-lookup"><span data-stu-id="b4f06-125">**visPLOJumpReverseDisplayOrder**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b4f06-126">Remarques</span><span class="sxs-lookup"><span data-stu-id="b4f06-126">Remarks</span></span>

<span data-ttu-id="b4f06-127">Vous pouvez également définir la valeur de cette cellule dans l’onglet **Disposition et positionnement** dans la boîte de dialogue **Mise en page** (sous l’onglet **Création**, cliquez sur la flèche **Mise en page**, puis cliquez sur **Disposition et positionnement**).</span><span class="sxs-lookup"><span data-stu-id="b4f06-127">You can also set the value of this cell on the **Layout and Routing** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then click **Layout and Routing**).</span></span>
  
<span data-ttu-id="b4f06-128">Pour obtenir une référence à la cellule LineJumpCode par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="b4f06-128">To get a reference to the LineJumpCode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b4f06-129">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="b4f06-129">Cell name:</span></span>  <br/> |<span data-ttu-id="b4f06-130">LineJumpCode</span><span class="sxs-lookup"><span data-stu-id="b4f06-130">LineJumpCode</span></span>  <br/> |
   
<span data-ttu-id="b4f06-131">Pour obtenir une référence à la cellule LineJumpCode à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="b4f06-131">To get a reference to the LineJumpCode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b4f06-132">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="b4f06-132">Section index:</span></span>  <br/> |<span data-ttu-id="b4f06-133">**Définis**</span><span class="sxs-lookup"><span data-stu-id="b4f06-133">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="b4f06-134">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="b4f06-134">Row index:</span></span>  <br/> |<span data-ttu-id="b4f06-135">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="b4f06-135">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="b4f06-136">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="b4f06-136">Cell index:</span></span>  <br/> |<span data-ttu-id="b4f06-137">**visPLOJumpCode**</span><span class="sxs-lookup"><span data-stu-id="b4f06-137">**visPLOJumpCode**</span></span> <br/> |
   

