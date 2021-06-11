---
title: DisplayMode Cell (Action Tags Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60039
localization_priority: Normal
ms.assetid: 0dfad40b-f97e-0c4a-2102-7344d1317b82
description: Détermine si la balise d’action s’affiche lorsque l’utilisateur déplace le pointeur sur la balise, lorsque la forme est sélectionnée ou en tout temps.
ms.openlocfilehash: 0254ad361c63dfdeddaf8a1c2173e99aa1c05398
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415816"
---
# <a name="displaymode-cell-action-tags-section"></a><span data-ttu-id="9d2f6-103">DisplayMode Cell (Action Tags Section)</span><span class="sxs-lookup"><span data-stu-id="9d2f6-103">DisplayMode Cell (Action Tags Section)</span></span>

<span data-ttu-id="9d2f6-104">Détermine si la balise d’action s’affiche lorsque l’utilisateur déplace le pointeur sur la balise, lorsque la forme est sélectionnée ou en tout temps.</span><span class="sxs-lookup"><span data-stu-id="9d2f6-104">Determines whether the action tag appears when the user moves the pointer over the tag, when the shape is selected, or all the time.</span></span>
  
> [!NOTE]
> <span data-ttu-id="9d2f6-105">Dans les versions précédentes de Microsoft Visio, les balises d’action sont appelées « balises actives ».</span><span class="sxs-lookup"><span data-stu-id="9d2f6-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="9d2f6-106">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="9d2f6-106">**Value**</span></span>|<span data-ttu-id="9d2f6-107">**Mode d’affichage**</span><span class="sxs-lookup"><span data-stu-id="9d2f6-107">**Display Mode**</span></span>|<span data-ttu-id="9d2f6-108">**Constante d'automation**</span><span class="sxs-lookup"><span data-stu-id="9d2f6-108">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="9d2f6-109">0</span><span class="sxs-lookup"><span data-stu-id="9d2f6-109">0</span></span>  <br/> | <span data-ttu-id="9d2f6-110">S’affiche lorsque la souris est suspendue sur la balise (valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="9d2f6-110">Appears when the mouse is paused over the tag (the default).</span></span>  <br/> |<span data-ttu-id="9d2f6-111">**visSmartTagDispModeMouseOver**</span><span class="sxs-lookup"><span data-stu-id="9d2f6-111">**visSmartTagDispModeMouseOver**</span></span> <br/> |
| <span data-ttu-id="9d2f6-112">1</span><span class="sxs-lookup"><span data-stu-id="9d2f6-112">1</span></span>  <br/> | <span data-ttu-id="9d2f6-113">Apparaît tant que la forme est sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="9d2f6-113">Appears while the shape is selected.</span></span>  <br/> |<span data-ttu-id="9d2f6-114">**visSmartTagDispModeShapeSelected**</span><span class="sxs-lookup"><span data-stu-id="9d2f6-114">**visSmartTagDispModeShapeSelected**</span></span> <br/> |
| <span data-ttu-id="9d2f6-115">2</span><span class="sxs-lookup"><span data-stu-id="9d2f6-115">2</span></span>  <br/> | <span data-ttu-id="9d2f6-116">Apparaît tout le temps.</span><span class="sxs-lookup"><span data-stu-id="9d2f6-116">Appears all the time.</span></span>  <br/> |<span data-ttu-id="9d2f6-117">**visSmartTagDispModeAlways**</span><span class="sxs-lookup"><span data-stu-id="9d2f6-117">**visSmartTagDispModeAlways**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9d2f6-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="9d2f6-118">Remarks</span></span>

<span data-ttu-id="9d2f6-119">Les balises d’action n’apparaissent pas dans les résultats imprimés ou publiés.</span><span class="sxs-lookup"><span data-stu-id="9d2f6-119">Action tags do not appear on printed or published output.</span></span> 
  
<span data-ttu-id="9d2f6-120">Si une balise d’action est définie pour une page et si cette cellule contient la valeur 1, la balise n’apparaît jamais, car une page ne peut pas être sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="9d2f6-120">If an action tag is defined for a page, and this cell contains a value of 1, the tag never appears because a page cannot be selected.</span></span> 
  
<span data-ttu-id="9d2f6-121">Pour obtenir une référence à la cellule DisplayMode à partir du nom d’une autre formule ou d’un programme à l’aide de la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="9d2f6-121">To get a reference to the DisplayMode cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9d2f6-122">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="9d2f6-122">Cell name:</span></span>  <br/> | <span data-ttu-id="9d2f6-123">SmartTags.</span><span class="sxs-lookup"><span data-stu-id="9d2f6-123">SmartTags.</span></span>  <span data-ttu-id="9d2f6-124">*nom*  . DisplayMode où SmartTags.</span><span class="sxs-lookup"><span data-stu-id="9d2f6-124">*name*  .DisplayMode           where SmartTags.</span></span> <span data-ttu-id="9d2f6-125">*name est*  le nom de la ligne de balise d’action</span><span class="sxs-lookup"><span data-stu-id="9d2f6-125">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="9d2f6-126">Pour obtenir une référence à la cellule DisplayMode à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="9d2f6-126">To get a reference to the DisplayMode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9d2f6-127">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="9d2f6-127">Section index:</span></span>  <br/> |<span data-ttu-id="9d2f6-128">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="9d2f6-128">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="9d2f6-129">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="9d2f6-129">Row index:</span></span>  <br/> |<span data-ttu-id="9d2f6-130">**visRowSmartTag**  +   *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="9d2f6-130">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="9d2f6-131">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="9d2f6-131">Cell index:</span></span>  <br/> |<span data-ttu-id="9d2f6-132">**visSmartTagDisplayMode**</span><span class="sxs-lookup"><span data-stu-id="9d2f6-132">**visSmartTagDisplayMode**</span></span> <br/> |
   

