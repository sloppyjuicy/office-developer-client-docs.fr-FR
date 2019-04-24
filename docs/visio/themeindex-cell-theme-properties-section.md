---
title: ThemeIndex Cell (Theme Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21002267-1400-4398-b937-f5b289cf0ed2
description: Stocke l'énumération du thème Microsoft Visio intégré appliqué au document, sous la forme d'un nombre entier. Lorsqu'un nouveau thème est choisi pour le document, la cellule ThemeIndex du document et toutes les pages et formes qu'il contient sont mises à jour avec l'index du thème intégré.
ms.openlocfilehash: 6ddede864a54fbd7127552499d3ee1ae3d36efc1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360528"
---
# <a name="themeindex-cell-theme-properties-section"></a><span data-ttu-id="222e3-104">ThemeIndex Cell (Theme Properties Section)</span><span class="sxs-lookup"><span data-stu-id="222e3-104">ThemeIndex Cell (Theme Properties Section)</span></span>

<span data-ttu-id="222e3-105">Stocke l'énumération du thème Microsoft Visio intégré appliqué au document, sous la forme d'un nombre entier.</span><span class="sxs-lookup"><span data-stu-id="222e3-105">Stores the enumeration of the built-in Microsoft Visio theme applied to the document, as an integer.</span></span> <span data-ttu-id="222e3-106">Lorsqu'un nouveau thème est choisi pour le document, la cellule **ThemeIndex** du document et toutes les pages et formes qu'il contient sont mises à jour avec l'index du thème intégré.</span><span class="sxs-lookup"><span data-stu-id="222e3-106">When a new theme is chosen for the document, the **ThemeIndex** cell for the document and all pages and shapes it contains is updated with the index of the built-in theme.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="222e3-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="222e3-107">Remarks</span></span>

<span data-ttu-id="222e3-108">Pour obtenir une référence à la cellule **ThemeIndex** par un nom à partir d'une autre formule, par valeur de l'attribut **N** d'un élément de **cellule** ou d'un programme en faisant appel à la propriété **CellsU** , utilisez:</span><span class="sxs-lookup"><span data-stu-id="222e3-108">To get a reference to the **ThemeIndex** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="222e3-109">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="222e3-109">Cell name:</span></span>  <br/> | <span data-ttu-id="222e3-110">ThemeIndex</span><span class="sxs-lookup"><span data-stu-id="222e3-110">ThemeIndex</span></span>  <br/> |
   
<span data-ttu-id="222e3-111">Pour obtenir une référence à la cellule **ThemeIndex** à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants:</span><span class="sxs-lookup"><span data-stu-id="222e3-111">To get a reference to the **ThemeIndex** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="222e3-112">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="222e3-112">Section index:</span></span>  <br/> |<span data-ttu-id="222e3-113">**Définis**</span><span class="sxs-lookup"><span data-stu-id="222e3-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="222e3-114">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="222e3-114">Row index:</span></span>  <br/> |<span data-ttu-id="222e3-115">**visRowThemeProperties**</span><span class="sxs-lookup"><span data-stu-id="222e3-115">**visRowThemeProperties**</span></span> <br/> |
| <span data-ttu-id="222e3-116">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="222e3-116">Cell index:</span></span>  <br/> |<span data-ttu-id="222e3-117">**visThemeIndex**</span><span class="sxs-lookup"><span data-stu-id="222e3-117">**visThemeIndex**</span></span> <br/> |
   

