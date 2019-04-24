---
title: SketchFillChange Cell (Additional Effect Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 939f8f90-dee5-4175-b32a-e2964eb40681
description: Détermine le degré de randomisation du remplissage de la forme à partir de la géométrie de la forme lors de l'utilisation d'un effet d'esquisse, sous la forme d'un pourcentage de la longueur d'une section. Si la valeur de la cellule SketchFillChange est définie sur 0%, la géométrie de délimitation du remplissage d'une forme correspond à la géométrie de la forme. Si la valeur est 100%, la géométrie de délimitation du remplissage de la forme ne suit pas la géométrie de la forme.
ms.openlocfilehash: 8726e9dd6ca6257fb8dbbbef3dce1d4ec344e28b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339810"
---
# <a name="sketchfillchange-cell-additional-effect-properties-section"></a><span data-ttu-id="8ea58-105">SketchFillChange Cell (Additional Effect Properties Section)</span><span class="sxs-lookup"><span data-stu-id="8ea58-105">SketchFillChange Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="8ea58-106">Détermine le degré de randomisation du remplissage de la forme à partir de la géométrie de la forme lors de l'utilisation d'un effet d'esquisse, sous la forme d'un pourcentage de la longueur d'une section.</span><span class="sxs-lookup"><span data-stu-id="8ea58-106">Determines the amount of randomization of the shape's fill from the shape's geometry when using a sketch effect, as a percentage of the length of a section.</span></span> <span data-ttu-id="8ea58-107">Si la valeur de la cellule **SketchFillChange** est définie sur 0%, la géométrie de délimitation du remplissage d'une forme correspond à la géométrie de la forme.</span><span class="sxs-lookup"><span data-stu-id="8ea58-107">If the value of the **SketchFillChange** cell is set to 0%, the bounding geometry of a shape's fill matches the shape's geometry.</span></span> <span data-ttu-id="8ea58-108">Si la valeur est 100%, la géométrie de délimitation du remplissage de la forme ne suit pas la géométrie de la forme.</span><span class="sxs-lookup"><span data-stu-id="8ea58-108">If the value is 100%, the bounding geometry of the shape's fill does not follow the geometry of the shape.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="8ea58-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="8ea58-109">Remarks</span></span>

<span data-ttu-id="8ea58-110">Pour obtenir de meilleurs résultats, la plage de valeurs idéale pour la cellule **SketchFillChange** est comprise entre 15% et 50%.</span><span class="sxs-lookup"><span data-stu-id="8ea58-110">For best results, the ideal range of values for the **SketchFillChange** cell is between 15% and 50%.</span></span> <span data-ttu-id="8ea58-111">Une valeur inférieure à 15% est à peine perceptible; une valeur supérieure à 50% est de plus en plus aléatoire.</span><span class="sxs-lookup"><span data-stu-id="8ea58-111">A value below 15% is barely noticeable; a value greater than 50% is increasingly more randomized.</span></span> 
  
<span data-ttu-id="8ea58-112">Pour obtenir une référence à la cellule **SketchFillChange** par un nom à partir d'une autre formule, par valeur de l'attribut **N** d'un élément de **cellule** ou d'un programme en faisant appel à la propriété **CellsU** , utilisez:</span><span class="sxs-lookup"><span data-stu-id="8ea58-112">To get a reference to the **SketchFillChange** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8ea58-113">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="8ea58-113">Cell name:</span></span>  <br/> | <span data-ttu-id="8ea58-114">SketchFillChange</span><span class="sxs-lookup"><span data-stu-id="8ea58-114">SketchFillChange</span></span>  <br/> |
   
<span data-ttu-id="8ea58-115">Pour obtenir une référence à la cellule **SketchFillChange** à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants:</span><span class="sxs-lookup"><span data-stu-id="8ea58-115">To get a reference to the **SketchFillChange** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8ea58-116">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="8ea58-116">Section index:</span></span>  <br/> |<span data-ttu-id="8ea58-117">**Définis**</span><span class="sxs-lookup"><span data-stu-id="8ea58-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="8ea58-118">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="8ea58-118">Row index:</span></span>  <br/> |<span data-ttu-id="8ea58-119">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="8ea58-119">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="8ea58-120">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="8ea58-120">Cell index:</span></span>  <br/> |<span data-ttu-id="8ea58-121">**visSketchFillChange**</span><span class="sxs-lookup"><span data-stu-id="8ea58-121">**visSketchFillChange**</span></span> <br/> |
   

