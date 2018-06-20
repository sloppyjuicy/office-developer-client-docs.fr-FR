---
title: ThemeIndex, cellule (Section Propriétés de thème)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21002267-1400-4398-b937-f5b289cf0ed2
description: Stocke l’énumération du thème Microsoft Visio intégrée appliquée au document, comme un entier. Lorsque vous choisissez un nouveau thème pour le document, la cellule ThemeIndex pour le document et toutes les pages et les formes qu’il contient est mis à jour avec l’index du thème intégré.
ms.openlocfilehash: 8a9202631bc4d9131d52dea1f852983e1d7528e5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789882"
---
# <a name="themeindex-cell-theme-properties-section"></a><span data-ttu-id="0d13e-104">ThemeIndex, cellule (Section Propriétés de thème)</span><span class="sxs-lookup"><span data-stu-id="0d13e-104">ThemeIndex Cell (Theme Properties Section)</span></span>

<span data-ttu-id="0d13e-105">Stocke l’énumération du thème Microsoft Visio intégrée appliquée au document, comme un entier.</span><span class="sxs-lookup"><span data-stu-id="0d13e-105">Stores the enumeration of the built-in Microsoft Visio theme applied to the document, as an integer.</span></span> <span data-ttu-id="0d13e-106">Lorsque vous choisissez un nouveau thème pour le document, la cellule **ThemeIndex** pour le document et toutes les pages et les formes qu’il contient est mis à jour avec l’index du thème intégré.</span><span class="sxs-lookup"><span data-stu-id="0d13e-106">When a new theme is chosen for the document, the **ThemeIndex** cell for the document and all pages and shapes it contains is updated with the index of the built-in theme.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="0d13e-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="0d13e-107">Remarks</span></span>

<span data-ttu-id="0d13e-108">Pour obtenir une référence à la cellule **ThemeIndex** par un nom à partir d’une autre formule, par la valeur de l’attribut **N** d’un élément de **cellule** ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="0d13e-108">To get a reference to the **ThemeIndex** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0d13e-109">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="0d13e-109">Cell name:</span></span>  <br/> | <span data-ttu-id="0d13e-110">ThemeIndex</span><span class="sxs-lookup"><span data-stu-id="0d13e-110">ThemeIndex</span></span>  <br/> |
   
<span data-ttu-id="0d13e-111">Pour obtenir une référence à la cellule **ThemeIndex** par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="0d13e-111">To get a reference to the **ThemeIndex** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0d13e-112">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="0d13e-112">Section index:</span></span>  <br/> |<span data-ttu-id="0d13e-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="0d13e-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="0d13e-114">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="0d13e-114">Row index:</span></span>  <br/> |<span data-ttu-id="0d13e-115">**visRowThemeProperties**</span><span class="sxs-lookup"><span data-stu-id="0d13e-115">**visRowThemeProperties**</span></span> <br/> |
| <span data-ttu-id="0d13e-116">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="0d13e-116">Cell index:</span></span>  <br/> |<span data-ttu-id="0d13e-117">**visThemeIndex**</span><span class="sxs-lookup"><span data-stu-id="0d13e-117">**visThemeIndex**</span></span> <br/> |
   

