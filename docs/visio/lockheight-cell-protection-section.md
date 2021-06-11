---
title: LockHeight, cellule (section Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm635
localization_priority: Normal
ms.assetid: 218b957e-5af6-e53b-1453-a84164ae456e
description: Verrouille la hauteur d'une forme afin qu'elle demeure intacte lorsque la forme est redimensionnée.
ms.openlocfilehash: 099f6597656d4389476818253f34e741ddd404de
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432085"
---
# <a name="lockheight-cell-protection-section"></a><span data-ttu-id="17b73-103">LockHeight, cellule (section Protection)</span><span class="sxs-lookup"><span data-stu-id="17b73-103">LockHeight Cell (Protection Section)</span></span>

<span data-ttu-id="17b73-104">Verrouille la hauteur d'une forme afin qu'elle demeure intacte lorsque la forme est redimensionnée.</span><span class="sxs-lookup"><span data-stu-id="17b73-104">Locks the height of the shape so that its height remains unchanged when the shape is resized.</span></span>
  
|<span data-ttu-id="17b73-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="17b73-105">**Value**</span></span>|<span data-ttu-id="17b73-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="17b73-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="17b73-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="17b73-107">TRUE</span></span>  <br/> | <span data-ttu-id="17b73-108">La hauteur est verrouillée.</span><span class="sxs-lookup"><span data-stu-id="17b73-108">Height is locked.</span></span>  <br/> |
| <span data-ttu-id="17b73-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="17b73-109">FALSE</span></span>  <br/> | <span data-ttu-id="17b73-110">La hauteur n'est pas verrouillée.</span><span class="sxs-lookup"><span data-stu-id="17b73-110">Height is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="17b73-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="17b73-111">Remarks</span></span>

<span data-ttu-id="17b73-112">Pour obtenir une référence à la cellule LockHeight par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="17b73-112">To get a reference to the LockHeight cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="17b73-113">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="17b73-113">Cell name:</span></span>  <br/> | <span data-ttu-id="17b73-114">LockHeight</span><span class="sxs-lookup"><span data-stu-id="17b73-114">LockHeight</span></span>  <br/> |
   
<span data-ttu-id="17b73-115">Pour obtenir une référence à la cellule LockHeight à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="17b73-115">To get a reference to the LockHeight cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="17b73-116">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="17b73-116">Section index:</span></span>  <br/> |<span data-ttu-id="17b73-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="17b73-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="17b73-118">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="17b73-118">Row index:</span></span>  <br/> |<span data-ttu-id="17b73-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="17b73-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="17b73-120">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="17b73-120">Cell index:</span></span>  <br/> |<span data-ttu-id="17b73-121">**visLockHeight**</span><span class="sxs-lookup"><span data-stu-id="17b73-121">**visLockHeight**</span></span> <br/> |
   

