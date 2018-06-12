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
ms.openlocfilehash: bf2d0f7e50a3126611662af8e068485986c26a13
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789391"
---
# <a name="readonly-cell-actions-section"></a><span data-ttu-id="b2588-103">ReadOnly, cellule (section Actions)</span><span class="sxs-lookup"><span data-stu-id="b2588-103">ReadOnly Cell (Actions Section)</span></span>

<span data-ttu-id="b2588-104">Contrôle si l’action d’un menu contextuel ou de balise d’action est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="b2588-104">Controls whether the action on an action tag or shortcut menu is read-only.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="b2588-105">Dans les versions précédentes de Microsoft Visio, les balises d’action sont appelées « balises actives ».</span><span class="sxs-lookup"><span data-stu-id="b2588-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="b2588-106">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="b2588-106">**Value**</span></span>|<span data-ttu-id="b2588-107">**Description**</span><span class="sxs-lookup"><span data-stu-id="b2588-107">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b2588-108">TRUE</span><span class="sxs-lookup"><span data-stu-id="b2588-108">TRUE</span></span>  <br/> |<span data-ttu-id="b2588-109">L'action apparaît dans le menu mais est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="b2588-109">The action appears on the menu but is read-only.</span></span>  <br/> |
|<span data-ttu-id="b2588-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="b2588-110">FALSE</span></span>  <br/> |<span data-ttu-id="b2588-111">L'action apparaît dans le menu et peut être sélectionnée (valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="b2588-111">The action appears on the menu and can be selected (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b2588-112">Note</span><span class="sxs-lookup"><span data-stu-id="b2588-112">Remarks</span></span>

<span data-ttu-id="b2588-113">Lorsqu’une action est en lecture seule, il apparaît dans le menu contextuel ou de balise d’action, mais vous ne pouvez pas le sélectionner.</span><span class="sxs-lookup"><span data-stu-id="b2588-113">When an action is read-only, it appears on the action tag or shortcut menu but you cannot select it.</span></span> <span data-ttu-id="b2588-114">Il n’est pas grisée mais apparaît sur un fond de couleur, comme une étiquette.</span><span class="sxs-lookup"><span data-stu-id="b2588-114">It is not dimmed but rather appears on a colored background, like a label.</span></span> <span data-ttu-id="b2588-115">Pour rendre l’élément de menu apparaît estompé, utilisez la cellule Disabled.</span><span class="sxs-lookup"><span data-stu-id="b2588-115">To make the menu item appear dimmed, use the Disabled cell.</span></span> 
  
<span data-ttu-id="b2588-116">Pour obtenir une référence à la cellule ReadOnly par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="b2588-116">To get a reference to the ReadOnly cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b2588-117">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="b2588-117">Cell name:</span></span>  <br/> |<span data-ttu-id="b2588-118">Actions.</span><span class="sxs-lookup"><span data-stu-id="b2588-118">Actions.</span></span> <span data-ttu-id="b2588-119">*nom* . Actions ReadOnlywhere.</span><span class="sxs-lookup"><span data-stu-id="b2588-119">*name*  .ReadOnlywhere Actions.</span></span>  <span data-ttu-id="b2588-120">*nom* est le nom de la ligne Actions</span><span class="sxs-lookup"><span data-stu-id="b2588-120">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="b2588-121">Pour obtenir une référence à la cellule ReadOnly par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="b2588-121">To get a reference to the ReadOnly cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b2588-122">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="b2588-122">Section index:</span></span>  <br/> |<span data-ttu-id="b2588-123">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="b2588-123">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="b2588-124">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="b2588-124">Row index:</span></span>  <br/> |<span data-ttu-id="b2588-125">**visRowAction** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="b2588-125">**visRowAction** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="b2588-126">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="b2588-126">Cell index:</span></span>  <br/> |<span data-ttu-id="b2588-127">**visActionReadOnly**</span><span class="sxs-lookup"><span data-stu-id="b2588-127">**visActionReadOnly**</span></span> <br/> |
   

