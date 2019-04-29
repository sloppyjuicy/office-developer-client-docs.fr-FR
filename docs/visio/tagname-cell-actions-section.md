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
ms.openlocfilehash: e7bf5db940934d168ac2adb86d05b0374b0fd265
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412715"
---
# <a name="tagname-cell-actions-section"></a><span data-ttu-id="267ec-103">TagName, cellule (section Actions)</span><span class="sxs-lookup"><span data-stu-id="267ec-103">TagName Cell (Actions Section)</span></span>

<span data-ttu-id="267ec-104">Contient le nom de la balise d’action à laquelle cette action est associée.</span><span class="sxs-lookup"><span data-stu-id="267ec-104">Contains the name of the action tag that this action is associated with.</span></span>
  
> [!NOTE]
> <span data-ttu-id="267ec-105">Dans les versions précédentes de Microsoft Visio, les balises d’action sont appelées « balises actives ».</span><span class="sxs-lookup"><span data-stu-id="267ec-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="267ec-106">Remarques</span><span class="sxs-lookup"><span data-stu-id="267ec-106">Remarks</span></span>

<span data-ttu-id="267ec-107">La cellule TagName de la section Actions fonctionne avec la cellule TagName de la section Action Tags pour associer une balise d’action à ses actions.</span><span class="sxs-lookup"><span data-stu-id="267ec-107">The TagName cell in the Actions section works together with the TagName cell in the Action Tags section to associate an action tag with its actions.</span></span> 
  
- <span data-ttu-id="267ec-108">Si la cellule TagName d'une ligne actions est vide, l'action apparaît dans un menu contextuel, pas dans un menu de balise d'action.</span><span class="sxs-lookup"><span data-stu-id="267ec-108">If the TagName cell in an Actions row is blank, the action appears on a shortcut menu, not on an action tag menu.</span></span>
    
- <span data-ttu-id="267ec-109">Si la valeur d'une cellule TagName de la ligne actions correspond à la valeur de la cellule TagName d'une ligne Smart Tags, l'action apparaît dans le menu de la balise d'action.</span><span class="sxs-lookup"><span data-stu-id="267ec-109">If a TagName cell value in the Actions row matches the TagName cell value in a Smart Tags row, the action appears on the action tag menu.</span></span>
    
- <span data-ttu-id="267ec-110">Si la cellule TagName d'une action a une valeur mais qu'elle ne correspond pas à la valeur TagName de la ligne de la balise de la forme, cette action n'apparaît pas dans les menus de la balise d'action ou dans les menus contextuels.</span><span class="sxs-lookup"><span data-stu-id="267ec-110">If an action's TagName cell has a value but it does not match the TagName value in any shape tag row, that action does not appear on any action tag menus or shortcut menus.</span></span>
    
- <span data-ttu-id="267ec-111">Si plusieurs lignes Smart Tags contiennent la même valeur TagName, elles présentent toutes les mêmes actions.</span><span class="sxs-lookup"><span data-stu-id="267ec-111">If several smart tag rows have the same TagName value, they will all show the same actions.</span></span>
    
<span data-ttu-id="267ec-112">Pour obtenir une référence à la cellule TagName par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="267ec-112">To get a reference to the TagName cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="267ec-113">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="267ec-113">Cell name:</span></span>  <br/> |<span data-ttu-id="267ec-114">Mesures.</span><span class="sxs-lookup"><span data-stu-id="267ec-114">Actions.</span></span> <span data-ttu-id="267ec-115">*nom* . Actions Tagnameoù.</span><span class="sxs-lookup"><span data-stu-id="267ec-115">*name*  .TagNamewhere Actions.</span></span>  <span data-ttu-id="267ec-116">*Name* est le nom de la ligne d'actions</span><span class="sxs-lookup"><span data-stu-id="267ec-116">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="267ec-117">Pour obtenir une référence à la cellule TagName par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="267ec-117">To get a reference to the TagName cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="267ec-118">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="267ec-118">Section index:</span></span>  <br/> |<span data-ttu-id="267ec-119">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="267ec-119">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="267ec-120">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="267ec-120">Row index:</span></span>  <br/> |<span data-ttu-id="267ec-121">**visRowAction** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="267ec-121">**visRowAction** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="267ec-122">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="267ec-122">Cell index:</span></span>  <br/> |<span data-ttu-id="267ec-123">**visActionTagName**</span><span class="sxs-lookup"><span data-stu-id="267ec-123">**visActionTagName**</span></span> <br/> |
   

