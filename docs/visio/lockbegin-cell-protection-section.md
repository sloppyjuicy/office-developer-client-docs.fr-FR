---
title: LockBegin, cellule (section Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm600
localization_priority: Normal
ms.assetid: cce34aba-caae-51ee-992e-92a490b68ea5
description: Verrouille le point de début (BeingX, BeginY) d'une forme 1D à un emplacement donné.
ms.openlocfilehash: c9b9a0e9b69de9b76d78ca7cebfb69116bd2fb72
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788982"
---
# <a name="lockbegin-cell-protection-section"></a><span data-ttu-id="a2804-103">LockBegin, cellule (section Protection)</span><span class="sxs-lookup"><span data-stu-id="a2804-103">LockBegin Cell (Protection Section)</span></span>

<span data-ttu-id="a2804-104">Verrouille le point de début (BeingX, BeginY) d'une forme 1D à un emplacement donné.</span><span class="sxs-lookup"><span data-stu-id="a2804-104">Locks the begin point (BeginX, BeginY) of a 1-D shape to a specific location.</span></span>
  
|<span data-ttu-id="a2804-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="a2804-105">**Value**</span></span>|<span data-ttu-id="a2804-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="a2804-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="a2804-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="a2804-107">TRUE</span></span>  <br/> | <span data-ttu-id="a2804-108">Le point de début est verrouillé.</span><span class="sxs-lookup"><span data-stu-id="a2804-108">Begin point is locked.</span></span>  <br/> |
| <span data-ttu-id="a2804-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="a2804-109">FALSE</span></span>  <br/> | <span data-ttu-id="a2804-110">Le point de début n'est pas verrouillé.</span><span class="sxs-lookup"><span data-stu-id="a2804-110">Begin is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a2804-111">Note</span><span class="sxs-lookup"><span data-stu-id="a2804-111">Remarks</span></span>

<span data-ttu-id="a2804-112">Pour obtenir une référence à la cellule LockBegin par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="a2804-112">To get a reference to the LockBegin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a2804-113">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="a2804-113">Cell name:</span></span>  <br/> | <span data-ttu-id="a2804-114">LockBegin</span><span class="sxs-lookup"><span data-stu-id="a2804-114">LockBegin</span></span>  <br/> |
   
<span data-ttu-id="a2804-115">Pour obtenir une référence à la cellule LockBegin par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="a2804-115">To get a reference to the LockBegin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a2804-116">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="a2804-116">Section index:</span></span>  <br/> |<span data-ttu-id="a2804-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a2804-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="a2804-118">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="a2804-118">Row index:</span></span>  <br/> |<span data-ttu-id="a2804-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="a2804-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="a2804-120">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="a2804-120">Cell index:</span></span>  <br/> |<span data-ttu-id="a2804-121">**visLockBegin**</span><span class="sxs-lookup"><span data-stu-id="a2804-121">**visLockBegin**</span></span> <br/> |
   

