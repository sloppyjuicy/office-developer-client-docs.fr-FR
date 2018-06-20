---
title: IsDropTarget, cellule (section Group Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm495
localization_priority: Normal
ms.assetid: 8140fc7b-b99c-54bb-7af3-7de6fcdae7d3
description: Détermine si le groupe accepte une forme qui y est déposée.
ms.openlocfilehash: 326ead15bcdc72797853daee797d8f08d459a638
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788857"
---
# <a name="isdroptarget-cell-group-properties-section"></a><span data-ttu-id="33076-103">IsDropTarget, cellule (section Group Properties)</span><span class="sxs-lookup"><span data-stu-id="33076-103">IsDropTarget Cell (Group Properties Section)</span></span>

<span data-ttu-id="33076-104">Détermine si le groupe accepte une forme qui y est déposée.</span><span class="sxs-lookup"><span data-stu-id="33076-104">Determines whether the group allows you to add a shape to it by dropping it on the group.</span></span>
  
|<span data-ttu-id="33076-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="33076-105">**Value**</span></span>|<span data-ttu-id="33076-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="33076-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="33076-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="33076-107">TRUE</span></span>  <br/> |<span data-ttu-id="33076-108">Il est possible d'ajouter une forme au groupe en l'y déposant.</span><span class="sxs-lookup"><span data-stu-id="33076-108">Can add a shape to the group by dropping it onto the group.</span></span>  <br/> |
|<span data-ttu-id="33076-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="33076-109">FALSE</span></span>  <br/> |<span data-ttu-id="33076-110">Il n'est pas possible d'ajouter une forme au groupe.</span><span class="sxs-lookup"><span data-stu-id="33076-110">Cannot drop shape onto the group.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="33076-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="33076-111">Remarks</span></span>

<span data-ttu-id="33076-112">Vous pouvez également définir cette valeur en sélectionnant le groupe, en cliquant sur **comportement** sous l’onglet [développeur](run-in-developer-mode-display-the-developer-tab.md) , puis activez la case à cocher **accepter les formes insérées** .</span><span class="sxs-lookup"><span data-stu-id="33076-112">You can also set this value by selecting the group, clicking **Behavior** on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then selecting the **Accept dropped shapes** check box.</span></span> 
  
<span data-ttu-id="33076-113">Pour ajouter une forme à un groupe en la faisant glisser sur le groupe, vous devez également activer le comportement de forme similaire.</span><span class="sxs-lookup"><span data-stu-id="33076-113">To add a shape to a group by dropping it on the group, you must also enable similar shape behavior.</span></span> <span data-ttu-id="33076-114">Vous devez sélectionner la forme et cliquez sur **comportement** sous l’onglet [développeur](run-in-developer-mode-display-the-developer-tab.md) , puis activez la case à cocher **Ajouter la forme aux groupes lors de l’insertion** .</span><span class="sxs-lookup"><span data-stu-id="33076-114">You must select the shape, click **Behavior** on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then select the **Add shape to groups on drop** check box.</span></span> <span data-ttu-id="33076-115">Cette valeur est stockée dans la cellule IsDropSource de la section Miscellaneous.</span><span class="sxs-lookup"><span data-stu-id="33076-115">This value is stored in the IsDropSource cell in the Miscellaneous section.</span></span> 
  
<span data-ttu-id="33076-116">Pour obtenir une référence à la cellule IsDropTarget par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="33076-116">To get a reference to the IsDropTarget cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="33076-117">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="33076-117">Cell name:</span></span>  <br/> |<span data-ttu-id="33076-118">IsDropTarget</span><span class="sxs-lookup"><span data-stu-id="33076-118">IsDropTarget</span></span>  <br/> |
   
<span data-ttu-id="33076-119">Pour obtenir une référence à la cellule IsDropTarget par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="33076-119">To get a reference to the IsDropTarget cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="33076-120">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="33076-120">Section index:</span></span>  <br/> |<span data-ttu-id="33076-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="33076-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="33076-122">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="33076-122">Row index:</span></span>  <br/> |<span data-ttu-id="33076-123">**visRowGroup**</span><span class="sxs-lookup"><span data-stu-id="33076-123">**visRowGroup**</span></span> <br/> |
|<span data-ttu-id="33076-124">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="33076-124">Cell index:</span></span>  <br/> |<span data-ttu-id="33076-125">**visGroupIsDropTarget**</span><span class="sxs-lookup"><span data-stu-id="33076-125">**visGroupIsDropTarget**</span></span> <br/> |
   

