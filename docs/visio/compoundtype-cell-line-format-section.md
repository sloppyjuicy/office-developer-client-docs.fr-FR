---
title: CompoundType, cellule (Section Line Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3e2a88ad-d92c-4550-8da3-fa7fdd032e73
description: Détermine le type de la ligne d’une forme composé.
ms.openlocfilehash: 663b683030251c8b57324f1d2bdf492463c50eef
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788300"
---
# <a name="compoundtype-cell-line-format-section"></a><span data-ttu-id="17e86-103">CompoundType, cellule (Section Line Format)</span><span class="sxs-lookup"><span data-stu-id="17e86-103">CompoundType Cell (Line Format Section)</span></span>

<span data-ttu-id="17e86-104">Détermine le type de la ligne d’une forme composé.</span><span class="sxs-lookup"><span data-stu-id="17e86-104">Determines the compound type of the line of a shape.</span></span> 
  
|<span data-ttu-id="17e86-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="17e86-105">**Value**</span></span>|<span data-ttu-id="17e86-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="17e86-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="17e86-107">0</span><span class="sxs-lookup"><span data-stu-id="17e86-107">0</span></span>  <br/> |<span data-ttu-id="17e86-108">Simple</span><span class="sxs-lookup"><span data-stu-id="17e86-108">Simple</span></span>  <br/> |
|<span data-ttu-id="17e86-109">1</span><span class="sxs-lookup"><span data-stu-id="17e86-109">1</span></span>  <br/> |<span data-ttu-id="17e86-110">Double</span><span class="sxs-lookup"><span data-stu-id="17e86-110">Double</span></span>  <br/> |
|<span data-ttu-id="17e86-111">2</span><span class="sxs-lookup"><span data-stu-id="17e86-111">2</span></span>  <br/> |<span data-ttu-id="17e86-112">Épais fin</span><span class="sxs-lookup"><span data-stu-id="17e86-112">Thick thin</span></span>  <br/> |
|<span data-ttu-id="17e86-113">3</span><span class="sxs-lookup"><span data-stu-id="17e86-113">3</span></span>  <br/> |<span data-ttu-id="17e86-114">Épais fin</span><span class="sxs-lookup"><span data-stu-id="17e86-114">Thin thick</span></span>  <br/> |
|<span data-ttu-id="17e86-115">4</span><span class="sxs-lookup"><span data-stu-id="17e86-115">4</span></span>  <br/> |<span data-ttu-id="17e86-116">Triple</span><span class="sxs-lookup"><span data-stu-id="17e86-116">Triple</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="17e86-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="17e86-117">Remarks</span></span>

<span data-ttu-id="17e86-118">Pour obtenir une référence à la cellule **CompoundType** par un nom à partir d’une autre formule, par la valeur de l’attribut **N** d’un élément de **cellule** ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="17e86-118">To get a reference to the **CompoundType** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="17e86-119">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="17e86-119">Cell name:</span></span>  <br/> | <span data-ttu-id="17e86-120">CompoundType</span><span class="sxs-lookup"><span data-stu-id="17e86-120">CompoundType</span></span>  <br/> |
   
<span data-ttu-id="17e86-121">Pour obtenir une référence à la cellule **CompoundType** par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="17e86-121">To get a reference to the **CompoundType** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="17e86-122">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="17e86-122">Section index:</span></span>  <br/> |<span data-ttu-id="17e86-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="17e86-123">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="17e86-124">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="17e86-124">Row index:</span></span>  <br/> |<span data-ttu-id="17e86-125">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="17e86-125">**visRowLine**</span></span> <br/> |
| <span data-ttu-id="17e86-126">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="17e86-126">Cell index:</span></span>  <br/> |<span data-ttu-id="17e86-127">**visCompoundType**</span><span class="sxs-lookup"><span data-stu-id="17e86-127">**visCompoundType**</span></span> <br/> |
   

