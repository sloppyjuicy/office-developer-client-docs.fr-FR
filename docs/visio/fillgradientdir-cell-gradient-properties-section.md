---
title: FillGradientDir Cell (Gradient Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e8156ff1-c540-44b8-8b69-ba4d54883260
description: Détermine la direction du dégradé de remplissage. Un dégradé peut être linéaire, radial, rectangulaire ou suivre un chemin d’accès.
ms.openlocfilehash: 53aad056c7fc1674e00e142fd72a10134103b390
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406716"
---
# <a name="fillgradientdir-cell-gradient-properties-section"></a><span data-ttu-id="4731a-104">FillGradientDir Cell (Gradient Properties Section)</span><span class="sxs-lookup"><span data-stu-id="4731a-104">FillGradientDir Cell (Gradient Properties Section)</span></span>

<span data-ttu-id="4731a-105">Détermine la direction du dégradé de remplissage.</span><span class="sxs-lookup"><span data-stu-id="4731a-105">Determines the direction of the fill gradient.</span></span> <span data-ttu-id="4731a-106">Un dégradé peut être linéaire, radial, rectangulaire ou suivre un chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="4731a-106">A gradient can be linear, radial, rectangular, or follow a path.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="4731a-107">Un dégradé linéaire est le seul dégradé qui prend une valeur d’angle supplémentaire (comme déterminé par la **cellule FillGradientDir).**</span><span class="sxs-lookup"><span data-stu-id="4731a-107">A linear gradient is the only gradient that takes an additional angle value (as determined by **FillGradientDir** cell).</span></span> <span data-ttu-id="4731a-108">Toutes les autres directions de dégradé ont des éumérations prédéfinie.</span><span class="sxs-lookup"><span data-stu-id="4731a-108">All other gradient directions have preset enumerations.</span></span> 
  
****

|<span data-ttu-id="4731a-109">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="4731a-109">**Value**</span></span>|<span data-ttu-id="4731a-110">**Description**</span><span class="sxs-lookup"><span data-stu-id="4731a-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4731a-111">0</span><span class="sxs-lookup"><span data-stu-id="4731a-111">0</span></span>  <br/> |<span data-ttu-id="4731a-112">Dégradé linéaire.</span><span class="sxs-lookup"><span data-stu-id="4731a-112">Linear gradient.</span></span> <span data-ttu-id="4731a-113">La **cellule FillGradientAngle** détermine la direction du dégradé.</span><span class="sxs-lookup"><span data-stu-id="4731a-113">The **FillGradientAngle** cell determines the direction of the gradient.</span></span>  <br/> |
|<span data-ttu-id="4731a-114">1-7</span><span class="sxs-lookup"><span data-stu-id="4731a-114">1-7</span></span>  <br/> |<span data-ttu-id="4731a-115">Dégradés radiaux.</span><span class="sxs-lookup"><span data-stu-id="4731a-115">Radial gradients.</span></span> <span data-ttu-id="4731a-116">Le dégradé étend l’extérieur dans un cercle à partir d’un point central.</span><span class="sxs-lookup"><span data-stu-id="4731a-116">The gradient extends outwards in a circle from a central point.</span></span>  <br/> |
|<span data-ttu-id="4731a-117">8-12</span><span class="sxs-lookup"><span data-stu-id="4731a-117">8-12</span></span>  <br/> |<span data-ttu-id="4731a-118">Dégradés rectangulaires.</span><span class="sxs-lookup"><span data-stu-id="4731a-118">Rectangular gradients.</span></span> <span data-ttu-id="4731a-119">Le dégradé s’étend sous la forme d’une ligne directionnelle à partir d’une origine avec un fondu rectangulaire.</span><span class="sxs-lookup"><span data-stu-id="4731a-119">The gradient extends as a directional line from an origin with a rectangular-shaped fade.</span></span>  <br/> |
|<span data-ttu-id="4731a-120">13 </span><span class="sxs-lookup"><span data-stu-id="4731a-120">13</span></span>  <br/> |<span data-ttu-id="4731a-121">Dégradé de chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="4731a-121">Path gradient.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4731a-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="4731a-122">Remarks</span></span>

<span data-ttu-id="4731a-123">Pour obtenir une référence à la cellule **FillGradientDir** par un nom à partir d’une autre formule, de l’attribut **N** d’un élément **Cell** ou d’un programme en faisant appel à la propriété **CellsU,** utilisez :</span><span class="sxs-lookup"><span data-stu-id="4731a-123">To get a reference to the **FillGradientDir** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4731a-124">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="4731a-124">Cell name:</span></span>  <br/> | <span data-ttu-id="4731a-125">FillGradientDir</span><span class="sxs-lookup"><span data-stu-id="4731a-125">FillGradientDir</span></span>  <br/> |
   
<span data-ttu-id="4731a-126">Pour obtenir une référence à la **cellule FillGradientDir** à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="4731a-126">To get a reference to the **FillGradientDir** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4731a-127">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="4731a-127">Section index:</span></span>  <br/> |<span data-ttu-id="4731a-128">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="4731a-128">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="4731a-129">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="4731a-129">Row index:</span></span>  <br/> |<span data-ttu-id="4731a-130">**visRowGradientProperties**</span><span class="sxs-lookup"><span data-stu-id="4731a-130">**visRowGradientProperties**</span></span> <br/> |
| <span data-ttu-id="4731a-131">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="4731a-131">Cell index:</span></span>  <br/> |<span data-ttu-id="4731a-132">**visFillGradientDir**</span><span class="sxs-lookup"><span data-stu-id="4731a-132">**visFillGradientDir**</span></span> <br/> |
   

