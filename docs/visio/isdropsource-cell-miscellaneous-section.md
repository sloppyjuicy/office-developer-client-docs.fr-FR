---
title: IsDropSource, cellule (section Miscellaneous)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm490
localization_priority: Normal
ms.assetid: 3b20e6ef-f1ac-5bb0-5ac3-4df3ae5e9bf9
description: Détermine si la forme peut être ajoutée à un groupe en la faisant glisser sur ce groupe.
ms.openlocfilehash: e8cb02a66f745530f12c7c8be56b9bdd771121b7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421892"
---
# <a name="isdropsource-cell-miscellaneous-section"></a><span data-ttu-id="2e666-103">IsDropSource, cellule (section Miscellaneous)</span><span class="sxs-lookup"><span data-stu-id="2e666-103">IsDropSource Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="2e666-104">Détermine si la forme peut être ajoutée à un groupe en la faisant glisser sur ce groupe.</span><span class="sxs-lookup"><span data-stu-id="2e666-104">Determines whether the shape can be added to a group by dropping it onto the group.</span></span>
  
|<span data-ttu-id="2e666-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="2e666-105">**Value**</span></span>|<span data-ttu-id="2e666-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="2e666-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2e666-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="2e666-107">TRUE</span></span>  <br/> |<span data-ttu-id="2e666-108">La forme peut être ajoutée à un groupe par glisser-déposer sur ce groupe.</span><span class="sxs-lookup"><span data-stu-id="2e666-108">Can add the shape to a group by dropping it onto the group.</span></span>  <br/> |
|<span data-ttu-id="2e666-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="2e666-109">FALSE</span></span>  <br/> |<span data-ttu-id="2e666-110">La forme ne peut être ajoutée au groupe.</span><span class="sxs-lookup"><span data-stu-id="2e666-110">Cannot add the shape to a group.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2e666-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="2e666-111">Remarks</span></span>

<span data-ttu-id="2e666-112">Vous pouvez également définir cette valeur en sélectionnant la forme, en cliquant sur **Comportement** sous l’onglet [Développeur](run-in-developer-mode-display-the-developer-tab.md), puis en cochant la case **Ajouter la forme aux groupes lors de l’insertion**.</span><span class="sxs-lookup"><span data-stu-id="2e666-112">You can also set this value by selecting the shape, clicking **Behavior** on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then selecting the **Add shape to groups on drop** check box.</span></span> 
  
<span data-ttu-id="2e666-p101">Outre l’activation de ce comportement pour la forme, vous devez également activer un groupe pour accepter d’y déposer des formes. Pour ce faire, sélectionnez le groupe, cliquez sur **Comportement** sous l’onglet [Développeur](run-in-developer-mode-display-the-developer-tab.md), puis activez la case à cocher **Accepter les formes insérées**. Cette valeur est stockée dans la cellule IsDropTarget de la section Group Properties.</span><span class="sxs-lookup"><span data-stu-id="2e666-p101">In addition to enabling this behavior for a shape, you must also enable a group to accept shapes that are dragged into it. To do so, select the group, click **Behavior** on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then select the **Accept dropped shapes** check box. This value is stored in the IsDropTarget cell in the Group Properties section.</span></span> 
  
<span data-ttu-id="2e666-116">Pour obtenir une référence à la cellule IsDropSource par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="2e666-116">To get a reference to the IsDropSource cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2e666-117">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="2e666-117">Cell name:</span></span>  <br/> |<span data-ttu-id="2e666-118">IsDropSource</span><span class="sxs-lookup"><span data-stu-id="2e666-118">IsDropSource</span></span>  <br/> |
   
<span data-ttu-id="2e666-119">Pour obtenir une référence à la cellule IsDropSource à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="2e666-119">To get a reference to the IsDropSource cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2e666-120">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="2e666-120">Section index:</span></span>  <br/> |<span data-ttu-id="2e666-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="2e666-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="2e666-122">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="2e666-122">Row index:</span></span>  <br/> |<span data-ttu-id="2e666-123">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="2e666-123">**visRowMisc**</span></span> <br/> |
|<span data-ttu-id="2e666-124">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="2e666-124">Cell index:</span></span>  <br/> |<span data-ttu-id="2e666-125">**visDropSource**</span><span class="sxs-lookup"><span data-stu-id="2e666-125">**visDropSource**</span></span> <br/> |
   

