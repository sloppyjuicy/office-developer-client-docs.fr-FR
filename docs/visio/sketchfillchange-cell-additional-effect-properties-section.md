---
title: SketchFillChange, cellule (Section Propriétés de l’effet supplémentaires)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 939f8f90-dee5-4175-b32a-e2964eb40681
description: Détermine la quantité de randomisation de remplissage d’une forme à partir de la géométrie de lors de l’utilisation d’un effet esquisse, sous forme de pourcentage de la longueur d’une section. Si la valeur de la cellule SketchFillChange est définie sur 0 %, la géométrie de délimitation de remplissage d’une forme correspond à la géométrie d’une forme. Si la valeur est 100 %, la géométrie de remplissage de la forme de délimitation ne suit pas la géométrie de la forme.
ms.openlocfilehash: 8dda34e03188909e167a4abda6f62da3d43c4dd7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789756"
---
# <a name="sketchfillchange-cell-additional-effect-properties-section"></a><span data-ttu-id="b1635-105">SketchFillChange, cellule (Section Propriétés de l’effet supplémentaires)</span><span class="sxs-lookup"><span data-stu-id="b1635-105">SketchFillChange Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="b1635-106">Détermine la quantité de randomisation de remplissage d’une forme à partir de la géométrie de lors de l’utilisation d’un effet esquisse, sous forme de pourcentage de la longueur d’une section.</span><span class="sxs-lookup"><span data-stu-id="b1635-106">Determines the amount of randomization of the shape's fill from the shape's geometry when using a sketch effect, as a percentage of the length of a section.</span></span> <span data-ttu-id="b1635-107">Si la valeur de la cellule **SketchFillChange** est définie sur 0 %, la géométrie de délimitation de remplissage d’une forme correspond à la géométrie d’une forme.</span><span class="sxs-lookup"><span data-stu-id="b1635-107">If the value of the **SketchFillChange** cell is set to 0%, the bounding geometry of a shape's fill matches the shape's geometry.</span></span> <span data-ttu-id="b1635-108">Si la valeur est 100 %, la géométrie de remplissage de la forme de délimitation ne suit pas la géométrie de la forme.</span><span class="sxs-lookup"><span data-stu-id="b1635-108">If the value is 100%, the bounding geometry of the shape's fill does not follow the geometry of the shape.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b1635-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="b1635-109">Remarks</span></span>

<span data-ttu-id="b1635-110">Pour obtenir les meilleurs résultats, la plage de valeurs de la cellule **SketchFillChange** idéale est comprise entre 15 et 50 %.</span><span class="sxs-lookup"><span data-stu-id="b1635-110">For best results, the ideal range of values for the **SketchFillChange** cell is between 15% and 50%.</span></span> <span data-ttu-id="b1635-111">Une valeur inférieure à 15 % est à peine visible ; une valeur supérieure à 50 % est plus plus aléatoire.</span><span class="sxs-lookup"><span data-stu-id="b1635-111">A value below 15% is barely noticeable; a value greater than 50% is increasingly more randomized.</span></span> 
  
<span data-ttu-id="b1635-112">Pour obtenir une référence à la cellule **SketchFillChange** par un nom à partir d’une autre formule, par la valeur de l’attribut **N** d’un élément de **cellule** ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="b1635-112">To get a reference to the **SketchFillChange** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b1635-113">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="b1635-113">Cell name:</span></span>  <br/> | <span data-ttu-id="b1635-114">SketchFillChange</span><span class="sxs-lookup"><span data-stu-id="b1635-114">SketchFillChange</span></span>  <br/> |
   
<span data-ttu-id="b1635-115">Pour obtenir une référence à la cellule **SketchFillChange** par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="b1635-115">To get a reference to the **SketchFillChange** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b1635-116">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="b1635-116">Section index:</span></span>  <br/> |<span data-ttu-id="b1635-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b1635-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="b1635-118">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="b1635-118">Row index:</span></span>  <br/> |<span data-ttu-id="b1635-119">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="b1635-119">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="b1635-120">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="b1635-120">Cell index:</span></span>  <br/> |<span data-ttu-id="b1635-121">**visSketchFillChange**</span><span class="sxs-lookup"><span data-stu-id="b1635-121">**visSketchFillChange**</span></span> <br/> |
   

