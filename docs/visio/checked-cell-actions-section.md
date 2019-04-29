---
title: Checked, cellule (section Actions)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm155
localization_priority: Normal
ms.assetid: 50937e29-eaa1-0cd0-53cc-dc17e7793e55
description: Indique si une option est cochée dans le menu contextuel ou de balise d’action.
ms.openlocfilehash: 870823f28d802e7cafa81efbe5617f27b6714885
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438329"
---
# <a name="checked-cell-actions-section"></a><span data-ttu-id="f49a6-103">Checked, cellule (section Actions)</span><span class="sxs-lookup"><span data-stu-id="f49a6-103">Checked Cell (Actions Section)</span></span>

<span data-ttu-id="f49a6-104">Indique si une option est cochée dans le menu contextuel ou de balise d’action.</span><span class="sxs-lookup"><span data-stu-id="f49a6-104">Indicates whether an item is checked on the shortcut or action tag menu.</span></span>
  
> [!NOTE]
> <span data-ttu-id="f49a6-105">Dans les versions précédentes de Microsoft Visio, les balises d’action sont appelées « balises actives ».</span><span class="sxs-lookup"><span data-stu-id="f49a6-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="f49a6-106">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="f49a6-106">**Value**</span></span>|<span data-ttu-id="f49a6-107">**Description**</span><span class="sxs-lookup"><span data-stu-id="f49a6-107">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f49a6-108">TRUE</span><span class="sxs-lookup"><span data-stu-id="f49a6-108">TRUE</span></span>  <br/> |<span data-ttu-id="f49a6-109">La coche est affichée.</span><span class="sxs-lookup"><span data-stu-id="f49a6-109">Check mark is displayed.</span></span>  <br/> |
|<span data-ttu-id="f49a6-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="f49a6-110">FALSE</span></span>  <br/> |<span data-ttu-id="f49a6-111">La coche n'est pas affichée (valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="f49a6-111">Check mark is not displayed (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f49a6-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="f49a6-112">Remarks</span></span>

<span data-ttu-id="f49a6-113">Pour obtenir une référence à la cellule Checked à partir du nom d’une autre formule ou d’un programme à l’aide de la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="f49a6-113">To get a reference to the Checked cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f49a6-114">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="f49a6-114">Cell name:</span></span>  <br/> |<span data-ttu-id="f49a6-115">Mesures.</span><span class="sxs-lookup"><span data-stu-id="f49a6-115">Actions.</span></span> <span data-ttu-id="f49a6-116">*nom* . Checked WHERE actions.</span><span class="sxs-lookup"><span data-stu-id="f49a6-116">*name*  .Checked           where Actions.</span></span> <span data-ttu-id="f49a6-117">*Name* est le nom de la ligne d'actions</span><span class="sxs-lookup"><span data-stu-id="f49a6-117">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="f49a6-118">Pour obtenir une référence à la cellule Checked à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="f49a6-118">To get a reference to the Checked cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f49a6-119">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="f49a6-119">Section index:</span></span>  <br/> |<span data-ttu-id="f49a6-120">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="f49a6-120">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="f49a6-121">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="f49a6-121">Row index:</span></span>  <br/> |<span data-ttu-id="f49a6-122">**visRowAction** +  *i* où *i* = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="f49a6-122">**visRowAction** +  *i*           where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
|<span data-ttu-id="f49a6-123">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="f49a6-123">Cell index:</span></span>  <br/> |<span data-ttu-id="f49a6-124">**visActionChecked**</span><span class="sxs-lookup"><span data-stu-id="f49a6-124">**visActionChecked**</span></span> <br/> |
   

