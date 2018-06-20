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
description: Verrouille un objet à partir d’un autre programme afin d’être découpé avec l’outil découpe.
ms.openlocfilehash: d7f231d5dcb022548477e0817c9d408a8d1b86ec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788994"
---
# <a name="lockcrop-cell-protection-section"></a><span data-ttu-id="c8316-103">LockCrop, cellule (section Protection)</span><span class="sxs-lookup"><span data-stu-id="c8316-103">LockCrop Cell (Protection Section)</span></span>

<span data-ttu-id="c8316-104">Verrouille un objet à partir d’un autre programme afin d’être découpé avec l’outil **découpe** .</span><span class="sxs-lookup"><span data-stu-id="c8316-104">Locks an object from another program against being cropped with the **Crop** tool.</span></span> 
  
|<span data-ttu-id="c8316-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="c8316-105">**Value**</span></span>|<span data-ttu-id="c8316-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="c8316-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="c8316-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="c8316-107">TRUE</span></span>  <br/> | <span data-ttu-id="c8316-108">La forme ne peut pas être découpée.</span><span class="sxs-lookup"><span data-stu-id="c8316-108">Shape cannot be cropped</span></span>  <br/> |
| <span data-ttu-id="c8316-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="c8316-109">FALSE</span></span>  <br/> | <span data-ttu-id="c8316-110">La forme peut être découpée.</span><span class="sxs-lookup"><span data-stu-id="c8316-110">Shape can be cropped.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c8316-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="c8316-111">Remarks</span></span>

<span data-ttu-id="c8316-112">Pour obtenir une référence à la cellule LockCrop par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="c8316-112">To get a reference to the LockCrop cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c8316-113">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="c8316-113">Cell name:</span></span>  <br/> | <span data-ttu-id="c8316-114">LockCrop</span><span class="sxs-lookup"><span data-stu-id="c8316-114">LockCrop</span></span>  <br/> |
   
<span data-ttu-id="c8316-115">Pour obtenir une référence à la cellule LockCrop par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="c8316-115">To get a reference to the LockCrop cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c8316-116">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="c8316-116">Section index:</span></span>  <br/> |<span data-ttu-id="c8316-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c8316-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c8316-118">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="c8316-118">Row index:</span></span>  <br/> |<span data-ttu-id="c8316-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="c8316-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="c8316-120">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="c8316-120">Cell index:</span></span>  <br/> |<span data-ttu-id="c8316-121">**visLockCrop**</span><span class="sxs-lookup"><span data-stu-id="c8316-121">**visLockCrop**</span></span> <br/> |
   

