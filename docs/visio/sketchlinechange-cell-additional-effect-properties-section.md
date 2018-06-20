---
title: SketchLineChange, cellule (Section Propriétés de l’effet supplémentaires)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 39192535-b55b-4c49-b63f-edb542c7a2e5
description: Détermine la quantité de randomisation de ligne de la forme de géométrie de la forme lors de l’utilisation d’un effet esquisse, sous forme de pourcentage de la longueur d’une section. Si la valeur de la cellule SketchLineChange est définie sur 0 %, la géométrie d’une ligne de la forme correspond à la géométrie d’une forme. Si la valeur est 100 %, la géométrie d’une ligne de la forme ne suit pas la géométrie de la forme.
ms.openlocfilehash: 57d2af1a914710d7e5a58686b577014ceb7af424
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789751"
---
# <a name="sketchlinechange-cell-additional-effect-properties-section"></a><span data-ttu-id="290ef-105">SketchLineChange, cellule (Section Propriétés de l’effet supplémentaires)</span><span class="sxs-lookup"><span data-stu-id="290ef-105">SketchLineChange Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="290ef-106">Détermine la quantité de randomisation de ligne de la forme de géométrie de la forme lors de l’utilisation d’un effet esquisse, sous forme de pourcentage de la longueur d’une section.</span><span class="sxs-lookup"><span data-stu-id="290ef-106">Determines the amount of randomization of the shape's line from the shape's geometry when using a sketch effect, as a percentage of the length of a section.</span></span> <span data-ttu-id="290ef-107">Si la valeur de la cellule **SketchLineChange** est définie sur 0 %, la géométrie d’une ligne de la forme correspond à la géométrie d’une forme.</span><span class="sxs-lookup"><span data-stu-id="290ef-107">If the value of the **SketchLineChange** cell is set to 0%, the geometry of the shape's line matches the shape's geometry.</span></span> <span data-ttu-id="290ef-108">Si la valeur est 100 %, la géométrie d’une ligne de la forme ne suit pas la géométrie de la forme.</span><span class="sxs-lookup"><span data-stu-id="290ef-108">If the value is 100%, the geometry of the shape's line does not follow the geometry of the shape.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="290ef-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="290ef-109">Remarks</span></span>

<span data-ttu-id="290ef-110">Pour obtenir les meilleurs résultats, la plage de valeurs de la cellule **SketchLineChange** idéale est comprise entre 15 et 50 %.</span><span class="sxs-lookup"><span data-stu-id="290ef-110">For best results, the ideal range of values for the **SketchLineChange** cell is between 15% and 50%.</span></span> <span data-ttu-id="290ef-111">Une valeur inférieure à 15 % est à peine visible ; une valeur supérieure à 50 % pourrait randomize trop la ligne.</span><span class="sxs-lookup"><span data-stu-id="290ef-111">A value below 15% is barely noticeable; a value greater than 50% could randomize the line too much.</span></span> 
  
<span data-ttu-id="290ef-112">Pour obtenir une référence à la cellule **SketchLineChange** par un nom à partir d’une autre formule, par la valeur de l’attribut **N** d’un élément de **cellule** ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="290ef-112">To get a reference to the **SketchLineChange** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="290ef-113">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="290ef-113">Cell name:</span></span>  <br/> | <span data-ttu-id="290ef-114">SketchLineChange</span><span class="sxs-lookup"><span data-stu-id="290ef-114">SketchLineChange</span></span>  <br/> |
   
<span data-ttu-id="290ef-115">Pour obtenir une référence à la cellule **SketchLineChange** par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="290ef-115">To get a reference to the **SketchLineChange** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="290ef-116">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="290ef-116">Section index:</span></span>  <br/> |<span data-ttu-id="290ef-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="290ef-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="290ef-118">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="290ef-118">Row index:</span></span>  <br/> |<span data-ttu-id="290ef-119">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="290ef-119">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="290ef-120">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="290ef-120">Cell index:</span></span>  <br/> |<span data-ttu-id="290ef-121">**visSketchLineChange**</span><span class="sxs-lookup"><span data-stu-id="290ef-121">**visSketchLineChange**</span></span> <br/> |
   

