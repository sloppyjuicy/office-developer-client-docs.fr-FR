---
title: LineGradientDir Cell (Gradient Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c603f9a5-f887-47ce-90bb-d41ec2d1a6a1
description: Détermine la direction du dégradé de ligne. Un dégradé peut être linéaire, radial, rectangulaire ou suivre un tracé.
ms.openlocfilehash: 05dcc6904a4e67d97c632dba44635936b1c14049
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350959"
---
# <a name="linegradientdir-cell-gradient-properties-section"></a><span data-ttu-id="38341-104">LineGradientDir Cell (Gradient Properties Section)</span><span class="sxs-lookup"><span data-stu-id="38341-104">LineGradientDir Cell (Gradient Properties Section)</span></span>

<span data-ttu-id="38341-105">Détermine la direction du dégradé de ligne.</span><span class="sxs-lookup"><span data-stu-id="38341-105">Determines the direction of the line gradient.</span></span> <span data-ttu-id="38341-106">Un dégradé peut être linéaire, radial, rectangulaire ou suivre un tracé.</span><span class="sxs-lookup"><span data-stu-id="38341-106">A gradient can be linear, radial, rectangular, or follow a path.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="38341-107">Un dégradé linéaire est le seul dégradé qui prend une valeur d'angle supplémentaire (tel que déterminé par la cellule **LineGradientDir** ).</span><span class="sxs-lookup"><span data-stu-id="38341-107">A linear gradient is the only gradient that takes an additional angle value (as determined by **LineGradientDir** cell).</span></span> <span data-ttu-id="38341-108">Toutes les autres directions de dégradé ont des énumérations prédéfinies.</span><span class="sxs-lookup"><span data-stu-id="38341-108">All other gradient directions have preset enumerations.</span></span> 
  
|<span data-ttu-id="38341-109">**Value**</span><span class="sxs-lookup"><span data-stu-id="38341-109">**Value**</span></span>|<span data-ttu-id="38341-110">**Description**</span><span class="sxs-lookup"><span data-stu-id="38341-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="38341-111">0</span><span class="sxs-lookup"><span data-stu-id="38341-111">0</span></span>  <br/> |<span data-ttu-id="38341-112">Dégradé linéaire</span><span class="sxs-lookup"><span data-stu-id="38341-112">Linear gradient.</span></span> <span data-ttu-id="38341-113">La cellule **LineGradientAngle** détermine la direction du dégradé.</span><span class="sxs-lookup"><span data-stu-id="38341-113">The **LineGradientAngle** cell determines the direction of the gradient.</span></span>  <br/> |
|<span data-ttu-id="38341-114">1-7</span><span class="sxs-lookup"><span data-stu-id="38341-114">1-7</span></span>  <br/> |<span data-ttu-id="38341-115">Dégradés radiaux</span><span class="sxs-lookup"><span data-stu-id="38341-115">Radial gradients.</span></span> <span data-ttu-id="38341-116">Le dégradé s'étend vers l'extérieur d'un cercle à partir d'un point central.</span><span class="sxs-lookup"><span data-stu-id="38341-116">The gradient extends outwards in a circle from a central point.</span></span>  <br/> |
|<span data-ttu-id="38341-117">8-12</span><span class="sxs-lookup"><span data-stu-id="38341-117">8-12</span></span>  <br/> |<span data-ttu-id="38341-118">Dégradés rectangulaires.</span><span class="sxs-lookup"><span data-stu-id="38341-118">Rectangular gradients.</span></span> <span data-ttu-id="38341-119">Le dégradé s'étend sous la forme d'un trait directionnel à partir d'une origine avec un fondu en forme rectangulaire.</span><span class="sxs-lookup"><span data-stu-id="38341-119">The gradient extends as a directional line from an origin with a rectangular-shaped fade.</span></span>  <br/> |
|<span data-ttu-id="38341-120">kg</span><span class="sxs-lookup"><span data-stu-id="38341-120">13</span></span>  <br/> |<span data-ttu-id="38341-121">Dégradé du tracé.</span><span class="sxs-lookup"><span data-stu-id="38341-121">Path gradient.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="38341-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="38341-122">Remarks</span></span>

<span data-ttu-id="38341-123">Pour obtenir une référence à la cellule **LineGradientDir** par un nom à partir d'une autre formule, par valeur de l'attribut **N** d'un élément de **cellule** ou d'un programme en faisant appel à la propriété **CellsU** , utilisez:</span><span class="sxs-lookup"><span data-stu-id="38341-123">To get a reference to the **LineGradientDir** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="38341-124">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="38341-124">Cell name:</span></span>  <br/> | <span data-ttu-id="38341-125">LineGradientDir</span><span class="sxs-lookup"><span data-stu-id="38341-125">LineGradientDir</span></span>  <br/> |
   
<span data-ttu-id="38341-126">Pour obtenir une référence à la cellule **LineGradientDir** à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants:</span><span class="sxs-lookup"><span data-stu-id="38341-126">To get a reference to the **LineGradientDir** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="38341-127">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="38341-127">Section index:</span></span>  <br/> |<span data-ttu-id="38341-128">**Définis**</span><span class="sxs-lookup"><span data-stu-id="38341-128">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="38341-129">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="38341-129">Row index:</span></span>  <br/> |<span data-ttu-id="38341-130">**visRowGradientProperties**</span><span class="sxs-lookup"><span data-stu-id="38341-130">**visRowGradientProperties**</span></span> <br/> |
| <span data-ttu-id="38341-131">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="38341-131">Cell index:</span></span>  <br/> |<span data-ttu-id="38341-132">**visLineGradientDir**</span><span class="sxs-lookup"><span data-stu-id="38341-132">**visLineGradientDir**</span></span> <br/> |
   

