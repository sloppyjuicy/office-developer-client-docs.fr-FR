---
title: LockAspect, cellule (section Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251218
localization_priority: Normal
ms.assetid: e9bfced5-af29-f86c-8604-44ec9a573229
description: Verrouille le rapport hauteur/largeur de la forme afin que cette dernière puisse être dimensionnée uniquement de façon proportionnelle, ce qui signifie qu’il est impossible de modifier une seule cote à la fois.
ms.openlocfilehash: 83ce1aaf555cfaaa0109423e74ae930450b4c1e2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411581"
---
# <a name="lockaspect-cell-protection-section"></a><span data-ttu-id="2e7f5-103">LockAspect, cellule (section Protection)</span><span class="sxs-lookup"><span data-stu-id="2e7f5-103">LockAspect Cell (Protection Section)</span></span>

<span data-ttu-id="2e7f5-104">Verrouille le rapport hauteur/largeur de la forme afin que cette dernière puisse être dimensionnée uniquement de façon proportionnelle, ce qui signifie qu’il est impossible de modifier une seule cote à la fois.</span><span class="sxs-lookup"><span data-stu-id="2e7f5-104">Locks the aspect ratio of the shape so that the shape can only be sized proportionally; it cannot be sized in a single dimension.</span></span>
  
|<span data-ttu-id="2e7f5-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="2e7f5-105">**Value**</span></span>|<span data-ttu-id="2e7f5-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="2e7f5-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="2e7f5-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="2e7f5-107">TRUE</span></span>  <br/> | <span data-ttu-id="2e7f5-108">Le rapport hauteur/largeur est verrouillé.</span><span class="sxs-lookup"><span data-stu-id="2e7f5-108">Aspect ratio is locked.</span></span>  <br/> |
| <span data-ttu-id="2e7f5-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="2e7f5-109">FALSE</span></span>  <br/> | <span data-ttu-id="2e7f5-110">Le rapport hauteur/largeur n'est pas verrouillé.</span><span class="sxs-lookup"><span data-stu-id="2e7f5-110">Aspect ratio is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2e7f5-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="2e7f5-111">Remarks</span></span>

<span data-ttu-id="2e7f5-112">Pour obtenir une référence à la cellule LockAspect par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="2e7f5-112">To get a reference to the LockAspect cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2e7f5-113">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="2e7f5-113">Cell name:</span></span>  <br/> | <span data-ttu-id="2e7f5-114">LockAspect</span><span class="sxs-lookup"><span data-stu-id="2e7f5-114">LockAspect</span></span>  <br/> |
   
<span data-ttu-id="2e7f5-115">Pour obtenir une référence à la cellule LockAspect à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="2e7f5-115">To get a reference to the LockAspect cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2e7f5-116">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="2e7f5-116">Section index:</span></span>  <br/> |<span data-ttu-id="2e7f5-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="2e7f5-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="2e7f5-118">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="2e7f5-118">Row index:</span></span>  <br/> |<span data-ttu-id="2e7f5-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="2e7f5-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="2e7f5-120">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="2e7f5-120">Cell index:</span></span>  <br/> |<span data-ttu-id="2e7f5-121">**visLockAspect**</span><span class="sxs-lookup"><span data-stu-id="2e7f5-121">**visLockAspect**</span></span> <br/> |
   

