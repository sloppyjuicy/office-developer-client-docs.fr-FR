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
ms.openlocfilehash: 82f9e2806d1131a0acfd064f585c681fef0f209f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435361"
---
# <a name="selectmode-cell-group-properties-section"></a><span data-ttu-id="9e40a-103">SelectMode, cellule (section Group Properties)</span><span class="sxs-lookup"><span data-stu-id="9e40a-103">SelectMode Cell (Group Properties Section)</span></span>

<span data-ttu-id="9e40a-104">Détermine le mode de sélection d'une forme de groupe et de ses membres.</span><span class="sxs-lookup"><span data-stu-id="9e40a-104">Determines how you select a group shape and its members.</span></span>
  
|<span data-ttu-id="9e40a-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="9e40a-105">**Value**</span></span>|<span data-ttu-id="9e40a-106">**Mode de sélection**</span><span class="sxs-lookup"><span data-stu-id="9e40a-106">**Selection mode**</span></span>|<span data-ttu-id="9e40a-107">**Constante d'automation**</span><span class="sxs-lookup"><span data-stu-id="9e40a-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9e40a-108">0</span><span class="sxs-lookup"><span data-stu-id="9e40a-108">0</span></span>  <br/> |<span data-ttu-id="9e40a-109">Sélectionner uniquement la forme de groupe.</span><span class="sxs-lookup"><span data-stu-id="9e40a-109">Select the group shape only.</span></span>  <br/> |<span data-ttu-id="9e40a-110">**visGrpSelModeGroupOnly**</span><span class="sxs-lookup"><span data-stu-id="9e40a-110">**visGrpSelModeGroupOnly**</span></span> <br/> |
|<span data-ttu-id="9e40a-111">1</span><span class="sxs-lookup"><span data-stu-id="9e40a-111">1</span></span>  <br/> |<span data-ttu-id="9e40a-112">Sélectionner la forme de groupe en premier.</span><span class="sxs-lookup"><span data-stu-id="9e40a-112">Select the group shape first.</span></span>  <br/> |<span data-ttu-id="9e40a-113">**visGrpSelModeGroup1st**</span><span class="sxs-lookup"><span data-stu-id="9e40a-113">**visGrpSelModeGroup1st**</span></span> <br/> |
|<span data-ttu-id="9e40a-114">2</span><span class="sxs-lookup"><span data-stu-id="9e40a-114">2</span></span>  <br/> |<span data-ttu-id="9e40a-115">Sélectionner les membres du groupe en premier.</span><span class="sxs-lookup"><span data-stu-id="9e40a-115">Select the members of the group first.</span></span>  <br/> |<span data-ttu-id="9e40a-116">**visGrpSelModeMembers1st**</span><span class="sxs-lookup"><span data-stu-id="9e40a-116">**visGrpSelModeMembers1st**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9e40a-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="9e40a-117">Remarks</span></span>

<span data-ttu-id="9e40a-118">Vous pouvez également définir  cette valeur dans la boîte de dialogue [](run-in-developer-mode-display-the-developer-tab.md) Comportement (avec la forme de groupe sélectionnée, sous  l’onglet Développeur, dans le groupe Création de formes, cliquez sur **Comportement,** puis cliquez sur un mode dans la liste Sélection sous Comportement du  **groupe).**</span><span class="sxs-lookup"><span data-stu-id="9e40a-118">You can also set this value in the **Behavior** dialog box (with the group shape selected, on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, in the **Shape Design** group, click **Behavior**, and then click a mode in the **Selection** list under **Group Behavior** ).</span></span> 
  
<span data-ttu-id="9e40a-119">Pour obtenir une référence à la cellule SelectMode par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="9e40a-119">To get a reference to the SelectMode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9e40a-120">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="9e40a-120">Cell name:</span></span>  <br/> |<span data-ttu-id="9e40a-121">SelectMode</span><span class="sxs-lookup"><span data-stu-id="9e40a-121">SelectMode</span></span>  <br/> |
   
<span data-ttu-id="9e40a-122">Pour obtenir une référence à la cellule SelectMode à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="9e40a-122">To get a reference to the SelectMode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9e40a-123">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="9e40a-123">Section index:</span></span>  <br/> |<span data-ttu-id="9e40a-124">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="9e40a-124">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="9e40a-125">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="9e40a-125">Row index:</span></span>  <br/> |<span data-ttu-id="9e40a-126">**visRowGroup**</span><span class="sxs-lookup"><span data-stu-id="9e40a-126">**visRowGroup**</span></span> <br/> |
|<span data-ttu-id="9e40a-127">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="9e40a-127">Cell index:</span></span>  <br/> |<span data-ttu-id="9e40a-128">**visGroupSelectMode**</span><span class="sxs-lookup"><span data-stu-id="9e40a-128">**visGroupSelectMode**</span></span> <br/> |
   

