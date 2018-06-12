---
title: IsSnapTarget, cellule (section Group Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251626
localization_priority: Normal
ms.assetid: b58131f6-a566-d9ca-bad4-4f4b66e03aaf
description: Détermine si des formes peuvent être alignées sur un groupe ou sur des formes au sein du groupe.
ms.openlocfilehash: 89536923617f80768d7c14658cb07c97595824ea
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788872"
---
# <a name="issnaptarget-cell-group-properties-section"></a><span data-ttu-id="38cfe-103">IsSnapTarget, cellule (section Group Properties)</span><span class="sxs-lookup"><span data-stu-id="38cfe-103">IsSnapTarget Cell (Group Properties Section)</span></span>

<span data-ttu-id="38cfe-104">Détermine si des formes peuvent être alignées sur un groupe ou sur des formes au sein du groupe.</span><span class="sxs-lookup"><span data-stu-id="38cfe-104">Determines whether you snap to a group or to shapes within the group.</span></span>
  
|<span data-ttu-id="38cfe-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="38cfe-105">**Value**</span></span>|<span data-ttu-id="38cfe-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="38cfe-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="38cfe-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="38cfe-107">TRUE</span></span>  <br/> |<span data-ttu-id="38cfe-108">Active l'alignement sur des formes d'un groupe.</span><span class="sxs-lookup"><span data-stu-id="38cfe-108">Enable snapping to shapes within a group.</span></span>  <br/> |
|<span data-ttu-id="38cfe-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="38cfe-109">FALSE</span></span>  <br/> |<span data-ttu-id="38cfe-110">Active l'alignement uniquement sur le groupe.</span><span class="sxs-lookup"><span data-stu-id="38cfe-110">Snap only to the group.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="38cfe-111">Note</span><span class="sxs-lookup"><span data-stu-id="38cfe-111">Remarks</span></span>

<span data-ttu-id="38cfe-112">Vous pouvez également définir cette valeur en sélectionnant le groupe, en cliquant sur **comportement** sous l’onglet [développeur](run-in-developer-mode-display-the-developer-tab.md) , puis activez la case à cocher **Aligner sur les formes membres** .</span><span class="sxs-lookup"><span data-stu-id="38cfe-112">You can also set this value by selecting the group, clicking **Behavior** on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then selecting the **Snap to member shapes** check box.</span></span> 
  
<span data-ttu-id="38cfe-113">Pour obtenir une référence à la cellule IsSnapTarget par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="38cfe-113">To get a reference to the IsSnapTarget cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="38cfe-114">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="38cfe-114">Cell name:</span></span>  <br/> |<span data-ttu-id="38cfe-115">IsSnapTarget</span><span class="sxs-lookup"><span data-stu-id="38cfe-115">IsSnapTarget</span></span>  <br/> |
   
<span data-ttu-id="38cfe-116">Pour obtenir une référence à la cellule IsSnapTarget par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="38cfe-116">To get a reference to the IsSnapTarget cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="38cfe-117">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="38cfe-117">Section index:</span></span>  <br/> |<span data-ttu-id="38cfe-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="38cfe-118">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="38cfe-119">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="38cfe-119">Row index:</span></span>  <br/> |<span data-ttu-id="38cfe-120">**visRowGroup**</span><span class="sxs-lookup"><span data-stu-id="38cfe-120">**visRowGroup**</span></span> <br/> |
|<span data-ttu-id="38cfe-121">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="38cfe-121">Cell index:</span></span>  <br/> |<span data-ttu-id="38cfe-122">**visGroupIsSnapTarget**</span><span class="sxs-lookup"><span data-stu-id="38cfe-122">**visGroupIsSnapTarget**</span></span> <br/> |
   

