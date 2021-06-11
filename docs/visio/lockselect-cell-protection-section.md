---
title: LockSelect, cellule (section Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm660
localization_priority: Normal
ms.assetid: c96b45a5-719e-8c4b-71b9-cb2224d83e21
description: Empêche la sélection d'une forme.
ms.openlocfilehash: c9f762f390dbea1e4ff2bd5bcf9566b8c67df11f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409754"
---
# <a name="lockselect-cell-protection-section"></a><span data-ttu-id="73d7b-103">LockSelect, cellule (section Protection)</span><span class="sxs-lookup"><span data-stu-id="73d7b-103">LockSelect Cell (Protection Section)</span></span>

<span data-ttu-id="73d7b-104">Empêche la sélection d'une forme.</span><span class="sxs-lookup"><span data-stu-id="73d7b-104">Prevents a shape from being selected.</span></span>
  
|<span data-ttu-id="73d7b-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="73d7b-105">**Value**</span></span>|<span data-ttu-id="73d7b-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="73d7b-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="73d7b-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="73d7b-107">TRUE</span></span>  <br/> | <span data-ttu-id="73d7b-108">La forme ne peut pas être sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="73d7b-108">Shape cannot be selected.</span></span>  <br/> |
| <span data-ttu-id="73d7b-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="73d7b-109">FALSE</span></span>  <br/> | <span data-ttu-id="73d7b-110">La forme peut être sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="73d7b-110">Shape can be selected.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="73d7b-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="73d7b-111">Remarks</span></span>

<span data-ttu-id="73d7b-112">Pour que l'effet de LockSelect s'applique, la case **Formes** doit être activée dans la boîte de dialogue **Protéger le document**.</span><span class="sxs-lookup"><span data-stu-id="73d7b-112">In order for LockSelect to take effect, the **Shapes** check box must be selected in the **Protect Document** dialog box.</span></span> 
  
<span data-ttu-id="73d7b-113">Pour obtenir une référence à la cellule LockSelect par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="73d7b-113">To get a reference to the LockSelect cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="73d7b-114">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="73d7b-114">Cell name:</span></span>  <br/> | <span data-ttu-id="73d7b-115">LockSelect</span><span class="sxs-lookup"><span data-stu-id="73d7b-115">LockSelect</span></span>  <br/> |
   
<span data-ttu-id="73d7b-116">Pour obtenir une référence à la cellule LockSelect à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="73d7b-116">To get a reference to the LockSelect cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="73d7b-117">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="73d7b-117">Section index:</span></span>  <br/> |<span data-ttu-id="73d7b-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="73d7b-118">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="73d7b-119">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="73d7b-119">Row index:</span></span>  <br/> |<span data-ttu-id="73d7b-120">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="73d7b-120">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="73d7b-121">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="73d7b-121">Cell index:</span></span>  <br/> |<span data-ttu-id="73d7b-122">**visLockSelect**</span><span class="sxs-lookup"><span data-stu-id="73d7b-122">**visLockSelect**</span></span> <br/> |
   

