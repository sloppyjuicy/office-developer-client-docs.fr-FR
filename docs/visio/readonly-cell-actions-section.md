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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434234"
---
# <a name="readonly-cell-actions-section"></a><span data-ttu-id="95746-103">ReadOnly, cellule (section Actions)</span><span class="sxs-lookup"><span data-stu-id="95746-103">ReadOnly Cell (Actions Section)</span></span>

<span data-ttu-id="95746-104">Contrôle si l’action d’un menu contextuel ou de balise d’action est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="95746-104">Controls whether the action on an action tag or shortcut menu is read-only.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="95746-105">Dans les versions précédentes de Microsoft Visio, les balises d’action sont appelées « balises actives ».</span><span class="sxs-lookup"><span data-stu-id="95746-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="95746-106">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="95746-106">**Value**</span></span>|<span data-ttu-id="95746-107">**Description**</span><span class="sxs-lookup"><span data-stu-id="95746-107">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="95746-108">TRUE</span><span class="sxs-lookup"><span data-stu-id="95746-108">TRUE</span></span>  <br/> |<span data-ttu-id="95746-109">L'action apparaît dans le menu mais est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="95746-109">The action appears on the menu but is read-only.</span></span>  <br/> |
|<span data-ttu-id="95746-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="95746-110">FALSE</span></span>  <br/> |<span data-ttu-id="95746-111">L'action apparaît dans le menu et peut être sélectionnée (valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="95746-111">The action appears on the menu and can be selected (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="95746-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="95746-112">Remarks</span></span>

<span data-ttu-id="95746-113">Lorsqu’une action est en lecture seule, elle apparaît dans le menu contextuel ou de balise d’action, mais vous ne pouvez pas la sélectionner.</span><span class="sxs-lookup"><span data-stu-id="95746-113">When an action is read-only, it appears on the action tag or shortcut menu but you cannot select it.</span></span> <span data-ttu-id="95746-114">Elle n’est pas grisée, mais apparaît sur un arrière-plan de couleur, comme une étiquette.</span><span class="sxs-lookup"><span data-stu-id="95746-114">It is not dimmed but rather appears on a colored background, like a label.</span></span> <span data-ttu-id="95746-115">Pour griser l’option de menu, utilisez la cellule Disabled.</span><span class="sxs-lookup"><span data-stu-id="95746-115">To make the menu item appear dimmed, use the Disabled cell.</span></span> 
  
<span data-ttu-id="95746-116">Pour obtenir une référence à la cellule ReadOnly à partir du nom d’une autre formule ou d’un programme à l’aide de la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="95746-116">To get a reference to the ReadOnly cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="95746-117">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="95746-117">Cell name:</span></span>  <br/> |<span data-ttu-id="95746-118">Actions.</span><span class="sxs-lookup"><span data-stu-id="95746-118">Actions.</span></span> <span data-ttu-id="95746-119">*nom*  . ReadOnlywhere Actions.</span><span class="sxs-lookup"><span data-stu-id="95746-119">*name*  .ReadOnlywhere Actions.</span></span>  <span data-ttu-id="95746-120">*name*  est le nom de la ligne Actions</span><span class="sxs-lookup"><span data-stu-id="95746-120">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="95746-121">Pour obtenir une référence à la cellule ReadOnly à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="95746-121">To get a reference to the ReadOnly cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="95746-122">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="95746-122">Section index:</span></span>  <br/> |<span data-ttu-id="95746-123">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="95746-123">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="95746-124">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="95746-124">Row index:</span></span>  <br/> |<span data-ttu-id="95746-125">**visRowAction**  +   *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="95746-125">**visRowAction** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="95746-126">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="95746-126">Cell index:</span></span>  <br/> |<span data-ttu-id="95746-127">**visActionReadOnly**</span><span class="sxs-lookup"><span data-stu-id="95746-127">**visActionReadOnly**</span></span> <br/> |
   

