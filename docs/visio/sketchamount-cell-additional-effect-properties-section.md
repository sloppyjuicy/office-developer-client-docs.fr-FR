---
title: SketchAmount Cell (Additional Effect Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7c7353b7-f28e-4004-bf13-6e9714fbed37
description: Détermine le degré de déformation pour un effet d'esquisse, sous la forme d'un nombre entier compris entre 0 et 25.
ms.openlocfilehash: fd9ee3390d05f24d81d9c6677160155b0f0f0d35
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404420"
---
# <a name="sketchamount-cell-additional-effect-properties-section"></a><span data-ttu-id="c7006-103">SketchAmount Cell (Additional Effect Properties Section)</span><span class="sxs-lookup"><span data-stu-id="c7006-103">SketchAmount Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="c7006-104">Détermine le degré de déformation pour un effet d'esquisse, sous la forme d'un nombre entier compris entre 0 et 25.</span><span class="sxs-lookup"><span data-stu-id="c7006-104">Determines the amount of distortion for a sketch effect, as an integer between 0 and 25.</span></span> 
  
|<span data-ttu-id="c7006-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="c7006-105">**Value**</span></span>|<span data-ttu-id="c7006-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="c7006-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c7006-107">0</span><span class="sxs-lookup"><span data-stu-id="c7006-107">0</span></span>  <br/> |<span data-ttu-id="c7006-108">Aucun effet de croquis n'est appliqué à la forme.</span><span class="sxs-lookup"><span data-stu-id="c7006-108">The shape has no sketch effect applied to it.</span></span>  <br/> |
|<span data-ttu-id="c7006-109">1-25</span><span class="sxs-lookup"><span data-stu-id="c7006-109">1-25</span></span>  <br/> |<span data-ttu-id="c7006-110">La forme est dotée d'une distorsion d'esquisse, où la valeur 1 est la plus grande distorsion et 25 le moins.</span><span class="sxs-lookup"><span data-stu-id="c7006-110">The shape has sketch distortion applied to it, where a value of 1 is the most distortion and 25 is the least.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c7006-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="c7006-111">Remarks</span></span>

<span data-ttu-id="c7006-112">Pour obtenir une référence à la cellule **SketchAmount** par un nom à partir d'une autre formule, par valeur de l'attribut **N** d'un élément de **cellule** ou d'un programme en faisant appel à la propriété **CellsU** , utilisez:</span><span class="sxs-lookup"><span data-stu-id="c7006-112">To get a reference to the **SketchAmount** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c7006-113">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="c7006-113">Cell name:</span></span>  <br/> | <span data-ttu-id="c7006-114">SketchAmount</span><span class="sxs-lookup"><span data-stu-id="c7006-114">SketchAmount</span></span>  <br/> |
   
<span data-ttu-id="c7006-115">Pour obtenir une référence à la cellule **SketchAmount** à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants:</span><span class="sxs-lookup"><span data-stu-id="c7006-115">To get a reference to the **SketchAmount** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c7006-116">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="c7006-116">Section index:</span></span>  <br/> |<span data-ttu-id="c7006-117">**Définis**</span><span class="sxs-lookup"><span data-stu-id="c7006-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c7006-118">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="c7006-118">Row index:</span></span>  <br/> |<span data-ttu-id="c7006-119">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="c7006-119">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="c7006-120">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="c7006-120">Cell index:</span></span>  <br/> |<span data-ttu-id="c7006-121">**visSketchAmount**</span><span class="sxs-lookup"><span data-stu-id="c7006-121">**visSketchAmount**</span></span> <br/> |
   

