---
title: SelectMode, cellule (section Group Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm875
localization_priority: Normal
ms.assetid: 5ba68e05-f394-d7b7-390d-f0a9fdad011e
description: Détermine le mode de sélection d'une forme de groupe et de ses membres.
ms.openlocfilehash: 426b4a18bbd54887e4f60b92860a6c3846386671
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789609"
---
# <a name="selectmode-cell-group-properties-section"></a><span data-ttu-id="a5c7d-103">SelectMode, cellule (section Group Properties)</span><span class="sxs-lookup"><span data-stu-id="a5c7d-103">SelectMode Cell (Group Properties Section)</span></span>

<span data-ttu-id="a5c7d-104">Détermine le mode de sélection d'une forme de groupe et de ses membres.</span><span class="sxs-lookup"><span data-stu-id="a5c7d-104">Determines how you select a group shape and its members.</span></span>
  
|<span data-ttu-id="a5c7d-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="a5c7d-105">**Value**</span></span>|<span data-ttu-id="a5c7d-106">**Mode de sélection**</span><span class="sxs-lookup"><span data-stu-id="a5c7d-106">**Selection mode**</span></span>|<span data-ttu-id="a5c7d-107">**Constante d’Automation**</span><span class="sxs-lookup"><span data-stu-id="a5c7d-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a5c7d-108">0</span><span class="sxs-lookup"><span data-stu-id="a5c7d-108">0</span></span>  <br/> |<span data-ttu-id="a5c7d-109">Sélectionner uniquement la forme de groupe.</span><span class="sxs-lookup"><span data-stu-id="a5c7d-109">Select the group shape only.</span></span>  <br/> |<span data-ttu-id="a5c7d-110">**visGrpSelModeGroupOnly**</span><span class="sxs-lookup"><span data-stu-id="a5c7d-110">**visGrpSelModeGroupOnly**</span></span> <br/> |
|<span data-ttu-id="a5c7d-111">1</span><span class="sxs-lookup"><span data-stu-id="a5c7d-111">1</span></span>  <br/> |<span data-ttu-id="a5c7d-112">Sélectionner la forme de groupe en premier.</span><span class="sxs-lookup"><span data-stu-id="a5c7d-112">Select the group shape first.</span></span>  <br/> |<span data-ttu-id="a5c7d-113">**visGrpSelModeGroup1st**</span><span class="sxs-lookup"><span data-stu-id="a5c7d-113">**visGrpSelModeGroup1st**</span></span> <br/> |
|<span data-ttu-id="a5c7d-114">2</span><span class="sxs-lookup"><span data-stu-id="a5c7d-114">2</span></span>  <br/> |<span data-ttu-id="a5c7d-115">Sélectionner les membres du groupe en premier.</span><span class="sxs-lookup"><span data-stu-id="a5c7d-115">Select the members of the group first.</span></span>  <br/> |<span data-ttu-id="a5c7d-116">**visGrpSelModeMembers1st**</span><span class="sxs-lookup"><span data-stu-id="a5c7d-116">**visGrpSelModeMembers1st**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a5c7d-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="a5c7d-117">Remarks</span></span>

<span data-ttu-id="a5c7d-118">Vous pouvez également définir cette valeur dans la boîte de dialogue **comportement** (avec la forme de groupe, sous l’onglet [développeur](run-in-developer-mode-display-the-developer-tab.md) , dans le groupe **Création de la forme** , cliquez sur **comportement**, puis cliquez sur un mode dans la liste de **sélection** sous **de groupe Comportement** ).</span><span class="sxs-lookup"><span data-stu-id="a5c7d-118">You can also set this value in the **Behavior** dialog box (with the group shape selected, on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, in the **Shape Design** group, click **Behavior**, and then click a mode in the **Selection** list under **Group Behavior** ).</span></span> 
  
<span data-ttu-id="a5c7d-119">Pour obtenir une référence à la cellule SelectMode par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="a5c7d-119">To get a reference to the SelectMode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a5c7d-120">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="a5c7d-120">Cell name:</span></span>  <br/> |<span data-ttu-id="a5c7d-121">SelectMode</span><span class="sxs-lookup"><span data-stu-id="a5c7d-121">SelectMode</span></span>  <br/> |
   
<span data-ttu-id="a5c7d-122">Pour obtenir une référence à la cellule SelectMode par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="a5c7d-122">To get a reference to the SelectMode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a5c7d-123">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="a5c7d-123">Section index:</span></span>  <br/> |<span data-ttu-id="a5c7d-124">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a5c7d-124">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="a5c7d-125">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="a5c7d-125">Row index:</span></span>  <br/> |<span data-ttu-id="a5c7d-126">**visRowGroup**</span><span class="sxs-lookup"><span data-stu-id="a5c7d-126">**visRowGroup**</span></span> <br/> |
|<span data-ttu-id="a5c7d-127">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="a5c7d-127">Cell index:</span></span>  <br/> |<span data-ttu-id="a5c7d-128">**visGroupSelectMode**</span><span class="sxs-lookup"><span data-stu-id="a5c7d-128">**visGroupSelectMode**</span></span> <br/> |
   

