---
title: LockGroup, cellule (section Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251227
localization_priority: Normal
ms.assetid: 04b0fa5b-1680-cfe2-6aaf-0502ad196027
description: Verrouille un groupe afin d'empêcher sa dissociation.
ms.openlocfilehash: 0cb2c0653780dcb653e5903faaaa0ebf30ea9d69
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341791"
---
# <a name="lockgroup-cell-protection-section"></a><span data-ttu-id="0ccbe-103">LockGroup, cellule (section Protection)</span><span class="sxs-lookup"><span data-stu-id="0ccbe-103">LockGroup Cell (Protection Section)</span></span>

<span data-ttu-id="0ccbe-104">Verrouille un groupe afin d'empêcher sa dissociation.</span><span class="sxs-lookup"><span data-stu-id="0ccbe-104">Locks a group so that it cannot be ungrouped.</span></span>
  
|<span data-ttu-id="0ccbe-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="0ccbe-105">**Value**</span></span>|<span data-ttu-id="0ccbe-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="0ccbe-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0ccbe-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="0ccbe-107">TRUE</span></span>  <br/> |<span data-ttu-id="0ccbe-108">Le groupe ne peut pas être dissocié.</span><span class="sxs-lookup"><span data-stu-id="0ccbe-108">Group cannot be ungrouped.</span></span>  <br/> |
|<span data-ttu-id="0ccbe-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="0ccbe-109">FALSE</span></span>  <br/> |<span data-ttu-id="0ccbe-110">Le groupe peut être dissocié.</span><span class="sxs-lookup"><span data-stu-id="0ccbe-110">Group can be ungrouped.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0ccbe-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="0ccbe-111">Remarks</span></span>

<span data-ttu-id="0ccbe-112">La définition de la valeur LockGroupCell sur TRUE empêche également la suppression de toutes les formes qui sont membres du groupe.</span><span class="sxs-lookup"><span data-stu-id="0ccbe-112">Setting the LockGroupCell value to TRUE also prevents deletion of any shapes that are members of the group.</span></span>
  
<span data-ttu-id="0ccbe-113">Pour obtenir une référence à la cellule LockGroup par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="0ccbe-113">To get a reference to the LockGroup cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0ccbe-114">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="0ccbe-114">Cell name:</span></span>  <br/> |<span data-ttu-id="0ccbe-115">LockGroup</span><span class="sxs-lookup"><span data-stu-id="0ccbe-115">LockGroup</span></span>  <br/> |
   
<span data-ttu-id="0ccbe-116">Pour obtenir une référence à la cellule LockGroup à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="0ccbe-116">To get a reference to the LockGroup cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0ccbe-117">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="0ccbe-117">Section index:</span></span>  <br/> |<span data-ttu-id="0ccbe-118">**Définis**</span><span class="sxs-lookup"><span data-stu-id="0ccbe-118">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="0ccbe-119">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="0ccbe-119">Row index:</span></span>  <br/> |<span data-ttu-id="0ccbe-120">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="0ccbe-120">**visRowLock**</span></span> <br/> |
|<span data-ttu-id="0ccbe-121">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="0ccbe-121">Cell index:</span></span>  <br/> |<span data-ttu-id="0ccbe-122">**visLockGroup**</span><span class="sxs-lookup"><span data-stu-id="0ccbe-122">**visLockGroup**</span></span> <br/> |
   

