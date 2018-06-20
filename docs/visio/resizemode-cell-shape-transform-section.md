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
ms.openlocfilehash: a32f5dbc935e85a49ab585073ca6a31215fd102a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789507"
---
# <a name="resizemode-cell-shape-transform-section"></a><span data-ttu-id="e05af-103">ResizeMode, cellule (section Shape Transform)</span><span class="sxs-lookup"><span data-stu-id="e05af-103">ResizeMode Cell (Shape Transform Section)</span></span>

<span data-ttu-id="e05af-104">Indique le mode de redimensionnement actuel pour la forme.</span><span class="sxs-lookup"><span data-stu-id="e05af-104">Shows the current resize behavior setting for the shape.</span></span>
  
|<span data-ttu-id="e05af-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="e05af-105">**Value**</span></span>|<span data-ttu-id="e05af-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="e05af-106">**Description**</span></span>|<span data-ttu-id="e05af-107">**Constante d’Automation**</span><span class="sxs-lookup"><span data-stu-id="e05af-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e05af-108">0</span><span class="sxs-lookup"><span data-stu-id="e05af-108">0</span></span>  <br/> |<span data-ttu-id="e05af-109">Utiliser les paramètres du groupe</span><span class="sxs-lookup"><span data-stu-id="e05af-109">Use group's setting.</span></span>  <br/> |<span data-ttu-id="e05af-110">**visXFormResizeDontCare**</span><span class="sxs-lookup"><span data-stu-id="e05af-110">**visXFormResizeDontCare**</span></span> <br/> |
|<span data-ttu-id="e05af-111">1</span><span class="sxs-lookup"><span data-stu-id="e05af-111">1</span></span>  <br/> |<span data-ttu-id="e05af-112">Repositionner seulement</span><span class="sxs-lookup"><span data-stu-id="e05af-112">Reposition only.</span></span>  <br/> |<span data-ttu-id="e05af-113">**visXFormResizeSpread**</span><span class="sxs-lookup"><span data-stu-id="e05af-113">**visXFormResizeSpread**</span></span> <br/> |
|<span data-ttu-id="e05af-114">2</span><span class="sxs-lookup"><span data-stu-id="e05af-114">2</span></span>  <br/> |<span data-ttu-id="e05af-115">Mettre à l'échelle avec le groupe</span><span class="sxs-lookup"><span data-stu-id="e05af-115">Scale with group.</span></span>  <br/> |<span data-ttu-id="e05af-116">**visXFormResizeScale**</span><span class="sxs-lookup"><span data-stu-id="e05af-116">**visXFormResizeScale**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e05af-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="e05af-117">Remarks</span></span>

<span data-ttu-id="e05af-118">Vous pouvez également définir cette valeur sur l’onglet **comportement** dans la boîte de dialogue **comportement** (sous l’onglet [développeur](run-in-developer-mode-display-the-developer-tab.md), dans le groupe **Création de la forme** , cliquez sur **comportement**).</span><span class="sxs-lookup"><span data-stu-id="e05af-118">You can also set this value on the **Behavior** tab in the **Behavior** dialog box (on the [Developer](run-in-developer-mode-display-the-developer-tab.md)tab, in the **Shape Design** group, click **Behavior**).</span></span> <span data-ttu-id="e05af-119">Pour obtenir une référence à la cellule ResizeMode par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="e05af-119">To get a reference to the ResizeMode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e05af-120">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="e05af-120">Cell name:</span></span>  <br/> |<span data-ttu-id="e05af-121">ResizeMode</span><span class="sxs-lookup"><span data-stu-id="e05af-121">ResizeMode</span></span>  <br/> |
   
<span data-ttu-id="e05af-122">Pour obtenir une référence à la cellule ResizeMode par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="e05af-122">To get a reference to the ResizeMode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e05af-123">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="e05af-123">Section index:</span></span>  <br/> |<span data-ttu-id="e05af-124">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e05af-124">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="e05af-125">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="e05af-125">Row index:</span></span>  <br/> |<span data-ttu-id="e05af-126">**visRowXFormOut**</span><span class="sxs-lookup"><span data-stu-id="e05af-126">**visRowXFormOut**</span></span> <br/> |
|<span data-ttu-id="e05af-127">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="e05af-127">Cell index:</span></span>  <br/> |<span data-ttu-id="e05af-128">**visXFormResizeMode**</span><span class="sxs-lookup"><span data-stu-id="e05af-128">**visXFormResizeMode**</span></span> <br/> |
   

