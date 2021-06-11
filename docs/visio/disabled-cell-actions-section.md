---
title: Disabled, cellule (section Actions)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251337
localization_priority: Normal
ms.assetid: ebf66729-d794-a398-268a-84d761bf06b6
description: Indique si une option d’un menu contextuel ou de balise d’action est désactivée.
ms.openlocfilehash: ddf55f40056d7df7a2403e500bb4bae335930433
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431350"
---
# <a name="disabled-cell-actions-section"></a><span data-ttu-id="7e035-103">Disabled, cellule (section Actions)</span><span class="sxs-lookup"><span data-stu-id="7e035-103">Disabled Cell (Actions Section)</span></span>

<span data-ttu-id="7e035-104">Indique si une option d’un menu contextuel ou de balise d’action est désactivée.</span><span class="sxs-lookup"><span data-stu-id="7e035-104">Indicates whether an item on a shortcut or action tag menu is disabled.</span></span>
  
> [!NOTE]
> <span data-ttu-id="7e035-105">Dans les versions précédentes de Microsoft Visio, les balises d’action sont appelées « balises actives ».</span><span class="sxs-lookup"><span data-stu-id="7e035-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="7e035-106">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="7e035-106">**Value**</span></span>|<span data-ttu-id="7e035-107">**Description**</span><span class="sxs-lookup"><span data-stu-id="7e035-107">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7e035-108">TRUE</span><span class="sxs-lookup"><span data-stu-id="7e035-108">TRUE</span></span>  <br/> |<span data-ttu-id="7e035-109">Désactive (fait apparaître en grisé) le nom de la commande.</span><span class="sxs-lookup"><span data-stu-id="7e035-109">Disable (dim) command name.</span></span>  <br/> |
|<span data-ttu-id="7e035-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="7e035-110">FALSE</span></span>  <br/> |<span data-ttu-id="7e035-111">Active le nom de la commande (valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="7e035-111">Enable the command name (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7e035-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="7e035-112">Remarks</span></span>

<span data-ttu-id="7e035-113">Pour obtenir une référence à la cellule Disabled à partir du nom d’une autre formule ou d’un programme à l’aide de la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="7e035-113">To get a reference to the Disabled cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7e035-114">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="7e035-114">Cell name:</span></span>  <br/> |<span data-ttu-id="7e035-115">Actions.</span><span class="sxs-lookup"><span data-stu-id="7e035-115">Actions.</span></span> <span data-ttu-id="7e035-116">*nom*  . Désactivation de l’endroit où Actions.</span><span class="sxs-lookup"><span data-stu-id="7e035-116">*name*  .Disabled           where Actions.</span></span> <span data-ttu-id="7e035-117">*name*  est le nom de la ligne Actions</span><span class="sxs-lookup"><span data-stu-id="7e035-117">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="7e035-118">Pour obtenir une référence à la cellule Disabled à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="7e035-118">To get a reference to the Disabled cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7e035-119">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="7e035-119">Section index:</span></span>  <br/> |<span data-ttu-id="7e035-120">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="7e035-120">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="7e035-121">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="7e035-121">Row index:</span></span>  <br/> |<span data-ttu-id="7e035-122">**visRowAction**  +   *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="7e035-122">**visRowAction** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="7e035-123">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="7e035-123">Cell index:</span></span>  <br/> |<span data-ttu-id="7e035-124">**visActionDisabled**</span><span class="sxs-lookup"><span data-stu-id="7e035-124">**visActionDisabled**</span></span> <br/> |
   

