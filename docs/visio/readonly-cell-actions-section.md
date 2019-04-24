---
title: ReadOnly, cellule (section Actions)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60071
localization_priority: Normal
ms.assetid: 158b4188-570c-3817-bf34-8dc0c64befa5
description: Contrôle si l’action d’un menu contextuel ou de balise d’action est en lecture seule.
ms.openlocfilehash: f45f22001a4d7275bb9367414c8b04ea3c0d9c6e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359989"
---
# <a name="readonly-cell-actions-section"></a><span data-ttu-id="a22f4-103">ReadOnly, cellule (section Actions)</span><span class="sxs-lookup"><span data-stu-id="a22f4-103">ReadOnly Cell (Actions Section)</span></span>

<span data-ttu-id="a22f4-104">Contrôle si l’action d’un menu contextuel ou de balise d’action est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="a22f4-104">Controls whether the action on an action tag or shortcut menu is read-only.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="a22f4-105">Dans les versions précédentes de Microsoft Visio, les balises d’action sont appelées « balises actives ».</span><span class="sxs-lookup"><span data-stu-id="a22f4-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="a22f4-106">**Value**</span><span class="sxs-lookup"><span data-stu-id="a22f4-106">**Value**</span></span>|<span data-ttu-id="a22f4-107">**Description**</span><span class="sxs-lookup"><span data-stu-id="a22f4-107">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a22f4-108">TRUE</span><span class="sxs-lookup"><span data-stu-id="a22f4-108">TRUE</span></span>  <br/> |<span data-ttu-id="a22f4-109">L'action apparaît dans le menu mais est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="a22f4-109">The action appears on the menu but is read-only.</span></span>  <br/> |
|<span data-ttu-id="a22f4-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="a22f4-110">FALSE</span></span>  <br/> |<span data-ttu-id="a22f4-111">L'action apparaît dans le menu et peut être sélectionnée (valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="a22f4-111">The action appears on the menu and can be selected (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a22f4-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="a22f4-112">Remarks</span></span>

<span data-ttu-id="a22f4-113">Lorsqu’une action est en lecture seule, elle apparaît dans le menu contextuel ou de balise d’action, mais vous ne pouvez pas la sélectionner.</span><span class="sxs-lookup"><span data-stu-id="a22f4-113">When an action is read-only, it appears on the action tag or shortcut menu but you cannot select it.</span></span> <span data-ttu-id="a22f4-114">Elle n’est pas grisée, mais apparaît sur un arrière-plan de couleur, comme une étiquette.</span><span class="sxs-lookup"><span data-stu-id="a22f4-114">It is not dimmed but rather appears on a colored background, like a label.</span></span> <span data-ttu-id="a22f4-115">Pour griser l’option de menu, utilisez la cellule Disabled.</span><span class="sxs-lookup"><span data-stu-id="a22f4-115">To make the menu item appear dimmed, use the Disabled cell.</span></span> 
  
<span data-ttu-id="a22f4-116">Pour obtenir une référence à la cellule ReadOnly à partir du nom d’une autre formule ou d’un programme à l’aide de la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="a22f4-116">To get a reference to the ReadOnly cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a22f4-117">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="a22f4-117">Cell name:</span></span>  <br/> |<span data-ttu-id="a22f4-118">Mesures.</span><span class="sxs-lookup"><span data-stu-id="a22f4-118">Actions.</span></span> <span data-ttu-id="a22f4-119">*nom* . Actions Readonlyoù.</span><span class="sxs-lookup"><span data-stu-id="a22f4-119">*name*  .ReadOnlywhere Actions.</span></span>  <span data-ttu-id="a22f4-120">*Name* est le nom de la ligne d'actions</span><span class="sxs-lookup"><span data-stu-id="a22f4-120">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="a22f4-121">Pour obtenir une référence à la cellule ReadOnly à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="a22f4-121">To get a reference to the ReadOnly cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a22f4-122">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="a22f4-122">Section index:</span></span>  <br/> |<span data-ttu-id="a22f4-123">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="a22f4-123">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="a22f4-124">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="a22f4-124">Row index:</span></span>  <br/> |<span data-ttu-id="a22f4-125">**visRowAction** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="a22f4-125">**visRowAction** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="a22f4-126">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="a22f4-126">Cell index:</span></span>  <br/> |<span data-ttu-id="a22f4-127">**visActionReadOnly**</span><span class="sxs-lookup"><span data-stu-id="a22f4-127">**visActionReadOnly**</span></span> <br/> |
   

