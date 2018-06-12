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
ms.openlocfilehash: 8749b7d6db4a932b97c68ab5cf30b879a57d28f2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788839"
---
# <a name="invisible-cell-actions-section"></a><span data-ttu-id="db18a-103">Invisible, cellule (section Actions)</span><span class="sxs-lookup"><span data-stu-id="db18a-103">Invisible Cell (Actions Section)</span></span>

<span data-ttu-id="db18a-104">Indique si l’action est visible dans le menu contextuel ou de balise d’action.</span><span class="sxs-lookup"><span data-stu-id="db18a-104">Indicates whether the action is visible on the action tag or shortcut menu.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="db18a-105">Dans les versions précédentes de Microsoft Visio, les balises d’action sont appelées « balises actives ».</span><span class="sxs-lookup"><span data-stu-id="db18a-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="db18a-106">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="db18a-106">**Value**</span></span>|<span data-ttu-id="db18a-107">**Description**</span><span class="sxs-lookup"><span data-stu-id="db18a-107">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="db18a-108">TRUE</span><span class="sxs-lookup"><span data-stu-id="db18a-108">TRUE</span></span>  <br/> |<span data-ttu-id="db18a-109">L'action n'est pas visible dans le menu.</span><span class="sxs-lookup"><span data-stu-id="db18a-109">The action is not visible on the menu.</span></span>  <br/> |
|<span data-ttu-id="db18a-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="db18a-110">FALSE</span></span>  <br/> |<span data-ttu-id="db18a-111">L'action est visible dans le menu (valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="db18a-111">The action is visible on the menu (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="db18a-112">Note</span><span class="sxs-lookup"><span data-stu-id="db18a-112">Remarks</span></span>

<span data-ttu-id="db18a-113">Pour obtenir une référence à la cellule Invisible par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="db18a-113">To get a reference to the Invisible cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="db18a-114">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="db18a-114">Cell name:</span></span>  <br/> |<span data-ttu-id="db18a-115">Actions.</span><span class="sxs-lookup"><span data-stu-id="db18a-115">Actions.</span></span> <span data-ttu-id="db18a-116">*nom* . Actions Invisiblewhere.</span><span class="sxs-lookup"><span data-stu-id="db18a-116">*name*  .Invisiblewhere Actions.</span></span>  <span data-ttu-id="db18a-117">*nom* est le nom de la ligne Actions</span><span class="sxs-lookup"><span data-stu-id="db18a-117">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="db18a-118">Pour obtenir une référence à la cellule Invisible par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="db18a-118">To get a reference to the Invisible cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="db18a-119">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="db18a-119">Section index:</span></span>  <br/> |<span data-ttu-id="db18a-120">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="db18a-120">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="db18a-121">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="db18a-121">Row index:</span></span>  <br/> |<span data-ttu-id="db18a-122">**visRowAction** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="db18a-122">**visRowAction** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="db18a-123">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="db18a-123">Cell index:</span></span>  <br/> |<span data-ttu-id="db18a-124">**visActionInvisible**</span><span class="sxs-lookup"><span data-stu-id="db18a-124">**visActionInvisible**</span></span> <br/> |
   

