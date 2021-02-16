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
# <a name="resizemode-cell-shape-transform-section"></a><span data-ttu-id="b15ed-103">ResizeMode, cellule (section Shape Transform)</span><span class="sxs-lookup"><span data-stu-id="b15ed-103">ResizeMode Cell (Shape Transform Section)</span></span>

<span data-ttu-id="b15ed-104">Indique le mode de redimensionnement actuel pour la forme.</span><span class="sxs-lookup"><span data-stu-id="b15ed-104">Shows the current resize behavior setting for the shape.</span></span>
  
|<span data-ttu-id="b15ed-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="b15ed-105">**Value**</span></span>|<span data-ttu-id="b15ed-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="b15ed-106">**Description**</span></span>|<span data-ttu-id="b15ed-107">**Constante d'automation**</span><span class="sxs-lookup"><span data-stu-id="b15ed-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b15ed-108">0</span><span class="sxs-lookup"><span data-stu-id="b15ed-108">0</span></span>  <br/> |<span data-ttu-id="b15ed-109">Utiliser les paramètres du groupe</span><span class="sxs-lookup"><span data-stu-id="b15ed-109">Use group's setting.</span></span>  <br/> |<span data-ttu-id="b15ed-110">**visXFormResizeDontCare**</span><span class="sxs-lookup"><span data-stu-id="b15ed-110">**visXFormResizeDontCare**</span></span> <br/> |
|<span data-ttu-id="b15ed-111">1 </span><span class="sxs-lookup"><span data-stu-id="b15ed-111">1</span></span>  <br/> |<span data-ttu-id="b15ed-112">Repositionner seulement</span><span class="sxs-lookup"><span data-stu-id="b15ed-112">Reposition only.</span></span>  <br/> |<span data-ttu-id="b15ed-113">**visXFormResizeSpread**</span><span class="sxs-lookup"><span data-stu-id="b15ed-113">**visXFormResizeSpread**</span></span> <br/> |
|<span data-ttu-id="b15ed-114">2 </span><span class="sxs-lookup"><span data-stu-id="b15ed-114">2</span></span>  <br/> |<span data-ttu-id="b15ed-115">Mettre à l'échelle avec le groupe</span><span class="sxs-lookup"><span data-stu-id="b15ed-115">Scale with group.</span></span>  <br/> |<span data-ttu-id="b15ed-116">**visXFormResizeScale**</span><span class="sxs-lookup"><span data-stu-id="b15ed-116">**visXFormResizeScale**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b15ed-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="b15ed-117">Remarks</span></span>

<span data-ttu-id="b15ed-118">Vous pouvez également définir  cette valeur  sous l’onglet [](run-in-developer-mode-display-the-developer-tab.md)Comportement de la  boîte de dialogue Comportement (sous l’onglet Développeur, dans le groupe Création de formes, cliquez sur **Comportement).**</span><span class="sxs-lookup"><span data-stu-id="b15ed-118">You can also set this value on the **Behavior** tab in the **Behavior** dialog box (on the [Developer](run-in-developer-mode-display-the-developer-tab.md)tab, in the **Shape Design** group, click **Behavior**).</span></span> <span data-ttu-id="b15ed-119">Pour obtenir une référence à la cellule ResizeMode par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="b15ed-119">To get a reference to the ResizeMode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b15ed-120">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="b15ed-120">Cell name:</span></span>  <br/> |<span data-ttu-id="b15ed-121">ResizeMode</span><span class="sxs-lookup"><span data-stu-id="b15ed-121">ResizeMode</span></span>  <br/> |
   
<span data-ttu-id="b15ed-122">Pour obtenir une référence à la cellule ResizeMode à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="b15ed-122">To get a reference to the ResizeMode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b15ed-123">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="b15ed-123">Section index:</span></span>  <br/> |<span data-ttu-id="b15ed-124">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b15ed-124">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="b15ed-125">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="b15ed-125">Row index:</span></span>  <br/> |<span data-ttu-id="b15ed-126">**visRowXFormOut**</span><span class="sxs-lookup"><span data-stu-id="b15ed-126">**visRowXFormOut**</span></span> <br/> |
|<span data-ttu-id="b15ed-127">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="b15ed-127">Cell index:</span></span>  <br/> |<span data-ttu-id="b15ed-128">**visXFormResizeMode**</span><span class="sxs-lookup"><span data-stu-id="b15ed-128">**visXFormResizeMode**</span></span> <br/> |
   

