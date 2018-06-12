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
ms.openlocfilehash: 7c5bcdbfe5b7d8e796af49c8da6ef0fc233e3d62
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788271"
---
# <a name="checked-cell-actions-section"></a><span data-ttu-id="e560a-103">Checked, cellule (section Actions)</span><span class="sxs-lookup"><span data-stu-id="e560a-103">Checked Cell (Actions Section)</span></span>

<span data-ttu-id="e560a-104">Indique si une option est cochée dans le menu contextuel ou de balise d’action.</span><span class="sxs-lookup"><span data-stu-id="e560a-104">Indicates whether an item is checked on the shortcut or action tag menu.</span></span>
  
> [!NOTE]
> <span data-ttu-id="e560a-105">Dans les versions précédentes de Microsoft Visio, les balises d’action sont appelées « balises actives ».</span><span class="sxs-lookup"><span data-stu-id="e560a-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="e560a-106">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="e560a-106">**Value**</span></span>|<span data-ttu-id="e560a-107">**Description**</span><span class="sxs-lookup"><span data-stu-id="e560a-107">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e560a-108">TRUE</span><span class="sxs-lookup"><span data-stu-id="e560a-108">TRUE</span></span>  <br/> |<span data-ttu-id="e560a-109">Coche est affichée.</span><span class="sxs-lookup"><span data-stu-id="e560a-109">Check mark is displayed.</span></span>  <br/> |
|<span data-ttu-id="e560a-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="e560a-110">FALSE</span></span>  <br/> |<span data-ttu-id="e560a-111">Case à cocher n’est pas affichée (valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="e560a-111">Check mark is not displayed (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e560a-112">Note</span><span class="sxs-lookup"><span data-stu-id="e560a-112">Remarks</span></span>

<span data-ttu-id="e560a-113">Pour obtenir une référence à la cellule Checked par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="e560a-113">To get a reference to the Checked cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e560a-114">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="e560a-114">Cell name:</span></span>  <br/> |<span data-ttu-id="e560a-115">Actions.</span><span class="sxs-lookup"><span data-stu-id="e560a-115">Actions.</span></span> <span data-ttu-id="e560a-116">*nom* . Vérifiée où Actions.</span><span class="sxs-lookup"><span data-stu-id="e560a-116">*name*  .Checked           where Actions.</span></span> <span data-ttu-id="e560a-117">*nom* est le nom de la ligne Actions</span><span class="sxs-lookup"><span data-stu-id="e560a-117">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="e560a-118">Pour obtenir une référence à la cellule Checked par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="e560a-118">To get a reference to the Checked cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e560a-119">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="e560a-119">Section index:</span></span>  <br/> |<span data-ttu-id="e560a-120">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="e560a-120">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="e560a-121">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="e560a-121">Row index:</span></span>  <br/> |<span data-ttu-id="e560a-122">**visRowAction** +  *i* où *i* = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="e560a-122">**visRowAction** +  *i*           where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
|<span data-ttu-id="e560a-123">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="e560a-123">Cell index:</span></span>  <br/> |<span data-ttu-id="e560a-124">**visActionChecked**</span><span class="sxs-lookup"><span data-stu-id="e560a-124">**visActionChecked**</span></span> <br/> |
   

