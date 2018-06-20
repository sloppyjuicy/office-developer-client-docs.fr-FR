---
title: SketchAmount, cellule (Section Propriétés de l’effet supplémentaires)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7c7353b7-f28e-4004-bf13-6e9714fbed37
description: Détermine le degré de déformation pour un effet esquisse, comme un entier compris entre 0 et 25.
ms.openlocfilehash: d5ae954f2eab48722c48c9bc4b3f640403dbb3ec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789748"
---
# <a name="sketchamount-cell-additional-effect-properties-section"></a><span data-ttu-id="fc802-103">SketchAmount, cellule (Section Propriétés de l’effet supplémentaires)</span><span class="sxs-lookup"><span data-stu-id="fc802-103">SketchAmount Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="fc802-104">Détermine le degré de déformation pour un effet esquisse, comme un entier compris entre 0 et 25.</span><span class="sxs-lookup"><span data-stu-id="fc802-104">Determines the amount of distortion for a sketch effect, as an integer between 0 and 25.</span></span> 
  
|<span data-ttu-id="fc802-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="fc802-105">**Value**</span></span>|<span data-ttu-id="fc802-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="fc802-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fc802-107">0</span><span class="sxs-lookup"><span data-stu-id="fc802-107">0</span></span>  <br/> |<span data-ttu-id="fc802-108">La forme est sans effet esquisse appliqué.</span><span class="sxs-lookup"><span data-stu-id="fc802-108">The shape has no sketch effect applied to it.</span></span>  <br/> |
|<span data-ttu-id="fc802-109">1-25</span><span class="sxs-lookup"><span data-stu-id="fc802-109">1-25</span></span>  <br/> |<span data-ttu-id="fc802-110">La forme a déformation esquisse appliquée, où la valeur 1 est la plupart déformation et 25 le moins.</span><span class="sxs-lookup"><span data-stu-id="fc802-110">The shape has sketch distortion applied to it, where a value of 1 is the most distortion and 25 is the least.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fc802-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="fc802-111">Remarks</span></span>

<span data-ttu-id="fc802-112">Pour obtenir une référence à la cellule **SketchAmount** par un nom à partir d’une autre formule, par la valeur de l’attribut **N** d’un élément de **cellule** ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="fc802-112">To get a reference to the **SketchAmount** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fc802-113">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="fc802-113">Cell name:</span></span>  <br/> | <span data-ttu-id="fc802-114">SketchAmount</span><span class="sxs-lookup"><span data-stu-id="fc802-114">SketchAmount</span></span>  <br/> |
   
<span data-ttu-id="fc802-115">Pour obtenir une référence à la cellule **SketchAmount** par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="fc802-115">To get a reference to the **SketchAmount** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fc802-116">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="fc802-116">Section index:</span></span>  <br/> |<span data-ttu-id="fc802-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="fc802-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="fc802-118">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="fc802-118">Row index:</span></span>  <br/> |<span data-ttu-id="fc802-119">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="fc802-119">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="fc802-120">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="fc802-120">Cell index:</span></span>  <br/> |<span data-ttu-id="fc802-121">**visSketchAmount**</span><span class="sxs-lookup"><span data-stu-id="fc802-121">**visSketchAmount**</span></span> <br/> |
   

