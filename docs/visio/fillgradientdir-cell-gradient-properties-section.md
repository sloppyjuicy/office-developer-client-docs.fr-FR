---
title: FillGradientDir, cellule (Section Propriétés de dégradé)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e8156ff1-c540-44b8-8b69-ba4d54883260
description: Détermine la direction du dégradé du remplissage. Un dégradé peut être linéaire, radial, rectangulaire ou suivre un chemin d’accès.
ms.openlocfilehash: 9b4226892e70fcffe7a78d109bd852e6d4f93838
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788622"
---
# <a name="fillgradientdir-cell-gradient-properties-section"></a><span data-ttu-id="9b84d-104">FillGradientDir, cellule (Section Propriétés de dégradé)</span><span class="sxs-lookup"><span data-stu-id="9b84d-104">FillGradientDir Cell (Gradient Properties Section)</span></span>

<span data-ttu-id="9b84d-105">Détermine la direction du dégradé du remplissage.</span><span class="sxs-lookup"><span data-stu-id="9b84d-105">Determines the direction of the fill gradient.</span></span> <span data-ttu-id="9b84d-106">Un dégradé peut être linéaire, radial, rectangulaire ou suivre un chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="9b84d-106">A gradient can be linear, radial, rectangular, or follow a path.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="9b84d-107">Dégradé linéaire est le seul dégradé qui prend une valeur d’angle supplémentaires (tel que déterminé par la cellule **FillGradientDir** ).</span><span class="sxs-lookup"><span data-stu-id="9b84d-107">A linear gradient is the only gradient that takes an additional angle value (as determined by **FillGradientDir** cell).</span></span> <span data-ttu-id="9b84d-108">Toutes les autres directions dégradées ont prédéfinie énumérations.</span><span class="sxs-lookup"><span data-stu-id="9b84d-108">All other gradient directions have preset enumerations.</span></span> 
  
****

|<span data-ttu-id="9b84d-109">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="9b84d-109">**Value**</span></span>|<span data-ttu-id="9b84d-110">**Description**</span><span class="sxs-lookup"><span data-stu-id="9b84d-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9b84d-111">0</span><span class="sxs-lookup"><span data-stu-id="9b84d-111">0</span></span>  <br/> |<span data-ttu-id="9b84d-112">Dégradé linéaire.</span><span class="sxs-lookup"><span data-stu-id="9b84d-112">Linear gradient.</span></span> <span data-ttu-id="9b84d-113">La cellule **FillGradientAngle** détermine la direction du dégradé.</span><span class="sxs-lookup"><span data-stu-id="9b84d-113">The **FillGradientAngle** cell determines the direction of the gradient.</span></span>  <br/> |
|<span data-ttu-id="9b84d-114">1 à 7</span><span class="sxs-lookup"><span data-stu-id="9b84d-114">1-7</span></span>  <br/> |<span data-ttu-id="9b84d-115">Dégradé radial.</span><span class="sxs-lookup"><span data-stu-id="9b84d-115">Radial gradients.</span></span> <span data-ttu-id="9b84d-116">Dégradé s’étend vers l’extérieur d’un cercle à partir d’un point central.</span><span class="sxs-lookup"><span data-stu-id="9b84d-116">The gradient extends outwards in a circle from a central point.</span></span>  <br/> |
|<span data-ttu-id="9b84d-117">8-12</span><span class="sxs-lookup"><span data-stu-id="9b84d-117">8-12</span></span>  <br/> |<span data-ttu-id="9b84d-118">Dégradé rectangulaire.</span><span class="sxs-lookup"><span data-stu-id="9b84d-118">Rectangular gradients.</span></span> <span data-ttu-id="9b84d-119">Dégradé étend par un trait de direction à partir d’une origine de fondu rectangulaire.</span><span class="sxs-lookup"><span data-stu-id="9b84d-119">The gradient extends as a directional line from an origin with a rectangular-shaped fade.</span></span>  <br/> |
|<span data-ttu-id="9b84d-120">13</span><span class="sxs-lookup"><span data-stu-id="9b84d-120">13</span></span>  <br/> |<span data-ttu-id="9b84d-121">Dégradé de chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="9b84d-121">Path gradient.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9b84d-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="9b84d-122">Remarks</span></span>

<span data-ttu-id="9b84d-123">Pour obtenir une référence à la cellule **FillGradientDir** par un nom à partir d’une autre formule, par la valeur de l’attribut **N** d’un élément de **cellule** ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="9b84d-123">To get a reference to the **FillGradientDir** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9b84d-124">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="9b84d-124">Cell name:</span></span>  <br/> | <span data-ttu-id="9b84d-125">FillGradientDir</span><span class="sxs-lookup"><span data-stu-id="9b84d-125">FillGradientDir</span></span>  <br/> |
   
<span data-ttu-id="9b84d-126">Pour obtenir une référence à la cellule **FillGradientDir** par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="9b84d-126">To get a reference to the **FillGradientDir** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9b84d-127">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="9b84d-127">Section index:</span></span>  <br/> |<span data-ttu-id="9b84d-128">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="9b84d-128">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="9b84d-129">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="9b84d-129">Row index:</span></span>  <br/> |<span data-ttu-id="9b84d-130">**visRowGradientProperties**</span><span class="sxs-lookup"><span data-stu-id="9b84d-130">**visRowGradientProperties**</span></span> <br/> |
| <span data-ttu-id="9b84d-131">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="9b84d-131">Cell index:</span></span>  <br/> |<span data-ttu-id="9b84d-132">**visFillGradientDir**</span><span class="sxs-lookup"><span data-stu-id="9b84d-132">**visFillGradientDir**</span></span> <br/> |
   

