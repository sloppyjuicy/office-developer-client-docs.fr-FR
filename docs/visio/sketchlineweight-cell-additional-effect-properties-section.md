---
title: SketchLineWeight Cell (Additional Effect Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6cb838be-1d6d-48e1-8e9e-bd126f0c2385
description: Détermine l'épaisseur supplémentaire ajoutée à l'épaisseur de trait comme résultat d'un effet d'esquisse, en points de 0 à 50. L'épaisseur de trait d'une forme augmente au fur et à mesure que la valeur de la cellule SketchLineWeight augmente.
ms.openlocfilehash: 0ee71bbaec59f5c79b72314b08478f8028b4e0ba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404511"
---
# <a name="sketchlineweight-cell-additional-effect-properties-section"></a><span data-ttu-id="d49fb-104">SketchLineWeight Cell (Additional Effect Properties Section)</span><span class="sxs-lookup"><span data-stu-id="d49fb-104">SketchLineWeight Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="d49fb-105">Détermine l'épaisseur supplémentaire ajoutée à l'épaisseur de trait comme résultat d'un effet d'esquisse, en points de 0 à 50.</span><span class="sxs-lookup"><span data-stu-id="d49fb-105">Determines the additional thickness added to line weight as the result of a sketch effect, in points from 0 to 50.</span></span> <span data-ttu-id="d49fb-106">L'épaisseur de trait d'une forme augmente au fur et à mesure que la valeur de la cellule **SketchLineWeight** augmente.</span><span class="sxs-lookup"><span data-stu-id="d49fb-106">The thickness of a shape's line increases as the value of the **SketchLineWeight** cell increases.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d49fb-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="d49fb-107">Remarks</span></span>

<span data-ttu-id="d49fb-108">Pour obtenir une référence à la cellule **SketchLineWeight** par un nom à partir d'une autre formule, par valeur de l'attribut **N** d'un élément de **cellule** ou d'un programme en faisant appel à la propriété **CellsU** , utilisez:</span><span class="sxs-lookup"><span data-stu-id="d49fb-108">To get a reference to the **SketchLineWeight** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d49fb-109">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="d49fb-109">Cell name:</span></span>  <br/> | <span data-ttu-id="d49fb-110">SketchLineWeight</span><span class="sxs-lookup"><span data-stu-id="d49fb-110">SketchLineWeight</span></span>  <br/> |
   
<span data-ttu-id="d49fb-111">Pour obtenir une référence à la cellule **SketchLineWeight** à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants:</span><span class="sxs-lookup"><span data-stu-id="d49fb-111">To get a reference to the **SketchLineWeight** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d49fb-112">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="d49fb-112">Section index:</span></span>  <br/> |<span data-ttu-id="d49fb-113">**Définis**</span><span class="sxs-lookup"><span data-stu-id="d49fb-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="d49fb-114">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="d49fb-114">Row index:</span></span>  <br/> |<span data-ttu-id="d49fb-115">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="d49fb-115">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="d49fb-116">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="d49fb-116">Cell index:</span></span>  <br/> |<span data-ttu-id="d49fb-117">**visSketchLineWeight**</span><span class="sxs-lookup"><span data-stu-id="d49fb-117">**visSketchLineWeight**</span></span> <br/> |
   

