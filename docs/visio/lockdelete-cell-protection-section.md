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
ms.openlocfilehash: 00229dcabf45d2a3435039ffe05fd7eb4de75808
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788997"
---
# <a name="lockdelete-cell-protection-section"></a><span data-ttu-id="33a43-103">LockDelete, cellule (section Protection)</span><span class="sxs-lookup"><span data-stu-id="33a43-103">LockDelete Cell (Protection Section)</span></span>

<span data-ttu-id="33a43-104">Verrouille la forme afin d'empêcher sa suppression.</span><span class="sxs-lookup"><span data-stu-id="33a43-104">Locks the shape so that it cannot be deleted.</span></span>
  
|<span data-ttu-id="33a43-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="33a43-105">**Value**</span></span>|<span data-ttu-id="33a43-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="33a43-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="33a43-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="33a43-107">TRUE</span></span>  <br/> | <span data-ttu-id="33a43-108">La forme ne peut pas être supprimée.</span><span class="sxs-lookup"><span data-stu-id="33a43-108">Shape cannot be deleted</span></span>  <br/> |
| <span data-ttu-id="33a43-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="33a43-109">FALSE</span></span>  <br/> | <span data-ttu-id="33a43-110">La forme peut être supprimée.</span><span class="sxs-lookup"><span data-stu-id="33a43-110">Shape can be deleted.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="33a43-111">Note</span><span class="sxs-lookup"><span data-stu-id="33a43-111">Remarks</span></span>

<span data-ttu-id="33a43-112">Pour obtenir une référence à la cellule LockDelete par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="33a43-112">To get a reference to the LockDelete cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="33a43-113">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="33a43-113">Cell name:</span></span>  <br/> | <span data-ttu-id="33a43-114">LockDelete</span><span class="sxs-lookup"><span data-stu-id="33a43-114">LockDelete</span></span>  <br/> |
   
<span data-ttu-id="33a43-115">Pour obtenir une référence à la cellule LockDelete par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="33a43-115">To get a reference to the LockDelete cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="33a43-116">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="33a43-116">Section index:</span></span>  <br/> |<span data-ttu-id="33a43-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="33a43-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="33a43-118">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="33a43-118">Row index:</span></span>  <br/> |<span data-ttu-id="33a43-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="33a43-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="33a43-120">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="33a43-120">Cell index:</span></span>  <br/> |<span data-ttu-id="33a43-121">**visLockDelete**</span><span class="sxs-lookup"><span data-stu-id="33a43-121">**visLockDelete**</span></span> <br/> |
   

