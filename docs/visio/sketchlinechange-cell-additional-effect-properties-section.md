---
title: SketchLineChange Cell (Additional Effect Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 39192535-b55b-4c49-b63f-edb542c7a2e5
description: Détermine le degré de randomisation de la ligne de la forme par rapport à la géométrie de la forme lors de l'utilisation d'un effet d'esquisse, sous la forme d'un pourcentage de la longueur d'une section. Si la valeur de la cellule SketchLineChange est définie sur 0%, la géométrie de la ligne de la forme correspond à la géométrie de la forme. Si la valeur est 100%, la géométrie de la ligne de la forme ne suit pas la géométrie de la forme.
ms.openlocfilehash: ba57a4d2e43a91475f4c3ab4862f723eb2653a89
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315126"
---
# <a name="sketchlinechange-cell-additional-effect-properties-section"></a><span data-ttu-id="c5c92-105">SketchLineChange Cell (Additional Effect Properties Section)</span><span class="sxs-lookup"><span data-stu-id="c5c92-105">SketchLineChange Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="c5c92-106">Détermine le degré de randomisation de la ligne de la forme par rapport à la géométrie de la forme lors de l'utilisation d'un effet d'esquisse, sous la forme d'un pourcentage de la longueur d'une section.</span><span class="sxs-lookup"><span data-stu-id="c5c92-106">Determines the amount of randomization of the shape's line from the shape's geometry when using a sketch effect, as a percentage of the length of a section.</span></span> <span data-ttu-id="c5c92-107">Si la valeur de la cellule **SketchLineChange** est définie sur 0%, la géométrie de la ligne de la forme correspond à la géométrie de la forme.</span><span class="sxs-lookup"><span data-stu-id="c5c92-107">If the value of the **SketchLineChange** cell is set to 0%, the geometry of the shape's line matches the shape's geometry.</span></span> <span data-ttu-id="c5c92-108">Si la valeur est 100%, la géométrie de la ligne de la forme ne suit pas la géométrie de la forme.</span><span class="sxs-lookup"><span data-stu-id="c5c92-108">If the value is 100%, the geometry of the shape's line does not follow the geometry of the shape.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c5c92-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="c5c92-109">Remarks</span></span>

<span data-ttu-id="c5c92-110">Pour obtenir de meilleurs résultats, la plage de valeurs idéale pour la cellule **SketchLineChange** est comprise entre 15% et 50%.</span><span class="sxs-lookup"><span data-stu-id="c5c92-110">For best results, the ideal range of values for the **SketchLineChange** cell is between 15% and 50%.</span></span> <span data-ttu-id="c5c92-111">Une valeur inférieure à 15% est à peine perceptible; une valeur supérieure à 50% peut randomiser la ligne trop.</span><span class="sxs-lookup"><span data-stu-id="c5c92-111">A value below 15% is barely noticeable; a value greater than 50% could randomize the line too much.</span></span> 
  
<span data-ttu-id="c5c92-112">Pour obtenir une référence à la cellule **SketchLineChange** par un nom à partir d'une autre formule, par valeur de l'attribut **N** d'un élément de **cellule** ou d'un programme en faisant appel à la propriété **CellsU** , utilisez:</span><span class="sxs-lookup"><span data-stu-id="c5c92-112">To get a reference to the **SketchLineChange** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c5c92-113">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="c5c92-113">Cell name:</span></span>  <br/> | <span data-ttu-id="c5c92-114">SketchLineChange</span><span class="sxs-lookup"><span data-stu-id="c5c92-114">SketchLineChange</span></span>  <br/> |
   
<span data-ttu-id="c5c92-115">Pour obtenir une référence à la cellule **SketchLineChange** à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants:</span><span class="sxs-lookup"><span data-stu-id="c5c92-115">To get a reference to the **SketchLineChange** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c5c92-116">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="c5c92-116">Section index:</span></span>  <br/> |<span data-ttu-id="c5c92-117">**Définis**</span><span class="sxs-lookup"><span data-stu-id="c5c92-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c5c92-118">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="c5c92-118">Row index:</span></span>  <br/> |<span data-ttu-id="c5c92-119">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="c5c92-119">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="c5c92-120">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="c5c92-120">Cell index:</span></span>  <br/> |<span data-ttu-id="c5c92-121">**visSketchLineChange**</span><span class="sxs-lookup"><span data-stu-id="c5c92-121">**visSketchLineChange**</span></span> <br/> |
   

