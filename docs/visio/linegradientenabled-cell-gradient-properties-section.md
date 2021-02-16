---
title: LineGradientEnabled Cell (Gradient Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 276a661f-d14e-404a-a494-ae36601a8ce3
description: Détermine si un dégradé de trait est activé pour un trait ou la bordure d’une forme.
ms.openlocfilehash: 1d2b33275d26bb0c8e5550bcb7cf282c64d34544
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416376"
---
# <a name="linegradientenabled-cell-gradient-properties-section"></a><span data-ttu-id="33e5c-103">LineGradientEnabled Cell (Gradient Properties Section)</span><span class="sxs-lookup"><span data-stu-id="33e5c-103">LineGradientEnabled Cell (Gradient Properties Section)</span></span>

<span data-ttu-id="33e5c-104">Détermine si un dégradé de trait est activé pour un trait ou la bordure d’une forme.</span><span class="sxs-lookup"><span data-stu-id="33e5c-104">Determines whether a line gradient is enabled for a line or border of a shape.</span></span> 
  
|<span data-ttu-id="33e5c-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="33e5c-105">**Value**</span></span>|<span data-ttu-id="33e5c-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="33e5c-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="33e5c-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="33e5c-107">TRUE</span></span>  <br/> |<span data-ttu-id="33e5c-108">Le dégradé est affiché sur le trait ou la bordure d’une forme.</span><span class="sxs-lookup"><span data-stu-id="33e5c-108">Gradient is displayed on the line or border of a shape.</span></span>  <br/> |
|<span data-ttu-id="33e5c-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="33e5c-109">FALSE</span></span>  <br/> |<span data-ttu-id="33e5c-110">Les dégradés ne sont pas affichés sur le trait ou la bordure d’une forme.</span><span class="sxs-lookup"><span data-stu-id="33e5c-110">Gradients are not displayed on the line or border of a shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="33e5c-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="33e5c-111">Remarks</span></span>

<span data-ttu-id="33e5c-112">Pour obtenir une référence à la cellule **LineGradientEnabled** par un nom à partir d’une autre formule, de l’attribut **N** d’un élément **Cell** ou d’un programme en faisant appel à la propriété **CellsU,** utilisez :</span><span class="sxs-lookup"><span data-stu-id="33e5c-112">To get a reference to the **LineGradientEnabled** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="33e5c-113">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="33e5c-113">Cell name:</span></span>  <br/> | <span data-ttu-id="33e5c-114">LineGradientEnabled</span><span class="sxs-lookup"><span data-stu-id="33e5c-114">LineGradientEnabled</span></span>  <br/> |
   
<span data-ttu-id="33e5c-115">Pour obtenir une référence à la cellule **LineGradientEnabled** à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="33e5c-115">To get a reference to the **LineGradientEnabled** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="33e5c-116">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="33e5c-116">Section index:</span></span>  <br/> |<span data-ttu-id="33e5c-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="33e5c-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="33e5c-118">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="33e5c-118">Row index:</span></span>  <br/> |<span data-ttu-id="33e5c-119">**visRowGradientProperties**</span><span class="sxs-lookup"><span data-stu-id="33e5c-119">**visRowGradientProperties**</span></span> <br/> |
| <span data-ttu-id="33e5c-120">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="33e5c-120">Cell index:</span></span>  <br/> |<span data-ttu-id="33e5c-121">**visLineGradientEnabled**</span><span class="sxs-lookup"><span data-stu-id="33e5c-121">**visLineGradientEnabled**</span></span> <br/> |
   

