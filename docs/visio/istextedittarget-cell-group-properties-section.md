---
title: IsTextEditTarget, cellule (section Group Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251627
localization_priority: Normal
ms.assetid: 355cef8b-9213-479a-af95-b591f4bc51ad
description: Détermine l'attribution de texte à un groupe.
ms.openlocfilehash: 78a70dc0398745765bca12a1e768390b35fce8ce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314916"
---
# <a name="istextedittarget-cell-group-properties-section"></a><span data-ttu-id="c8b3b-103">IsTextEditTarget, cellule (section Group Properties)</span><span class="sxs-lookup"><span data-stu-id="c8b3b-103">IsTextEditTarget Cell (Group Properties Section)</span></span>

<span data-ttu-id="c8b3b-104">Détermine l'attribution de texte à un groupe.</span><span class="sxs-lookup"><span data-stu-id="c8b3b-104">Determines text assignment for a group.</span></span>
  
|<span data-ttu-id="c8b3b-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="c8b3b-105">**Value**</span></span>|<span data-ttu-id="c8b3b-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="c8b3b-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c8b3b-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="c8b3b-107">TRUE</span></span>  <br/> |<span data-ttu-id="c8b3b-108">Le texte est ajouté à la forme de groupe.</span><span class="sxs-lookup"><span data-stu-id="c8b3b-108">Text is added to the group shape.</span></span>  <br/> |
|<span data-ttu-id="c8b3b-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="c8b3b-109">FALSE</span></span>  <br/> |<span data-ttu-id="c8b3b-110">Le texte est ajouté dans le groupe à la forme qui se trouve au premier rang de la pile.</span><span class="sxs-lookup"><span data-stu-id="c8b3b-110">Text is added to the shape in the group at the top of the stacking order.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c8b3b-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="c8b3b-111">Remarks</span></span>

<span data-ttu-id="c8b3b-112">Vous pouvez également définir cette valeur en sélectionnant le groupe, en cliquant sur **Comportement** sous l’onglet [Développeur](run-in-developer-mode-display-the-developer-tab.md), puis activant la case à cocher **Modifier le texte du groupe**.</span><span class="sxs-lookup"><span data-stu-id="c8b3b-112">You can also set this value by selecting the group, clicking **Behavior** on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then selecting the **Edit text of group** check box.</span></span> 
  
<span data-ttu-id="c8b3b-p101">Les groupes créés dans les versions antérieures à Visio 2000 ont une valeur par défaut de FALSE. À partir de Visio 2000, la valeur par défaut est TRUE.</span><span class="sxs-lookup"><span data-stu-id="c8b3b-p101">Groups created in versions earlier than Visio 2000 have a default value of FALSE. Beginning with Visio version 2000, the default value is TRUE.</span></span> 
  
<span data-ttu-id="c8b3b-115">Pour obtenir une référence à la cellule IsTextEditTarget par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="c8b3b-115">To get a reference to the IsTextEditTarget cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c8b3b-116">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="c8b3b-116">Cell name:</span></span>  <br/> |<span data-ttu-id="c8b3b-117">IsTextEditTarget</span><span class="sxs-lookup"><span data-stu-id="c8b3b-117">IsTextEditTarget</span></span>  <br/> |
   
<span data-ttu-id="c8b3b-118">Pour obtenir une référence à la cellule IsTextEditTarget à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="c8b3b-118">To get a reference to the IsTextEditTarget cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c8b3b-119">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="c8b3b-119">Section index:</span></span>  <br/> |<span data-ttu-id="c8b3b-120">**Définis**</span><span class="sxs-lookup"><span data-stu-id="c8b3b-120">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="c8b3b-121">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="c8b3b-121">Row index:</span></span>  <br/> |<span data-ttu-id="c8b3b-122">**visRowGroup**</span><span class="sxs-lookup"><span data-stu-id="c8b3b-122">**visRowGroup**</span></span> <br/> |
|<span data-ttu-id="c8b3b-123">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="c8b3b-123">Cell index:</span></span>  <br/> |<span data-ttu-id="c8b3b-124">**visGroupIsTextEditTarget**</span><span class="sxs-lookup"><span data-stu-id="c8b3b-124">**visGroupIsTextEditTarget**</span></span> <br/> |
   

