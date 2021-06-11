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
ms.openlocfilehash: cae3eab64be3a91c48ae9f7fb49aa2a321087f43
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421444"
---
# <a name="issnaptarget-cell-group-properties-section"></a><span data-ttu-id="f6e84-103">IsSnapTarget, cellule (section Group Properties)</span><span class="sxs-lookup"><span data-stu-id="f6e84-103">IsSnapTarget Cell (Group Properties Section)</span></span>

<span data-ttu-id="f6e84-104">Détermine si des formes peuvent être alignées sur un groupe ou sur des formes au sein du groupe.</span><span class="sxs-lookup"><span data-stu-id="f6e84-104">Determines whether you snap to a group or to shapes within the group.</span></span>
  
|<span data-ttu-id="f6e84-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="f6e84-105">**Value**</span></span>|<span data-ttu-id="f6e84-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="f6e84-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f6e84-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="f6e84-107">TRUE</span></span>  <br/> |<span data-ttu-id="f6e84-108">Active l'alignement sur des formes d'un groupe.</span><span class="sxs-lookup"><span data-stu-id="f6e84-108">Enable snapping to shapes within a group.</span></span>  <br/> |
|<span data-ttu-id="f6e84-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="f6e84-109">FALSE</span></span>  <br/> |<span data-ttu-id="f6e84-110">Active l'alignement uniquement sur le groupe.</span><span class="sxs-lookup"><span data-stu-id="f6e84-110">Snap only to the group.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f6e84-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="f6e84-111">Remarks</span></span>

<span data-ttu-id="f6e84-112">Vous pouvez également définir cette valeur en sélectionnant le groupe, en cliquant sur **Comportement** sous l’onglet [Développeur](run-in-developer-mode-display-the-developer-tab.md), puis en activant la case à cocher **Aligner sur les formes membres**.</span><span class="sxs-lookup"><span data-stu-id="f6e84-112">You can also set this value by selecting the group, clicking **Behavior** on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then selecting the **Snap to member shapes** check box.</span></span> 
  
<span data-ttu-id="f6e84-113">Pour obtenir une référence à la cellule IsSnapTarget par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="f6e84-113">To get a reference to the IsSnapTarget cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f6e84-114">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="f6e84-114">Cell name:</span></span>  <br/> |<span data-ttu-id="f6e84-115">IsSnapTarget</span><span class="sxs-lookup"><span data-stu-id="f6e84-115">IsSnapTarget</span></span>  <br/> |
   
<span data-ttu-id="f6e84-116">Pour obtenir une référence à la cellule IsSnapTarget à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="f6e84-116">To get a reference to the IsSnapTarget cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f6e84-117">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="f6e84-117">Section index:</span></span>  <br/> |<span data-ttu-id="f6e84-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f6e84-118">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="f6e84-119">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="f6e84-119">Row index:</span></span>  <br/> |<span data-ttu-id="f6e84-120">**visRowGroup**</span><span class="sxs-lookup"><span data-stu-id="f6e84-120">**visRowGroup**</span></span> <br/> |
|<span data-ttu-id="f6e84-121">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="f6e84-121">Cell index:</span></span>  <br/> |<span data-ttu-id="f6e84-122">**visGroupIsSnapTarget**</span><span class="sxs-lookup"><span data-stu-id="f6e84-122">**visGroupIsSnapTarget**</span></span> <br/> |
   

