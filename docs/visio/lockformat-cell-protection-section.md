---
title: LockFormat, cellule (section Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm625
localization_priority: Normal
ms.assetid: e9a640f4-0af0-317c-b77b-f32c651e87b4
description: Verrouille la mise en forme d'une forme afin d'empêcher sa modification.
ms.openlocfilehash: c3e4d5be848e91554406e709ce6872ae49b5f38d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788999"
---
# <a name="lockformat-cell-protection-section"></a><span data-ttu-id="d7b23-103">LockFormat, cellule (section Protection)</span><span class="sxs-lookup"><span data-stu-id="d7b23-103">LockFormat Cell (Protection Section)</span></span>

<span data-ttu-id="d7b23-104">Verrouille la mise en forme d'une forme afin d'empêcher sa modification.</span><span class="sxs-lookup"><span data-stu-id="d7b23-104">Locks the formatting of a shape so it cannot be changed.</span></span>
  
|<span data-ttu-id="d7b23-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="d7b23-105">**Value**</span></span>|<span data-ttu-id="d7b23-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="d7b23-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="d7b23-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="d7b23-107">TRUE</span></span>  <br/> | <span data-ttu-id="d7b23-108">La mise en forme ne peut pas être modifiée.</span><span class="sxs-lookup"><span data-stu-id="d7b23-108">Formatting cannot be changed.</span></span>  <br/> |
| <span data-ttu-id="d7b23-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="d7b23-109">FALSE</span></span>  <br/> | <span data-ttu-id="d7b23-110">La mise en forme peut être modifiée.</span><span class="sxs-lookup"><span data-stu-id="d7b23-110">Formatting can be changed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d7b23-111">Note</span><span class="sxs-lookup"><span data-stu-id="d7b23-111">Remarks</span></span>

<span data-ttu-id="d7b23-112">Pour obtenir une référence à la cellule LockFormat par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="d7b23-112">To get a reference to the LockFormat cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d7b23-113">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="d7b23-113">Cell name:</span></span>  <br/> | <span data-ttu-id="d7b23-114">LockFormat</span><span class="sxs-lookup"><span data-stu-id="d7b23-114">LockFormat</span></span>  <br/> |
   
<span data-ttu-id="d7b23-115">Pour obtenir une référence à la cellule LockFormat par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="d7b23-115">To get a reference to the LockFormat cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d7b23-116">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="d7b23-116">Section index:</span></span>  <br/> |<span data-ttu-id="d7b23-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d7b23-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="d7b23-118">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="d7b23-118">Row index:</span></span>  <br/> |<span data-ttu-id="d7b23-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="d7b23-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="d7b23-120">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="d7b23-120">Cell index:</span></span>  <br/> |<span data-ttu-id="d7b23-121">**visLockFormat**</span><span class="sxs-lookup"><span data-stu-id="d7b23-121">**visLockFormat**</span></span> <br/> |
   

