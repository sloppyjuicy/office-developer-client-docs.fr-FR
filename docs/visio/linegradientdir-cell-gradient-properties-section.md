---
title: LineGradientDir, cellule (Section Propriétés de dégradé)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c603f9a5-f887-47ce-90bb-d41ec2d1a6a1
description: Détermine la direction du dégradé ligne. Un dégradé peut être linéaire, radial, rectangulaire ou suivre un chemin d’accès.
ms.openlocfilehash: 6243d7a6b470db0915ba6fc462f05b72a9814f66
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788958"
---
# <a name="linegradientdir-cell-gradient-properties-section"></a><span data-ttu-id="50865-104">LineGradientDir, cellule (Section Propriétés de dégradé)</span><span class="sxs-lookup"><span data-stu-id="50865-104">LineGradientDir Cell (Gradient Properties Section)</span></span>

<span data-ttu-id="50865-105">Détermine la direction du dégradé ligne.</span><span class="sxs-lookup"><span data-stu-id="50865-105">Determines the direction of the line gradient.</span></span> <span data-ttu-id="50865-106">Un dégradé peut être linéaire, radial, rectangulaire ou suivre un chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="50865-106">A gradient can be linear, radial, rectangular, or follow a path.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="50865-107">Dégradé linéaire est le seul dégradé qui prend une valeur d’angle supplémentaires (tel que déterminé par la cellule **LineGradientDir** ).</span><span class="sxs-lookup"><span data-stu-id="50865-107">A linear gradient is the only gradient that takes an additional angle value (as determined by **LineGradientDir** cell).</span></span> <span data-ttu-id="50865-108">Toutes les autres directions dégradées ont prédéfinie énumérations.</span><span class="sxs-lookup"><span data-stu-id="50865-108">All other gradient directions have preset enumerations.</span></span> 
  
|<span data-ttu-id="50865-109">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="50865-109">**Value**</span></span>|<span data-ttu-id="50865-110">**Description**</span><span class="sxs-lookup"><span data-stu-id="50865-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="50865-111">0</span><span class="sxs-lookup"><span data-stu-id="50865-111">0</span></span>  <br/> |<span data-ttu-id="50865-112">Dégradé linéaire.</span><span class="sxs-lookup"><span data-stu-id="50865-112">Linear gradient.</span></span> <span data-ttu-id="50865-113">La cellule **LineGradientAngle** détermine la direction du dégradé.</span><span class="sxs-lookup"><span data-stu-id="50865-113">The **LineGradientAngle** cell determines the direction of the gradient.</span></span>  <br/> |
|<span data-ttu-id="50865-114">1 à 7</span><span class="sxs-lookup"><span data-stu-id="50865-114">1-7</span></span>  <br/> |<span data-ttu-id="50865-115">Dégradé radial.</span><span class="sxs-lookup"><span data-stu-id="50865-115">Radial gradients.</span></span> <span data-ttu-id="50865-116">Dégradé s’étend vers l’extérieur d’un cercle à partir d’un point central.</span><span class="sxs-lookup"><span data-stu-id="50865-116">The gradient extends outwards in a circle from a central point.</span></span>  <br/> |
|<span data-ttu-id="50865-117">8-12</span><span class="sxs-lookup"><span data-stu-id="50865-117">8-12</span></span>  <br/> |<span data-ttu-id="50865-118">Dégradé rectangulaire.</span><span class="sxs-lookup"><span data-stu-id="50865-118">Rectangular gradients.</span></span> <span data-ttu-id="50865-119">Dégradé étend par un trait de direction à partir d’une origine de fondu rectangulaire.</span><span class="sxs-lookup"><span data-stu-id="50865-119">The gradient extends as a directional line from an origin with a rectangular-shaped fade.</span></span>  <br/> |
|<span data-ttu-id="50865-120">13</span><span class="sxs-lookup"><span data-stu-id="50865-120">13</span></span>  <br/> |<span data-ttu-id="50865-121">Dégradé de chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="50865-121">Path gradient.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="50865-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="50865-122">Remarks</span></span>

<span data-ttu-id="50865-123">Pour obtenir une référence à la cellule **LineGradientDir** par un nom à partir d’une autre formule, par la valeur de l’attribut **N** d’un élément de **cellule** ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="50865-123">To get a reference to the **LineGradientDir** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="50865-124">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="50865-124">Cell name:</span></span>  <br/> | <span data-ttu-id="50865-125">LineGradientDir</span><span class="sxs-lookup"><span data-stu-id="50865-125">LineGradientDir</span></span>  <br/> |
   
<span data-ttu-id="50865-126">Pour obtenir une référence à la cellule **LineGradientDir** par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="50865-126">To get a reference to the **LineGradientDir** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="50865-127">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="50865-127">Section index:</span></span>  <br/> |<span data-ttu-id="50865-128">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="50865-128">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="50865-129">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="50865-129">Row index:</span></span>  <br/> |<span data-ttu-id="50865-130">**visRowGradientProperties**</span><span class="sxs-lookup"><span data-stu-id="50865-130">**visRowGradientProperties**</span></span> <br/> |
| <span data-ttu-id="50865-131">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="50865-131">Cell index:</span></span>  <br/> |<span data-ttu-id="50865-132">**visLineGradientDir**</span><span class="sxs-lookup"><span data-stu-id="50865-132">**visLineGradientDir**</span></span> <br/> |
   

