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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332577"
---
# <a name="disabled-cell-actions-section"></a><span data-ttu-id="e17fc-103">Disabled, cellule (section Actions)</span><span class="sxs-lookup"><span data-stu-id="e17fc-103">Disabled Cell (Actions Section)</span></span>

<span data-ttu-id="e17fc-104">Indique si une option d’un menu contextuel ou de balise d’action est désactivée.</span><span class="sxs-lookup"><span data-stu-id="e17fc-104">Indicates whether an item on a shortcut or action tag menu is disabled.</span></span>
  
> [!NOTE]
> <span data-ttu-id="e17fc-105">Dans les versions précédentes de Microsoft Visio, les balises d’action sont appelées « balises actives ».</span><span class="sxs-lookup"><span data-stu-id="e17fc-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="e17fc-106">**Value**</span><span class="sxs-lookup"><span data-stu-id="e17fc-106">**Value**</span></span>|<span data-ttu-id="e17fc-107">**Description**</span><span class="sxs-lookup"><span data-stu-id="e17fc-107">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e17fc-108">TRUE</span><span class="sxs-lookup"><span data-stu-id="e17fc-108">TRUE</span></span>  <br/> |<span data-ttu-id="e17fc-109">Désactive (fait apparaître en grisé) le nom de la commande.</span><span class="sxs-lookup"><span data-stu-id="e17fc-109">Disable (dim) command name.</span></span>  <br/> |
|<span data-ttu-id="e17fc-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="e17fc-110">FALSE</span></span>  <br/> |<span data-ttu-id="e17fc-111">Active le nom de la commande (valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="e17fc-111">Enable the command name (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e17fc-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="e17fc-112">Remarks</span></span>

<span data-ttu-id="e17fc-113">Pour obtenir une référence à la cellule Disabled à partir du nom d’une autre formule ou d’un programme à l’aide de la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="e17fc-113">To get a reference to the Disabled cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e17fc-114">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="e17fc-114">Cell name:</span></span>  <br/> |<span data-ttu-id="e17fc-115">Mesures.</span><span class="sxs-lookup"><span data-stu-id="e17fc-115">Actions.</span></span> <span data-ttu-id="e17fc-116">*nom* . Désactivé pour les actions.</span><span class="sxs-lookup"><span data-stu-id="e17fc-116">*name*  .Disabled           where Actions.</span></span> <span data-ttu-id="e17fc-117">*Name* est le nom de la ligne d'actions</span><span class="sxs-lookup"><span data-stu-id="e17fc-117">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="e17fc-118">Pour obtenir une référence à la cellule Disabled à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="e17fc-118">To get a reference to the Disabled cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e17fc-119">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="e17fc-119">Section index:</span></span>  <br/> |<span data-ttu-id="e17fc-120">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="e17fc-120">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="e17fc-121">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="e17fc-121">Row index:</span></span>  <br/> |<span data-ttu-id="e17fc-122">**visRowAction** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="e17fc-122">**visRowAction** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="e17fc-123">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="e17fc-123">Cell index:</span></span>  <br/> |<span data-ttu-id="e17fc-124">**visActionDisabled**</span><span class="sxs-lookup"><span data-stu-id="e17fc-124">**visActionDisabled**</span></span> <br/> |
   

