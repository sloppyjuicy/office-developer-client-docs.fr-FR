---
title: ReplaceCopyCells, cellule (Section de comportement de forme modification)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2f36aefd-da49-47ea-9b90-2fa1a2298849
description: Indique une liste des cellules dans la feuille ShapeSheet qui sont copiés à partir d’une ancienne forme à la forme de remplacement lors d’une opération de remplacement de forme.
ms.openlocfilehash: 1e3b5e4dbc29372f75b7a7ed8013a7dd82d94e1d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789435"
---
# <a name="replacecopycells-cell-change-shape-behavior-section"></a><span data-ttu-id="fa761-103">ReplaceCopyCells, cellule (Section de comportement de forme modification)</span><span class="sxs-lookup"><span data-stu-id="fa761-103">ReplaceCopyCells Cell (Change Shape Behavior Section)</span></span>

<span data-ttu-id="fa761-104">Indique une liste des cellules dans la feuille ShapeSheet qui sont copiés à partir d’une ancienne forme à la forme de remplacement lors d’une opération de remplacement de forme.</span><span class="sxs-lookup"><span data-stu-id="fa761-104">Indicates a list of cells in the ShapeSheet that are copied from an old shape to the replacement shape during a shape replacement operation.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="fa761-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="fa761-105">Remarks</span></span>

<span data-ttu-id="fa761-106">La forme de base du remplacement doit contenir un appel de fonction **DEPENDSON** dans la cellule **ReplaceCopyCells** , où chaque argument de la fonction est une référence à une cellule.</span><span class="sxs-lookup"><span data-stu-id="fa761-106">The master shape of the replacement must contain a **DEPENDSON** function call in the **ReplaceCopyCells** cell, where each argument in the function is a reference to a cell.</span></span> <span data-ttu-id="fa761-107">Ces cellules sont copiés à la forme qui résulte d’une opération de remplacement de forme, où qu’ils soient dans la feuille ShapeSheet de la forme ancienne.</span><span class="sxs-lookup"><span data-stu-id="fa761-107">Those cells are copied from the old shape to the shape that results from a shape replacement operation, regardless of where they are in the ShapeSheet.</span></span> 
  
<span data-ttu-id="fa761-108">Les valeurs et les formules qui référencent d’autres cellules sont copiés à la forme obtenue.</span><span class="sxs-lookup"><span data-stu-id="fa761-108">Values and/or formulas that reference other cells are copied to the resulting shape.</span></span> <span data-ttu-id="fa761-109">Si la forme obtenue ne dispose pas de la cellule référencée, la cellule contient la valeur uniquement.</span><span class="sxs-lookup"><span data-stu-id="fa761-109">If the resulting shape does not have the referenced cell, the copied cell contains the value only.</span></span> 
  
<span data-ttu-id="fa761-110">Références de la cellule **ReplaceCopyCells** remplacent défini de protection sur cellules telle que définie dans la section **Protection** et les cellules **ReplaceLockText** , **ReplaceLockFormat**et **ReplaceLockShapeData**.</span><span class="sxs-lookup"><span data-stu-id="fa761-110">References in the **ReplaceCopyCells** cell override protection set on cells as defined in the **Protection** section and the **ReplaceLockFormat**, **ReplaceLockShapeData**, and **ReplaceLockText** cells.</span></span> 
  
<span data-ttu-id="fa761-111">Pour obtenir une référence à la cellule **ReplaceCopyCells** par un nom à partir d’une autre formule, par la valeur de l’attribut **N** d’un élément de **cellule** ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="fa761-111">To get a reference to the **ReplaceCopyCells** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fa761-112">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="fa761-112">Cell name:</span></span>  <br/> | <span data-ttu-id="fa761-113">ReplaceCopyCells</span><span class="sxs-lookup"><span data-stu-id="fa761-113">ReplaceCopyCells</span></span>  <br/> |
   
<span data-ttu-id="fa761-114">Pour obtenir une référence à la cellule **ReplaceCopyCells** par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="fa761-114">To get a reference to the **ReplaceCopyCells** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fa761-115">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="fa761-115">Section index:</span></span>  <br/> |<span data-ttu-id="fa761-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="fa761-116">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="fa761-117">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="fa761-117">Row index:</span></span>  <br/> |<span data-ttu-id="fa761-118">**visRowReplaceBehaviors**</span><span class="sxs-lookup"><span data-stu-id="fa761-118">**visRowReplaceBehaviors**</span></span> <br/> |
| <span data-ttu-id="fa761-119">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="fa761-119">Cell index:</span></span>  <br/> |<span data-ttu-id="fa761-120">**visReplaceCopyCells**</span><span class="sxs-lookup"><span data-stu-id="fa761-120">**visReplaceCopyCells**</span></span> <br/> |
   

