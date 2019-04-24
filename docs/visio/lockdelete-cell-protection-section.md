---
title: LockDelete, cellule (section Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251219
localization_priority: Normal
ms.assetid: 596c62b7-8d42-1854-d709-592db09a6a84
description: Verrouille la forme afin d'empêcher sa suppression.
ms.openlocfilehash: 0819969c9ba17a52de19341b359b33ceae5b44d8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359618"
---
# <a name="lockdelete-cell-protection-section"></a><span data-ttu-id="026af-103">LockDelete, cellule (section Protection)</span><span class="sxs-lookup"><span data-stu-id="026af-103">LockDelete Cell (Protection Section)</span></span>

<span data-ttu-id="026af-104">Verrouille la forme afin d'empêcher sa suppression.</span><span class="sxs-lookup"><span data-stu-id="026af-104">Locks the shape so that it cannot be deleted.</span></span>
  
|<span data-ttu-id="026af-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="026af-105">**Value**</span></span>|<span data-ttu-id="026af-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="026af-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="026af-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="026af-107">TRUE</span></span>  <br/> | <span data-ttu-id="026af-108">La forme ne peut pas être supprimée.</span><span class="sxs-lookup"><span data-stu-id="026af-108">Shape cannot be deleted</span></span>  <br/> |
| <span data-ttu-id="026af-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="026af-109">FALSE</span></span>  <br/> | <span data-ttu-id="026af-110">La forme peut être supprimée.</span><span class="sxs-lookup"><span data-stu-id="026af-110">Shape can be deleted.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="026af-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="026af-111">Remarks</span></span>

<span data-ttu-id="026af-112">Pour obtenir une référence à la cellule LockDelete par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="026af-112">To get a reference to the LockDelete cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="026af-113">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="026af-113">Cell name:</span></span>  <br/> | <span data-ttu-id="026af-114">LockDelete</span><span class="sxs-lookup"><span data-stu-id="026af-114">LockDelete</span></span>  <br/> |
   
<span data-ttu-id="026af-115">Pour obtenir une référence à la cellule LockDelete à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="026af-115">To get a reference to the LockDelete cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="026af-116">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="026af-116">Section index:</span></span>  <br/> |<span data-ttu-id="026af-117">**Définis**</span><span class="sxs-lookup"><span data-stu-id="026af-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="026af-118">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="026af-118">Row index:</span></span>  <br/> |<span data-ttu-id="026af-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="026af-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="026af-120">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="026af-120">Cell index:</span></span>  <br/> |<span data-ttu-id="026af-121">**visLockDelete**</span><span class="sxs-lookup"><span data-stu-id="026af-121">**visLockDelete**</span></span> <br/> |
   

