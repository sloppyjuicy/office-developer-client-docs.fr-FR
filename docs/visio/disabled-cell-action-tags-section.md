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
ms.openlocfilehash: 409327365f3daf78dba20b1874be5911a517df0f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788472"
---
# <a name="disabled-cell-action-tags-section"></a><span data-ttu-id="25078-103">Disabled, cellule (section Action Tags)</span><span class="sxs-lookup"><span data-stu-id="25078-103">Disabled Cell (Action Tags Section)</span></span>

<span data-ttu-id="25078-104">Indique si la balise d’action s’affiche dans la fenêtre de dessin.</span><span class="sxs-lookup"><span data-stu-id="25078-104">Indicates whether the action tag appears in the drawing window.</span></span>
  
> [!NOTE]
> <span data-ttu-id="25078-105">Dans les versions précédentes de Microsoft Visio, les balises d’action sont appelées « balises actives ».</span><span class="sxs-lookup"><span data-stu-id="25078-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="25078-106">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="25078-106">**Value**</span></span>|<span data-ttu-id="25078-107">**Description**</span><span class="sxs-lookup"><span data-stu-id="25078-107">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="25078-108">TRUE</span><span class="sxs-lookup"><span data-stu-id="25078-108">TRUE</span></span>  <br/> | <span data-ttu-id="25078-109">La balise d’action est désactivée.</span><span class="sxs-lookup"><span data-stu-id="25078-109">The action tag is disabled.</span></span>  <br/> |
| <span data-ttu-id="25078-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="25078-110">FALSE</span></span>  <br/> | <span data-ttu-id="25078-111">La balise d’action est activée (valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="25078-111">The action tag is enabled (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="25078-112">Note</span><span class="sxs-lookup"><span data-stu-id="25078-112">Remarks</span></span>

<span data-ttu-id="25078-113">Lorsqu’une balise d’action est désactivée, elle ne s’affiche plus du tout tant qu’elle n’est pas réactivée.</span><span class="sxs-lookup"><span data-stu-id="25078-113">When an action tag is disabled, it does not appear at all until it is re-enabled.</span></span> 
  
<span data-ttu-id="25078-114">Pour obtenir une référence à la cellule Disabled par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="25078-114">To get a reference to the Disabled cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="25078-115">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="25078-115">Cell name:</span></span>  <br/> | <span data-ttu-id="25078-116">Balises actives.</span><span class="sxs-lookup"><span data-stu-id="25078-116">SmartTags.</span></span>  <span data-ttu-id="25078-117">*nom* . Désactivé où SmartTags.</span><span class="sxs-lookup"><span data-stu-id="25078-117">*name*  .Disabled           where SmartTags.</span></span> <span data-ttu-id="25078-118">*nom* est le nom de la ligne de balise d’action</span><span class="sxs-lookup"><span data-stu-id="25078-118">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="25078-119">Pour obtenir une référence à la cellule Disabled par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="25078-119">To get a reference to the Disabled cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="25078-120">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="25078-120">Section index:</span></span>  <br/> |<span data-ttu-id="25078-121">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="25078-121">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="25078-122">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="25078-122">Row index:</span></span>  <br/> |<span data-ttu-id="25078-123">**visRowSmartTag** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="25078-123">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="25078-124">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="25078-124">Cell index:</span></span>  <br/> |<span data-ttu-id="25078-125">**visSmartTagDisabled**</span><span class="sxs-lookup"><span data-stu-id="25078-125">**visSmartTagDisabled**</span></span> <br/> |
   

