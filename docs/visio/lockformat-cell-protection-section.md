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
ms.openlocfilehash: e0d1bb8a65b8087136e57bb46ad9f5363da30030
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409677"
---
# <a name="lockformat-cell-protection-section"></a><span data-ttu-id="81a38-103">LockFormat, cellule (section Protection)</span><span class="sxs-lookup"><span data-stu-id="81a38-103">LockFormat Cell (Protection Section)</span></span>

<span data-ttu-id="81a38-104">Verrouille la mise en forme d'une forme afin d'empêcher sa modification.</span><span class="sxs-lookup"><span data-stu-id="81a38-104">Locks the formatting of a shape so it cannot be changed.</span></span>
  
|<span data-ttu-id="81a38-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="81a38-105">**Value**</span></span>|<span data-ttu-id="81a38-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="81a38-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="81a38-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="81a38-107">TRUE</span></span>  <br/> | <span data-ttu-id="81a38-108">La mise en forme ne peut pas être modifiée.</span><span class="sxs-lookup"><span data-stu-id="81a38-108">Formatting cannot be changed.</span></span>  <br/> |
| <span data-ttu-id="81a38-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="81a38-109">FALSE</span></span>  <br/> | <span data-ttu-id="81a38-110">La mise en forme peut être modifiée.</span><span class="sxs-lookup"><span data-stu-id="81a38-110">Formatting can be changed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="81a38-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="81a38-111">Remarks</span></span>

<span data-ttu-id="81a38-112">Pour obtenir une référence à la cellule LockFormat par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="81a38-112">To get a reference to the LockFormat cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="81a38-113">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="81a38-113">Cell name:</span></span>  <br/> | <span data-ttu-id="81a38-114">LockFormat</span><span class="sxs-lookup"><span data-stu-id="81a38-114">LockFormat</span></span>  <br/> |
   
<span data-ttu-id="81a38-115">Pour obtenir une référence à la cellule LockFormat à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="81a38-115">To get a reference to the LockFormat cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="81a38-116">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="81a38-116">Section index:</span></span>  <br/> |<span data-ttu-id="81a38-117">**Définis**</span><span class="sxs-lookup"><span data-stu-id="81a38-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="81a38-118">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="81a38-118">Row index:</span></span>  <br/> |<span data-ttu-id="81a38-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="81a38-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="81a38-120">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="81a38-120">Cell index:</span></span>  <br/> |<span data-ttu-id="81a38-121">**visLockFormat**</span><span class="sxs-lookup"><span data-stu-id="81a38-121">**visLockFormat**</span></span> <br/> |
   

