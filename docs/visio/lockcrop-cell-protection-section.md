---
title: LockCrop, cellule (section Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm610
localization_priority: Normal
ms.assetid: ae05de63-b527-66e6-2c79-056c9c92ec95
description: Verrouille un objet d'un autre programme afin d'empêcher qu'il ne soit découpé avec l'outil Découpe.
ms.openlocfilehash: bfb8bebd50908387fa3f94a8ca228935ef709133
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411854"
---
# <a name="lockcrop-cell-protection-section"></a><span data-ttu-id="edc5a-103">LockCrop, cellule (section Protection)</span><span class="sxs-lookup"><span data-stu-id="edc5a-103">LockCrop Cell (Protection Section)</span></span>

<span data-ttu-id="edc5a-104">Verrouille un objet d'un autre programme afin d'empêcher qu'il ne soit découpé avec l'outil **Découpe**.</span><span class="sxs-lookup"><span data-stu-id="edc5a-104">Locks an object from another program against being cropped with the **Crop** tool.</span></span> 
  
|<span data-ttu-id="edc5a-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="edc5a-105">**Value**</span></span>|<span data-ttu-id="edc5a-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="edc5a-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="edc5a-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="edc5a-107">TRUE</span></span>  <br/> | <span data-ttu-id="edc5a-108">La forme ne peut pas être découpée.</span><span class="sxs-lookup"><span data-stu-id="edc5a-108">Shape cannot be cropped</span></span>  <br/> |
| <span data-ttu-id="edc5a-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="edc5a-109">FALSE</span></span>  <br/> | <span data-ttu-id="edc5a-110">La forme peut être découpée.</span><span class="sxs-lookup"><span data-stu-id="edc5a-110">Shape can be cropped.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="edc5a-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="edc5a-111">Remarks</span></span>

<span data-ttu-id="edc5a-112">Pour obtenir une référence à la cellule LockCrop par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="edc5a-112">To get a reference to the LockCrop cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="edc5a-113">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="edc5a-113">Cell name:</span></span>  <br/> | <span data-ttu-id="edc5a-114">LockCrop</span><span class="sxs-lookup"><span data-stu-id="edc5a-114">LockCrop</span></span>  <br/> |
   
<span data-ttu-id="edc5a-115">Pour obtenir une référence à la cellule LockCrop à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="edc5a-115">To get a reference to the LockCrop cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="edc5a-116">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="edc5a-116">Section index:</span></span>  <br/> |<span data-ttu-id="edc5a-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="edc5a-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="edc5a-118">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="edc5a-118">Row index:</span></span>  <br/> |<span data-ttu-id="edc5a-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="edc5a-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="edc5a-120">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="edc5a-120">Cell index:</span></span>  <br/> |<span data-ttu-id="edc5a-121">**visLockCrop**</span><span class="sxs-lookup"><span data-stu-id="edc5a-121">**visLockCrop**</span></span> <br/> |
   

