---
title: ResizeMode, cellule (section Shape Transform)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251203
localization_priority: Normal
ms.assetid: 49816e46-fa83-3ee4-1451-9c85fbd0f519
description: Indique le mode de redimensionnement actuel pour la forme.
ms.openlocfilehash: 7e9080fcd4604e2dbdc1dae31992f05e5b512213
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421962"
---
# <a name="resizemode-cell-shape-transform-section"></a><span data-ttu-id="1e4b3-103">ResizeMode, cellule (section Shape Transform)</span><span class="sxs-lookup"><span data-stu-id="1e4b3-103">ResizeMode Cell (Shape Transform Section)</span></span>

<span data-ttu-id="1e4b3-104">Indique le mode de redimensionnement actuel pour la forme.</span><span class="sxs-lookup"><span data-stu-id="1e4b3-104">Shows the current resize behavior setting for the shape.</span></span>
  
|<span data-ttu-id="1e4b3-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="1e4b3-105">**Value**</span></span>|<span data-ttu-id="1e4b3-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="1e4b3-106">**Description**</span></span>|<span data-ttu-id="1e4b3-107">**Constante d'automation**</span><span class="sxs-lookup"><span data-stu-id="1e4b3-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1e4b3-108">0</span><span class="sxs-lookup"><span data-stu-id="1e4b3-108">0</span></span>  <br/> |<span data-ttu-id="1e4b3-109">Utiliser les paramètres du groupe</span><span class="sxs-lookup"><span data-stu-id="1e4b3-109">Use group's setting.</span></span>  <br/> |<span data-ttu-id="1e4b3-110">**visXFormResizeDontCare**</span><span class="sxs-lookup"><span data-stu-id="1e4b3-110">**visXFormResizeDontCare**</span></span> <br/> |
|<span data-ttu-id="1e4b3-111">0,1</span><span class="sxs-lookup"><span data-stu-id="1e4b3-111">1</span></span>  <br/> |<span data-ttu-id="1e4b3-112">Repositionner seulement</span><span class="sxs-lookup"><span data-stu-id="1e4b3-112">Reposition only.</span></span>  <br/> |<span data-ttu-id="1e4b3-113">**visXFormResizeSpread**</span><span class="sxs-lookup"><span data-stu-id="1e4b3-113">**visXFormResizeSpread**</span></span> <br/> |
|<span data-ttu-id="1e4b3-114">n°2</span><span class="sxs-lookup"><span data-stu-id="1e4b3-114">2</span></span>  <br/> |<span data-ttu-id="1e4b3-115">Mettre à l'échelle avec le groupe</span><span class="sxs-lookup"><span data-stu-id="1e4b3-115">Scale with group.</span></span>  <br/> |<span data-ttu-id="1e4b3-116">**visXFormResizeScale**</span><span class="sxs-lookup"><span data-stu-id="1e4b3-116">**visXFormResizeScale**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1e4b3-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="1e4b3-117">Remarks</span></span>

<span data-ttu-id="1e4b3-118">Vous pouvez également définir cette valeur sous l'onglet **comportement** dans la boîte de dialogue **comportement** (sous l'onglet [développeur](run-in-developer-mode-display-the-developer-tab.md), dans le groupe **création de forme** , cliquez sur **comportement**).</span><span class="sxs-lookup"><span data-stu-id="1e4b3-118">You can also set this value on the **Behavior** tab in the **Behavior** dialog box (on the [Developer](run-in-developer-mode-display-the-developer-tab.md)tab, in the **Shape Design** group, click **Behavior**).</span></span> <span data-ttu-id="1e4b3-119">Pour obtenir une référence à la cellule ResizeMode par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="1e4b3-119">To get a reference to the ResizeMode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1e4b3-120">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="1e4b3-120">Cell name:</span></span>  <br/> |<span data-ttu-id="1e4b3-121">ResizeMode</span><span class="sxs-lookup"><span data-stu-id="1e4b3-121">ResizeMode</span></span>  <br/> |
   
<span data-ttu-id="1e4b3-122">Pour obtenir une référence à la cellule ResizeMode à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="1e4b3-122">To get a reference to the ResizeMode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1e4b3-123">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="1e4b3-123">Section index:</span></span>  <br/> |<span data-ttu-id="1e4b3-124">**Définis**</span><span class="sxs-lookup"><span data-stu-id="1e4b3-124">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="1e4b3-125">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="1e4b3-125">Row index:</span></span>  <br/> |<span data-ttu-id="1e4b3-126">**visRowXFormOut**</span><span class="sxs-lookup"><span data-stu-id="1e4b3-126">**visRowXFormOut**</span></span> <br/> |
|<span data-ttu-id="1e4b3-127">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="1e4b3-127">Cell index:</span></span>  <br/> |<span data-ttu-id="1e4b3-128">**visXFormResizeMode**</span><span class="sxs-lookup"><span data-stu-id="1e4b3-128">**visXFormResizeMode**</span></span> <br/> |
   

