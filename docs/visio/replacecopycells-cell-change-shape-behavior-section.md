---
title: ReplaceCopyCells Cell (Change Shape Behavior Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2f36aefd-da49-47ea-9b90-2fa1a2298849
description: Indique la liste des cellules de la feuille ShapeSheet qui sont copiées d’une ancienne forme vers la forme de remplacement lors d’une opération de remplacement de forme.
ms.openlocfilehash: f2a7908a623c861d0284821b2d8ae5fc71690685
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409341"
---
# <a name="replacecopycells-cell-change-shape-behavior-section"></a><span data-ttu-id="cbfa2-103">ReplaceCopyCells Cell (Change Shape Behavior Section)</span><span class="sxs-lookup"><span data-stu-id="cbfa2-103">ReplaceCopyCells Cell (Change Shape Behavior Section)</span></span>

<span data-ttu-id="cbfa2-104">Indique la liste des cellules de la feuille ShapeSheet qui sont copiées d’une ancienne forme vers la forme de remplacement lors d’une opération de remplacement de forme.</span><span class="sxs-lookup"><span data-stu-id="cbfa2-104">Indicates a list of cells in the ShapeSheet that are copied from an old shape to the replacement shape during a shape replacement operation.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="cbfa2-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="cbfa2-105">Remarks</span></span>

<span data-ttu-id="cbfa2-106">La forme de base du remplacement doit contenir un appel de fonction **DEPENDSON** dans la cellule **ReplaceCopyCells,** où chaque argument de la fonction est une référence à une cellule.</span><span class="sxs-lookup"><span data-stu-id="cbfa2-106">The master shape of the replacement must contain a **DEPENDSON** function call in the **ReplaceCopyCells** cell, where each argument in the function is a reference to a cell.</span></span> <span data-ttu-id="cbfa2-107">Ces cellules sont copiées de l’ancienne forme vers la forme qui résulte d’une opération de remplacement de forme, quel que soit l’endroit où elles se trouve dans la feuille ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="cbfa2-107">Those cells are copied from the old shape to the shape that results from a shape replacement operation, regardless of where they are in the ShapeSheet.</span></span> 
  
<span data-ttu-id="cbfa2-108">Les valeurs et/ou formules qui font référence à d’autres cellules sont copiées dans la forme résultante.</span><span class="sxs-lookup"><span data-stu-id="cbfa2-108">Values and/or formulas that reference other cells are copied to the resulting shape.</span></span> <span data-ttu-id="cbfa2-109">Si la forme résultante ne possède pas la cellule référencé, la cellule copiée contient uniquement la valeur.</span><span class="sxs-lookup"><span data-stu-id="cbfa2-109">If the resulting shape does not have the referenced cell, the copied cell contains the value only.</span></span> 
  
<span data-ttu-id="cbfa2-110">Les références de la cellule **ReplaceCopyCells** remplacent la protection définie sur les cellules telles que définies dans la section **Protection** et les cellules **ReplaceLockFormat,** **ReplaceLockShapeData** et **ReplaceLockText.**</span><span class="sxs-lookup"><span data-stu-id="cbfa2-110">References in the **ReplaceCopyCells** cell override protection set on cells as defined in the **Protection** section and the **ReplaceLockFormat**, **ReplaceLockShapeData**, and **ReplaceLockText** cells.</span></span> 
  
<span data-ttu-id="cbfa2-111">Pour obtenir une référence à la cellule **ReplaceCopyCells** par un nom à partir d’une autre formule, de l’attribut **N** d’un élément **Cell** ou d’un programme en faisant appel à la propriété **CellsU,** utilisez :</span><span class="sxs-lookup"><span data-stu-id="cbfa2-111">To get a reference to the **ReplaceCopyCells** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cbfa2-112">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="cbfa2-112">Cell name:</span></span>  <br/> | <span data-ttu-id="cbfa2-113">ReplaceCopyCells</span><span class="sxs-lookup"><span data-stu-id="cbfa2-113">ReplaceCopyCells</span></span>  <br/> |
   
<span data-ttu-id="cbfa2-114">Pour obtenir une référence à la **cellule ReplaceCopyCells** à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="cbfa2-114">To get a reference to the **ReplaceCopyCells** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cbfa2-115">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="cbfa2-115">Section index:</span></span>  <br/> |<span data-ttu-id="cbfa2-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="cbfa2-116">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="cbfa2-117">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="cbfa2-117">Row index:</span></span>  <br/> |<span data-ttu-id="cbfa2-118">**visRowReplaceBehaviors**</span><span class="sxs-lookup"><span data-stu-id="cbfa2-118">**visRowReplaceBehaviors**</span></span> <br/> |
| <span data-ttu-id="cbfa2-119">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="cbfa2-119">Cell index:</span></span>  <br/> |<span data-ttu-id="cbfa2-120">**visReplaceCopyCells**</span><span class="sxs-lookup"><span data-stu-id="cbfa2-120">**visReplaceCopyCells**</span></span> <br/> |
   

