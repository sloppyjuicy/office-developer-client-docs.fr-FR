---
title: Invisible, cellule (section Actions)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60046
localization_priority: Normal
ms.assetid: 070b4468-c907-b201-1633-1d3e10ecc2b2
description: Indique si l’action est visible dans le menu contextuel ou de balise d’action.
ms.openlocfilehash: 69bc96e76f27a64d6e1443f045c27566f598c1db
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297241"
---
# <a name="invisible-cell-actions-section"></a><span data-ttu-id="568cd-103">Invisible, cellule (section Actions)</span><span class="sxs-lookup"><span data-stu-id="568cd-103">Invisible Cell (Actions Section)</span></span>

<span data-ttu-id="568cd-104">Indique si l’action est visible dans le menu contextuel ou de balise d’action.</span><span class="sxs-lookup"><span data-stu-id="568cd-104">Indicates whether the action is visible on the action tag or shortcut menu.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="568cd-105">Dans les versions précédentes de Microsoft Visio, les balises d’action sont appelées « balises actives ».</span><span class="sxs-lookup"><span data-stu-id="568cd-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="568cd-106">**Value**</span><span class="sxs-lookup"><span data-stu-id="568cd-106">**Value**</span></span>|<span data-ttu-id="568cd-107">**Description**</span><span class="sxs-lookup"><span data-stu-id="568cd-107">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="568cd-108">TRUE</span><span class="sxs-lookup"><span data-stu-id="568cd-108">TRUE</span></span>  <br/> |<span data-ttu-id="568cd-109">L'action n'est pas visible dans le menu.</span><span class="sxs-lookup"><span data-stu-id="568cd-109">The action is not visible on the menu.</span></span>  <br/> |
|<span data-ttu-id="568cd-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="568cd-110">FALSE</span></span>  <br/> |<span data-ttu-id="568cd-111">L'action est visible dans le menu (valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="568cd-111">The action is visible on the menu (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="568cd-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="568cd-112">Remarks</span></span>

<span data-ttu-id="568cd-113">Pour obtenir une référence à la cellule Invisible à partir du nom d’une autre formule ou d’un programme à l’aide de la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="568cd-113">To get a reference to the Invisible cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="568cd-114">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="568cd-114">Cell name:</span></span>  <br/> |<span data-ttu-id="568cd-115">Mesures.</span><span class="sxs-lookup"><span data-stu-id="568cd-115">Actions.</span></span> <span data-ttu-id="568cd-116">*nom* . Actions Invisibleoù.</span><span class="sxs-lookup"><span data-stu-id="568cd-116">*name*  .Invisiblewhere Actions.</span></span>  <span data-ttu-id="568cd-117">*Name* est le nom de la ligne d'actions</span><span class="sxs-lookup"><span data-stu-id="568cd-117">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="568cd-118">Pour obtenir une référence à la cellule Invisible à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="568cd-118">To get a reference to the Invisible cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="568cd-119">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="568cd-119">Section index:</span></span>  <br/> |<span data-ttu-id="568cd-120">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="568cd-120">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="568cd-121">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="568cd-121">Row index:</span></span>  <br/> |<span data-ttu-id="568cd-122">**visRowAction** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="568cd-122">**visRowAction** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="568cd-123">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="568cd-123">Cell index:</span></span>  <br/> |<span data-ttu-id="568cd-124">**visActionInvisible**</span><span class="sxs-lookup"><span data-stu-id="568cd-124">**visActionInvisible**</span></span> <br/> |
   

