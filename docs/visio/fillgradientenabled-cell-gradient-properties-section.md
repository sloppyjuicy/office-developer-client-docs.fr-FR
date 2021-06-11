---
title: FillGradientEnabled Cell (Gradient Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 80db9c0c-13c6-47de-967f-ade6e5899f14
description: Détermine si un dégradé de remplissage est activé pour cette forme.
ms.openlocfilehash: 17f617c13b632318be22b86a3354a194f0f835f5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431210"
---
# <a name="fillgradientenabled-cell-gradient-properties-section"></a><span data-ttu-id="b66d0-103">FillGradientEnabled Cell (Gradient Properties Section)</span><span class="sxs-lookup"><span data-stu-id="b66d0-103">FillGradientEnabled Cell (Gradient Properties Section)</span></span>

<span data-ttu-id="b66d0-104">Détermine si un dégradé de remplissage est activé pour cette forme.</span><span class="sxs-lookup"><span data-stu-id="b66d0-104">Determines whether a fill gradient is enabled for this shape.</span></span> 
  
|<span data-ttu-id="b66d0-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="b66d0-105">**Value**</span></span>|<span data-ttu-id="b66d0-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="b66d0-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b66d0-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="b66d0-107">TRUE</span></span>  <br/> |<span data-ttu-id="b66d0-108">Le remplissage dégradé est affiché sur la forme.</span><span class="sxs-lookup"><span data-stu-id="b66d0-108">Gradient fill is displayed on the shape.</span></span>  <br/> |
|<span data-ttu-id="b66d0-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="b66d0-109">FALSE</span></span>  <br/> |<span data-ttu-id="b66d0-110">Les remplissages dégradés ne sont pas affichés sur la forme.</span><span class="sxs-lookup"><span data-stu-id="b66d0-110">Gradient fills are not displayed on the shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b66d0-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="b66d0-111">Remarks</span></span>

<span data-ttu-id="b66d0-112">Pour obtenir une référence à la cellule **FillGradientEnabled** par un nom à partir d’une autre formule, de l’attribut **N** d’un élément **Cell** ou d’un programme en faisant appel à la propriété **CellsU,** utilisez :</span><span class="sxs-lookup"><span data-stu-id="b66d0-112">To get a reference to the **FillGradientEnabled** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b66d0-113">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="b66d0-113">Cell name:</span></span>  <br/> | <span data-ttu-id="b66d0-114">FillGradientEnabled</span><span class="sxs-lookup"><span data-stu-id="b66d0-114">FillGradientEnabled</span></span>  <br/> |
   
<span data-ttu-id="b66d0-115">Pour obtenir une référence à la **cellule FillGradientEnabled** à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="b66d0-115">To get a reference to the **FillGradientEnabled** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b66d0-116">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="b66d0-116">Section index:</span></span>  <br/> |<span data-ttu-id="b66d0-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b66d0-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="b66d0-118">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="b66d0-118">Row index:</span></span>  <br/> |<span data-ttu-id="b66d0-119">**visRowGradientProperties**</span><span class="sxs-lookup"><span data-stu-id="b66d0-119">**visRowGradientProperties**</span></span> <br/> |
| <span data-ttu-id="b66d0-120">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="b66d0-120">Cell index:</span></span>  <br/> |<span data-ttu-id="b66d0-121">\*\*visFillGradientEnabled \*\*</span><span class="sxs-lookup"><span data-stu-id="b66d0-121">\*\*visFillGradientEnabled \*\*</span></span> <br/> |
   

