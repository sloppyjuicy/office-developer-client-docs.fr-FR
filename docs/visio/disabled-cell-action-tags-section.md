---
title: Disabled, cellule (section Action Tags)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60038
localization_priority: Normal
ms.assetid: bf0a80c9-0fdb-e2cf-3ab0-74cb6338fdce
description: Indique si la balise d’action s’affiche dans la fenêtre de dessin.
ms.openlocfilehash: 867d36e27cb890509b0687500caf719362a711fb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439666"
---
# <a name="disabled-cell-action-tags-section"></a><span data-ttu-id="06762-103">Disabled, cellule (section Action Tags)</span><span class="sxs-lookup"><span data-stu-id="06762-103">Disabled Cell (Action Tags Section)</span></span>

<span data-ttu-id="06762-104">Indique si la balise d’action s’affiche dans la fenêtre de dessin.</span><span class="sxs-lookup"><span data-stu-id="06762-104">Indicates whether the action tag appears in the drawing window.</span></span>
  
> [!NOTE]
> <span data-ttu-id="06762-105">Dans les versions précédentes de Microsoft Visio, les balises d’action sont appelées « balises actives ».</span><span class="sxs-lookup"><span data-stu-id="06762-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="06762-106">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="06762-106">**Value**</span></span>|<span data-ttu-id="06762-107">**Description**</span><span class="sxs-lookup"><span data-stu-id="06762-107">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="06762-108">TRUE</span><span class="sxs-lookup"><span data-stu-id="06762-108">TRUE</span></span>  <br/> | <span data-ttu-id="06762-109">La balise d’action est désactivée.</span><span class="sxs-lookup"><span data-stu-id="06762-109">The action tag is disabled.</span></span>  <br/> |
| <span data-ttu-id="06762-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="06762-110">FALSE</span></span>  <br/> | <span data-ttu-id="06762-111">La balise d’action est activée (valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="06762-111">The action tag is enabled (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="06762-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="06762-112">Remarks</span></span>

<span data-ttu-id="06762-113">Lorsqu’une balise d’action est désactivée, elle ne s’affiche plus du tout tant qu’elle n’est pas réactivée.</span><span class="sxs-lookup"><span data-stu-id="06762-113">When an action tag is disabled, it does not appear at all until it is re-enabled.</span></span> 
  
<span data-ttu-id="06762-114">Pour obtenir une référence à la cellule Disabled à partir du nom d’une autre formule ou d’un programme à l’aide de la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="06762-114">To get a reference to the Disabled cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="06762-115">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="06762-115">Cell name:</span></span>  <br/> | <span data-ttu-id="06762-116">SmartTag.</span><span class="sxs-lookup"><span data-stu-id="06762-116">SmartTags.</span></span>  <span data-ttu-id="06762-117">*nom* . Désactivé où SmartTags.</span><span class="sxs-lookup"><span data-stu-id="06762-117">*name*  .Disabled           where SmartTags.</span></span> <span data-ttu-id="06762-118">*Name* est le nom de la ligne de balise d'action</span><span class="sxs-lookup"><span data-stu-id="06762-118">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="06762-119">Pour obtenir une référence à la cellule Disabled à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="06762-119">To get a reference to the Disabled cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="06762-120">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="06762-120">Section index:</span></span>  <br/> |<span data-ttu-id="06762-121">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="06762-121">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="06762-122">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="06762-122">Row index:</span></span>  <br/> |<span data-ttu-id="06762-123">**visRowSmartTag** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="06762-123">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="06762-124">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="06762-124">Cell index:</span></span>  <br/> |<span data-ttu-id="06762-125">**visSmartTagDisabled**</span><span class="sxs-lookup"><span data-stu-id="06762-125">**visSmartTagDisabled**</span></span> <br/> |
   

