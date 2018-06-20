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
ms.openlocfilehash: f2edfcb7cf9d21b2ecd97b335b07f30233903d5b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788847"
---
# <a name="isdropsource-cell-miscellaneous-section"></a><span data-ttu-id="f1637-103">IsDropSource, cellule (section Miscellaneous)</span><span class="sxs-lookup"><span data-stu-id="f1637-103">IsDropSource Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="f1637-104">Détermine si la forme peut être ajoutée à un groupe en la faisant glisser sur ce groupe.</span><span class="sxs-lookup"><span data-stu-id="f1637-104">Determines whether the shape can be added to a group by dropping it onto the group.</span></span>
  
|<span data-ttu-id="f1637-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="f1637-105">**Value**</span></span>|<span data-ttu-id="f1637-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="f1637-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f1637-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="f1637-107">TRUE</span></span>  <br/> |<span data-ttu-id="f1637-108">La forme peut être ajoutée à un groupe par glisser-déposer sur ce groupe.</span><span class="sxs-lookup"><span data-stu-id="f1637-108">Can add the shape to a group by dropping it onto the group.</span></span>  <br/> |
|<span data-ttu-id="f1637-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="f1637-109">FALSE</span></span>  <br/> |<span data-ttu-id="f1637-110">La forme ne peut être ajoutée au groupe.</span><span class="sxs-lookup"><span data-stu-id="f1637-110">Cannot add the shape to a group.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f1637-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="f1637-111">Remarks</span></span>

<span data-ttu-id="f1637-112">Vous pouvez également définir cette valeur en sélectionnant la forme, en cliquant sur **comportement** sous l’onglet [développeur](run-in-developer-mode-display-the-developer-tab.md) , puis activez la case à cocher **Ajouter la forme aux groupes lors de l’insertion** .</span><span class="sxs-lookup"><span data-stu-id="f1637-112">You can also set this value by selecting the shape, clicking **Behavior** on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then selecting the **Add shape to groups on drop** check box.</span></span> 
  
<span data-ttu-id="f1637-113">Outre l’activation de ce comportement pour une forme, vous devez également activer un groupe d’accepter les formes qui sont déplacés dans celui-ci.</span><span class="sxs-lookup"><span data-stu-id="f1637-113">In addition to enabling this behavior for a shape, you must also enable a group to accept shapes that are dragged into it.</span></span> <span data-ttu-id="f1637-114">Pour ce faire, sélectionnez le groupe, cliquez sur **comportement** sous l’onglet [développeur](run-in-developer-mode-display-the-developer-tab.md) , puis activez la case à cocher **accepter les formes insérées** .</span><span class="sxs-lookup"><span data-stu-id="f1637-114">To do so, select the group, click **Behavior** on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then select the **Accept dropped shapes** check box.</span></span> <span data-ttu-id="f1637-115">Cette valeur est stockée dans la cellule IsDropTarget dans la section Propriétés du groupe.</span><span class="sxs-lookup"><span data-stu-id="f1637-115">This value is stored in the IsDropTarget cell in the Group Properties section.</span></span> 
  
<span data-ttu-id="f1637-116">Pour obtenir une référence à la cellule IsDropSource par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="f1637-116">To get a reference to the IsDropSource cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f1637-117">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="f1637-117">Cell name:</span></span>  <br/> |<span data-ttu-id="f1637-118">IsDropSource</span><span class="sxs-lookup"><span data-stu-id="f1637-118">IsDropSource</span></span>  <br/> |
   
<span data-ttu-id="f1637-119">Pour obtenir une référence à la cellule IsDropSource par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="f1637-119">To get a reference to the IsDropSource cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f1637-120">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="f1637-120">Section index:</span></span>  <br/> |<span data-ttu-id="f1637-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f1637-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="f1637-122">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="f1637-122">Row index:</span></span>  <br/> |<span data-ttu-id="f1637-123">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="f1637-123">**visRowMisc**</span></span> <br/> |
|<span data-ttu-id="f1637-124">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="f1637-124">Cell index:</span></span>  <br/> |<span data-ttu-id="f1637-125">**visDropSource**</span><span class="sxs-lookup"><span data-stu-id="f1637-125">**visDropSource**</span></span> <br/> |
   

