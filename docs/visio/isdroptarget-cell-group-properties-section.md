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
ms.openlocfilehash: 50f545b3cbd4f7e1541a7f5e8ca32c34d0429c5e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410790"
---
# <a name="isdroptarget-cell-group-properties-section"></a><span data-ttu-id="b44c6-103">IsDropTarget, cellule (section Group Properties)</span><span class="sxs-lookup"><span data-stu-id="b44c6-103">IsDropTarget Cell (Group Properties Section)</span></span>

<span data-ttu-id="b44c6-104">Détermine si le groupe accepte une forme qui y est déposée.</span><span class="sxs-lookup"><span data-stu-id="b44c6-104">Determines whether the group allows you to add a shape to it by dropping it on the group.</span></span>
  
|<span data-ttu-id="b44c6-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="b44c6-105">**Value**</span></span>|<span data-ttu-id="b44c6-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="b44c6-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b44c6-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="b44c6-107">TRUE</span></span>  <br/> |<span data-ttu-id="b44c6-108">Il est possible d'ajouter une forme au groupe en l'y déposant.</span><span class="sxs-lookup"><span data-stu-id="b44c6-108">Can add a shape to the group by dropping it onto the group.</span></span>  <br/> |
|<span data-ttu-id="b44c6-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="b44c6-109">FALSE</span></span>  <br/> |<span data-ttu-id="b44c6-110">Il n'est pas possible d'ajouter une forme au groupe.</span><span class="sxs-lookup"><span data-stu-id="b44c6-110">Cannot drop shape onto the group.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b44c6-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="b44c6-111">Remarks</span></span>

<span data-ttu-id="b44c6-112">Vous pouvez également définir cette valeur en sélectionnant le groupe, en cliquant sur **Comportement** sous l’onglet [Développeur](run-in-developer-mode-display-the-developer-tab.md), puis en activant la case à cocher **Accepter les formes insérées**.</span><span class="sxs-lookup"><span data-stu-id="b44c6-112">You can also set this value by selecting the group, clicking **Behavior** on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then selecting the **Accept dropped shapes** check box.</span></span> 
  
<span data-ttu-id="b44c6-p101">Pour ajouter une forme à un groupe en l’y déposant, vous devez également activer le comportement similaire pour la forme. Sélectionnez la forme, cliquez sur **Comportement** sous l’onglet [Développeur](run-in-developer-mode-display-the-developer-tab.md), puis activez la case à cocher **Ajouter la forme aux groupes lors de l’insertion**. Cette valeur est stockée dans la cellule IsDropSource de la section Miscellaneous.</span><span class="sxs-lookup"><span data-stu-id="b44c6-p101">To add a shape to a group by dropping it on the group, you must also enable similar shape behavior. You must select the shape, click **Behavior** on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then select the **Add shape to groups on drop** check box. This value is stored in the IsDropSource cell in the Miscellaneous section.</span></span> 
  
<span data-ttu-id="b44c6-116">Pour obtenir une référence à la cellule IsDropTarget par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="b44c6-116">To get a reference to the IsDropTarget cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b44c6-117">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="b44c6-117">Cell name:</span></span>  <br/> |<span data-ttu-id="b44c6-118">IsDropTarget</span><span class="sxs-lookup"><span data-stu-id="b44c6-118">IsDropTarget</span></span>  <br/> |
   
<span data-ttu-id="b44c6-119">Pour obtenir une référence à la cellule IsDropTarget à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="b44c6-119">To get a reference to the IsDropTarget cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b44c6-120">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="b44c6-120">Section index:</span></span>  <br/> |<span data-ttu-id="b44c6-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b44c6-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="b44c6-122">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="b44c6-122">Row index:</span></span>  <br/> |<span data-ttu-id="b44c6-123">**visRowGroup**</span><span class="sxs-lookup"><span data-stu-id="b44c6-123">**visRowGroup**</span></span> <br/> |
|<span data-ttu-id="b44c6-124">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="b44c6-124">Cell index:</span></span>  <br/> |<span data-ttu-id="b44c6-125">**visGroupIsDropTarget**</span><span class="sxs-lookup"><span data-stu-id="b44c6-125">**visGroupIsDropTarget**</span></span> <br/> |
   

