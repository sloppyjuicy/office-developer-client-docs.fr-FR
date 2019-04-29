---
title: CompoundType Cell (Line Format Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3e2a88ad-d92c-4550-8da3-fa7fdd032e73
description: Détermine le type composé de la ligne d'une forme.
ms.openlocfilehash: 120975e419656234266cb8151b2fa37ef19602e5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407171"
---
# <a name="compoundtype-cell-line-format-section"></a><span data-ttu-id="b1631-103">CompoundType Cell (Line Format Section)</span><span class="sxs-lookup"><span data-stu-id="b1631-103">CompoundType Cell (Line Format Section)</span></span>

<span data-ttu-id="b1631-104">Détermine le type composé de la ligne d'une forme.</span><span class="sxs-lookup"><span data-stu-id="b1631-104">Determines the compound type of the line of a shape.</span></span> 
  
|<span data-ttu-id="b1631-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="b1631-105">**Value**</span></span>|<span data-ttu-id="b1631-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="b1631-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b1631-107">0</span><span class="sxs-lookup"><span data-stu-id="b1631-107">0</span></span>  <br/> |<span data-ttu-id="b1631-108">Simple</span><span class="sxs-lookup"><span data-stu-id="b1631-108">Simple</span></span>  <br/> |
|<span data-ttu-id="b1631-109">0,1</span><span class="sxs-lookup"><span data-stu-id="b1631-109">1</span></span>  <br/> |<span data-ttu-id="b1631-110">Double</span><span class="sxs-lookup"><span data-stu-id="b1631-110">Double</span></span>  <br/> |
|<span data-ttu-id="b1631-111">n°2</span><span class="sxs-lookup"><span data-stu-id="b1631-111">2</span></span>  <br/> |<span data-ttu-id="b1631-112">Épais fin</span><span class="sxs-lookup"><span data-stu-id="b1631-112">Thick thin</span></span>  <br/> |
|<span data-ttu-id="b1631-113">3</span><span class="sxs-lookup"><span data-stu-id="b1631-113">3</span></span>  <br/> |<span data-ttu-id="b1631-114">Fin épais</span><span class="sxs-lookup"><span data-stu-id="b1631-114">Thin thick</span></span>  <br/> |
|<span data-ttu-id="b1631-115">4</span><span class="sxs-lookup"><span data-stu-id="b1631-115">4</span></span>  <br/> |<span data-ttu-id="b1631-116">Triple</span><span class="sxs-lookup"><span data-stu-id="b1631-116">Triple</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b1631-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="b1631-117">Remarks</span></span>

<span data-ttu-id="b1631-118">Pour obtenir une référence à la cellule **CompoundType** par un nom à partir d'une autre formule, par valeur de l'attribut **N** d'un élément de **cellule** ou d'un programme en faisant appel à la propriété **CellsU** , utilisez:</span><span class="sxs-lookup"><span data-stu-id="b1631-118">To get a reference to the **CompoundType** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b1631-119">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="b1631-119">Cell name:</span></span>  <br/> | <span data-ttu-id="b1631-120">CompoundType</span><span class="sxs-lookup"><span data-stu-id="b1631-120">CompoundType</span></span>  <br/> |
   
<span data-ttu-id="b1631-121">Pour obtenir une référence à la cellule **CompoundType** à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants:</span><span class="sxs-lookup"><span data-stu-id="b1631-121">To get a reference to the **CompoundType** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b1631-122">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="b1631-122">Section index:</span></span>  <br/> |<span data-ttu-id="b1631-123">**Définis**</span><span class="sxs-lookup"><span data-stu-id="b1631-123">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="b1631-124">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="b1631-124">Row index:</span></span>  <br/> |<span data-ttu-id="b1631-125">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="b1631-125">**visRowLine**</span></span> <br/> |
| <span data-ttu-id="b1631-126">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="b1631-126">Cell index:</span></span>  <br/> |<span data-ttu-id="b1631-127">**visCompoundType**</span><span class="sxs-lookup"><span data-stu-id="b1631-127">**visCompoundType**</span></span> <br/> |
   

