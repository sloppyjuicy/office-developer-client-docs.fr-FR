---
title: LockVtxEdit, cellule (section Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251224
localization_priority: Normal
ms.assetid: 966cde5c-f04e-7149-3660-720ffa4f7079
description: Verrouille les sommets d’une forme afin d’empêcher leur modification.
ms.openlocfilehash: 1703769fe54171a14f7052f0f6686e1eb5ec92fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417664"
---
# <a name="lockvtxedit-cell-protection-section"></a><span data-ttu-id="9edbe-103">LockVtxEdit, cellule (section Protection)</span><span class="sxs-lookup"><span data-stu-id="9edbe-103">LockVtxEdit Cell (Protection Section)</span></span>

<span data-ttu-id="9edbe-104">Verrouille les sommets d’une forme afin d’empêcher leur modification.</span><span class="sxs-lookup"><span data-stu-id="9edbe-104">Locks the vertices of a shape so that they cannot be edited.</span></span>
  
|<span data-ttu-id="9edbe-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="9edbe-105">**Value**</span></span>|<span data-ttu-id="9edbe-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="9edbe-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9edbe-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="9edbe-107">TRUE</span></span>  <br/> |<span data-ttu-id="9edbe-108">Les sommets ne peuvent pas être modifiés.</span><span class="sxs-lookup"><span data-stu-id="9edbe-108">Vertices cannot be edited.</span></span>  <br/> |
|<span data-ttu-id="9edbe-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="9edbe-109">FALSE</span></span>  <br/> |<span data-ttu-id="9edbe-110">Les sommets peuvent être modifiés.</span><span class="sxs-lookup"><span data-stu-id="9edbe-110">Vertices can be edited.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9edbe-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="9edbe-111">Remarks</span></span>

<span data-ttu-id="9edbe-112">Pour obtenir une référence à la cellule LockVtxEdit par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="9edbe-112">To get a reference to the LockVtxEdit cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9edbe-113">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="9edbe-113">Cell name:</span></span>  <br/> |<span data-ttu-id="9edbe-114">LockVtxEdit</span><span class="sxs-lookup"><span data-stu-id="9edbe-114">LockVtxEdit</span></span>  <br/> |
   
<span data-ttu-id="9edbe-115">Pour obtenir une référence à la cellule LockVtxEdit à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="9edbe-115">To get a reference to the LockVtxEdit cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9edbe-116">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="9edbe-116">Section index:</span></span>  <br/> |<span data-ttu-id="9edbe-117">**Définis**</span><span class="sxs-lookup"><span data-stu-id="9edbe-117">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="9edbe-118">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="9edbe-118">Row index:</span></span>  <br/> |<span data-ttu-id="9edbe-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="9edbe-119">**visRowLock**</span></span> <br/> |
|<span data-ttu-id="9edbe-120">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="9edbe-120">Cell index:</span></span>  <br/> |<span data-ttu-id="9edbe-121">**visLockVtxEdit**</span><span class="sxs-lookup"><span data-stu-id="9edbe-121">**visLockVtxEdit**</span></span> <br/> |
   

