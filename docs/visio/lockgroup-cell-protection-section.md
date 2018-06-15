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
ms.openlocfilehash: 4d09d514a3fff8ada40c67eb9cd9537539a1039a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19789019"
---
# <a name="lockgroup-cell-protection-section"></a><span data-ttu-id="dd44c-103">LockGroup, cellule (section Protection)</span><span class="sxs-lookup"><span data-stu-id="dd44c-103">LockGroup Cell (Protection Section)</span></span>

<span data-ttu-id="dd44c-104">Verrouille un groupe afin d'empêcher sa dissociation.</span><span class="sxs-lookup"><span data-stu-id="dd44c-104">Locks a group so that it cannot be ungrouped.</span></span>
  
|<span data-ttu-id="dd44c-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="dd44c-105">**Value**</span></span>|<span data-ttu-id="dd44c-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="dd44c-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="dd44c-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="dd44c-107">TRUE</span></span>  <br/> |<span data-ttu-id="dd44c-108">Le groupe ne peut pas être dissocié.</span><span class="sxs-lookup"><span data-stu-id="dd44c-108">Group cannot be ungrouped.</span></span>  <br/> |
|<span data-ttu-id="dd44c-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="dd44c-109">FALSE</span></span>  <br/> |<span data-ttu-id="dd44c-110">Le groupe peut être dissocié.</span><span class="sxs-lookup"><span data-stu-id="dd44c-110">Group can be ungrouped.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dd44c-111">Note</span><span class="sxs-lookup"><span data-stu-id="dd44c-111">Remarks</span></span>

<span data-ttu-id="dd44c-112">La définition de la valeur LockGroupCell sur TRUE empêche également la suppression de toutes les formes qui sont membres du groupe.</span><span class="sxs-lookup"><span data-stu-id="dd44c-112">Setting the LockGroupCell value to TRUE also prevents deletion of any shapes that are members of the group.</span></span>
  
<span data-ttu-id="dd44c-113">Pour obtenir une référence à la cellule LockGroup par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="dd44c-113">To get a reference to the LockGroup cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dd44c-114">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="dd44c-114">Cell name:</span></span>  <br/> |<span data-ttu-id="dd44c-115">LockGroup</span><span class="sxs-lookup"><span data-stu-id="dd44c-115">LockGroup</span></span>  <br/> |
   
<span data-ttu-id="dd44c-116">Pour obtenir une référence à la cellule LockGroup par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="dd44c-116">To get a reference to the LockGroup cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dd44c-117">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="dd44c-117">Section index:</span></span>  <br/> |<span data-ttu-id="dd44c-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="dd44c-118">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="dd44c-119">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="dd44c-119">Row index:</span></span>  <br/> |<span data-ttu-id="dd44c-120">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="dd44c-120">**visRowLock**</span></span> <br/> |
|<span data-ttu-id="dd44c-121">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="dd44c-121">Cell index:</span></span>  <br/> |<span data-ttu-id="dd44c-122">**visLockGroup**</span><span class="sxs-lookup"><span data-stu-id="dd44c-122">**visLockGroup**</span></span> <br/> |
   

