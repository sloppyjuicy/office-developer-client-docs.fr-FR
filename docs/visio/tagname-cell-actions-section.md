---
title: TagName, cellule (section Actions)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60087
localization_priority: Normal
ms.assetid: e593e95d-f975-481d-69cd-619049d4427d
description: Contient le nom de la balise d’action à laquelle cette action est associée.
ms.openlocfilehash: e1495a34769cbcfdd687491855d1f9c761de2b4e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789865"
---
# <a name="tagname-cell-actions-section"></a><span data-ttu-id="c8f9f-103">TagName, cellule (section Actions)</span><span class="sxs-lookup"><span data-stu-id="c8f9f-103">TagName Cell (Actions Section)</span></span>

<span data-ttu-id="c8f9f-104">Contient le nom de la balise d’action à laquelle cette action est associée.</span><span class="sxs-lookup"><span data-stu-id="c8f9f-104">Contains the name of the action tag that this action is associated with.</span></span>
  
> [!NOTE]
> <span data-ttu-id="c8f9f-105">Dans les versions précédentes de Microsoft Visio, les balises d’action sont appelées « balises actives ».</span><span class="sxs-lookup"><span data-stu-id="c8f9f-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c8f9f-106">Notes</span><span class="sxs-lookup"><span data-stu-id="c8f9f-106">Remarks</span></span>

<span data-ttu-id="c8f9f-107">La cellule TagName de la section Actions fonctionne avec la cellule TagName de la section Action Tags pour associer une balise d’action à ses actions.</span><span class="sxs-lookup"><span data-stu-id="c8f9f-107">The TagName cell in the Actions section works together with the TagName cell in the Action Tags section to associate an action tag with its actions.</span></span> 
  
- <span data-ttu-id="c8f9f-108">Si la cellule TagName d’une ligne Actions est vide, l’action apparaît dans un menu contextuel et pas dans un menu de balise d’action.</span><span class="sxs-lookup"><span data-stu-id="c8f9f-108">If the TagName cell in an Actions row is blank, the action appears on a shortcut menu, not on an action tag menu.</span></span>
    
- <span data-ttu-id="c8f9f-109">Si la valeur d’une cellule TagName de la ligne Actions correspond à la cellule TagName d’une ligne Smart Tags, l’action apparaît dans le menu de balise d’action.</span><span class="sxs-lookup"><span data-stu-id="c8f9f-109">If a TagName cell value in the Actions row matches the TagName cell value in a Smart Tags row, the action appears on the action tag menu.</span></span>
    
- <span data-ttu-id="c8f9f-110">Si la cellule TagName d’une action a une valeur, mais elle ne correspond pas à la valeur TagName d’une ligne de balise de forme, cette action n’apparaît pas dans les menus de balise d’action ou les menus contextuels.</span><span class="sxs-lookup"><span data-stu-id="c8f9f-110">If an action's TagName cell has a value but it does not match the TagName value in any shape tag row, that action does not appear on any action tag menus or shortcut menus.</span></span>
    
- <span data-ttu-id="c8f9f-111">Si plusieurs lignes Smart Tags contiennent la même valeur TagName, elles présentent toutes les mêmes actions.</span><span class="sxs-lookup"><span data-stu-id="c8f9f-111">If several smart tag rows have the same TagName value, they will all show the same actions.</span></span>
    
<span data-ttu-id="c8f9f-112">Pour obtenir une référence à la cellule TagName par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="c8f9f-112">To get a reference to the TagName cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c8f9f-113">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="c8f9f-113">Cell name:</span></span>  <br/> |<span data-ttu-id="c8f9f-114">Actions.</span><span class="sxs-lookup"><span data-stu-id="c8f9f-114">Actions.</span></span> <span data-ttu-id="c8f9f-115">*nom* . Actions TagNamewhere.</span><span class="sxs-lookup"><span data-stu-id="c8f9f-115">*name*  .TagNamewhere Actions.</span></span>  <span data-ttu-id="c8f9f-116">*nom* est le nom de la ligne Actions</span><span class="sxs-lookup"><span data-stu-id="c8f9f-116">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="c8f9f-117">Pour obtenir une référence à la cellule TagName par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="c8f9f-117">To get a reference to the TagName cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c8f9f-118">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="c8f9f-118">Section index:</span></span>  <br/> |<span data-ttu-id="c8f9f-119">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="c8f9f-119">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="c8f9f-120">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="c8f9f-120">Row index:</span></span>  <br/> |<span data-ttu-id="c8f9f-121">**visRowAction** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="c8f9f-121">**visRowAction** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="c8f9f-122">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="c8f9f-122">Cell index:</span></span>  <br/> |<span data-ttu-id="c8f9f-123">**visActionTagName**</span><span class="sxs-lookup"><span data-stu-id="c8f9f-123">**visActionTagName**</span></span> <br/> |
   

