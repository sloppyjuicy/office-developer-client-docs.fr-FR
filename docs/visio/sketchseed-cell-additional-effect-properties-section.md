---
title: SketchSeed Cell (Additional Effect Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f62650d-36f8-4c6e-b79f-c9c397a5954d
description: Représente une valeur de randomisation utilisée pour déterminer la géométrie d’un effet de croquis, sous la forme d’un nombre d’caractères positif. La valeur de la cellule SketchSeed est créée de manière aléatoire lorsqu’un effet de croquis est appliqué à la forme.
ms.openlocfilehash: 3ec58fbfa183d1a6d7bb6960672658f9a6cca073
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434395"
---
# <a name="sketchseed-cell-additional-effect-properties-section"></a><span data-ttu-id="b3659-104">SketchSeed Cell (Additional Effect Properties Section)</span><span class="sxs-lookup"><span data-stu-id="b3659-104">SketchSeed Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="b3659-105">Représente une valeur de randomisation utilisée pour déterminer la géométrie d’un effet de croquis, sous la forme d’un nombre d’caractères positif.</span><span class="sxs-lookup"><span data-stu-id="b3659-105">Represents a randomization value used to determine the geometry of a sketch effect, as a positive integer.</span></span> <span data-ttu-id="b3659-106">La valeur de la **cellule SketchSeed** est créée de manière aléatoire lorsqu’un effet de croquis est appliqué à la forme.</span><span class="sxs-lookup"><span data-stu-id="b3659-106">The value of the **SketchSeed** cell is randomly created when a sketch effect is applied to the shape.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b3659-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="b3659-107">Remarks</span></span>

<span data-ttu-id="b3659-108">Pour obtenir une référence à la cellule **SketchSeed** par un nom à partir d’une autre formule, de l’attribut **N** d’un élément **Cell** ou d’un programme en faisant appel à la propriété **CellsU,** utilisez :</span><span class="sxs-lookup"><span data-stu-id="b3659-108">To get a reference to the **SketchSeed** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b3659-109">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="b3659-109">Cell name:</span></span>  <br/> | <span data-ttu-id="b3659-110">SketchSeed</span><span class="sxs-lookup"><span data-stu-id="b3659-110">SketchSeed</span></span>  <br/> |
   
<span data-ttu-id="b3659-111">Pour obtenir une référence à la cellule **SketchSeed** à l’aide d’un index à partir d’un programme, utilisez la **propriété CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="b3659-111">To get a reference to the **SketchSeed** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b3659-112">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="b3659-112">Section index:</span></span>  <br/> |<span data-ttu-id="b3659-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b3659-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="b3659-114">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="b3659-114">Row index:</span></span>  <br/> |<span data-ttu-id="b3659-115">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="b3659-115">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="b3659-116">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="b3659-116">Cell index:</span></span>  <br/> |<span data-ttu-id="b3659-117">**visSketchSeed**</span><span class="sxs-lookup"><span data-stu-id="b3659-117">**visSketchSeed**</span></span> <br/> |
   

