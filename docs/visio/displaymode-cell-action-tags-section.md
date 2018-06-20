---
title: DisplayMode, cellule (Section Action Tags)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60039
localization_priority: Normal
ms.assetid: 0dfad40b-f97e-0c4a-2102-7344d1317b82
description: Détermine si la balise d’action apparaît lorsque l’utilisateur déplace le pointeur au-dessus de la balise, quand la forme est sélectionnée ou tout le temps.
ms.openlocfilehash: 4cb0666ca8de28247309de4fc0d2ff23e8b37d8a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788465"
---
# <a name="displaymode-cell-action-tags-section"></a><span data-ttu-id="2b139-103">DisplayMode, cellule (Section Action Tags)</span><span class="sxs-lookup"><span data-stu-id="2b139-103">DisplayMode Cell (Action Tags Section)</span></span>

<span data-ttu-id="2b139-104">Détermine si la balise d’action apparaît lorsque l’utilisateur déplace le pointeur au-dessus de la balise, quand la forme est sélectionnée ou tout le temps.</span><span class="sxs-lookup"><span data-stu-id="2b139-104">Determines whether the action tag appears when the user moves the pointer over the tag, when the shape is selected, or all the time.</span></span>
  
> [!NOTE]
> <span data-ttu-id="2b139-105">Dans les versions précédentes de Microsoft Visio, les balises d’action sont appelées « balises actives ».</span><span class="sxs-lookup"><span data-stu-id="2b139-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="2b139-106">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="2b139-106">**Value**</span></span>|<span data-ttu-id="2b139-107">**Mode d’affichage**</span><span class="sxs-lookup"><span data-stu-id="2b139-107">**Display Mode**</span></span>|<span data-ttu-id="2b139-108">**Constante d’Automation**</span><span class="sxs-lookup"><span data-stu-id="2b139-108">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="2b139-109">0</span><span class="sxs-lookup"><span data-stu-id="2b139-109">0</span></span>  <br/> | <span data-ttu-id="2b139-110">S’affiche lorsque vous positionnez la souris au-dessus de la balise (valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="2b139-110">Appears when the mouse is paused over the tag (the default).</span></span>  <br/> |<span data-ttu-id="2b139-111">**visSmartTagDispModeMouseOver**</span><span class="sxs-lookup"><span data-stu-id="2b139-111">**visSmartTagDispModeMouseOver**</span></span> <br/> |
| <span data-ttu-id="2b139-112">1</span><span class="sxs-lookup"><span data-stu-id="2b139-112">1</span></span>  <br/> | <span data-ttu-id="2b139-113">Apparaît tant que la forme est sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="2b139-113">Appears while the shape is selected.</span></span>  <br/> |<span data-ttu-id="2b139-114">**visSmartTagDispModeShapeSelected**</span><span class="sxs-lookup"><span data-stu-id="2b139-114">**visSmartTagDispModeShapeSelected**</span></span> <br/> |
| <span data-ttu-id="2b139-115">2</span><span class="sxs-lookup"><span data-stu-id="2b139-115">2</span></span>  <br/> | <span data-ttu-id="2b139-116">Apparaît tout le temps.</span><span class="sxs-lookup"><span data-stu-id="2b139-116">Appears all the time.</span></span>  <br/> |<span data-ttu-id="2b139-117">**visSmartTagDispModeAlways**</span><span class="sxs-lookup"><span data-stu-id="2b139-117">**visSmartTagDispModeAlways**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2b139-118">Notes</span><span class="sxs-lookup"><span data-stu-id="2b139-118">Remarks</span></span>

<span data-ttu-id="2b139-119">Les balises d’action n’apparaissent pas dans les résultats imprimés ou publiés.</span><span class="sxs-lookup"><span data-stu-id="2b139-119">Action tags do not appear on printed or published output.</span></span> 
  
<span data-ttu-id="2b139-120">Si une balise d’action est définie pour une page et si cette cellule contient la valeur 1, la balise n’apparaît jamais, car une page ne peut pas être sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="2b139-120">If an action tag is defined for a page, and this cell contains a value of 1, the tag never appears because a page cannot be selected.</span></span> 
  
<span data-ttu-id="2b139-121">Pour obtenir une référence à la cellule DisplayMode par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="2b139-121">To get a reference to the DisplayMode cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2b139-122">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="2b139-122">Cell name:</span></span>  <br/> | <span data-ttu-id="2b139-123">Balises actives.</span><span class="sxs-lookup"><span data-stu-id="2b139-123">SmartTags.</span></span>  <span data-ttu-id="2b139-124">*nom* . DisplayMode où SmartTags.</span><span class="sxs-lookup"><span data-stu-id="2b139-124">*name*  .DisplayMode           where SmartTags.</span></span> <span data-ttu-id="2b139-125">*nom* est le nom de la ligne de balise d’action</span><span class="sxs-lookup"><span data-stu-id="2b139-125">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="2b139-126">Pour obtenir une référence à la cellule DisplayMode par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="2b139-126">To get a reference to the DisplayMode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2b139-127">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="2b139-127">Section index:</span></span>  <br/> |<span data-ttu-id="2b139-128">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="2b139-128">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="2b139-129">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="2b139-129">Row index:</span></span>  <br/> |<span data-ttu-id="2b139-130">**visRowSmartTag** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="2b139-130">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="2b139-131">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="2b139-131">Cell index:</span></span>  <br/> |<span data-ttu-id="2b139-132">**visSmartTagDisplayMode**</span><span class="sxs-lookup"><span data-stu-id="2b139-132">**visSmartTagDisplayMode**</span></span> <br/> |
   

