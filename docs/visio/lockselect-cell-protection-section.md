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
ms.openlocfilehash: 082e993f7773640f59022c46458563d491197908
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19789026"
---
# <a name="lockselect-cell-protection-section"></a><span data-ttu-id="ca045-103">LockSelect, cellule (section Protection)</span><span class="sxs-lookup"><span data-stu-id="ca045-103">LockSelect Cell (Protection Section)</span></span>

<span data-ttu-id="ca045-104">Empêche la sélection d'une forme.</span><span class="sxs-lookup"><span data-stu-id="ca045-104">Prevents a shape from being selected.</span></span>
  
|<span data-ttu-id="ca045-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="ca045-105">**Value**</span></span>|<span data-ttu-id="ca045-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="ca045-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="ca045-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="ca045-107">TRUE</span></span>  <br/> | <span data-ttu-id="ca045-108">La forme ne peut pas être sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="ca045-108">Shape cannot be selected.</span></span>  <br/> |
| <span data-ttu-id="ca045-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="ca045-109">FALSE</span></span>  <br/> | <span data-ttu-id="ca045-110">La forme peut être sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="ca045-110">Shape can be selected.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ca045-111">Note</span><span class="sxs-lookup"><span data-stu-id="ca045-111">Remarks</span></span>

<span data-ttu-id="ca045-112">Dans l’ordre pour que l’effet de LockSelect, la case **formes** doit être sélectionnée dans la boîte de dialogue **Protéger le Document** .</span><span class="sxs-lookup"><span data-stu-id="ca045-112">In order for LockSelect to take effect, the **Shapes** check box must be selected in the **Protect Document** dialog box.</span></span> 
  
<span data-ttu-id="ca045-113">Pour obtenir une référence à la cellule LockSelect par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="ca045-113">To get a reference to the LockSelect cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ca045-114">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="ca045-114">Cell name:</span></span>  <br/> | <span data-ttu-id="ca045-115">LockSelect</span><span class="sxs-lookup"><span data-stu-id="ca045-115">LockSelect</span></span>  <br/> |
   
<span data-ttu-id="ca045-116">Pour obtenir une référence à la cellule LockSelect par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="ca045-116">To get a reference to the LockSelect cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ca045-117">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="ca045-117">Section index:</span></span>  <br/> |<span data-ttu-id="ca045-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ca045-118">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="ca045-119">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="ca045-119">Row index:</span></span>  <br/> |<span data-ttu-id="ca045-120">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="ca045-120">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="ca045-121">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="ca045-121">Cell index:</span></span>  <br/> |<span data-ttu-id="ca045-122">**visLockSelect**</span><span class="sxs-lookup"><span data-stu-id="ca045-122">**visLockSelect**</span></span> <br/> |
   

